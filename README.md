# NETWORKWALKS-Prakriti-B084-WK1-PM1-CYBERSECURITY-LAB-SETUP
This repository consists of Week 1 Project of cybersecurity lab setup

📌 Project Overview

This project focuses on setting up a virtual cybersecurity and penetration-testing laboratory using VirtualBox and Kali Linux.

The purpose of the lab is to create a controlled environment where cybersecurity tools, network scanning, reconnaissance, vulnerability assessment, and other security-testing activities can be performed safely and repeatedly.

The lab is configured on a private virtual network so that additional machines can be added later and used as targets for authorized security testing.

🎯 Objectives

The main objectives of this project are to:

  - Install and configure VirtualBox.
  - Install/import Kali Linux as a virtual machine.
  - Create a private NAT Network for the cybersecurity lab.
  - Configure network connectivity for Kali Linux.
  - Assign a consistent IP address to the Kali VM.
  - Verify network connectivity and DNS resolution.
  - Take a clean VM snapshot for recovery.
  - Document the complete setup process.
  - Prepare the environment for future cybersecurity projects.

🛡️ Purpose of the Lab

The lab provides an isolated and controlled environment for cybersecurity learning and authorized security testing.

It can be used for activities such as:

  * Network reconnaissance
  * Port scanning
  * Vulnerability assessment
  * Packet analysis
  * Web security testing
  * Exploitation practice
  * Security-tool experimentation

🏗️ Lab Architecture

<img width="1905" height="1025" alt="2-screenshot-kali-home-page" src="https://github.com/user-attachments/assets/baedf1cc-28d9-4dfa-8346-352fdc0641a3" />

⚙️ Lab Configuration

| Component     | Configuration |
| ------------- | ------------- |
| Host OS       | Windows 11    |
| Host RAM      | 8 GB          |
| Processor     | Intel Core i5 |
| Hypervisor    | VirtualBox 7.2|
| Security OS   | Kali Linux 2025.1|
| Kali RAM      | 2048 MB       |
| Virtual Network | NAT Network |
| Network Address | 10.0.0.0/24 |
| Kali IP Address | 10.0.0.2/24 |
| Default Gateway | 10.0.0.1 |
| DNS Server      | 8.8.8.8 |

🪜 Lab Setup Procedure

**Step 1: Installing VirtualBox**

VirtualBox was installed on pc as the hypervisor.

**Step 2: Creating NAT Network**

A dedicated NAT Network was created in VirtualBox.

Configuration: Network Name: NatNetwork IPv4 Prefix: 10.0.0.0/24 DHCP: Enabled IPv6: Disabled

<img width="1905" height="1063" alt="3-screenshot-kali-linux-network-settings" src="https://github.com/user-attachments/assets/37d4921f-458b-41ac-af54-5dcd168b0cb2" />

A NAT Network was selected because multiple virtual machines connected to the same NAT Network can communicate with one another while also having outbound network connectivity.

**Step 3: Configuring Kali Linux Network Adapter**

The Kali Linux virtual machine was already downloaded and imported into VirtualBox.

The VM network adapter was configured as follows:

Adapter 1
Attached to: NAT Network
Network:     NatNetwork
Adapter Type: Intel PRO/1000 MT Desktop

The VM was allocated:

RAM: 2048 MB

<img width="1905" height="1025" alt="2-screenshot-kali-home-page" src="https://github.com/user-attachments/assets/4f70ad20-3186-49eb-99f0-687988a85e7b" />

**Step 4: Configuring Kali Linux Network**

The Kali Linux network configuration was checked and configured with a consistent IPv4 address.

Example configuration:

IP Address: 10.0.0.2
Subnet Mask: 255.255.255.0
Gateway: 10.0.0.1
DNS: 8.8.8.8

<img width="1905" height="1066" alt="4-screenshot-kali-linux-network-config" src="https://github.com/user-attachments/assets/474af4e4-ddb3-4552-921c-dabca8423ecf" />

**Step 5: Creating a VM Snapshot**

After completing the initial configuration, a VirtualBox snapshot was created.

Snapshot name:

*After Configuration*

🔎 Lab Verification

| **Test** | **Command** | **Expected Result** |
| Check IP Address | ip a | Correct Kali IP shown |
| Test Internet Connectivity | ping 8.8.8.8 | Successful Replies |

🐞 Problems Encountered & Solutions

I encountered one problem in which I mistyped the IP address early on during the network configuration of VirtualBox. Instead of 10.0.0.0/24, I typed 10.0.2.0/24 which resulted in 100% packet loss later when I tried to verify internet connectivity (ping google.com).
After fixing the problem, all the packets were transferred without any error.

💡 What I Learned

Through this project, I learned how to create and configure a virtual environment for cybersecurity practice.

The most important concepts I learned include:

**1. NAT vs NAT Network**
A standard NAT configuration and a NAT Network serve different purposes.

A NAT Network allows multiple VMs connected to the same virtual network to communicate with one another while providing network address translation for external connectivity.

This makes it useful for building a multi-machine cybersecurity laboratory.

**2. Virtual Machine Networking**
I learned how VirtualBox virtual network adapters connect virtual machines to different types of networks and how network configuration affects communication between machines.

**3. Static IP Configuration**
I learned how to configure and verify IPv4 addressing, subnet masks, gateways, and DNS settings in Kali Linux.

**4. VM Snapshots**
I got to know that a clean snapshot should be created before performing risky or experimental activities.

This provides a recovery point for future cybersecurity exercises.

**5. Documentation**
I learned that documenting commands, configuration, screenshots, problems, and solutions is an important part of a professional cybersecurity project and that documentation helps us track our progress as well as increases our credibility.

👤 Author  
Prakriti Acharya  
LinkedIn: https://www.linkedin.com/in/prakriti-acharya-a57200246/  

📌 Project Information  
Program Name: Cybersecurity at Networkwalks | Week: 01 | Project: Cybersecurity & Pentesting Lab Setup | Repository: GitHub

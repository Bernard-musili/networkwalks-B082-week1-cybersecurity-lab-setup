# cybersecurity-lab-setup
The lab provides an isolated and controlled environment for cybersecurity learning and authorized security testing. It can be used for activities such as:(port scanning,network reconnaissance,vulnerability assessment,packet analysis,web security testing, exploitation practice, security tool experimentation)
This repository contains my practical cybersecurity and ethical hacking laboratory environment. The lab is designed to provide a controlled environment where I can practice penetration testing, ethical hacking, network security, and other cybersecurity activities without affecting production systems.

The lab is implemented using Oracle VirtualBox and multiple virtual machines connected through an isolated NAT Network.

Lab Objectives

The main objectives of my cybersecurity lab are to:

Set up a practical cybersecurity and ethical hacking environment.
Install and configure Kali Linux for security testing.
Configure multiple virtual machines on a common laboratory network.
Practice network reconnaissance and security testing in a controlled environment.
Test communication between virtual machines.
Create VM snapshots for easy recovery during practical exercises.
Provide a foundation for future CTF challenges and cybersecurity practical labs.
Laboratory Environment
Host Computer

The recommended host computer specifications from the lab guide are:

RAM: 8 GB or more
Storage: 256 GB SSD or more
Processor: Intel Core i3/i5 or equivalent
Operating System: Windows 10 or another supported host OS
Virtualization Platform

I use:

Oracle VirtualBox
7-Zip

VirtualBox is used to create, configure, and manage the virtual machines used in the laboratory.

Virtual Machines

The laboratory can contain the following virtual machines:

Virtual Machine	Purpose
Kali Linux	Penetration testing and ethical hacking
Windows 10/11/7	Target and testing environment
Android	Optional mobile security testing
Additional VMs	CTFs and future cybersecurity challenges
Network Configuration

All laboratory virtual machines are connected through a custom VirtualBox NAT Network.

Network
Network: 10.0.0.0/24

Example IP addresses used in the laboratory include:

10.0.0.2
10.0.0.7
10.0.0.9
10.0.0.10
10.0.0.11
10.0.0.16

The actual IP allocation depends on the configuration of the individual virtual machines.

Lab Topology

The general structure of my laboratory is:

                    HOST COMPUTER
                         |
                    VirtualBox
                         |
                NAT Network
                  10.0.0.0/24
                         |
       +-----------------+-----------------+
       |                 |                 |
   Kali Linux         Windows VM       Android VM
   10.0.0.x            10.0.0.x          10.0.0.x
       |
 Penetration Testing
   & Security Lab
Setup Procedure
Phase 1: Kali Linux

I set up the laboratory using the following process:

Install 7-Zip.
Install Oracle VirtualBox.
Create a custom NAT Network using the 10.0.0.0/24 network.
Download and import the Kali Linux virtual machine.
Configure the Kali Linux network settings.
Test network connectivity.
Take a snapshot of the configured Kali Linux virtual machine.
Phase 2: Additional Virtual Machines

After setting up Kali Linux, I configure the additional virtual machines:

Install or import Windows 10/11/7 as required.
Install or import Android where required.
Connect the virtual machines to the same NAT Network.
Configure their IP addresses.
Test communication between the virtual machines using ping.
Take snapshots of the configured virtual machines.
Network Connectivity Testing

I verify that the machines can communicate with each other by performing ping tests.

For example:

ping 10.0.0.10

and:

ping 10.0.0.7

Successful responses confirm that the virtual machines can communicate over the configured laboratory network.

Kali Linux Network Configuration

Kali Linux is configured to operate on the laboratory network.

Example configuration:

IP Address: 10.0.0.x
Subnet Mask: 255.255.255.0
Network: 10.0.0.0/24

For Kali Linux versions where internet connectivity problems occur, the lab guide provides the following command:

sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0

The guide also notes that 10.0.0.1 may be used where necessary for internet connectivity troubleshooting.

Snapshots

I create snapshots after successfully configuring each important virtual machine.

Snapshots are important because they allow me to restore a virtual machine to a known working state after performing penetration testing, configuration changes, or other potentially disruptive activities.

Tools and Technologies

The laboratory may be used with cybersecurity tools such as:

Kali Linux
Nmap
Wireshark
Burp Suite
Metasploit
Gobuster
Nikto
Other security-testing tools required for practical exercises

These tools are used only within the controlled laboratory environment and for authorized cybersecurity practice.

Future Practical Exercises

After completing the basic lab setup, the environment can be extended with additional virtual machines for:

Capture The Flag (CTF) challenges
Network reconnaissance
Vulnerability assessment
Web application security testing
Password security testing
Digital forensics exercises
Network traffic analysis
Incident response practice
Other cybersecurity practical exercises

The lab guide also indicates that additional offline virtual machines may be introduced for CTF practical labs and challenges.

Laboratory Completion Checklist

Install 7-Zip

Install VirtualBox

Create the 10.0.0.0/24 NAT Network

Install/import Kali Linux

Configure Kali Linux networking

Create Kali Linux snapshot

Install/import Windows VM

Configure Windows networking

Test connectivity between VMs

Create Windows VM snapshot

Install Android VM where required

Test Android connectivity where applicable

Prepare the lab for cybersecurity and CTF exercises

Expected Outcome

At the end of the setup, I should have a functional and isolated cybersecurity laboratory in which multiple virtual machines can communicate through the 10.0.0.0/24 NAT Network. Kali Linux will serve as the primary security-testing machine, while Windows, Android, and other virtual machines will provide target environments for authorized practical exercises.

Reference

This laboratory setup is based on the Practical Lab Environment Setup for Pentesting, Ethical Hacking & Cybersecurity guide provided by Networkwalks Academy.

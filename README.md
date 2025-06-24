# cybersecurity-ozcazual-project

The OzCazual Infrastructure Security Project - Worked on Brute-Force Protection in the final project of Certificate IV in Cybersecurity.

# Scenario

A local clothing company by the name of OzCazual have had a large increase in online visitors to their website over the last year and the company has also had an influx of employees working remotely. There are growing concerns that the company may face service interruptions and/or data breaches if they don’t get on top of their infrastructure and security.

OzCazual currently have on premises servers running their local data share for employees to share files and a webserver to run their e-commerce storefront.

Currently, remote staff are accessing the file share over the internet and the on-premises router is port-forwarding port 445 so that staff can reach the network share.

## Topology:

### Synology NAS

This Synology NAS is being used to store and share data between staff and also holds some confidential information about the business and customers.
There are user accounts created for each staff member, no two-factor authentication has been enabled for any users.
Port 445 has been forwarded on the router to connect to the SMB share on the NAS.

### Ubuntu 16.04 LTS

Xeon 5110/4GB Ram
Powers the webserver which runs: Apache 2.2, PHP 7.2, MySQL 5.5, WordPress 5.4.

### Windows Server 2012

Used for active directory so that staff can login to computers.
Port forwarding has been setup to allow working from home staff to also login.

## Objective:

OzCazual would like you and your team to upgrade their infrastructure and network topology to be more secure and safely transport information to the remote staff.

You are required to build the infrastructure in a virtual environment such as VirtualBox, VMware, or even a cloud solution such as Azure or AWS.

At a minimum, you must implement the following machines.

- Windows Server
- Linux Web Server

At a minimum, you must implement the following forms of protection

- IDS/IPS/
- Brute-force Protection
- 2FA/MFA
- Virus/malware Protection
- Firewall/Denial of Service protection

# Folder Structure

- [Docs/](/Docs/)
  - [Design_Diagram_and_Network_Diagram](/Docs/Design_Diagram_and_Network_Diagram.pdf) => This file represents the upgraded infrastructure design and their network
  - [Assets/](/Docs/Assets/) => This folder has the documentation of the infrastructural assets such as VMs and related software installations and configurations
  - [Playbooks/](/Docs/Playbooks/) => This folder has the documentation of Playbooks (Defences) on Brute-Force Protection of VMs
  - [Runbooks/](/Docs/Runbooks/) => This Folder has the documentation of Runbooks (Brute-Force Attacks) against the initial VM setup, for testing the defences and also has the observations

# Home-Labs
Documentation and logs for my Windows Server 2022 and CompTIA A+ lab environments.
# Executive Summary 
This project demonstrates the deployment and configuration of a Windows Server 2022 environment to manage network identities and security. By moving away from local account management, this lab establishes a centralized authority (Domain Controller) to govern user access and security policies, simulating a professional enterprise network.
# Technical Environment
Hypervisor: Oracle VM VirtualBox (Running on macOS).

Storage: External SSD (ExFAT) to simulate high-capacity mobile lab environments.

Operating System: Windows Server 2022 Standard (Desktop Experience).

Network Topology: Static IPv4 configuration with localized DNS resolution.

# Lab Methodology 
Phase 1: Infrastructure Setup 

Static IP Configuration: Configured a persistent internal IP address to ensure reliable DNS and authentication services.

Role Deployment: Installed Active Directory Domain Services (AD DS) and promoted the server to a Forest Root Domain (TomTech.local).

Phase 2: Directory Structure & User Provisioning

I implemented a structured Organizational Unit (OU) hierarchy to reflect a departmental business model.

OU Hierarchy: Created Employees and Management containers to separate administrative and general staff roles.

User Lifecycle Management: Provisioned initial user accounts for staff members, including Billy H and Josh M, implementing "Change Password at Next Logon" security protocols.

# Cybersecurity & Troubleshooting Insights
The "Gateway" Challenge: Encountered a total loss of connectivity after manual IP assignment.

Resolution: Conducted a root-cause analysis using ipconfig /all. Identified a mismatch in the Default Gateway and corrected the entry to align with the VirtualBox NAT interface.

Security Best Practice: Used 127.0.0.1 (Loopback) as the Preferred DNS to ensure the Domain Controller manages its own name resolution, a critical requirement for Active Directory health.

# Visual Proof 
![Lab Screenshot](AD-Managment-.pdf) 

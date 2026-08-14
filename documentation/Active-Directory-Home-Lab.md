

 
Contents
Introduction	2
Project Objectives	2
Lab Environment	3
Host Machine	3
Virtual Machines	3
Project Implementation	3
Lessons Learned	4
Skills Demonstrated	5
Future Improvements	6




















Introduction
This project documents the design and implementation of a Microsoft Active Directory home lab using Windows Server 2025 and VMware Workstation Pro. The purpose of the lab is to simulate a real-world enterprise environment and develop practical system administration and IT support skills through hands-on experience.
The project demonstrates the deployment of a Windows Server virtual machine, the configuration of networking, the installation of Active Directory Domain Services (AD DS), DNS and DHCP services, and the management of users, computers, groups and Group Policy.
Each stage of the implementation is documented with screenshots and explanations to provide evidence of the practical work completed.
Project Objectives
The objectives of this project are to:
•	Build a Windows Server 2025 virtual machine. 
•	Configure a secure server environment. 
•	Deploy Active Directory Domain Services. 
•	Configure DNS. 
•	Configure DHCP. 
•	Create and manage Active Directory users and groups. 
•	Join Windows 11 Enterprise clients to the domain. 
•	Configure Group Policy Objects (GPOs). 
•	Simulate an enterprise network environment. 
•	Develop practical IT Support and Windows Server administration skills.





Lab Environment
Host Machine
Host Operating System: Windows 11 
Processor: AMD Ryzen 7 9800X3D 
Memory: 32 GB DDR5 RAM 
Storage: 2 TB NVMe SSD
Virtualization Platform: VMware Workstation Pro 26
Virtual Machines
Machine	Operating System	Purpose
DC01	Windows Server 2025 Standard	Domain Controller
PC01	Windows 11 Enterprise	Domain Cilent














Project Implementation
Step 1 – Create the Virtual Machine
Objective
Create a Windows Server 2025 virtual machine using VMware Workstation Pro.
Actions Performed
•	Created a new virtual machine. 
•	Selected the Windows Server 2025 Standard Evaluation ISO. 
•	Named the virtual machine DC01. 
•	Configured the hardware: 
o	4 GB RAM 
o	2 CPU cores 
o	60 GB virtual hard disk 
o	NAT networking 
•	Powered on the virtual machine. 
Outcome
The virtual machine was successfully created and booted into the Windows Server installer.
Screenshot
<img width="895" height="503" alt="image" src="https://github.com/user-attachments/assets/eb68395c-1b2c-4672-a1b3-d27e7927e816" />


 
Step 2 – Server Manager - Local Server
Objective
Verify the successful installation of Windows Server 2025 and review the initial server configuration.
Actions Performed
•	Opened Server Manager. 
•	Navigated to Local Server. 
•	Verified the server information and default configuration. 
Outcome
Windows Server 2025 was successfully installed and the Local Server dashboard was displayed.
Screenshot
 






Step 3 – Server Renamed to DC01
Objective
Rename the server to DC01 before configuring Active Directory.
Actions Performed
•	Opened the computer name settings. 
•	Changed the computer name to DC01. 
•	Restarted the server to apply the changes. 
Outcome
The server was successfully renamed to DC01.
Screenshot
 







Step 4 – Network Adapter Renamed to LAN
Objective
Rename the default network adapter to improve network management.
Actions Performed
•	Opened Network Connections. 
•	Renamed Ethernet0 to LAN. 
Outcome
The network adapter was successfully renamed to LAN.
Screenshot
 








Step 5 – Static IPv4 Configuration
Objective
Configure a static IPv4 address for the server.
Actions Performed
•	Configured the following network settings: 
o	IP Address: 192.168.79.10 
o	Subnet Mask: 255.255.255.0 
o	Default Gateway: 192.168.79.2 
o	Preferred DNS Server: 192.168.79.10 
Outcome
A static IPv4 address was successfully assigned to the server.
Screenshot
 





Step 6 – VMware Snapshot Created
Objective
Create a VMware snapshot after completing the initial server configuration to provide a restore point before installing server roles and features.
Actions Performed
•	Opened VMware Workstation Pro. 
•	Created a snapshot of the virtual machine. 
•	Named the snapshot Fresh Windows Server Installation. 
•	Added a description documenting the current server configuration. 
Outcome
A restore point was successfully created, allowing the virtual machine to be reverted to a known working state if configuration issues occur during later stages of the project.
Screenshot
 





Step 7 – Add Roles and Features Wizard
Objective
Begin the installation of Active Directory Domain Services (AD DS) by launching the Add Roles and Features Wizard in Server Manager.
Actions Performed
•	Opened Server Manager. 
•	Selected Manage from the menu bar. 
•	Clicked Add Roles and Features. 
•	Launched the Add Roles and Features Wizard. 
•	Verified that the destination server was DC01. 
Outcome
The Add Roles and Features Wizard opened successfully and is ready to install Active Directory Domain Services.
Screenshot
 


Step 8 – Select Destination Server
Objective
Select the target server that will receive the Active Directory Domain Services (AD DS) role.
Actions Performed
•	Selected Role-based or feature-based installation. 
•	Chose Select a server from the server pool. 
•	Verified that DC01 was selected as the destination server. 
•	Confirmed the server IP address was 192.168.79.10. 
•	Verified the operating system was Windows Server 2025 Standard Evaluation. 
Outcome
The destination server was successfully selected, allowing the Active Directory installation to continue on DC01.
Screenshot
 




Step 9 – Confirm Active Directory Installation
Objective
Review the installation configuration before installing the Active Directory Domain Services (AD DS) role on the server.
Actions Performed
•	Reviewed the selected server roles and required features. 
•	Confirmed that Active Directory Domain Services was selected for installation. 
•	Verified that the required management tools, including the Group Policy Management feature and Remote Server Administration Tools (RSAT), would be installed automatically. 
•	Confirmed the installation settings before proceeding. 
Outcome
The installation configuration was successfully verified, confirming that the required roles and features were ready to be installed on DC01.
Screenshot
 




Step 10 – Install Active Directory Domain Services
Objective
Install the Active Directory Domain Services (AD DS) role and its associated management tools on the Windows Server 2025 server.
Actions Performed
•	Reviewed the installation summary. 
•	Started the installation of the Active Directory Domain Services role. 
•	Allowed Windows Server to install all required components, including: 
o	Active Directory Domain Services 
o	Group Policy Management 
o	Remote Server Administration Tools (RSAT) 
o	Active Directory Administrative Center 
o	Active Directory PowerShell Module 
Outcome
The installation of Active Directory Domain Services began successfully and Windows Server started deploying the required roles and management tools.
Screenshot
 

Step 11 – Active Directory Installation Complete
Objective
Verify that the Active Directory Domain Services (AD DS) role was successfully installed and confirm that the server is ready to be promoted to a Domain Controller.
Actions Performed
•	Waited for the installation of Active Directory Domain Services to complete. 
•	Verified that the installation completed successfully. 
•	Confirmed that Windows Server displayed the "Promote this server to a domain controller" option. 
•	Verified that the required management tools were installed successfully. 
Outcome
The Active Directory Domain Services role was successfully installed on DC01. The server is now ready to be promoted to the first Domain Controller for the home.lab Active Directory environment.
Screenshot
 




Step 12 – Promote Server to Domain Controller
Objective
Begin the process of promoting DC01 from a standalone Windows Server to the first Domain Controller in a new Active Directory forest.
Actions Performed
•	Opened the Server Manager notification menu. 
•	Confirmed that Active Directory Domain Services had been installed successfully. 
•	Selected the Promote this server to a domain controller option. 
Outcome
The Active Directory Domain Services Configuration Wizard was made available, allowing the server to be configured as the first Domain Controller for the home.lab domain.
Screenshot
 




Step 13 – Configure Active Directory Deployment
Objective
Start the Active Directory Domain Services Configuration Wizard and choose the deployment type for the new Active Directory environment.
Actions Performed
•	Opened the Active Directory Domain Services Configuration Wizard. 
•	Accessed the Deployment Configuration page. 
•	Reviewed the available deployment options: 
o	Add a domain controller to an existing domain. 
o	Add a new domain to an existing forest. 
o	Add a new forest. 
•	Prepared to create a new Active Directory forest. 
Outcome
The Domain Services Configuration Wizard was successfully launched and was ready to create a new Active Directory forest.
Screenshot 


Step 14 – Create the Active Directory Forest
Objective
Create a new Active Directory forest by defining the root domain name for the organisation.
Actions Performed
•	Selected Add a new forest as the deployment operation. 
•	Entered home.lab as the Root Domain Name. 
•	Verified that the deployment configuration was ready to create the first Active Directory forest. 
Outcome
The Active Directory Configuration Wizard was successfully configured to create a new forest named home.lab, which will serve as the root domain for the lab environment.
Screenshot
 





Step 15 – Configure Domain Controller Options
Objective
Configure the settings for the first Domain Controller in the new Active Directory forest.
Actions Performed
•	Selected Windows Server 2025 as both the Forest Functional Level and Domain Functional Level. 
•	Enabled the DNS Server role. 
•	Enabled the Global Catalog (GC) option. 
•	Left the Read-only Domain Controller (RODC) option disabled. 
•	Created and confirmed the Directory Services Restore Mode (DSRM) password. 
Outcome
The Domain Controller configuration was successfully prepared with the required services and recovery password, allowing the Active Directory deployment to continue.
Screenshot
 



Step 16 – Configure DNS Options
Objective
Review the DNS configuration before promoting the server to a Domain Controller.
Actions Performed
•	Reviewed the DNS Options page. 
•	Left Create DNS delegation unselected. 
•	Verified the warning indicating that a DNS delegation could not be created because no authoritative parent zone exists. 
Outcome
The DNS configuration was confirmed. The delegation warning was expected because DC01 is the first Domain Controller and DNS server in a brand-new Active Directory forest (home.lab).
Screenshot
 





Step 17 – Configure the NetBIOS Domain Name
Objective
Verify the NetBIOS name that will be assigned to the new Active Directory domain.
Actions Performed
•	Reviewed the Additional Options page. 
•	Verified that Windows automatically generated the NetBIOS domain name. 
•	Confirmed the NetBIOS name HOME without making any changes. 
Outcome
The NetBIOS domain name HOME was accepted as the short name for the home.lab Active Directory domain.
Screenshot
 







Step 18 – Configure Active Directory Database Paths
Objective
Review and confirm the storage locations for the Active Directory database, log files, and SYSVOL folder.
Actions Performed
•	Opened the Paths configuration page. 
•	Reviewed the default locations for: 
o	Active Directory database folder (C:\Windows\NTDS) 
o	Log files folder (C:\Windows\NTDS) 
o	SYSVOL folder (C:\Windows\SYSVOL) 
•	Left all locations at their default settings. 
Outcome
The default storage locations for the Active Directory database, transaction logs, and SYSVOL folder were accepted, allowing the installation to continue.
Screenshot
 



Step 19 – Review Active Directory Configuration
Objective
Review all Active Directory Domain Services configuration settings before promoting the server to a domain controller.
Actions Performed
•	Reviewed the deployment summary. 
•	Verified the new forest name: 
o	home.lab 
•	Verified the NetBIOS name: 
o	HOME 
•	Confirmed: 
o	Forest Functional Level: Windows Server 2025 
o	Domain Functional Level: Windows Server 2025 
o	DNS Server installation enabled 
o	Global Catalog enabled 
o	Default database and SYSVOL locations 
Outcome
All Active Directory configuration settings were reviewed and confirmed before running the prerequisite checks.
Screenshot
 
Step 20 – Prerequisites Check
Objective
Validate the server configuration before promoting it to the first domain controller.
Actions Performed
•	Ran the Active Directory prerequisite validation. 
•	The wizard checked the server configuration. 
•	Validation failed because the local Administrator account password did not meet Windows password complexity requirements. 
Outcome
The prerequisite check identified that the Administrator password must be changed before the server can be promoted to a domain controller.
Screenshot
 






Step 20 – Active Directory Prerequisites Check
Objective
Verify that all requirements are met before promoting the server to the first Active Directory Domain Controller.
Actions Performed
•	Ran the Active Directory Domain Services prerequisite check. 
•	Verified the server configuration. 
•	Confirmed all required roles and services were installed successfully. 
•	Reviewed the DNS delegation warning, which is expected when creating a new forest. 
Outcome
All prerequisite checks completed successfully, confirming that the server was ready to be promoted to the first domain controller in the home.lab forest.
Screenshot
 




Step 21 – Active Directory Installation
Objective
Begin the promotion of the server to the first Domain Controller in the home.lab Active Directory forest.
Actions Performed
•	Clicked Install after all prerequisite checks passed. 
•	Started the Active Directory Domain Services installation. 
•	Began promoting DC01 to a Domain Controller. 
•	Installation process initialized and configuration tasks started. 
Outcome
The Active Directory installation process started successfully. Windows began configuring the server as the first Domain Controller for the home.lab forest.
Screenshot
 





Step 22 – Server Restart After Domain Controller Promotion
Objective
Complete the Active Directory Domain Services installation and restart the server.
Actions Performed
•	Waited for the Active Directory installation to complete. 
•	The server automatically restarted after the promotion process. 
•	Windows finalized the Domain Controller configuration during startup. 
Outcome
The server rebooted successfully to complete the promotion process and apply all Active Directory configurations.
Screenshot
No screenshot captured because the server restarted automatically immediately after installation completed.
















Step 22 – Domain Controller Promotion Completed
Objective
Verify that the server was successfully promoted to the first Domain Controller in the home.lab Active Directory forest.
Actions Performed
•	Allowed the server to restart automatically after the Active Directory installation. 
•	Logged back into the server. 
•	Opened Server Manager. 
•	Verified that the server joined the home.lab domain. 
•	Confirmed the static IP configuration remained unchanged. 
Outcome
The server was successfully promoted to the first Domain Controller for the home.lab Active Directory environment. Active Directory Domain Services and DNS were configured successfully, providing the foundation for centralised user and computer management.
Screenshot
 





Lessons Learned


Skills Demonstrated































Future Improvements


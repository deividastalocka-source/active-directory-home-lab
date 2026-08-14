# Microsoft Active Directory Home Lab

## Introduction

This project documents the creation of a Microsoft Active Directory Home Lab using Windows Server 2025 and VMware Workstation Pro.

The purpose of the lab is to gain practical experience with enterprise Windows Server administration by deploying and configuring an Active Directory Domain Services (AD DS) environment from the ground up. Throughout the project, each stage of the deployment process is documented to demonstrate the configuration, implementation and validation of core Active Directory services.

The lab has been developed as part of my professional development towards a career in IT Support and Systems Administration. It provides hands-on experience with server deployment, domain services, networking and technical documentation while following a structured implementation process.

---

## Project Objectives

The objectives of this project are to:

- Build a Windows Server 2025 virtual environment using VMware Workstation Pro.
- Configure a stable server environment with a static IPv4 address.
- Install and configure Active Directory Domain Services (AD DS).
- Promote the server to a Domain Controller.
- Create and configure an Active Directory forest.
- Document each stage of the implementation with supporting screenshots.
- Develop practical skills relevant to enterprise IT environments.

---

## Lab Environment

| Component | Details |
|-----------|---------|
| Hypervisor | VMware Workstation Pro |
| Operating System | Windows Server 2025 |
| Server Name | DC01 |
| Domain | home.lab |
| Server Role | Domain Controller |
| Active Directory | Active Directory Domain Services (AD DS) |

---

## Technologies Used

- Windows Server 2025
- Active Directory Domain Services (AD DS)
- VMware Workstation Pro

---

## Current Progress

- ✅ Create Virtual Machine
- ✅ Install Windows Server 2025
- ✅ Configure Administrator Account
- ✅ Rename Server to DC01
- ✅ Configure Static IPv4 Address
- ✅ Create VMware Snapshot
- ✅ Install Active Directory Domain Services
- ✅ Promote Server to Domain Controller
- ✅ Create the **home.lab** Active Directory Forest
- ⏳ Configure DNS
- ⏳ Configure DHCP
- ⏳ Create Organisational Units (OUs)
- ⏳ Create Users and Groups
- ⏳ Configure Group Policy Objects (GPOs)
- ⏳ Join Windows 11 Client to the Domain

---

## Project Implementation
## Step 1 – Create the Virtual Machine

### Objective

Create a new virtual machine in VMware Workstation Pro to host Windows Server 2025.

### Actions Performed

- Created a new virtual machine using VMware Workstation Pro.
- Selected the Windows Server 2025 installation media.
- Configured the virtual hardware to support the operating system.

### Outcome

A virtual machine was successfully created and prepared for the installation of Windows Server 2025.

> **Screenshot:** `screenshots/01-create-virtual-machine.png`

---

## Step 2 – Configure Virtual Machine Hardware

### Objective

Configure the virtual hardware to provide sufficient resources for the Active Directory environment.

### Actions Performed

- Allocated CPU cores.
- Assigned memory.
- Configured virtual storage.
- Configured the network adapter.

### Outcome

The virtual machine met the hardware requirements required for Windows Server 2025.

> **Screenshot:** `screenshots/02-vm-hardware.png`

---

## Step 3 – Install Windows Server 2025

### Objective

Install Windows Server 2025 onto the virtual machine.

### Actions Performed

- Booted from the installation media.
- Selected the appropriate Windows Server edition.
- Completed the installation process.

### Outcome

Windows Server 2025 was successfully installed.

> **Screenshot:** `screenshots/03-windows-installation.png`

---

## Step 4 – Configure the Administrator Account

### Objective

Complete the initial Windows Server configuration.

### Actions Performed

- Configured the local Administrator password.
- Logged into Windows Server.

### Outcome

The server was successfully configured for first-time use.

> **Screenshot:** `screenshots/04-administrator-account.png`

---

## Step 5 – Verify Windows Server Installation

### Objective

Confirm that Windows Server installed successfully before continuing with additional configuration.

### Actions Performed

- Logged into Windows Server.
- Verified that the operating system loaded successfully.
- Confirmed the desktop environment was functioning correctly.

### Outcome

The operating system was verified and ready for configuration.

> **Screenshot:** `screenshots/05-server-desktop.png`

---

## Step 6 – Rename the Server

### Objective

Rename the server to **DC01** to follow standard enterprise naming conventions.

### Actions Performed

- Opened System Properties.
- Renamed the computer to **DC01**.
- Restarted the server to apply the changes.

### Outcome

The server was successfully renamed to **DC01**.

> **Screenshot:** `screenshots/06-rename-server.png`

---

## Step 7 – Configure a Static IPv4 Address

### Objective

Assign a static IPv4 address to ensure consistent network identification for the Domain Controller.

### Actions Performed

- Opened the network adapter settings.
- Configured a static IPv4 address.
- Configured the subnet mask.
- Configured the default gateway.
- Assigned the preferred DNS server.

### Outcome

The server was successfully configured with a static IPv4 address.

> **Screenshot:** `screenshots/07-static-ip.png`

---

## Step 8 – Verify Network Connectivity

### Objective

Verify that the server could communicate across the network before installing Active Directory.

### Actions Performed

- Confirmed the network configuration.
- Tested connectivity.

### Outcome

The server network configuration was verified successfully.

> **Screenshot:** `screenshots/08-network-test.png`

---

## Step 9 – Create a VMware Snapshot

### Objective

Create a recovery point before making major system changes.

### Actions Performed

- Created a VMware snapshot following the initial server configuration.

### Outcome

A restore point was created, allowing the virtual machine to be rolled back if required.

> **Screenshot:** `screenshots/09-vmware-snapshot.png`

---

## Step 10 – Open Server Manager

### Objective

Prepare Windows Server for the installation of Active Directory Domain Services.

### Actions Performed

- Opened Server Manager.
- Verified that the server was ready for role installation.

### Outcome

The server was prepared for Active Directory Domain Services installation.

> **Screenshot:** `screenshots/10-server-manager.png`

## Step 11 – Add Roles and Features

### Objective

Begin the installation of Active Directory Domain Services (AD DS) using the Add Roles and Features Wizard.

### Actions Performed

- Opened **Server Manager**.
- Selected **Add Roles and Features**.
- Chose a **Role-based or feature-based installation**.

### Outcome

The server was prepared for Active Directory Domain Services installation.

> **Screenshot:** `screenshots/11-add-roles-and-features.png`

---

## Step 12 – Select Destination Server

### Objective

Select the local server as the installation target.

### Actions Performed

- Selected **DC01** from the server pool.

### Outcome

The installation target was confirmed successfully.

> **Screenshot:** `screenshots/12-select-server.png`

---

## Step 13 – Select Active Directory Domain Services

### Objective

Select the Active Directory Domain Services server role.

### Actions Performed

- Enabled **Active Directory Domain Services (AD DS)**.
- Accepted the required management tools.

### Outcome

The AD DS role was selected for installation.

> **Screenshot:** `screenshots/13-select-ad-ds.png`

---

## Step 14 – Confirm Required Features

### Objective

Install the supporting management tools required for Active Directory.

### Actions Performed

- Reviewed the required features.
- Accepted the automatically selected management tools.

### Outcome

All required dependencies were included.

> **Screenshot:** `screenshots/14-required-features.png`

---

## Step 15 – Additional Features

### Objective

Review optional Windows Server features.

### Actions Performed

- Continued without selecting additional features.

### Outcome

The installation proceeded using the default configuration.

> **Screenshot:** `screenshots/15-additional-features.png`

---

## Step 16 – Active Directory Domain Services Information

### Objective

Review the information provided before installing Active Directory Domain Services.

### Actions Performed

- Reviewed Microsoft's information regarding AD DS.

### Outcome

The server was ready to begin installation.

> **Screenshot:** `screenshots/16-ad-information.png`

---

## Step 17 – Installation Confirmation

### Objective

Confirm the installation settings before deployment.

### Actions Performed

- Reviewed the installation summary.
- Enabled automatic restart if required.
- Started the installation.

### Outcome

The installation process began successfully.

> **Screenshot:** `screenshots/17-confirm-installation.png`

---

## Step 18 – Install Active Directory Domain Services

### Objective

Install the Active Directory Domain Services role.

### Actions Performed

- Allowed Windows Server to install AD DS and its supporting components.

### Outcome

The AD DS role installed successfully.

> **Screenshot:** `screenshots/18-ad-installation.png`

---

## Step 19 – Promote the Server to a Domain Controller

### Objective

Configure the server as the first Domain Controller in a new Active Directory forest.

### Actions Performed

- Selected **Promote this server to a domain controller**.
- Chose **Add a new forest**.
- Entered the root domain name:

```
home.lab
```

### Outcome

The Active Directory forest configuration process was started.

> **Screenshot:** `screenshots/19-promote-domain-controller.png`

---

## Step 20 – Configure Domain Controller Options

### Objective

Configure the Domain Controller settings.

### Actions Performed

- Selected the appropriate forest and domain functional levels.
- Enabled the DNS Server role.
- Configured the Directory Services Restore Mode (DSRM) password.

### Outcome

The Domain Controller configuration was completed successfully.

> **Screenshot:** `screenshots/20-domain-controller-options.png`

---

## Step 21 – Active Directory Prerequisites Check

### Objective

Verify that all configuration requirements were satisfied before installation.

### Actions Performed

- Ran the Active Directory prerequisites check.
- Resolved the password complexity requirement.
- Re-ran the validation.

### Outcome

All prerequisite checks completed successfully.

> **Screenshot:** `screenshots/21-prerequisites-check.png`

---

## Step 22 – Install the Active Directory Forest

### Objective

Create the **home.lab** Active Directory forest.

### Actions Performed

- Started the Active Directory deployment process.
- Allowed Windows Server to complete the forest installation.

### Outcome

The server was promoted successfully to a Domain Controller and the **home.lab** forest was created.

> **Screenshot:** `screenshots/22-install-forest.png`

---

## Step 23 – Restart the Server

### Objective

Complete the Domain Controller promotion process.

### Actions Performed

- Allowed Windows Server to restart automatically.

### Outcome

The server rebooted successfully after Active Directory installation.

> **Screenshot:** `screenshots/23-server-restart.png`

---

## Step 24 – Verify Domain Controller Deployment

### Objective

Confirm that the Domain Controller and Active Directory forest were created successfully.

### Actions Performed

- Logged into the server.
- Verified the **home.lab** domain.
- Confirmed Active Directory Domain Services was operational.

### Outcome

Windows Server 2025 was successfully configured as the first Domain Controller within the **home.lab** Active Directory forest.

> **Screenshot:** `screenshots/24-domain-controller-complete.png`

---

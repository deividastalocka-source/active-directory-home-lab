# Windows Server Setup

This section documents the deployment and initial configuration of the Windows Server 2025 virtual machine before Active Directory Domain Services (AD DS) is installed.

The objective is to prepare a stable Windows Server environment that can later be promoted to a Domain Controller.

---

# Step 1 – Create the Virtual Machine

## Objective

Create a Windows Server 2025 virtual machine using VMware Workstation Pro.

## Actions Performed

- Created a new virtual machine.
- Selected the Windows Server 2025 Standard Evaluation ISO.
- Named the virtual machine **DC01**.
- Configured the virtual hardware:
  - 4 GB RAM
  - 2 CPU cores
  - 60 GB virtual hard disk
  - NAT networking
- Powered on the virtual machine.

## Outcome

The virtual machine was successfully created and booted into the Windows Server installer.

![Virtual Machine Created](../screenshots/01%20-%20Virtual%20Machine%20Created.png)

---

# Step 2 – Server Manager - Local Server

## Objective

Verify the successful installation of Windows Server 2025 and review the initial server configuration.

## Actions Performed

- Opened **Server Manager**.
- Navigated to **Local Server**.
- Verified the server information and default configuration.

## Outcome

Windows Server 2025 was successfully installed and the Local Server dashboard was displayed.

![Server Manager - Local Server](../screenshots/02%20-%20Server%20Manager%20-%20Local%20Server.png)

---

# Step 3 – Rename Server to DC01

## Objective

Rename the server to **DC01** before configuring Active Directory.

## Actions Performed

- Opened the computer name settings.
- Changed the computer name to **DC01**.
- Restarted the server.

## Outcome

The server was successfully renamed to **DC01**.

![Server Renamed to DC01](../screenshots/03%20-%20Server%20Renamed%20to%20DC01.png)

---

# Step 4 – Rename the Network Adapter

## Objective

Rename the default network adapter to improve administration and identification.

## Actions Performed

- Opened **Network Connections**.
- Renamed **Ethernet0** to **LAN**.

## Outcome

The network adapter was successfully renamed to **LAN**.

![Network Adapter Renamed to LAN](../screenshots/04%20-%20Network%20Adapter%20Renamed%20to%20LAN.png)

---

# Step 5 – Configure a Static IPv4 Address

## Objective

Configure a static IPv4 address for the server.

## Actions Performed

Configured the following network settings:

- IP Address: **192.168.79.10**
- Subnet Mask: **255.255.255.0**
- Default Gateway: **192.168.79.2**
- Preferred DNS Server: **192.168.79.10**

## Outcome

A static IPv4 address was successfully assigned to the server.

![Static IPv4 Configuration](../screenshots/05%20-%20Static%20IPv4%20Configuration.png)

---

# Step 6 – Create a VMware Snapshot

## Objective

Create a VMware snapshot after completing the initial server configuration.

This provides a restore point before installing Windows Server roles and features.

## Actions Performed

- Opened VMware Workstation Pro.
- Created a snapshot.
- Named the snapshot **Fresh Windows Server Installation**.
- Added a description documenting the current server configuration.

## Outcome

A restore point was successfully created, allowing the virtual machine to be reverted to a known working state if configuration issues occur during later stages of the project.

![VMware Snapshot Created](../screenshots/06%20-%20VMware%20Snapshot%20Created.png)

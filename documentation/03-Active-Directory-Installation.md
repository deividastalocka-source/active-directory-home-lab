# Active Directory Installation

This section documents the installation of **Active Directory Domain Services (AD DS)** on the Windows Server 2025 virtual machine.

The objective is to prepare the server for promotion to the first Domain Controller within a new Active Directory forest.

---

# Add Roles and Features Wizard

## Objective

Begin the installation of Active Directory Domain Services (AD DS) using the **Add Roles and Features Wizard** in Server Manager.

## Actions Performed

- Opened **Server Manager**.
- Selected **Manage** from the menu bar.
- Clicked **Add Roles and Features**.
- Launched the **Add Roles and Features Wizard**.
- Verified that **DC01** was selected as the destination server.

## Outcome

The Add Roles and Features Wizard opened successfully and was ready to install Active Directory Domain Services.

![Add Roles and Features Wizard](../screenshots/07%20-%20Add%20Roles%20and%20Features%20Wizard.png)

---

# Server Selection

## Objective

Select the destination server that will receive the Active Directory Domain Services role.

## Actions Performed

- Selected **Role-based or feature-based installation**.
- Chose **Select a server from the server pool**.
- Verified that **DC01** was selected.
- Confirmed the server IP address was **192.168.79.10**.
- Verified the operating system was **Windows Server 2025 Standard Evaluation**.

## Outcome

The destination server was successfully selected, allowing the Active Directory installation to continue.

![Server Selection](../screenshots/08%20-%20Server%20Selection.png)

---

# Active Directory Installation Confirmation

## Objective

Review the installation configuration before installing Active Directory Domain Services.

## Actions Performed

- Reviewed the selected server roles.
- Confirmed that **Active Directory Domain Services** was selected.
- Verified that the required management tools would be installed automatically, including:
  - Group Policy Management
  - Remote Server Administration Tools (RSAT)

## Outcome

The installation configuration was successfully verified and was ready to proceed.

![Active Directory Installation Confirmation](../screenshots/09%20-%20Active%20Directory%20Installation%20Confirmation.png)

---

# Active Directory Installation

## Objective

Install the Active Directory Domain Services role and its associated management tools.

## Actions Performed

- Reviewed the installation summary.
- Started the installation.
- Allowed Windows Server to install:
  - Active Directory Domain Services
  - Group Policy Management
  - Remote Server Administration Tools (RSAT)
  - Active Directory Administrative Center
  - Active Directory PowerShell Module

## Outcome

Windows Server successfully began installing Active Directory Domain Services and all required management tools.

![Active Directory Installation in Progress](../screenshots/10%20-%20Active%20Directory%20Installation%20in%20Progress.png)

---

# Active Directory Installation Complete

## Objective

Verify that Active Directory Domain Services was installed successfully.

## Actions Performed

- Waited for the installation to complete.
- Confirmed that installation completed successfully.
- Verified that the **Promote this server to a domain controller** option appeared.
- Confirmed that all required management tools had been installed.

## Outcome

Active Directory Domain Services was successfully installed on **DC01**. The server was now ready to be promoted to the first Domain Controller in the **home.lab** Active Directory environment.

![Active Directory Installation Complete](../screenshots/11%20-%20Active%20Directory%20Installation%20Complete.png)

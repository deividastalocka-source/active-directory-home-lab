# Domain Controller Configuration

This section documents the promotion of **DC01** from a standalone Windows Server 2025 installation to the first Domain Controller in a new Active Directory forest.

The process includes creating the **home.lab** forest, configuring Domain Controller settings, validating prerequisites and verifying a successful deployment.

---

# Promote Server to Domain Controller

## Objective

Begin the promotion of **DC01** from a standalone Windows Server installation to the first Domain Controller in a new Active Directory forest.

## Actions Performed

- Opened the **Server Manager** notification menu.
- Confirmed that Active Directory Domain Services had been installed successfully.
- Selected **Promote this server to a domain controller**.

## Outcome

The Active Directory Domain Services Configuration Wizard opened successfully and was ready to configure the first Domain Controller for the **home.lab** domain.

![Promote Server to Domain Controller](../screenshots/12%20-%20Promote%20Server%20to%20Domain%20Controller.png)

---

# Deployment Configuration

## Objective

Configure the deployment type for the new Active Directory environment.

## Actions Performed

- Opened the **Active Directory Domain Services Configuration Wizard**.
- Selected **Add a new forest**.
- Reviewed the available deployment options.

## Outcome

The deployment configuration was prepared to create a new Active Directory forest.

![Deployment Configuration](../screenshots/13%20-%20Deployment%20Configuration.png)

---

# Root Domain Name

## Objective

Configure the root domain name for the Active Directory forest.

## Actions Performed

- Entered **home.lab** as the root domain name.
- Verified the deployment configuration before continuing.

## Outcome

The new Active Directory forest was configured using **home.lab** as the root domain.

![Root Domain Name](../screenshots/14%20-%20Root%20Domain%20Name%20-%20home.lab.png)

---

# Domain Controller Options

## Objective

Configure the settings for the first Domain Controller.

## Actions Performed

- Selected **Windows Server 2025** for the Forest Functional Level.
- Selected **Windows Server 2025** for the Domain Functional Level.
- Enabled the **DNS Server** role.
- Enabled the **Global Catalog (GC)**.
- Created the **Directory Services Restore Mode (DSRM)** password.

## Outcome

The Domain Controller options were configured successfully.

![Domain Controller Options](../screenshots/15%20-%20Domain%20Controller%20Options.png)

---

# DNS Options

## Objective

Review the DNS configuration before promoting the server.

## Actions Performed

- Reviewed the DNS configuration.
- Left **Create DNS Delegation** unselected.
- Verified the DNS delegation warning.

## Outcome

The DNS configuration was confirmed successfully. The delegation warning was expected because this server was creating a new forest.

![DNS Options](../screenshots/16%20-%20DNS%20Options.png)

---

# NetBIOS Domain Name

## Objective

Verify the automatically generated NetBIOS name.

## Actions Performed

- Reviewed the generated NetBIOS name.
- Confirmed **HOME** without making any changes.

## Outcome

The NetBIOS domain name was successfully configured.

![NetBIOS Domain Name](../screenshots/17%20-%20NetBIOS%20Domain%20Name.png)

---

# Active Directory Database Paths

## Objective

Review the storage locations used by Active Directory.

## Actions Performed

Reviewed the default locations for:

- Active Directory database
- Log files
- SYSVOL folder

Accepted the default configuration.

## Outcome

The default Active Directory storage locations were successfully configured.

![Active Directory Database Paths](../screenshots/18%20-%20Active%20Directory%20Database%20Paths.png)

---

# Review Active Directory Configuration

## Objective

Review all Active Directory configuration settings before running the prerequisite checks.

## Actions Performed

Verified:

- Forest name (**home.lab**)
- NetBIOS name (**HOME**)
- Forest Functional Level
- Domain Functional Level
- DNS Server installation
- Global Catalog
- Default database locations

## Outcome

The Active Directory configuration was successfully reviewed and confirmed.

![Review Active Directory Configuration](../screenshots/19%20-%20Review%20Active%20Directory%20Configuration.png)

---

# Initial Prerequisites Check

## Objective

Validate the server configuration before promotion.

## Actions Performed

- Ran the prerequisite validation.
- Identified a password complexity issue with the local Administrator account.

## Outcome

The prerequisite check failed because the Administrator password did not satisfy Windows password complexity requirements.

After updating the password to meet the required policy, the validation was performed again.

![Prerequisites Check Failed](../screenshots/20%20-%20Prerequisites%20Check%20Failed%20-%20Administrator%20Password.png)

---

# Successful Prerequisites Check

## Objective

Verify that all Active Directory requirements had been satisfied.

## Actions Performed

- Re-ran the prerequisite validation.
- Confirmed all required services were installed.
- Reviewed the expected DNS delegation warning.

## Outcome

All prerequisite checks completed successfully and the server was ready to be promoted to the first Domain Controller.

![Prerequisites Check Passed](../screenshots/21%20-%20Active%20Directory%20Prerequisites%20Check%20Passed.png)

---

# Active Directory Installation

## Objective

Promote the server to the first Domain Controller within the **home.lab** forest.

## Actions Performed

- Selected **Install**.
- Started the Active Directory Domain Services installation.
- Allowed Windows Server to complete the promotion process.

## Outcome

Windows Server successfully began promoting **DC01** to a Domain Controller.

![Active Directory Installation Started](../screenshots/22%20-%20Active%20Directory%20Installation%20Started.png)

---

# Domain Controller Promotion Complete

## Objective

Verify that the Domain Controller deployment completed successfully.

## Actions Performed

- Allowed Windows Server to restart automatically.
- Logged back into the server.
- Opened Server Manager.
- Confirmed the server joined the **home.lab** domain.
- Verified the static IPv4 configuration remained unchanged.

## Outcome

**DC01** was successfully promoted to the first Domain Controller within the **home.lab** Active Directory forest.

Active Directory Domain Services and DNS were successfully configured, providing the foundation for centralised user, computer and policy management.

![DC01 Successfully Promoted to Domain Controller](../screenshots/23%20-%20DC01%20Successfully%20Promoted%20to%20Domain%20Controller.png)

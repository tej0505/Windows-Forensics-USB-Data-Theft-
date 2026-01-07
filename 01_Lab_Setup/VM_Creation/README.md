## Step-wise Virtual Machine Setup

### Overview

To ensure forensic integrity and to accurately replicate real-world DFIR workflows, **two separate Windows 10 virtual machines** were created and used throughout this project:

1. **Suspect Machine (Attack VM)** – Used to simulate insider threat activity and generate forensic artifacts
2. **Forensic Analysis Machine (Investigation VM)** – Used exclusively for disk imaging, forensic analysis, and reporting

This separation is a critical forensic best practice and ensures that analysis tools do not contaminate the suspect system.

---

## Step 1: Windows 10 Installation (Base Setup)

Two independent Windows 10 virtual machines were created using **VMware Workstation**.

**Common steps for both machines:**

* A new virtual machine was created in VMware Workstation
* Windows 10 was installed using default installation settings
* Standard hardware configuration was used to resemble a typical workstation
* Systems were fully installed and verified to boot successfully

After installation, each machine was configured for its specific role.

---

## Step 2: Creation of Suspect Machine (Attack VM)

The first Windows 10 virtual machine was configured as the **suspect system**, representing a normal corporate employee workstation.

**Steps performed:**

* A **normal (non-administrative) user account** was created
* No forensic or security tools were installed
* The system was kept minimal to avoid altering forensic artifacts

### Data Preparation on Suspect Machine

As part of the lab environment setup, legitimate confidential data was prepared **before any attack activity**.

**Actions performed:**

* A folder named **CONFIDENTIAL** was created
* The following sensitive files were placed inside the folder:

  * salary.xlsx
  * employee_details.xlsx
  * client_list.xlsx
    
<img width="787" height="350" alt="Screenshot from 2025-12-29 12-39-44" src="https://github.com/user-attachments/assets/4329ea7f-eb0a-4d0c-a0b1-7b6e8b4ed6c1" />

**Purpose:**
This step ensures that the data existed legitimately on the system prior to the incident.
The attacker later accessed, copied, and deleted these files but **did not create them**, which accurately reflects real insider threat scenarios.

---

## Step 3: Creation of Forensic Analysis Machine (Investigation VM)

The second Windows 10 virtual machine was configured as a **dedicated forensic workstation**.

**Steps performed:**

* A separate Windows 10 virtual machine was created using VMware
* The system was isolated from the suspect machine
* The following forensic tools were installed:

  * **FTK Imager** – for forensic disk acquisition and hash verification
  * <img width="1120" height="630" alt="image" src="https://github.com/user-attachments/assets/92e04fc4-ce08-4edc-942b-7a3d05019c71" />

  * **Autopsy** – for forensic analysis, artifact extraction, and timeline reconstruction
  * <img width="1200" height="665" alt="image" src="https://github.com/user-attachments/assets/5b1c65e7-f877-407e-a15e-01da5aeff442" />


**Purpose:**
This machine was used exclusively to:

* Acquire a forensic disk image of the suspect VM
* Verify MD5 and SHA1 hash values
* Analyze forensic artifacts
* Reconstruct the timeline of events
* Prepare the final forensic investigation report

No attack activity was performed on this system.

---

## Importance of Using Two Separate Virtual Machines

Using two distinct virtual machines is essential for both **attack simulation** and **forensic analysis**:

* Prevents contamination of digital evidence
* Preserves forensic integrity
* Accurately reflects real-world DFIR investigations
* Ensures repeatability and credibility of findings

This setup demonstrates proper forensic methodology, ethical investigation practices, and a strong understanding of digital forensic workflows.

---

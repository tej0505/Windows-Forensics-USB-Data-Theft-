# Lab Setup and Environment Preparation

This section documents the complete preparation of the forensic lab environment used in this project. The lab was designed to realistically simulate an insider threat scenario while maintaining forensic integrity and ethical standards.

As part of the lab setup, **two primary folders were created inside this directory** to clearly separate environment preparation from simulated attacker behavior:

* **VM_Creation** – Documents the creation and configuration of virtual machines
* **Attacker_Actions** – Documents simulated insider threat activities performed on the suspect system

This structured approach ensures clarity, repeatability, and professional documentation.

---

## Folder Structure Created in This Section

```
01_Lab_Setup/
├── VM_Creation/
└── Attacker_Actions/
```

Each folder contains screenshots and explanations relevant to that phase of the investigation.

---

## Virtual Machine Creation (VM_Creation)

This folder documents the step-wise creation of **two separate virtual machines**, following digital forensic best practices.

### 1. Suspect Machine (Attack Environment)

The first virtual machine was created to simulate a normal corporate employee workstation where the incident occurs.

**Steps performed:**

* A Windows 10 virtual machine was created using VMware Workstation
* Default system and hardware settings were applied
* A normal (non-administrative) user account was created
* No forensic or security tools were installed on this system
* A folder named **CONFIDENTIAL** was created as part of the lab environment
* The following sensitive files were placed inside the folder:

  * salary.xlsx
  * employee_details.xlsx
  * client_list.xlsx

**Purpose:**
This machine represents the suspect system and was used to host legitimate confidential data and generate forensic artifacts through simulated insider activity.

---

### 2. Forensic Analysis Machine (Investigation Environment)

A second virtual machine was created to perform evidence acquisition and forensic analysis.

**Steps performed:**

* A separate Windows 10 virtual machine was created using VMware Workstation
* The system was isolated from the suspect machine to prevent evidence contamination
* The following forensic tools were installed:

  * FTK Imager – for forensic disk acquisition and hash verification
  * Autopsy – for forensic analysis, artifact extraction, and timeline reconstruction

**Purpose:**
This machine was used exclusively for forensic investigation and report preparation.

---

## Simulated Attacker Actions (Attacker_Actions)

This folder documents insider threat activity intentionally performed on the suspect machine to generate real forensic evidence. All actions were conducted in a controlled virtual lab environment for learning purposes only.

### Attacker actions performed:

* USB device insertion
* Access to confidential files
* Copying files to external USB storage
* Permanent deletion of files and folders to hide evidence
* Suspicious browser activity, including accessing local files and visiting a keylogger download website

These actions generated forensic artifacts such as USB registry entries, recent documents, shell bags, deleted file records, browser history, and timeline events, which were later analyzed during the investigation.

---

## Forensic Best Practices Followed

* Separate virtual machines used for attack simulation and forensic analysis
* Suspect system powered off prior to imaging
* Evidence acquired using industry-standard forensic tools
* No real user data or illegal datasets were used

This lab setup reflects real-world **Digital Forensics and Incident Response (DFIR)** workflows and ensures ethical, repeatable, and reliable investigation results.


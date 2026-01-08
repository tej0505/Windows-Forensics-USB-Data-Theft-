# Windows Forensics – USB Data Theft Investigation

## Project Overview

This repository presents a **simulated digital forensic investigation** of a suspected insider data theft incident on a Windows 10 system.
The project demonstrates an **end-to-end Digital Forensics and Incident Response (DFIR) workflow**, including incident simulation, forensic acquisition, artifact analysis, timeline reconstruction, and formal reporting.

The primary objective of the investigation was to determine whether confidential data was **accessed, copied to an external USB device, and intentionally deleted** to conceal user activity.

All activities were conducted in a **controlled virtual lab environment** using industry-standard forensic tools.

---

## Investigation Scenario

An employee was suspected of unauthorized data handling involving removable media. The alleged actions included:

* Connecting an external USB storage device
* Accessing confidential corporate files
* Copying sensitive data to removable storage
* Permanently deleting files to hide evidence
* Performing suspicious browser activity

A forensic investigation was initiated to reconstruct events and determine intent using forensic artifacts recovered from disk images.

> Note: This project uses **only simulated data** created for educational and demonstration purposes.

---

## Tools and Technologies Used

* **FTK Imager** – Forensic disk acquisition and hash verification
* **Autopsy** – Digital forensic analysis and timeline reconstruction
* **VMware Workstation** – Virtualized forensic lab environment
* **Windows 10** – Suspect and forensic workstation operating systems

---

## Investigation Methodology

The investigation followed accepted forensic best practices and included the following phases:

1. **Lab Setup**

   * Two isolated virtual machines were created:

     * Suspect (Attack) Machine
     * Forensic Analysis Workstation

2. **Incident Simulation**

   * Confidential files were accessed
   * External USB device was connected
   * Files were copied and permanently deleted
   * Browser activity was generated to simulate malicious behavior

3. **Evidence Acquisition**

   * The suspect system was powered off
   * A full physical disk image was acquired using FTK Imager
   * MD5 and SHA1 hashes were generated and verified

4. **Forensic Analysis**

   * Disk image analyzed using Autopsy
   * Artifacts examined included:

     * USB device history
     * Recent documents
     * Shell Bags
     * Deleted files
     * Registry artifacts
     * Web history

5. **Timeline Reconstruction**

   * All artifacts were correlated to reconstruct the sequence of events
   * USB insertion, file access, deletion, and browser activity were aligned chronologically

6. **Reporting**

   * Findings were documented in a formal forensic report
   * Screenshots and supporting evidence were preserved

---

## Repository Structure

```
Windows-Forensics-USB-Data-Theft/
│
├── 01_Lab_Setup/
│   ├── VM_Creation/
│   └── Attacker_Actions/
│
├── 02_Evidence_Acquisition/
│
├── 03_Forensic_Analysis/
│
├── 04_Timeline_Reconstruction/
│
├── 05_Report/
│   └── Final_Forensic_Report.pdf
│
├── README.md
└── LICENSE
```

---

## Key Findings Summary

* External USB device was connected to the system
* Confidential files were accessed and opened
* Sensitive data was copied to removable media
* Confidential folders were permanently deleted
* Browser artifacts indicate suspicious activity
* Timeline correlation confirms intentional behavior

---

## Ethical Notice

This project was conducted strictly for **educational and demonstration purposes**.
No real user data, victims, or illegal datasets were used. All activities were performed in a controlled virtual environment following ethical forensic practices.

---

## Author

**Tejas K. Mahale**
Digital Forensics and Incident Response (DFIR) Lab Project

---

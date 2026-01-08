# Digital Forensic Investigation Report

**Case: Windows USB Data Theft**

This folder contains the **final forensic investigation report** documenting a simulated insider data theft incident on a Windows 10 system.
The report was prepared following **standard digital forensic methodology**, maintaining evidence integrity, repeatability, and clear documentation.

---

## Report Overview

The investigation focuses on identifying whether an employee:

* Connected an external USB storage device
* Accessed confidential files
* Copied sensitive data
* Attempted to delete evidence
* Engaged in suspicious browser activity

All analysis was conducted on a **forensically acquired disk image**, not on the live system.

---

## Case Details

| Field           | Value                                                     |
| --------------- | --------------------------------------------------------- |
| **Case Name**   | Windows USB Data Theft                                    |
| **Case ID**     | 2026-USB-001                                              |
| **Examiner**    | Tejas K. Mahale                                           |
| **Environment** | Controlled Virtual Lab (Zorin OS Host / Windows 10 Guest) |
| **Tools Used**  | FTK Imager, Autopsy                                       |
| **Report Type** | Academic & Practical DFIR Lab (Simulated Incident)        |

---

## Evidence Summary

* **Evidence Type:** Windows 10 disk image (E01 format)
* **Acquisition Tool:** FTK Imager
* **Hash Verification:** MD5 & SHA1 (Match confirmed)
* **Image Segments:** `.E01` – `.E05`
* **Analysis Tool:** Autopsy v4.22.1

Evidence integrity was preserved throughout the investigation.

---

## Key Findings (High-Level)

The forensic analysis established that:

* A **USB device** was connected to the system
* The **CONFIDENTIAL** folder was accessed
* Sensitive files including `salary.xlsx` were opened
* Files were **permanently deleted** after access
* The **Recycle Bin was cleared**
* Suspicious **browser activity** including keylogger download was observed
* Timeline correlation confirms **intentional and unauthorized activity**

---

## Timeline Reconstruction

Artifacts from multiple sources were correlated, including:

* USB registry artifacts
* Recent Documents
* Shell Bags
* Deleted files metadata
* Browser history

This correlation produced a **defensible, chronological reconstruction** of the incident from initial access to evidence destruction.

---

## Report Contents

The full report includes:

* Executive Summary
* Case Information & Scope
* Evidence Description & Hash Verification
* Chain of Custody
* Acquisition Methodology
* Analysis Methodology
* Detailed Findings with artifacts
* Timeline of Events
* Data Correlation
* Conclusion & Recommendations
* Limitations
* References
* Appendix with screenshots

---

## Ethical & Legal Notice

⚠️ **Important**

* This investigation was conducted in a **simulated lab environment**
* No real victim data was used
* No illegal datasets were analyzed
* All actions were performed for **educational and professional training purposes**

---

## File in This Folder

📄 **Final_Forensic_Report.pdf**
The complete, formatted forensic investigation report.

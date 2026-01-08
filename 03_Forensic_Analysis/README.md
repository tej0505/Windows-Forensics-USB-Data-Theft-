# Forensic Analysis Using Autopsy

This section documents the complete forensic analysis of the acquired Windows 10 disk image using **Autopsy**.
The goal of this phase was to examine system artifacts, user activity, and evidence of data exfiltration in a structured and forensically sound manner.

All analysis was performed on a **verified E01 disk image** created using FTK Imager.
The original suspect system was not accessed during this phase.

---

## Step 1: Launching Autopsy

Autopsy was opened on the forensic analysis virtual machine.

**Purpose:**

* Begin forensic examination in a controlled environment
* Ensure analysis is isolated from the suspect system

📸 Screenshot: Autopsy application opened

  <img width="766" height="495" alt="Screenshot from 2025-12-29 20-53-27" src="https://github.com/user-attachments/assets/49983d03-9ee5-4f13-bfbb-b69ccd89e30d" />
  

---

## Step 2: Creating a New Case

A new forensic case was created in Autopsy.

**Case setup actions:**

* Entered a unique case name
* Selected a dedicated case folder destination
* Ensured proper storage location for case data

**Purpose:**

* Organizes all evidence and artifacts
* Maintains structured case management

📸 Screenshot: Case name and destination folder selection

  <img width="901" height="650" alt="Screenshot from 2025-12-29 20-58-18" src="https://github.com/user-attachments/assets/ec1acda3-d7db-4e45-b99b-f75be95e9fed" />


---

## Step 3: Entering Optional Case Information

Optional examiner and case details were entered.

**Information included:**

* Examiner name
* Organization
* Email address
* Phone number

**Purpose:**

* Improves case documentation
* Aligns with professional forensic reporting standards

📸 Screenshot: Optional case information filled

  <img width="903" height="587" alt="Screenshot from 2025-12-29 21-00-19" src="https://github.com/user-attachments/assets/9e549778-16cb-47ee-a3f5-5ab6aa1a243a" />


---

## Step 4: Adding a Data Source

The forensic disk image was added to the case.

**Data source selection:**

* Data Source Type: Disk Image or VM File
* Image Format: E01
* Source: Suspect Windows 10 virtual machine image

**Purpose:**

* Enables Autopsy to process and analyze the acquired evidence

📸 Screenshot: Data source selection screen

  <img width="1013" height="673" alt="Screenshot from 2025-12-29 21-03-15" src="https://github.com/user-attachments/assets/6a6f7512-d445-4275-a5dd-165e3d72ff3d" />


---

## Step 5: Configuring Ingest Modules

Relevant ingest modules were selected to extract forensic artifacts.

**Modules enabled:**

* Recent Activity
* File Type Identification
* Hash Lookup
* Extension Mismatch Detector
* Embedded File Extractor
* Keyword Search
* Email Parser
* Encryption Detection
* Interesting Files Identifier

**Coverage Provided Automatically:**

* Registry artifacts
* USB activity
* Prefetch data
* Recycle Bin artifacts
* Web artifacts
* Timeline events

**Purpose:**

* Ensures comprehensive artifact extraction
* Balances depth of analysis with processing efficiency

📸 Screenshot: Ingest modules selection

  <img width="1013" height="673" alt="Screenshot from 2025-12-29 21-05-10" src="https://github.com/user-attachments/assets/acdbb406-e4f1-4ded-92e1-55133ecd8a9b" />

<img width="299" height="406" alt="Screenshot from 2025-12-30 14-32-13" src="https://github.com/user-attachments/assets/3ac21a47-d6da-42d2-8e4f-89e432dfce19" />



---

## Step 6: Data Source Processing

After configuration, the data source ingestion process was started.

**What happened:**

* Autopsy parsed the disk image
* Extracted system and user artifacts
* Indexed files and metadata

**Purpose:**

* Converts raw disk data into analyzable forensic artifacts

📸 Screenshot: Data source processing in progress

  <img width="1013" height="673" alt="Screenshot from 2025-12-29 21-08-40" src="https://github.com/user-attachments/assets/fc1b2fcf-d417-4877-a19d-abeda1ce3539" />


---

## Step 7: Ingest Process Completion

The ingest process completed successfully.

**Outcome:**

* All selected modules executed
* Artifacts extracted without errors
* Case ready for analysis

📸 Screenshot: Ingest process completed

  <img width="1013" height="673" alt="Screenshot from 2025-12-29 21-12-45" src="https://github.com/user-attachments/assets/a779c52f-ca39-4017-beda-a3a3b2ca0a69" />


---

## Step 8: Initial Case Overview

After ingestion, Autopsy displayed a structured overview of the case.

**Visible sections included:**

* Data Sources
* Tags
* Operating System information
* User Accounts
* File Views
* Results

**Purpose:**

* Confirms successful ingestion
* Provides starting point for detailed analysis

📸 Screenshot: Autopsy case overview

  <img width="1023" height="730" alt="Screenshot from 2026-01-06 23-06-26" src="https://github.com/user-attachments/assets/99dc7bd6-a8fe-42f4-9c4a-61f7ed168684" />


---

## Step 9: USB Device Analysis

USB artifacts were examined to identify external device usage.

**Artifact location:**

* Data Artifacts → USB Device Attached

**Findings included:**

* Device identifiers
* Connection timestamps
* Confirmation of removable media usage

**Purpose:**

* Establishes physical USB interaction
* Supports data exfiltration investigation

📸 Screenshot: USB device attached artifacts

  <img width="1023" height="730" alt="Screenshot from 2026-01-06 23-09-53" src="https://github.com/user-attachments/assets/2d55c7fa-b1ad-45a8-8830-08e835671dad" />


---

## Step 10: Recent Documents Analysis

Recently accessed files were examined.

**Artifact location:**

* Data Artifacts → Recent Documents

**Findings included:**

* Accessed confidential files
* File paths
* Access timestamps

**Purpose:**

* Confirms user interaction with sensitive data

📸 Screenshot: Recent documents artifacts

  <img width="1023" height="730" alt="Screenshot from 2026-01-06 23-11-40" src="https://github.com/user-attachments/assets/31aa9d0a-8b0c-4595-ada1-a0085f1ba38a" />


---

## Step 11: Shell Bags Analysis

Shell Bag artifacts were analyzed to identify folder navigation history.

**Artifact location:**

* Data Artifacts → Shell Bags

**Findings included:**

* Access to CONFIDENTIAL folder
* Persistent folder access records

**Purpose:**

* Proves folder navigation even after deletion

📸 Screenshot: Shell Bags artifacts

  <img width="1023" height="730" alt="Screenshot from 2026-01-06 23-16-20" src="https://github.com/user-attachments/assets/ccb314b4-346f-4b1e-ab64-66318ca96e1f" />

<img width="757" height="553" alt="Screenshot from 2026-01-06 23-16-53" src="https://github.com/user-attachments/assets/7a6b9e05-e1fc-42fc-bdc0-9be17990fb17" />


---

## Step 12: File and Web Activity Analysis

File views and web-related artifacts were examined.

**Analysis included:**

* Web history
* Web cache
* Browser downloads
* Local file access via browser

**Purpose:**

* Identifies suspicious browsing behavior
* Supports malicious intent findings

📸 Screenshot: Web activity and cache artifacts

<img width="1022" height="752" alt="Screenshot from 2026-01-06 23-26-26" src="https://github.com/user-attachments/assets/4238b24a-598d-4b30-b7de-044fd8cb7daa" />

  <img width="1022" height="752" alt="Screenshot from 2026-01-06 23-26-51" src="https://github.com/user-attachments/assets/35073e87-6f14-4595-bcbe-6dda58ad5a78" />


---

## Step 13: Confidential File Access Evidence

Specific attention was given to evidence showing access to confidential data.

**Findings included:**

* Accessed confidential folder
* Opened sensitive files
* Correlated timestamps with USB usage

**Purpose:**

* Directly supports unauthorized access findings

📸 Screenshot: Confidential file access artifacts

  <img width="1022" height="752" alt="Screenshot from 2026-01-06 23-20-20" src="https://github.com/user-attachments/assets/f4b02032-b4ee-46f3-9844-c9a0f3167631" />

<img width="1022" height="752" alt="Screenshot from 2026-01-06 23-20-42" src="https://github.com/user-attachments/assets/1adaf6a0-82a4-4567-8d9f-6234f5b6487c" />

<img width="1022" height="752" alt="Screenshot from 2026-01-06 23-21-56" src="https://github.com/user-attachments/assets/5e8c29a2-5e88-43e3-9b48-a995a3f879e1" />

<img width="1022" height="752" alt="Screenshot from 2026-01-06 23-23-28" src="https://github.com/user-attachments/assets/7f62e106-6453-49e4-a0ed-db86411d3620" />


---

## Summary

The forensic analysis phase successfully revealed:

* USB device usage
* Access to confidential files
* Data exfiltration indicators
* Evidence deletion behavior
* Suspicious browser activity

All findings were derived from verified forensic artifacts and later documented in the final forensic report.


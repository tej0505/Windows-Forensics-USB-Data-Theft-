# Evidence Acquisition Using FTK Imager

This section documents the **complete forensic disk acquisition process** performed on the suspect Windows 10 virtual machine using **FTK Imager**.
The objective was to create a **forensically sound, bit-by-bit image** of the suspect system while preserving evidence integrity and maintaining a clear chain of custody.

All actions were performed from a **separate forensic analysis virtual machine**, ensuring that the suspect system was not altered during acquisition.

---

## Step 0: Powering Off the Suspect Virtual Machine

Before acquisition, the suspect Windows 10 virtual machine was **gracefully shut down**.

**Purpose:**

* Prevents data modification
* Avoids disk writes during acquisition
* Ensures evidence integrity

This step ensures the disk is captured in a static and consistent state.

📸 *Screenshot:* Suspect VM powered off

   <img width="882" height="524" alt="Screenshot from 2026-01-07 23-43-14" src="https://github.com/user-attachments/assets/0f385269-ec13-4911-a1f8-ad97300caa79" />

---

## Step 1: Launching FTK Imager

FTK Imager was opened on the **forensic analysis virtual machine** after confirming that the suspect virtual machine was fully powered off.

**Purpose:**

* Ensures no writes occur on the suspect disk
* Maintains forensic soundness
* Follows industry-standard acquisition practice

📸 Screenshot: FTK Imager application opened

<img width="1120" height="630" alt="image" src="https://github.com/user-attachments/assets/f7b74e45-763f-4867-a71e-1c46cce1cae9" />




---

## Step 2: Initiating Disk Image Creation

From the FTK Imager menu, the option **Create Disk Image** was selected to begin the acquisition process.

**Purpose:**

* Initiates the imaging workflow
* Ensures structured evidence handling

📸 Screenshot: Create Disk Image option selected

 <img width="900" height="550" alt="Screenshot from 2025-12-29 16-24-06" src="https://github.com/user-attachments/assets/0a7f00a4-fe52-4ee8-ba87-57d6db191367" />


---

## Step 3: Selecting the Source Evidence Type

The **Physical Drive** option was selected as the source type.

**Reason:**

* Captures the entire disk
* Includes allocated space, unallocated space, slack space, and deleted file remnants
* Provides the most complete forensic copy


## Step 4: Selecting the Suspect Source Drive

The suspect Windows 10 virtual disk was identified and selected from the list of available physical drives.

**Source Details:**

* VMware virtual disk
* Corresponds to the suspect Windows 10 VM

**Troubleshooting Note:**
If the suspect drive is not visible:

* Ensure the suspect VM is powered off
* Confirm the analysis VM has access to the virtual disk
* Run FTK Imager with administrative privileges

📸 Screenshot: Source drive selection

<img width="900" height="550" alt="Screenshot from 2025-12-29 16-32-24" src="https://github.com/user-attachments/assets/4b27afcb-abd0-46ff-824d-59c6f6bd7188" />

---

## Step 5: Selecting Image Destination Type

The destination image type was set to **E01 (Expert Witness Format)**.

**Why E01 was chosen:**

* Supports compression
* Allows segmentation
* Stores metadata within the image
* Supports hash verification

📸 Screenshot: Destination image type selection (E01)

 <img width="554" height="398" alt="Screenshot from 2025-12-29 16-36-42" src="https://github.com/user-attachments/assets/24b8b23f-be35-462f-8a59-089ea2a6b328" />


---

## Step 6: Entering Evidence Item Information

The Evidence Item Information screen was completed with case-specific details.

**Information entered included:**

* Case Number
* Evidence Number
* Unique Evidence Description
* Examiner Name

**Purpose:**

* Ensures proper documentation
* Supports chain of custody
* Aligns with legal and forensic standards

📸 Screenshot: Evidence Item Information filled

<img width="554" height="398" alt="Screenshot from 2025-12-29 16-39-04" src="https://github.com/user-attachments/assets/b3aec14f-9c91-445f-b154-ec85c61cac98" />


---

## Step 7: Selecting Image Destination and Filename

The destination folder for the forensic image was selected, and a descriptive filename was assigned.

**Details included:**

* Dedicated evidence storage directory
* Clearly named image file identifying the suspect system

**Purpose:**

* Prevents evidence mix-up
* Ensures organized evidence storage

📸 Screenshot: Image destination folder and filename selection


<img width="554" height="398" alt="Screenshot from 2025-12-29 16-41-31" src="https://github.com/user-attachments/assets/c29725e0-dcad-4877-ad03-19f26b5ddd01" />

---

## Step 8: Review of Disk Image Creation Summary

Before imaging began, FTK Imager displayed a summary of all selected options.

**Summary included:**

* Source drive
* Destination folder
* Image format
* Case metadata

**Purpose:**

* Final verification before acquisition
* Reduces risk of configuration errors

📸 Screenshot: Disk image creation summary screen


<img width="559" height="431" alt="Screenshot from 2025-12-29 16-42-22" src="https://github.com/user-attachments/assets/6835a63b-e7d5-4142-9cbb-a0bbcadca900" />


---

## Step 9: Disk Imaging Process Execution

The disk imaging process was initiated and allowed to complete without interruption.

**What happened:**

* Bit-by-bit copy of the disk created
* Progress monitored within FTK Imager

📸 Screenshot: Imaging process in progress

<img width="559" height="431" alt="Screenshot from 2025-12-29 16-47-25" src="https://github.com/user-attachments/assets/cca9c94a-bb28-4a1d-8610-c7197d3e6a29" />


---

## Step 10: Hash Calculation and Verification

Upon completion of imaging, FTK Imager automatically performed hash verification.

**Hashes Generated:**

* MD5
* SHA1

**Purpose:**

* Confirms image integrity
* Proves the image is an exact replica of the source disk

📸 Screenshot: Hash verification in progress

<img width="559" height="431" alt="Screenshot from 2025-12-29 16-59-33" src="https://github.com/user-attachments/assets/73896239-d679-4b6e-85cb-7c7a911080d8" />


---

## Step 11: Imaging Completion and Summary

FTK Imager displayed a final confirmation screen indicating successful image creation and verification.

**Outcome:**

* Image created successfully
* Hash verification confirmed a match
* No errors reported

📸 Screenshot: Image creation completion summary

<img width="630" height="463" alt="Screenshot from 2025-12-29 17-08-39" src="https://github.com/user-attachments/assets/b8521a58-6f07-4c27-b69d-28579d793ee2" />


---

## Step 12: Verification of Created Image Files

The destination folder was opened to confirm the presence of the created forensic image files.

**Observed Files:**

* Segmented E01 image files
* Associated metadata files

**Purpose:**

* Confirms evidence availability
* Prepares image for analysis in Autopsy

📸 Screenshot: File explorer showing E01 image files

<img width="678" height="188" alt="Screenshot from 2025-12-29 20-38-46" src="https://github.com/user-attachments/assets/24cd96d3-471d-486a-a919-ec26052bac59" />


---

## Summary

The evidence acquisition phase was completed using accepted forensic standards:

* Suspect system powered off before imaging
* Acquisition performed from a separate forensic workstation
* Full physical disk captured
* Cryptographic hash verification performed
* Evidence properly documented and preserved

The resulting forensic image was used for all subsequent analysis, timeline reconstruction, and reporting.

---


# Simulated Attacker Actions

This section documents the **step-by-step insider threat activity** performed on the suspect Windows 10 virtual machine.
All actions were intentionally executed in a controlled lab environment to generate forensic artifacts for investigation and learning purposes.

The attacker actions were performed **after the confidential data already existed on the system** and are documented below in chronological order.

---

## Step 1: USB Device Insertion

An external USB storage device was inserted into the suspect system.

**Purpose:**
This action simulates the introduction of removable media commonly used for data exfiltration.
It generates USB-related artifacts in the Windows registry, which are critical for proving external device usage.

📸 *Screenshot:* USB device attached to the system

   <img width="661" height="269" alt="Screenshot from 2025-12-29 12-40-43" src="https://github.com/user-attachments/assets/ca2609fc-9465-414b-8679-08fb127e0df0" />


---

## Step 2: Accessing Confidential Files

The attacker navigated to the pre-existing **CONFIDENTIAL** folder and opened sensitive files.

**Files accessed included:**

* salary.xlsx
* employee_details.xlsx
* client_list.xlsx

**Purpose:**
This step simulates unauthorized access to sensitive organizational data.
It generates artifacts such as Recent Documents, Shell Bags, and file access timestamps.

📸 *Screenshot:* CONFIDENTIAL folder and files opened

   <img width="787" height="350" alt="Screenshot from 2025-12-29 12-39-44" src="https://github.com/user-attachments/assets/ca920480-e9ec-4413-a6dc-1ca442351018" />



---

## Step 3: Copying Files to External USB Storage

The confidential files were copied from the local system to the connected USB device.

**Purpose:**
This action represents **data exfiltration** and is a key component of the insider threat scenario.
It generates file system artifacts that can be correlated with USB connection events.

📸 *Screenshot:* Files copied to USB drive

   <img width="936" height="654" alt="Screenshot from 2025-12-29 12-42-02" src="https://github.com/user-attachments/assets/d7b4da9d-61e8-49a0-8a96-5dd503337768" />

---

## Step 4: Deleting Confidential Files

After copying the data, the attacker deleted the **CONFIDENTIAL** folder and its contents from the system.

**Purpose:**
This action demonstrates an attempt to remove traces of unauthorized access.
It generates deleted file records and supports identification of anti-forensic behavior.

📸 *Screenshot:* Deletion of confidential files


   <img width="936" height="654" alt="Screenshot from 2025-12-29 12-45-18" src="https://github.com/user-attachments/assets/918e7d32-4878-474b-8134-5c453e00f72f" />


---

## Step 5: Clearing the Recycle Bin

The attacker emptied the Recycle Bin to permanently remove deleted files.

**Purpose:**
This step strengthens evidence of intentional concealment by ensuring files are no longer easily recoverable through standard means.

📸 *Screenshot:* Recycle Bin emptied


   <img width="792" height="576" alt="Screenshot from 2025-12-29 12-47-51" src="https://github.com/user-attachments/assets/769b372b-2dfc-48ab-a273-ce2aa882da0b" />


---

## Step 6: Suspicious Browser Activity (Keylogger Search & Download)

The attacker used a web browser to search for and access a keylogger-related website.

**Purpose:**
This activity indicates further malicious intent beyond data theft and generates browser history and download artifacts used in forensic analysis.

📸 *Screenshot:* Browser search and keylogger download page


   
   <img width="986" height="712" alt="Screenshot from 2025-12-29 12-50-29" src="https://github.com/user-attachments/assets/0a25ceb7-9a6d-4838-9ca5-96c925e8cb8d" />

---

## Step 7: USB Device Ejection

After completing the actions, the USB device was safely ejected from the system.

**Purpose:**
This marks the end of external device usage and helps define the data exfiltration window during timeline reconstruction.


---

## Summary

The above steps collectively simulate a realistic insider threat scenario involving:

* External device usage
* Unauthorized file access
* Data exfiltration
* Anti-forensic actions
* Malicious browsing behavior

Each action generated forensic artifacts that were later analyzed using FTK Imager and Autopsy to reconstruct the timeline and establish intent.

---

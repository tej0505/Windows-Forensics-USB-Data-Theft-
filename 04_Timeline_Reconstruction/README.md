# Timeline Reconstruction

This section documents the **reconstruction of events** using forensic artifacts extracted during analysis.
The purpose of timeline reconstruction is to correlate independent evidence sources into a **single chronological sequence**, allowing investigator intent and actions to be clearly established.

The timeline was created using **Autopsy’s built-in Timeline feature** based on the previously ingested disk image.

---

## Step 1: Opening the Timeline View

After completion of ingest processing, the **Timeline** view was opened from the Autopsy interface.

**Action performed:**

* Navigated to the Timeline tab

**Purpose:**

* Visualize all system and user events chronologically
* Centralize artifact correlation

📸 Screenshot: Timeline view opened

<img width="1022" height="629" alt="Screenshot from 2026-01-08 20-11-04" src="https://github.com/user-attachments/assets/49a259c8-2780-4de4-9679-b44edf096eac" />


---

## Step 2: Applying Timeline Filters

Relevant filters were applied to focus on investigation-specific activity.

**Filters applied included:**

* USB device events
* File created events
* File accessed events
* File deleted events
* Recent documents activity
* Web activity events

**Purpose:**

* Reduce noise from irrelevant system activity
* Highlight attacker-related behavior

📸 Screenshot: Timeline filters applied

<img width="1031" height="528" alt="image" src="https://github.com/user-attachments/assets/927c0f3a-053d-4a8f-82b0-e8529d0390b8" />

---

## Step 3: Identifying USB Connection Events

USB-related events were identified within the timeline.

**Artifacts correlated:**

* Registry-based USB connection records
* USB device attachment timestamps

**Purpose:**

* Establish the starting point of potential data exfiltration
* Define the attack window

📸 Screenshot: USB insertion events in timeline

  <img width="1021" height="648" alt="image" src="https://github.com/user-attachments/assets/fc5f4a11-ab11-45ef-87cc-8ea6c48d9a52" />


---

## Step 4: Correlating File Access Activity

File access events related to confidential data were identified.

**Artifacts included:**

* Recent Documents entries
* Shell Bag folder access records
* File open timestamps

**Purpose:**

* Confirm unauthorized access to sensitive files
* Correlate access with USB presence

📸 Screenshot: File access events in timeline

  <img width="1021" height="648" alt="image" src="https://github.com/user-attachments/assets/9ba51b7f-e79d-46ae-bff2-5f5ca8b5a645" />


---

## Step 5: Correlating File Deletion Activity

Deletion events were examined within the timeline.

**Artifacts included:**

* Deleted files
* Recycle Bin activity
* Permanent deletion timestamps

**Purpose:**

* Identify attempts to conceal activity
* Establish post-exfiltration behavior

📸 Screenshot: File deletion events in timeline

I did't find the timeline but it was confirm that file is deleted when i was doing analysis.

---

## Step 6: Correlating Web Activity

Web-related events were included in the timeline.

**Artifacts included:**

* Browser history entries
* Download activity
* Web cache timestamps

**Purpose:**

* Identify suspicious browsing behavior
* Support malicious intent assessment

📸 Screenshot: Web activity events in timeline

<img width="1021" height="685" alt="image" src="https://github.com/user-attachments/assets/2306a8d0-4576-43ad-b22f-d1904d0d53a8" />

<img width="1021" height="685" alt="image" src="https://github.com/user-attachments/assets/262d8ceb-7636-4691-848c-bd5c236e9fb9" />

---

## Step 7: Reconstructing the Full Sequence of Events

By correlating all artifacts, a complete event sequence was reconstructed.

**Reconstructed sequence:**

1. USB device connected to the system
2. Confidential folder accessed
3. Sensitive files opened
4. Files copied to external USB storage
5. Confidential files deleted
6. Recycle Bin cleared
7. Suspicious browser activity observed
8. USB device ejected

**Purpose:**

* Provide a clear, defensible narrative
* Support conclusions with multiple corroborating artifacts

📸 Screenshot: Full timeline reconstruction

<img width="1021" height="685" alt="image" src="https://github.com/user-attachments/assets/d5ee5ac0-3664-45e0-a552-93fe7fff897d" />

---

## Summary

The timeline reconstruction phase successfully demonstrated:

* Precise sequencing of attacker actions
* Strong correlation between USB usage and file activity
* Clear intent to exfiltrate and conceal data
* Consistency across independent forensic artifacts

This timeline formed the foundation for the final findings and conclusions presented in the forensic report.


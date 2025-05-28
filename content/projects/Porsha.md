+++
date = '2023-04-13T21:52:45+01:00'
draft = false
title = 'Porsha 🫆' 
summary = "A Python based Digital Forensic Toolkit."
technologies = ["Python", "PyQt6", "pytsk3", "Scapy", "Hachoir"]
+++


## Project Overview

**Porsha** is a foundational digital forensics toolkit with a user‑friendly **PyQt6** GUI. It provides three main forensic workflows: Disk Analysis, Network Analysis, and File Utilities, leveraging open‑source Python libraries under the hood.

---

### 🛠️ Features

- **📀 Disk Analysis**  
  - Open and parse raw disk images (`.dd`, `.img`, `.raw`).  
  - Display volume/partition layouts with `pytsk3`.  
  - Browse filesystem structures (FAT, NTFS) and view file metadata.

- **🌐 Network Analysis**  
  - Load and analyze PCAP/PCAPNG captures.  
  - Summarize packet counts and timestamps using `Scapy`.  
  - List unique IP/TCP/UDP conversations.

- **🧰 File Utilities**  
  - **Hashing:** Compute MD5 & SHA‑256 with Python’s `hashlib`.  
  - **Metadata Extraction:** Parse EXIF, document metadata via `Hachoir`.

- **🔄 Responsive GUI**  
  - Tasks run in background threads (`QThread`) to keep the interface interactive.  
  - Real‑time status updates and logging to `porsha_toolkit.log`.

---

### 🔗 Explore the Repository

- **GitHub Repository:** [Ashfaaq98/Porsha](https://github.com/Ashfaaq98/Porsha)

---

### 🚧 Work in Progress

This project is actively being improved. I’m currently exploring new features. Stay tuned for updates!
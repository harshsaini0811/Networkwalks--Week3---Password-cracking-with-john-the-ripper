<div align="center">

# 🔐 Password Cracking & Hash Analysis (Task 3)

**John the Ripper (JTR) • Hash Extraction • Dictionary Attack Lab**

![Curriculum](https://img.shields.io/badge/Lab-Networkwalks_Cybersecurity-0A66C2?style=for-the-badge)
![Tool](https://img.shields.io/badge/Tool-John_the_Ripper_(JTR)-1E293B?style=for-the-badge&logo=kalilinux&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-16A34A?style=for-the-badge)

</div>

---

## 📌 Overview

This repository documents the practical execution of **Task 3**, focused on installing **John the Ripper (JTR)** and auditing password-protected PDF files using hash extraction and wordlist-based cracking workflows. The objective is to understand how cryptographic file hashes are extracted, tested against structured dictionaries, and leveraged to recover weak credentials in an authorised lab environment.

---

## 🛠️ Tools & Components

| Tool / Resource | Purpose |
| :--- | :--- |
| **John the Ripper (JTR)** | Local CLI-based password auditing and offline hash cracking tool. |
| **Networkwalks Hash Calculator** | Extracts cryptographic `$pdf$` encryption hashes from locked PDF documents. |
| **Networkwalks Password Cracker** | Executes dictionary attacks by hashing wordlist entries and matching them against target `$pdf$` hashes. |
| **Password Wordlists** | Structured dictionaries containing common passwords and patterns used for offline testing. |

---

## ⚙️ Step-by-Step Methodology

1. **JTR Installation & Setup**
   * Installed and configured **John the Ripper (JTR)** on the local system and verified command-line functionality.
   * Organised the target locked PDF files and password dictionary directories for testing.

2. **Cryptographic Hash Extraction**
   * Loaded the encrypted PDF targets into the **Hash Calculator** utility to extract their underlying `$pdf$` hashes.

3. **Dictionary Attack Execution**
   * Submitted the extracted `$pdf$` hashes into the **Password Cracker** utility and JTR workflow.
   * Ran wordlist-driven matching against each target hash until valid plaintext passwords were identified.

4. **File Decryption & Flag Verification**
   * Used the recovered passwords to unlock the protected PDF documents and retrieve the challenge completion flags.

---

## 🛡️ Key Security Takeaways & Remediation

* **Dictionary & Pattern Weaknesses:** Common words and keyboard-walk sequences are cracked within seconds once a file hash is extracted.
* **Strong Passphrase Policy:** Sensitive documents should be encrypted using high-entropy passphrases (14+ characters combining uppercase, lowercase, digits, and special characters).
* **Modern Hashing Algorithms:** Systems storing user credentials should implement salted, memory-hard hashing functions such as **Argon2id** or **bcrypt** to resist high-speed offline cracking.

---

## 📁 Repository Structure

```text
Task-03-Password-Cracking-JTR/
├── README.md
└── screenshots/
    ├── 01-hash-extraction.png
    ├── 02-password-cracked.png
    └── 03-flag-captured.png
```

---

> **⚠️ Ethical & Spoiler Notice:** All hash extractions and password recovery exercises were performed strictly on authorised Networkwalks training files within an isolated educational environment. Recovered passwords and challenge flags are redacted from screenshots to avoid spoilers for other learners.

# Hacker101 CTF - Photo Gallery Writeup

## 1. Introduction to the Challenge and Objective
This write-up covers the resolution of the **Photo Gallery** challenge from **Hacker101 CTF**. The objective of this lab is to evaluate a web application that manages image uploads and galleries, exploiting potential flaws in input validation, file handling, and access controls to recover all hidden flags.

---

## 2. Reconnaissance & Surface Analysis
* **Core Functionality:** The platform allowed users to upload, view, and manage photos within structured albums or galleries.
* **Attack Surface:** Key focus areas included filename handling, extension filtering, parameter manipulation in requests, and session authorization across endpoints.

---

## 3. Exploitation Strategy
1. **File Upload Analysis:** Tested constraints around file types, extensions, and storage directories to bypass restrictions.
2. **Path / Parameter Manipulation:** Checked how references to images and galleries were handled to uncover unauthorized data access.
3. **Flag Recovery:** Successfully located and extracted all flags tied to restricted administrative galleries and hidden file functions.

---

## 4. Lessons Learned
* **Robust File Validation:** File uploads must validate true file types (using magic bytes/headers) rather than relying solely on file extensions.
* **Secure Storage & Access Control:** Uploaded user assets must be isolated and protected behind strict authorization checks.

---

## 5. References
* [Hacker101 CTF](https://hacker101.com/) - Official security challenge platform.
* [OWASP Unrestricted File Upload Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Unrestricted_File_Upload_Cheat_Sheet.html)

---

## Acknowledgments
Special thanks to **HackerOne** and the creators of **Hacker101** for providing an exceptional platform for hands-on web security practice.

---

> 📝 **Note on Flags:** All flags in this repository have been replaced with the standard placeholder format (`^FLAG^xxxxxxxx...$FLAG$`) to comply with platform guidelines.

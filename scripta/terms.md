# Terms of Service

**Last Updated:** September 20, 2026

**Applies to:** Scripta (v1.1.5 and above)

Welcome to **Scripta** ("the Service", "the Application", "we", "our"). Scripta is an open-source, hybrid text editor and live document viewer running directly in your web browser.

By accessing, installing, browsing, or using Scripta, you agree to be bound by these Terms of Service ("Terms"). If you do not agree with these Terms, please discontinue use of the Application immediately.

---

### 1. Open Source License & Intellectual Property

- **Apache License, Version 2.0:** Scripta is free and open-source software distributed under the terms of the **Apache License, Version 2.0** ("the License").
- **Your Rights:** Subject to the terms and conditions of the License, you are granted a perpetual, worldwide, non-exclusive, no-charge, royalty-free, irrevocable copyright and patent license to reproduce, prepare derivative works of, publicly display, sublicense, and distribute the work and derivative works in source or object form.
- **Attribution & Notice:** Any redistribution or derivative work must retain all original copyright, patent, trademark, and attribution notices from the source code, as specified in the Apache License 2.0.
- **Trademarks:** The name "Scripta", the creator name "TrongAJTT", and associated project logos and brand assets are protected under trademark principles. Nothing in this License grants permission to use trade names or trademarks except for customary descriptive use in acknowledging original authorship.

### 2. Client-Side Architecture & Data Custody

- **Local Processing:** Scripta operates primarily as a **client-side** application without intermediary backend servers. Your files, documents, text entries, line bookmarks, and automation scripts are processed and stored locally within your device's browser sandbox.
- **User Ownership:** You retain full and exclusive ownership of all intellectual property, text, code, and content that you open, create, or process within Scripta.
- **Data Custody & Backups:** Unless you explicitly choose to utilize optional third-party cloud sync features, Scripta does not maintain remote servers or automatic cloud backups of your files. You are solely responsible for maintaining adequate backups, version control, and data protection for all files and projects you edit.

### 3. File System & Directory Access

- **Native File & Folder I/O:** Scripta utilizes modern browser APIs (including the W3C File System Access API) to allow direct reading and writing to your local disk, individual files, or folders upon your explicit prompt authorization.
- **Workspace Folders:** When opening or saving a local folder as a workspace, Scripta may generate a `.workspace.scripta` manifest file inside the selected folder to retain workspace metadata and tab ordering.
- **Fallback Operations:** For browsers that do not support the File System Access API, file operations rely on standard browser file uploads, client-generated Blob downloads, and client-side ZIP packaging (via `fflate`).
- **File System Integrity:** While Scripta includes automatic session persistence via IndexedDB and external file change detection, we cannot guarantee against data loss resulting from hardware failure, operating system conflicts, or abrupt browser termination.

### 4. Optional Third-Party Cloud Integration & User Responsibilities

- **Third-Party Services:** Scripta provides optional integration with third-party cloud storage providers (specifically **GitHub** and **Dropbox**). All cloud interactions occur directly between your web browser and the third party's official APIs.
- **Account Credentials & Tokens:** You are solely responsible for obtaining, maintaining, configuring, and securing your own third-party credentials (such as GitHub Personal Access Tokens and Dropbox OAuth authorizations). You agree to abide by the respective terms of service and policies of each cloud provider.
- **Zero-Knowledge Encryption & Master Password Custody:**
  - Scripta provides optional client-side **AES-GCM-256** encryption for synchronized workspace files.
  - Because Scripta implements a strict Zero-Knowledge model, **we do not know, store, or recover your Master Password**.
  - **IMPORTANT:** If you lose or forget your Master Password, your encrypted cloud workspace files CANNOT be decrypted or recovered by Scripta developers. You assume 100% responsibility for securely retaining your Master Password.
- **No Liability for Cloud Provider Downtime or Data Loss:** We are not responsible for any service interruptions, API rate limits, file corruption, transmission errors, unauthorized account access, or data loss caused by or occurring within third-party cloud providers.

### 5. Scripts & Automation Engine (User-Provided Code)

- **User Execution Responsibility:** The Application includes a Script Manager and Web Worker execution engine allowing you to author, import, configure, and execute custom JavaScript/TypeScript scripts and functions.
- **Assumption of Risk:** All scripts and functions execute locally within your browser. You assume **100% responsibility and risk** for the code you write or import from third parties.
- **No Liability for Script Outcomes:** We are not responsible or liable for any unintended data mutation, text corruption, infinite loops, high memory consumption, or data loss caused by user-authored, imported, or executed scripts.
- **Untrusted Code Caution:** Never import or execute scripts or JSON bundles from untrusted sources.

### 6. Live Document & Code Previews

- Scripta provides real-time document and diagram renderers (including Markdown, Mermaid, HTML/CSS, SVG, Math/KaTeX, and WebAssembly Python).
- **Sanitization:** Web-based previews (such as HTML/CSS) are sanitized using client-side libraries (**DOMPurify**) to reduce security vulnerabilities. However, you should exercise prudent discretion when previewing untrusted documents or code snippets.

### 7. Disclaimer of Warranties

TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW:

- THE APPLICATION IS PROVIDED ON AN **"AS IS"** AND **"AS AVAILABLE"** BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, EITHER EXPRESS OR IMPLIED.
- THIS INCLUDES, WITHOUT LIMITATION, ANY IMPLIED WARRANTIES OR CONDITIONS OF TITLE, NON-INFRINGEMENT, MERCHANTABILITY, OR FITNESS FOR A PARTICULAR PURPOSE.
- WE DO NOT WARRANT THAT SCRIPTA WILL BE ERROR-FREE, UNINTERRUPTED, BUG-FREE, SECURE, COMPATIBLE WITH ALL BROWSER COMBINATIONS, OR FREE FROM DATA CORRUPTION UNDER ALL HARDWARE AND SOFTWARE CONDITIONS.

### 8. Limitation of Liability

IN NO EVENT AND UNDER NO LEGAL THEORY, WHETHER IN TORT (INCLUDING NEGLIGENCE), CONTRACT, OR OTHERWISE:

- SHALL THE AUTHOR(S), CONTRIBUTOR(S), OR COPYRIGHT HOLDER(S) BE LIABLE TO YOU FOR DAMAGES, INCLUDING ANY DIRECT, INDIRECT, SPECIAL, INCIDENTAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES OF ANY CHARACTER.
- THIS INCLUDES, BUT IS NOT LIMITED TO, DAMAGES FOR LOSS OF DATA, LOSS OF PROFITS, LOSS OF GOODWILL, WORK STOPPAGE, COMPUTER FAILURE OR MALFUNCTION, SYSTEM CRASHES, OR ANY OTHER COMMERCIAL LOSSES ARISING OUT OF THE USE OR INABILITY TO USE THE APPLICATION, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

### 9. Third-Party Libraries & Dependencies

Scripta is built upon modern open-source web technologies and libraries (such as CodeMirror 6, React, Vite, marked, Mermaid, DOMPurify, fflate, and Lucide Icons). Each third-party dependency is governed by its respective open-source license.

### 10. Modifications to Terms

We reserve the right to revise or replace these Terms at any time as the Application evolves. Any revisions will take effect upon publication of the updated Terms in this repository and within the Application documentation. Your continued use of Scripta following the posting of any changes constitutes acceptance of those revisions.

### 11. Community, Contributions & Support

Scripta is developed as a open-source project. If you have questions regarding these Terms, or wish to contribute to the codebase:

- **GitHub Repository:** [https://github.com/TrongAJTT/scripta](https://github.com/TrongAJTT/scripta)
- **Support email:** `trong.ajtt.dev@gmail.com`

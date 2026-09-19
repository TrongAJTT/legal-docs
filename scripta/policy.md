# Privacy Policy

**Last Updated:** September 20, 2026

**Applies to:** Scripta (v1.1.5 and above)

Your privacy is paramount and represents a foundational design principle of **Scripta** ("the Application", "we", "our"). Scripta is architected from the ground up as a **client-side, offline-first** hybrid text editor and live document viewer with no intermediary servers.

This Privacy Policy outlines how the Application functions, detailing our zero-data-collection philosophy and how your data remains exclusively under your ownership and control.

---

### 1. Zero Personal Data Collection

- **No User Accounts:** You do not need to register, create an account, log in, or provide any personal details (such as your name, email address, phone number, or billing information) to use any feature of Scripta.
- **No Identity Tracking:** We do not collect, process, record, or store any personal identifiers, IP addresses, geographical locations, or device fingerprints.

### 2. File & Document Processing Architecture

- **Strictly Client-Side Processing:** By default, all text editing, code inspection, document formatting, file conversions, and live previews occur entirely within your browser's local sandbox memory.
- **No Proprietary Backend or Intermediary Servers:** Scripta does not operate, route traffic through, or maintain any backend servers, proxy services, or proprietary cloud databases.
- **Local Memory Isolation:** Neither the developers nor any unauthorized third parties have access to the files you open or the code you execute in Scripta.

### 3. Optional User-Initiated Cloud Workspace Sync

Scripta includes an optional **Cloud Workspace Sync** feature allowing you to back up and synchronize workspaces directly between your browser and your personal cloud storage accounts:

- **Direct Client-to-Cloud Communication:** All synchronization requests are transmitted directly from your web browser to the respective cloud provider's official API endpoints (GitHub REST API or Dropbox API) over secure, encrypted HTTPS connections. There is no middleman or intermediary server.
- **Supported Providers:**
  - **GitHub:** Uses your Personal Access Token (PAT) to commit workspace files directly to a repository and branch specified solely by you.
  - **Dropbox:** Uses OAuth 2.0 PKCE (Proof Key for Code Exchange) to authenticate directly from your browser. Files are stored exclusively in your dedicated, sandboxed App Folder (`/Apps/Scripta Text Editor/workspaces/`), without access to any other files in your Dropbox.
- **Client-Side Zero-Knowledge Encryption (AES-GCM-256):**
  - When encryption is enabled, workspace content is encrypted entirely on your device using **AES-GCM-256** with a key derived via **PBKDF2** (100,000 iterations) from your chosen Master Password prior to transmission.
  - Neither Scripta developers nor the cloud storage providers possess the decryption key. Only parties with your Master Password can decrypt your synchronized files.
- **Local Credential Protection:**
  - Cloud access tokens (GitHub PAT or Dropbox OAuth tokens) are stored locally within your browser's IndexedDB.
  - Authentication tokens are encrypted using non-extractable device keys generated via the browser's native **Web Crypto API**, ensuring that credentials remain protected and tied solely to your local browser environment.
- **Revocation & Disconnection:** You can disconnect any cloud provider or delete local credentials at any time directly through the Application's Cloud Sync interface.

### 4. Zero Telemetry, Analytics, and Advertising

- **Zero Third-Party Telemetry:** Scripta does **NOT** integrate analytics SDKs, user behavior trackers, session recording tools, or telemetry frameworks (such as Google Analytics, Meta Pixel, PostHog, or Hotjar).
- **No Advertising Cookies:** We do not serve advertisements, use ad-tracking cookies, or engage in cross-site behavioral tracking.

### 5. Local Storage & Session Persistence

Scripta leverages browser-native local storage mechanisms solely to deliver a responsive, seamless desktop-like user experience:

- **IndexedDB:**
  - **Session Restoration & Crash Recovery:** Safely persists your open tabs, tab order, pinned/locked states, line bookmarks, and unsaved changes locally so you can resume work after closing or refreshing the browser.
  - **Automation Scripts & Functions:** Securely stores custom JavaScript scripts, reusable functions, and execution samples created or installed by you.
  - **Workspaces & Directory Handles:** Stores custom workspace groupings, metadata, and authorized local folder handles.
  - **Cloud Authentication State:** Stores device-encrypted cloud tokens and connection status.
- **LocalStorage:**
  - Saves your personal editor preferences (such as Dark/Light theme, font size, line numbers, word wrap, tab size, and UI layout toggles).
- **Security Boundary:** All data in IndexedDB and LocalStorage resides exclusively in your browser's origin-bound sandboxed storage (`Origin Private Storage`). No other website or external service can access this data.

### 6. Local File System & Directory Access API

- Scripta utilizes the modern W3C **File System Access API** (`showOpenFilePicker`, `showSaveFilePicker`, `showDirectoryPicker`) to open individual files or entire local folders as workspaces.
- **Explicit Authorization Only:** Reading from and writing to files or folders occurs solely when you explicitly grant permission through your operating system's native file/directory picker dialog.
- **Workspace Folder Manifest:** When linking a physical directory to a workspace, Scripta stores a lightweight `.workspace.scripta` configuration file inside the selected folder to retain workspace metadata and tab ordering locally.
- **No Background Scanning:** The Application cannot and does not scan, index, or access files or folders outside of the exact directories or files you explicitly select and authorize.
- **Cross-Browser Fallback:** On browsers without File System Access API support, file operations gracefully degrade to standard HTML5 file inputs (`<input type="file">`), Blob downloads, or client-generated ZIP archives (powered by `fflate`). All fallbacks execute 100% locally within browser memory without server interaction.

### 7. Script & Automation Engine Execution

- Scripta features an advanced client-side automation engine allowing you to write, edit, and execute custom text transformation scripts and modular functions.
- **Sandboxed Web Workers:** All user scripts execute in isolated Web Worker threads within your local browser process.
- **No External Code Transmission:** Script source code, arguments, execution inputs, and results are never transmitted to external servers for evaluation.

### 8. Live Document & Code Previews

- Previews for **Markdown**, **Mermaid Diagrams**, **HTML/CSS**, **SVG**, and **Math/KaTeX** are rendered directly in the browser DOM using client-side rendering engines.
- **HTML Sanitization:** HTML previews are sanitized locally using **DOMPurify** to help mitigate cross-site scripting (XSS) risks when previewing web content.
- **External Resources:** If you author or preview documents containing links to external assets (e.g., remote images or external stylesheets), your browser may fetch those assets directly from their respective remote hosts as standard HTTP GET requests.

### 9. Offline-First PWA (Progressive Web App)

- Scripta is an installable Progressive Web App powered by a Service Worker.
- Application static assets (HTML, CSS, JavaScript bundles, fonts, icons) are cached locally in your browser cache upon the initial visit.
- Once loaded, Scripta functions completely offline without any active network connection (e.g., in Airplane mode).

### 10. Your Data Rights & Deletion

You retain absolute custody and control over your data. You may inspect, export, or permanently delete your stored data at any time:

- **Exporting Data:** Use the **Export JSON** feature in Script Manager to create offline JSON backup files of your scripts and functions.
- **Clearing Session Data:** Close your open tabs to purge in-memory tab state.
- **Disconnecting Cloud Accounts:** Disconnect cloud providers in the Cloud Sync dialog to permanently remove stored authentication tokens and credentials.
- **Wiping Local Storage:** Clear your browser data (via your browser's Settings > Privacy / Site Settings > Clear Browsing Data / Storage for this site). This immediately and permanently deletes all IndexedDB databases, stored scripts, bookmarks, and saved preferences.

### 11. Changes to this Privacy Policy

We may update this Privacy Policy periodically to reflect architectural improvements or new capabilities in upcoming releases of Scripta. Any updates will be published with an updated _Last Updated_ revision date in this repository and within the Application's documentation.

### 12. Contact & Open Source Community

Scripta is open-source software developed transparently on GitHub. If you have questions, feedback, or concerns regarding security and privacy, please open an issue or start a discussion on our official repository:

- **GitHub Repository:** [https://github.com/TrongAJTT/scripta](https://github.com/TrongAJTT/scripta)
- **Support email:** `trong.ajtt.dev@gmail.com`

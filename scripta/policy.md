# Privacy Policy

**Last Updated:** September 18, 2026

**Applies to:** Scripta (v1.1.x and above)

Your privacy is paramount and represents a foundational design principle of **Scripta** ("the Application", "we", "our"). Scripta is architected from the ground up as a **100% client-side, offline-first** hybrid text editor and live document viewer.

This Privacy Policy outlines how the Application functions, detailing our zero-data-collection philosophy and how your data remains exclusively under your ownership and control.

---

### 1. Zero Personal Data Collection

- **No User Accounts:** You do not need to register, create an account, log in, or provide any personal details (such as your name, email address, phone number, or billing information) to use any feature of Scripta.
- **No Identity Tracking:** We do not collect, process, record, or store any personal identifiers, IP addresses, geographical locations, or device fingerprints.

### 2. Zero File & Document Transmission

- **Strictly Client-Side Processing:** All text editing, code inspection, document formatting, file conversions, and live previews occur entirely within your browser's local sandbox memory.
- **No Cloud Uploads:** The contents of your files, open tabs, notes, and workspaces are **NEVER** uploaded, transmitted across the Internet, or stored on any remote server, backend, or cloud database.
- **Local Memory Isolation:** Neither the developers nor any third parties have access to the files you open or the code you execute in Scripta.

### 3. Zero Telemetry, Analytics, and Advertising

- **Zero Third-Party Telemetry:** Scripta does **NOT** integrate analytics SDKs, user behavior trackers, session recording tools, or telemetry frameworks (such as Google Analytics, Meta Pixel, PostHog, or Hotjar).
- **No Advertising Cookies:** We do not serve advertisements, use ad-tracking cookies, or engage in cross-site behavioral tracking.

### 4. Local Storage & Session Persistence

Scripta leverages browser-native local storage mechanisms solely to deliver a responsive, seamless desktop-like user experience:

- **IndexedDB:**
  - **Session Restoration & Crash Recovery:** Safely persists your open tabs, tab order, pinned/locked states, line bookmarks, and unsaved changes locally so you can resume work after closing or refreshing the browser.
  - **Automation Scripts & Functions:** Securely stores custom JavaScript scripts, reusable functions, and execution samples created or installed by you.
  - **Workspaces:** Stores your custom workspace groupings and associations.
- **LocalStorage:**
  - Saves your personal editor preferences (such as Dark/Light theme, font size, line numbers, word wrap, tab size, and UI layout toggles).
- **Security Boundary:** All data in IndexedDB and LocalStorage resides exclusively in your browser's origin-bound sandboxed storage (`Origin Private Storage`). No other website or external service can access this data.

### 5. Local File System Access API

- Scripta utilizes the modern W3C **File System Access API** (`showOpenFilePicker`, `showSaveFilePicker`) to open and save files directly to your physical file system.
- **Explicit Authorization Only:** Reading and writing files occurs solely when you explicitly grant permission through your operating system's native file dialog.
- **No Background Scanning:** The Application cannot and does not scan, index, or access files or folders outside of the exact files you explicitly select.
- **Cross-Browser Fallback:** On browsers without File System Access API support, file operations gracefully degrade to standard HTML5 file inputs (`<input type="file">`) and direct memory-generated Blob downloads. These fallbacks remain 100% client-side without any server roundtrip.

### 6. Script & Automation Engine Execution

- Scripta features an advanced client-side automation engine allowing you to write, edit, and execute custom text transformation scripts and modular functions.
- **Sandboxed Web Workers:** All user scripts execute in isolated Web Worker threads within your local browser process.
- **No External Code Transmission:** Script source code, arguments, execution inputs, and results are never transmitted to external servers for evaluation.

### 7. Live Document & Code Previews

- Previews for **Markdown**, **Mermaid Diagrams**, **HTML/CSS**, **SVG**, and **Math/KaTeX** are rendered directly in the browser DOM using client-side rendering engines.
- **HTML Sanitization:** HTML previews are sanitized locally using **DOMPurify** to help mitigate cross-site scripting (XSS) risks when previewing web content.
- **External Resources:** If you author or preview documents containing links to external assets (e.g., remote images or external stylesheets), your browser may fetch those assets directly from their respective remote hosts as standard HTTP GET requests.

### 8. Offline-First PWA (Progressive Web App)

- Scripta is an installable Progressive Web App powered by a Service Worker.
- Application static assets (HTML, CSS, JavaScript bundles, fonts, icons) are cached locally in your browser cache upon the initial visit.
- Once loaded, Scripta functions completely offline without any active network connection (e.g., in Airplane mode).

### 9. Your Data Rights & Deletion

You retain absolute custody and control over your data. You may inspect, export, or permanently delete your stored data at any time:

- **Exporting Data:** Use the **Export JSON** feature in Script Manager to create offline JSON backup files of your scripts and functions.
- **Clearing Session Data:** Close your open tabs to purge in-memory tab state.
- **Wiping Local Storage:** Clear your browser data (via your browser's Settings > Privacy / Site Settings > Clear Browsing Data / Storage for this site). This immediately and permanently deletes all IndexedDB databases, stored scripts, bookmarks, and saved preferences.

### 10. Changes to this Privacy Policy

We may update this Privacy Policy periodically to reflect architectural improvements or new capabilities in upcoming releases of Scripta. Any updates will be published with an updated _Last Updated_ revision date in this repository and within the Application's documentation.

### 11. Contact & Open Source Community

Scripta is open-source software developed transparently on GitHub. If you have questions, feedback, or concerns regarding security and privacy, please open an issue or start a discussion on our official repository:

- **GitHub Repository:** [https://github.com/TrongAJTT/scripta](https://github.com/TrongAJTT/scripta)
- **Support email:** `trong.ajtt.dev@gmail.com`

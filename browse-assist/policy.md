# Privacy Policy for Browse Assist

**Last Updated:** November 9, 2026

**Effective Date:** November 9, 2026  

Browse Assist ("we", "us", or "our") is committed to protecting your privacy. This Privacy Policy explains our practices regarding data collection, usage, and disclosure when you install and use the **Browse Assist** browser extension (the "Extension").

---

## 1. Summary - Zero Data Collection

> **We do not collect, transmit, sell, or monetize your personal data.**  
> Browse Assist is built on a local-first architecture inspired by the "PowerToys for Web Browsing" philosophy. All operations, settings, and feature states remain strictly on your local device. We have no backend servers, no analytics dashboards, and zero tracking mechanisms.  
> Browse Assist adheres to the Chrome Web Store Developer Program Policies, including the Limited Use requirements. We do not use or transfer user data for personalized advertising, creditworthiness, or lending purposes.

---

## 2. Information We Do NOT Collect

Browse Assist does **NOT**:
- Collect personally identifiable information (such as your name, email address, physical address, phone number, or IP address).
- Track or record your browsing history, URLs visited, search queries, or web activity.
- Collect passwords, form inputs, credit card details, or any sensitive personal data.
- Read or transmit the contents of the web pages you visit to any remote server.
- Use analytics libraries, telemetry SDKs, crash-reporting third-party tools, or tracking cookies.

---

## 3. Data Stored Locally on Your Device

Browse Assist saves minimal configuration data solely to remember your preferences and ensure your custom settings persist across browser sessions:

- **User Preferences and Feature Settings:** Your chosen presets for Smooth Scrolling, Super Drag directions, video wheel steps, badge preferences, enabled/disabled feature toggles, and Quick Hub ordering.
- **Storage Mechanism:** Stored locally on your device using the browser's native `chrome.storage.local` API (via `@plasmohq/storage`).
- **Data Retention & Deletion:** This data remains on your machine until you manually reset your preferences via the extension settings or uninstall the extension. Uninstalling Browse Assist immediately and automatically removes all locally stored extension data from your browser.

---

## 4. Permissions & Justification

Browse Assist requests only the minimum set of permissions necessary to deliver its core Quality-of-Life functionality. Below is a complete breakdown of every permission requested in accordance with Chrome Web Store and Mozilla Add-ons policies:

| Permission | Purpose & Scope |
| :--- | :--- |
| **`storage`** | Required to save and persist your user preferences, toggled states, and layout configurations locally in `chrome.storage.local`. No data is synced to external servers. |
| **`contextMenus`**<br>*(or **`menus`** in Firefox)* | Required to display context menu shortcuts on right-click (such as *"Clean Link on Copy"*, *"Copy Link Text"*, and *"Markdown Link Copy"*). |
| **`clipboardWrite`** | Required to write clean links, Markdown links, or extracted color hex codes (from Color Picker) to your operating system clipboard **only upon your explicit click or action**. Browse Assist never reads from your clipboard (`clipboardRead` is not requested). |
| **`search`** | Used exclusively by the **Super Drag** feature to query your browser's default search engine when you highlight and drag text. |

*Note on Browser Commands & Action APIs:* Keyboard shortcuts (`commands`) and badge indicators (`action`) run locally within your browser's runtime environment and do not transmit or access personal data.

---

## 5. Third-Party Services & External Links

- **No Third-Party APIs:** The Extension operates entirely offline and does not integrate with any third-party APIs, CDNs, or advertising networks.
- **External Web Links:** The extension popup contains optional outbound links (e.g., links to documentation, the project homepage, GitHub repository, and voluntary sponsorship platforms like GitHub Sponsors or Buy Me a Coffee). Clicking these links opens external websites in a new tab. Those websites are governed by their respective privacy policies, and we encourage you to review them.

---

## 6. Children's Privacy

Browse Assist does not knowingly collect or solicit any personal information from children under the age of 13 (or under 16 in the European Union). Because we do not collect personal data of any kind, we comply with COPPA (Children’s Online Privacy Protection Act) and the EU General Data Protection Regulation (GDPR).

---

## 7. Changes to This Privacy Policy

We may update this Privacy Policy from time to time to reflect modifications to the Extension's features or changes in applicable regulatory requirements. Any updates will be reflected with a revised **Last Updated** date at the top of this document. Continued use of the Extension following any modifications constitutes your acknowledgment of the updated policy.

---

## 8. Contact Information

If you have any questions, suggestions, or concerns regarding this Privacy Policy or the security of Browse Assist, please contact:

- **Email:** [trong.ajtt.dev@gmail.com](mailto:trong.ajtt.dev@gmail.com)
- **GitHub Repository:** [https://github.com/TrongAJTT/browse-assist](https://github.com/TrongAJTT/browse-assist)
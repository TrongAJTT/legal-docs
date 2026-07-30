### Privacy Policy for Quiet Please

**Effective Date:** July 30, 2026

**Last Updated:** July 30, 2026

**1. Introduction**

Thank you for choosing Quiet Please. We are committed to protecting your privacy. This Privacy Policy explains our practices regarding data collection, usage, and the permissions required by the Quiet Please browser extension.

**2. Data Collection & Processing (Zero Data Policy)**

Quiet Please is designed with privacy as its core principle. **We do not collect, store, track, transmit, or sell any personal data, browsing history, or audio.**

- **Local Evaluation:** All tab muting decisions, URL pattern matching, and audio hardware detection are executed strictly **client-side** (locally on your device). Your visited URLs, page titles, and device labels never leave your browser and are never uploaded to any external servers.
- **Audio Privacy Guarantee:** Although browser security requires temporary microphone permission (`audio`) to unmask audio output device labels via `navigator.mediaDevices.enumerateDevices()`, the microphone audio stream is stopped immediately (`track.stop()`) and discarded. **No audio is ever recorded, listened to, or transmitted.**

**3. Local Storage and Preferences**

To maintain your preferred settings across sessions, Quiet Please saves your custom URL rules, audio device keywords, trigger modes, and manual mute overrides locally on your device using `chrome.storage.local`. This data is used solely to maintain your preferred settings and is never transmitted to our servers or any third parties.

**4. Browser Extension Permissions**

To function correctly as a smart tab mute manager, the Quiet Please browser extension requires specific permissions:

- **`audio` / Microphone:** Browser security APIs conceal hardware output device labels (e.g. "Headphones", "Realtek Speaker") until temporary access is requested. Used strictly to inspect output device names; stream is stopped and discarded immediately.
- **`tabs`:** Required to inspect active tab URLs and muting states to evaluate your custom Mutelist and Whitelist rules.
- **`storage`:** Used to save your settings, preferences, URL rules, and manual mute overrides locally on your device via `chrome.storage.local`.
- **`offscreen`:** Required in Chromium Manifest V3 browsers to run device label detection in the background without affecting browsing performance.
- **`host_permissions` (HTTP/HTTPS):** Required to evaluate webpage domain patterns against your custom URL rules.

**5. Third-Party Services**

Quiet Please operates independently. We do not use third-party analytics (such as Google Analytics), trackers, or advertising SDKs within our extension. Any donation or external repository links are governed by the privacy policies of those respective platforms.

**6. Changes to This Policy**

We reserve the right to update this Privacy Policy to reflect changes in extension features or browser security standards. Any changes will be reflected by the "Last Updated" date at the top of this document.

**7. Contact Us**

If you have any questions or concerns regarding this Privacy Policy or our privacy practices, please contact the developer via the official GitHub repository or support email: *trong.ajtt.dev@gmail.com*.

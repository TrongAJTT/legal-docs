### Privacy Policy for Imify

**Effective Date:** April 29, 2026

**Last Updated:** April 29, 2026

**1. Introduction**

Thank you for choosing Imify. We are committed to protecting your privacy. This Privacy Policy explains our practices regarding data collection, usage, and the permissions required by the Imify platform (including our web application and browser extension).

**2. Data Collection & Processing (Zero Data Policy)**

Imify is designed with privacy as its core principle. **We do not collect, store, track, transmit, or sell any personal data, browsing history, or images.** 

All image processing, format conversion, and compression are executed strictly **client-side** (locally on your device) utilizing WebAssembly (WASM) and Web Workers. Your files and data never leave your browser and are never uploaded to any external servers.

**3. Local Storage and Preferences**

To enhance your experience, Imify saves your tool presets, UI preferences, and workspace configurations locally on your device using LocalStorage or IndexedDB. This data is used solely to maintain your preferred settings across sessions and is never transmitted to our servers or any third parties.

**4. Browser Extension Permissions**

To function correctly as a powerful and seamless image processor, the Imify browser extension requires specific permissions. Here is exactly why we need them:
- **`contextMenus`:** Adds the "Imify" option to your right-click menu for quick image processing.
- **`host_permissions` (HTTP/HTTPS):** Allows Imify to capture and process images from any website you visit and supports the "Import from URL" feature.
- **`downloads`:** Allows the extension to save processed images or ZIP files directly to your local storage.
- **`offscreen`:** Required to use the OffscreenCanvas API for high-performance image processing in the background without affecting your browsing speed.
- **`sidePanel`:** Enables the interactive sidebar interface for advanced features like the Difference Checker and Image Inspector.
- **`storage`:** Used to save your custom tool presets and UI preferences locally on your device.
- **`content_scripts`:** Injects minimal, temporary UI elements (like progress indicators) to show processing status directly on the current webpage.

**5. Third-Party Services**

Imify operates independently. We do not use third-party analytics (like Google Analytics), trackers, or advertising SDKs within our tools. Our donation links (PayPal, GitHub, Buy Me A Coffee) are external and governed by the privacy policies of those respective platforms.

**6. Changes to This Policy**

We reserve the right to update this Privacy Policy to reflect changes in our features or legal requirements. Any changes will be reflected by the "Last Updated" date at the top of this document.

**7. Contact Us**

If you have any questions or concerns regarding this Privacy Policy or our privacy practices, please contact the developer via the official GitHub repository or support email: *trong.ajtt.dev@gmail.com*.

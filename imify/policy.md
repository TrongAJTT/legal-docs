### Privacy Policy for Imify

**Effective Date:** March 23, 2026

**Last Updated:** April 1, 2026

**1. Introduction**

Thank you for choosing Imify. We are committed to protecting your privacy. This Privacy Policy explains our practices regarding data collection, usage, and the permissions required by the Imify browser extension.

**2. Data Collection & Processing (Zero Data Policy)**

Imify is designed with privacy as its core principle. **We do not collect, store, track, transmit, or sell any personal data, browsing history, or images.** 
All image processing, format conversion, and compression are executed strictly **client-side** (locally on your device) utilizing WebAssembly (WASM) and Web Workers. Your files and data never leave your browser and are never uploaded to any external servers.

**3. Permissions Explained**

To function correctly as a seamless image processor, Imify requires specific browser permissions. Here is exactly why we need them:
*   **`<all_urls>` & `host_permissions`:** Required to allow the Context Menu (Right-click) to capture and fetch images from any website you are currently visiting, and to support the "Import from URL" feature.
*   **`content_scripts`:** Required to inject temporary UI elements (such as a Progress Bar or loading Spinner) into the current webpage so you can see the conversion status without opening a separate tab.
*   **`downloads`:** Required to automatically save the converted images, ZIP files, or PDFs directly to your local storage without repeatedly prompting the "Save As" dialog.

**4. Third-Party Services**

Imify operates independently. We do not use third-party analytics (like Google Analytics), trackers, or advertising SDKs within the extension.

**5. Changes to This Policy**

If we update this Privacy Policy to reflect changes in our features or legal requirements, we will update the "Effective Date" at the top of this document.

**6. Contact Us**

If you have any questions or concerns regarding this Privacy Policy or the open-source libraries we use, please contact the developer via the official GitHub repository or support email: *trong.ajtt.dev@gmail.com*.
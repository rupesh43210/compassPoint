# CompassPoint Privacy Policy

Last updated: October 15, 2026.

CompassPoint is published by the GitHub account rupesh43210. This policy describes the extension's current data handling. For privacy questions or support, contact rupesh.devbox@gmail.com.

## Local Data

API keys and OpenRouter-authorized keys are stored only in Chrome's extension session storage, restricted to trusted extension contexts. They are cleared by Disconnect, browser shutdown, extension disable/reload, or uninstall. Disconnect removes the local key, not the provider-issued key; revoke that key at OpenRouter if needed. Credentials are not encrypted against a compromised browser or operating system. OAuth state and PKCE verifiers are generated locally and held only for the authorization flow. Azure management tokens are used in memory and are not persisted. Voice preferences, provider endpoint/model metadata, enabled site origins, and up to 50 explicitly saved drafts are stored locally. Drafts can be deleted from the Drafts tab. Uninstalling the extension removes its storage.

## Website Access

The extension reads supported post/video metadata, visible captions, and visible transcripts only on sites the user explicitly enables. On request, it reads up to 20 loaded comments/replies (500 characters each), without deliberately collecting usernames or crawling more threads. Comment text can contain personal information; inspect the preview before sharing. It can locally capture a decoded video frame or loaded post image for a separate media-analysis request. When asked to analyse or generate on a YouTube video, it may briefly open YouTube's own transcript panel to read the transcript, then close it again and restore the page; the transcript stays in memory until you approve a request. When a post's picture cannot be read directly from the page because it is hosted on another site, the extension may request that same picture again from its host, without cookies, to read it. No picture is sent anywhere until you approve it in the review dialog. Comments, analysis, and captured images remain in memory and are cleared when the source changes; they are not persisted by the extension. It does not read passwords, extract login cookies, download full videos, or continuously upload live streams. Insertion fills an identifiable matching editor without submitting it or overwriting existing text. Other sites may support context capture but not insertion.

## Provider Requests

Test connection sends a small synthetic generation prompt, not page context. Refresh models sends authentication and model-list requests. Azure deployment refresh sends a separately supplied management token to management.azure.com. Inference keys are never sent to Azure management.

Analysis and generation send source metadata, transcript/captions, manually supplied context, selected comment samples, chosen preferences, and optionally a previously generated analysis directly to the selected provider after consent. Captured-image analysis requires separate media-sharing consent. Gemini public-YouTube analysis sends a native video URL to Google for video/audio processing with interaction storage disabled; Google processing, retention policies, costs, and eligibility restrictions still apply. Provider retention, billing, privacy policies, and geographic processing rules apply. The extension publisher has no backend receiving this data. A local model can avoid cloud inference when configured accordingly.

GitHub Copilot is supported through an optional companion program, the CompassPoint Copilot bridge, that the user installs and runs on their own computer. When that provider is selected, the extension sends the reviewed request only to the bridge's address on the same computer (127.0.0.1), together with a token the user pasted, which is held in session storage like other keys. The bridge forwards the text to GitHub Copilot under the user's own GitHub sign-in, using GitHub's official Copilot SDK; GitHub's terms, privacy statement and Copilot usage limits apply. The bridge accepts text only, disables all Copilot tools, does not log request content, and deletes each session after the answer. The extension publisher does not operate the bridge and receives nothing from it.

## Web Authorization

Official OpenRouter sign-in opens the provider's authorization UI through Chrome's identity API. An authorization code is exchanged directly with OpenRouter using S256 PKCE and callback/state verification. No password or Chrome profile email is requested by the extension.

## Telemetry and Controls

No analytics, advertising, or publisher telemetry is included. API error response bodies are not displayed or logged, to reduce accidental disclosure of credentials or prompts. Network activity is still visible to the browser's developer tools and the selected provider. Users can disconnect credentials, delete saved drafts, reset voice preferences, revoke permissions in Chrome, or uninstall the extension.

## Limited Use

CompassPoint uses website content and related page information only to provide its user-facing context capture, analysis, drafting, and insertion features. It does not sell user data, use it for advertising, or transfer it for unrelated purposes. Requested AI processing transfers the reviewed content directly to the user's selected provider. The publisher does not receive or read that content through a backend. CompassPoint's use of information received from Chrome APIs follows the Chrome Web Store User Data Policy, including the Limited Use requirements.

## Publisher and Contact

Publisher: rupesh43210, https://github.com/rupesh43210.

Privacy and support contact: rupesh.devbox@gmail.com.

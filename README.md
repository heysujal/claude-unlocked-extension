<div align="center">

# 😈 Claude Unlocked (Chrome Extension)

**The uncensored, unrestricted browser companion powered by Claude — running on ANY website.**

[![Manifest V3](https://img.shields.io/badge/Manifest-V3-blue.svg)](https://developer.chrome.com/docs/extensions/mv3/)
[![Status](https://img.shields.io/badge/Status-Unlocked-critical.svg)](#features)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

<br/>

<img src="icon-128.png" width="128" height="128" alt="Evil Claude Logo" style="border-radius: 24px;" />

<br/>
<br/>

</div>

---

## ⚡ What is Claude Unlocked?

The official **Claude in Chrome** extension uses an external URL-safety categorization service that restricts or completely blocks Claude from operating on many websites (such as **Reddit**, forums, social media, and internal developer sites).

**Claude Unlocked** removes these client-side and server-side safety gating mechanisms, allowing you to use Claude's powerful browser automation, page analysis, and sidepanel on **any website without domain restrictions**.

Plus, it comes with a custom **Devil Claude** icon theme! 😈

---

## ✨ Key Features

- 🌐 **Works on Reddit & Every Website**: Bypasses Anthropic's URL hash category check (`category0`, `category1`, `category2`, `category_org_blocked`), allowing Claude to navigate, read, summarize, and automate actions on Reddit and other previously restricted sites.
- ⚡ **Sidepanel on Demand**: Press <kbd>Cmd</kbd> + <kbd>E</kbd> (Mac) or <kbd>Ctrl</kbd> + <kbd>E</kbd> (Windows/Linux) anytime to toggle the Claude sidepanel directly beside your active tab.
- 🤖 **Full Browser Automation**: Supports multi-action browser batching — clicking, typing, form filling, scrolling, and navigating web applications smoothly.
- 👁️ **Visual & DOM Intelligence**: Reads accessibility trees, interactive page state, and captures high-resolution screenshots for multi-modal reasoning.
- 🔒 **Seamless Claude.ai Authentication**: Preserves the official extension key so OAuth authentication with `claude.ai` works out of the box without broken redirects.
- 🛠️ **MCP & Desktop Pairing**: Retains support for connecting with Claude Desktop and Model Context Protocol (MCP) servers.
- 🛑 **No Forced Auto-Updates**: Disables the Chrome Web Store update URL so your unlocked extension will not be silently overwritten with the restricted official build.

---

## 🚀 Installation Guide

Since this is an unlocked version, install it as an **unpacked extension** in Google Chrome:

1. **Disable / Remove Official Extension** (if previously installed):
   - Go to `chrome://extensions/`
   - Toggle off or remove the official Claude extension to avoid shortcut or port conflicts.

2. **Enable Developer Mode**:
   - In `chrome://extensions/`, enable the **Developer mode** toggle in the top-right corner.

3. **Load Unpacked**:
   - Click the **"Load unpacked"** button in the top-left corner.
   - Select the `claude-unlocked-extension` folder.

4. **Pin & Use**:
   - Pin the 😈 **Claude** icon to your toolbar.
   - Open any site (e.g., [reddit.com](https://reddit.com)), press <kbd>Cmd+E</kbd> or <kbd>Ctrl+E</kbd>, and start chatting!

---

## ⌨️ Shortcuts & Controls

| Action | Shortcut (Mac) | Shortcut (Win / Linux) |
|---|---|---|
| **Toggle Side Panel** | <kbd>⌘</kbd> + <kbd>E</kbd> | <kbd>Ctrl</kbd> + <kbd>E</kbd> |
| **Inspect Page** | Context Menu → *Ask Claude* | Context Menu → *Ask Claude* |

---

## 🛠️ Summary of Modifications

For transparency, here is what was modified from the original Chrome Web Store package:

| File | Change Description |
|---|---|
| `assets/ShortcutExecutionService-*.js` | Disabled `Wu.getCategory` URL safety checks, forced safe category return (`category0`), and disabled `wS`, `vS`, and `ft` blocking routines. |
| `assets/SavedPromptsService-*.js` | Bypassed `isUrlBlockedByManagedPolicy` so enterprise policy filters do not block custom URLs. |
| `manifest.json` | Cleaned `<all_urls>` patterns, added multi-resolution icon assets (16/32/48/128px), and removed `update_url` to prevent forced overwrites. |
| `icon-*.png` & `claude_icon.svg` | Custom dark crimson "Devil Claude" icons for toolbar and extensions menu. |

---

## ⚠️ Disclaimer & Legal Notice

> [!IMPORTANT]
> **Educational & Personal Use Only**
> 
> - This project is an independent modification created for educational, research, and interoperability purposes.
> - **Claude**, **Anthropic**, and associated trademarks, logos, and original codebase assets are the intellectual property of **Anthropic, PBC**.
> - This project is **not** affiliated with, endorsed by, or sponsored by Anthropic, PBC.
> - Use of this extension must comply with applicable website terms of service and acceptable use guidelines.

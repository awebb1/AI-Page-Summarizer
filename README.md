# Page Summarizer

A Chrome extension that summarizes any webpage using AI and saves the notes directly to your Obsidian vault.

![Page Summarizer](https://img.shields.io/badge/Chrome-Extension-8b5cf6?style=for-the-badge&logo=google-chrome&logoColor=white)
![AI Powered](https://img.shields.io/badge/AI-Powered-10b981?style=for-the-badge)
![Obsidian](https://img.shields.io/badge/Obsidian-Compatible-7c3aed?style=for-the-badge)

## ✨ Features

- 🎯 **One-Click Summarize** - Floating button appears on whitelisted sites
- 🌐 **Any Website** - Whitelist specific sites or enable on ALL sites
- 🤖 **AI-Powered** - Uses Claude (Anthropic) or GPT-4 (OpenAI)
- 📁 **Direct to Obsidian** - Saves notes via Obsidian's Local REST API
- 📋 **Progress Log** - See exactly what's happening during summarization
- 🎨 **Smart Extraction** - Automatically finds main content, ignores navigation

## 📦 Installation

### 1. Install Obsidian Plugin

1. Open Obsidian
2. Go to **Settings → Community Plugins → Browse**
3. Search for **"Local REST API"** by Adam Coddington
4. Install and enable it
5. Copy the **API Key** from the plugin settings

### 2. Install the Extension

1. Download or clone this repository
2. Open Chrome and go to `chrome://extensions/`
3. Enable **Developer mode** (toggle in top right)
4. Click **Load unpacked**
5. Select the `extension` folder

### 3. Configure

1. Click the extension icon in Chrome
2. Go to the **Settings** tab:
   - Choose AI Provider (Anthropic or OpenAI)
   - Enter your AI API key
   - Enter your Obsidian API key
3. Go to the **Folders** tab:
   - Select or type where to save notes
4. Go to the **Sites** tab:
   - Add sites you want to summarize

## 🚀 Usage

1. Navigate to any whitelisted webpage
2. Click the purple **Summarize** button (top-right corner)
3. Watch the progress log
4. Notes appear in Obsidian automatically!

## ⚙️ Settings

### Sites Tab
- **Add current site** - Whitelist the current page's domain
- **Enable on ALL sites** - Show the button everywhere
- **Manual add** - Add domains like `example.com` or wildcards like `*.example.com`

### Settings Tab
- **AI Provider** - Choose between Anthropic (Claude) or OpenAI (GPT-4)
- **AI API Key** - Your API key for the chosen provider
- **Obsidian API Key** - From Obsidian's Local REST API plugin

### Folders Tab
- **Select existing folder** - Choose from your vault's folders
- **Type new path** - Create new folder structure like `Notes/Summaries`
- **Vault Root** - Save directly to the vault root

## 💰 API Costs

Approximate costs per page summary:
- **Anthropic (Claude)**: ~$0.003-0.01
- **OpenAI (GPT-4o)**: ~$0.005-0.02

## 🔧 Troubleshooting

### Button doesn't appear
- Check the Sites tab - is the site whitelisted?
- Try enabling "Enable on ALL sites" temporarily
- Refresh the page after adding a site

### "Obsidian not connected"
- Make sure Obsidian is open
- Check that Local REST API plugin is enabled
- Verify the API key is correct

### Summary fails
- Check your AI API key is valid
- Make sure you have API credits
- Check the browser console for errors

## 🏗️ Project Structure

```
page-summarizer/
├── extension/
│   ├── manifest.json     # Extension configuration
│   ├── background.js     # API calls & orchestration
│   ├── content.js        # Button injection & page extraction
│   ├── popup.html        # Settings UI
│   ├── popup.js          # Settings logic
│   ├── styles.css        # Button & log styling
│   └── icons/            # Extension icons
└── README.md
```

## 📝 License

MIT License - feel free to use, modify, and distribute!

## 🤝 Contributing

Contributions welcome! Please open an issue or PR.

---

Made with 💜 for the note-taking community

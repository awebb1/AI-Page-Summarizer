# Page Summarizer

A Chrome extension that summarizes any webpage using AI and saves the notes directly to your Obsidian vault.

![Page Summarizer](https://img.shields.io/badge/Chrome-Extension-8b5cf6?style=for-the-badge&logo=google-chrome&logoColor=white)
![AI Powered](https://img.shields.io/badge/AI-Powered-10b981?style=for-the-badge)
![Obsidian](https://img.shields.io/badge/Obsidian-Compatible-7c3aed?style=for-the-badge)

## ✨ Features

- 🎯 **One-Click Summarize** - Floating button appears on whitelisted sites
- 🌐 **Any Website** - Whitelist specific sites or enable on ALL sites
- 🤖 **AI-Powered** - Uses Claude (Anthropic) or GPT (OpenAI) with dynamic model selection
- 📁 **Direct to Obsidian** - Saves notes via Obsidian's Local REST API
- 📋 **Progress Log** - Draggable log panel shows real-time progress
- 🎨 **Customizable Theme** - Pick any color for the button and UI
- 📚 **Study Mode** - Generate cheatsheets and study questions with revealable answers
- 💰 **Cost Tracking** - See token usage and estimated costs per summarization
- ✏️ **Custom Prompts** - Modify the AI prompt to suit your needs
- 🔄 **Draggable UI** - Button and log panel can be dragged anywhere on the page

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
   - Enter your AI API key (Anthropic or OpenAI - auto-detected)
   - Enter your Obsidian API key
   - Choose your preferred theme color
3. Go to the **Folders** tab:
   - Select or type where to save notes
4. Go to the **Sites** tab:
   - Add sites you want to summarize

## 🚀 Usage

1. Navigate to any whitelisted webpage
2. Hover over the floating button (bottom-right by default)
3. Click **Summarize**
4. Watch the progress in the draggable log panel
5. Notes appear in Obsidian automatically!

### Button Behavior
- The button stays tucked away (small, low opacity) until you hover over it
- Drag the button anywhere on the page - position is saved
- Drag the log panel by its header to reposition it

## 📚 Summarization Modes

### Standard Mode
Creates a comprehensive summary with key takeaways.

### Study Mode
Enhanced mode for learning, with two optional features:

#### 📝 Cheatsheet
- Extracts key concepts, important examples, and AI-generated insights
- Appends to a single file (e.g., `Cheatsheet.md`) across multiple pages
- Each page entry is collapsible with source links

#### ❓ Study Questions
- Generates quiz questions based on the content
- Answers are hidden using Obsidian callout syntax (click to reveal)
- Appends to a single file for comprehensive review

## ⚙️ Settings

### Sites Tab
- **Add current site** - Whitelist the current page's domain
- **Enable on ALL sites** - Show the button everywhere
- **Manual add** - Add domains like `example.com` or wildcards like `*.example.com`

### Settings Tab
- **AI API Key** - Your Anthropic or OpenAI API key (provider auto-detected)
- **AI Model** - Dynamically fetched from your API provider
- **Obsidian API Key** - From Obsidian's Local REST API plugin
- **Theme Color** - Pick any color for the button and UI accents
- **Reset Positions** - Reset button and log panel to default positions

### Folders Tab
- **Select existing folder** - Choose from your vault's folders (nested up to 4 levels)
- **Type new path** - Create new folder structure like `Notes/Summaries`
- **Vault Root** - Save directly to the vault root

### Mode Tab
- **Standard/Study** - Choose summarization mode
- **Cheatsheet** - Enable and configure cheatsheet file location
- **Study Questions** - Enable and configure study questions file location

### Prompt Tab
- **Custom Prompt** - Edit the AI prompt template
- **Variables** - Use `{title}`, `{url}`, `{content}` placeholders
- **Reset** - Restore the default prompt

## 💰 API Costs

The extension tracks and displays costs per summarization. Approximate costs:
- **Anthropic (Claude Sonnet)**: ~$0.003-0.01 per page
- **OpenAI (GPT-4o)**: ~$0.005-0.02 per page

Costs vary based on page length and model selected. Study mode with cheatsheet and questions enabled will use 3x the tokens (3 separate API calls).

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

### Models not loading
- Verify your API key is correct
- Check your internet connection
- The extension fetches models directly from Anthropic/OpenAI APIs

## 🏗️ Project Structure

```
page-summarizer/
├── extension/
│   ├── manifest.json     # Extension configuration
│   ├── background.js     # API calls & orchestration
│   ├── content.js        # Button injection & page extraction
│   ├── popup.html        # Settings UI
│   ├── popup.js          # Settings logic
│   └── styles.css        # Button & log styling
├── LICENSE
└── README.md
```

## 📝 License

MIT License - feel free to use, modify, and distribute!

## 🤝 Contributing

Contributions welcome! Please open an issue or PR.

---

Made with 💜 for the note-taking community

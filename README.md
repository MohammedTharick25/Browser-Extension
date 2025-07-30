# 📌 Leads Tracker Chrome Extension

**Leads Tracker** is a lightweight Chrome extension that helps you save, view, and manage URLs (leads) directly from your browser. You can add links manually, capture the current tab, and clear your entire list with a simple double-click.

---

## ✨ Features

- **Save Input**: Manually enter and save a URL.
- **Save Tab**: Automatically save the URL of the active tab.
- **View Leads**: Display saved URLs as clickable links.
- **Delete All**: Double-click the delete button to clear all saved leads.
- **Persistent Storage**: Data is stored using `localStorage`.

---

## 🔧 Installation

1. Download or clone this repository to your computer.
2. Open Chrome and navigate to `chrome://extensions/`.
3. Enable **Developer mode** (toggle in the top-right).
4. Click **"Load unpacked"** and select the project folder.
5. The **Leads Tracker** extension will appear in your extensions bar.

---

## 🧠 How It Works

- **Popup UI (`index.html`)**  
  Contains an input field and three buttons:
  - `SAVE INPUT` → Adds the typed URL to the list
  - `SAVE TAB` → Captures the URL of the current tab
  - `DELETE ALL` → Clears the list when double-clicked

- **Script (`index.js`)**  
  - Stores leads in an array
  - Saves them to `localStorage`
  - Renders links inside a `<ul>` element
  - Uses `chrome.tabs.query` to get the current tab’s URL

- **Styling (`index.css`)**  
  Clean and minimal layout with green highlight color for buttons and links

---

## 📄 manifest.json

Here’s the extension configuration you’re using:

{
  "manifest_version": 3,
  "version": "1.0",
  "name": "Leads tracker",
  "action": {
    "default_popup": "index.html",
    "default_icon": "icon.png"
  },
  "permissions": ["tabs"]
}

## Author
Developed by Mohammed Tharick

# Grocery Shopping Assistant v3.2.2

Mobile-first Progressive Web App (PWA) for building a grocery shopping list and generating a research-ready ChatGPT prompt.

## GitHub Pages

This folder is ready to publish directly from the `main` branch root using GitHub Pages. No Node.js server, npm install, `.env` file, or API key is required.

1. Create a GitHub repository (for example `grocery-shopping-assistant`).
2. Upload the contents of this folder to the repository root. Do **not** upload this folder as an extra nested directory. `index.html` should be at the repository root.
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Choose branch **main** and folder **/ (root)**, then save.
6. Open the published HTTPS address in Safari on your iPhone.
7. Tap **Share → Add to Home Screen**.

## Local iPhone data

The app stores the following data in the browser's local storage on the iPhone: 

- Grocery Library
- Current Shopping List
- Selected retailers
- ZIP/local area
- Maximum-store setting
- Search preferences
- Shopping strategy
- Additional instructions

The app does not send this shopping data to GitHub, SerpApi, or a separate application server. The generated shopping prompt is only sent to ChatGPT when you copy/share/paste it yourself.

**Important:** clearing Safari website data, deleting the app/site data, or using a different browser/device can remove or separate the locally stored data. The current version intentionally keeps the shopping data on the iPhone rather than in a cloud database.

## Updating the app

When a newer version is published to the same GitHub Pages site, the service worker can cache the new application files. Close and reopen the Home Screen app if an update does not appear immediately. Your local shopping data is stored under a separate local-storage key and is retained across app-code updates.

## No SerpApi

SerpApi is not used or required. ChatGPT performs the current web research after the generated prompt is supplied to ChatGPT.


## Data safety
Shopping lists, grocery library, and preferences are stored locally in the browser on the device. v3.2.2 adds **Backup My Data** and **Restore Backup** so you can save a JSON backup before clearing Safari data or moving to another device.

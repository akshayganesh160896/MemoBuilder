# Memo Builder

Memo Builder converts pasted Excel-style name data into a simple name/count table.

## What it does
- Accepts copied content from Excel (rows and cells).
- Handles names in separate cells.
- Handles multiple names in one cell when separated by commas.
- Outputs one row per individual name with total occurrence count.
- Sorts output by count first, then alphabetically by last name.
- Attempts to merge likely spelling variants (typos) into one counted name.
- Highlights merged rows so you can review possible typo merges.

## How to use
1. Open `index.html` in your browser.
2. Paste your Excel data into the input box.
3. Click **Build Memo Table**.
4. Use **Copy 2-Column** to copy `Name` + `Count` directly for Excel.
5. Use **Download TSV** or **Download CSV** to save the output.

## Publish (fastest)
### Option 1: Netlify Drop (no Git required)
1. Go to [Netlify Drop](https://app.netlify.com/drop).
2. Drag the full `Memo Builder` folder onto the page.
3. Netlify gives you a live URL immediately.

### Option 2: GitHub Pages
1. Create a new GitHub repo and upload all files in this folder.
2. In repo settings, open **Pages**.
3. Set source to **Deploy from branch** and pick `main` + `/ (root)`.
4. Save and wait for the Pages URL to appear.

## Install as an app
- This project now includes PWA files (`manifest.webmanifest` + `sw.js`).
- After publishing over HTTPS, open the site in Chrome/Edge and click **Install app** from the address bar/menu.
- On iPhone/iPad Safari: Share -> **Add to Home Screen**.

## Notes
- Counting is case-insensitive (`john doe` and `John Doe` count together).
- Display formatting normalizes names to title case.

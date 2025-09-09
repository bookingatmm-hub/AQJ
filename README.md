# Order Form (Tally-like Prefill Form)

A minimal static order form (inspired by Tally.so) that supports **Google Sheets prefill**, hidden fields, locked catalogue/price, and Google Drive PDF embedding.  
Deployed with **GitHub Pages**.

---

## 🚀 Features
- Hidden fields for **SNO, PARTY, DISTRICT, STATE, PHONE**.
- Locked (read-only) fields for **Catalogue Number & Price**.
- Prefill values from:
  - **Google Sheets** (published to web).
  - **Direct URL query parameters** (e.g., `?sno=101&party=ABC&price=500`).
- Embed daily-changing **Google Drive PDF** via preview link.
- Submit to **Formspree** (or any webhook endpoint).
- Minimal UI with theme colors:  
  - Orange `#F37021`  
  - Navy `#1E2A38`  

---

## 📂 Files
- `index.html` → Main form page
- `styles.css` → Styling (modern + minimal)
- `logo.png` → Your logo file (place in repo root)
- `README.md` → This guide

---

## ⚙️ Setup

### 1. Clone or Create Repository
1. Go to [GitHub](https://github.com).
2. Create a **new repository** (public or private).
3. Clone it locally or upload these files:
   - `index.html`
   - `styles.css`
   - `README.md`
   - `logo.png`

### 2. Publish Google Sheet
1. Open your Google Sheet.
2. Go to **File → Share → Publish to web**.
3. Copy the **CSV link**.
4. Replace the value of `PUBLISHED_SHEET_CSV_URL` inside `index.html`:
   ```js
   const PUBLISHED_SHEET_CSV_URL = "https://docs.google.com/spreadsheets/d/e/.../pub?output=csv";

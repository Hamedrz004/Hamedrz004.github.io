# Google Sheet Categorizer (Dify Workflow)

This project is a simple web form that connects to a [Dify](https://dify.ai) workflow for categorizing data in a Google Sheet.  
It allows you to enter the sheet details and category labels, then sends the data securely to your workflow through a Netlify proxy.

---

## 🚀 Features
- Collects user input for:
  - **Sheet ID**
  - **Sheet label** (e.g., `Sheet1`)
  - **Input range** (`read_from` → `read_to`)
  - **Output range** (`write_from` → `write_to`)
  - **Categories** (e.g., `1-objects 2-fruits ...`)
- Sends the data to your Dify workflow via a secure proxy.
- Displays the workflow response directly on the page.

---

## 🖥️ Usage
1. Open the site in your browser.
2. Fill in the required fields:
   - Sheet ID
   - Label (e.g., `Sheet1`)
   - Input range (e.g., `A1` → `A5`)
   - Output range (e.g., `B1` → `B5`)
   - Categories (e.g., `1-objects 2-fruits ...`)
3. Click **Run Workflow**.
4. The response from Dify will appear below the form.

---

## 🧩 Example Form Code
```html
<form id="sheetForm">
  <label for="sheet_id">Sheet ID</label>
  <input id="sheet_id" name="sheet_id" required />

  <label for="label">Label of the Sheet (e.g. Sheet1)</label>
  <input id="label" name="label" required />

  <label for="read_from">Read from cell</label>
  <input id="read_from" name="read_from" value="A1" required />

  <label for="read_to">To cell</label>
  <input id="read_to" name="read_to" value="A5" required />

  <label for="write_from">Write from cell</label>
  <input id="write_from" name="write_from" required />

  <label for="write_to">To cell</label>
  <input id="write_to" name="write_to" required />

  <label for="categories">Categories</label>
  <textarea id="categories" name="categories" rows="3" required></textarea>

  <button type="submit">Run Workflow</button>
</form>

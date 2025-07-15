# XSS-Vulnerable User Search Page

A simple static HTML “User Search” page that demonstrates a DOM-based XSS vulnerability via unsanitized use of `innerHTML`. **Do not deploy this in production.** It’s provided for educational and testing purposes only.

---

## 📄 File

- `index.html` — Contains the full HTML/CSS/JS for the vulnerable user search page.

---

## 🚀 Features

- **Hard-coded user list** (15 example Singaporean-style users)  
- **Live search** filtering as you type  
- **URL-backed query**: reads and writes `?q=…` parameter without reloading  
- **Vulnerable display** of the search query via `innerHTML` (DOM-based XSS)

---

## ⚠️ Vulnerability

The `<p id="query">` element is updated with:

```js
queryDisplay.innerHTML = "Query: " + userInput;

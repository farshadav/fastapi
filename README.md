# FastAPI Wikipedia Search Comparison 🧠⚡

This is a simple FastAPI project that demonstrates how a **small change in an API parameter** can drastically improve the accuracy of search results — using Wikipedia as the example.

### 🧪 Why this app?

While exploring the Wikipedia Python API, I noticed odd behavior:
- Searching for `"pizza"` gave me a result about **town squares**
- Searching for `"piazza"` gave me a result about **Italian food**

That’s when I learned that Wikipedia’s API uses **auto-suggest and fuzzy matching**, which can lead to surprising bugs.

---

### 💡 What this app shows

This app includes **two search versions**, side by side:

- 🔹 **Version A – Basic**  
  Uses `wikipedia.summary(query)` — the default behavior (fast, but error-prone)

- 🔸 **Version B – Improved**  
  Uses `wikipedia.page(query, auto_suggest=False)`  
  Adds a fallback to `wikipedia.search()` for better accuracy

You can run both and compare how a single parameter (`auto_suggest`) improves reliability.

---

### 🚀 Quickstart

#### 1. Clone this repo
```bash
git clone https://github.com/yourusername/fastapi-wikipedia-comparison.git
cd fastapi-wikipedia-comparison

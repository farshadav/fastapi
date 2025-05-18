# FastAPI Wikipedia Search Comparison 🧠⚡

This is a simple FastAPI project that demonstrates how a **small change in an API parameter** can drastically improve the accuracy of search results — using Wikipedia as the example.

### 🧪 Why this app?

While exploring the Wikipedia Python API, I noticed odd behavior:
- Searching for `"pizza"` gave me a result about **town squares**
- Searching for `"piazza"` gave me a result about **Italian food**

That’s when I learned that Wikipedia’s API uses **auto-suggest and fuzzy matching**, which can lead to surprising bugs.

### 💡 What this app shows

This app includes **two search versions**, side by side:

- 🔹 **Version A – Basic**  
  Uses `wikipedia.summary(query)` — the default behavior (fast, but error-prone)

- 🔸 **Version B – Improved**  
  Uses `wikipedia.page(query, auto_suggest=False)`  
  Adds a fallback to `wikipedia.search()` for better accuracy

You can run both and compare how a single parameter (`auto_suggest`) improves reliability.

### 🚀 Quickstart

#### 1. Clone this repo
```bash
git clone https://github.com/farshadav/fastapi.git
cd fastapi
```

#### 2. Install dependencies
```bash
pip install fastapi uvicorn wikipedia jinja2 python-multipart
```

#### 3. Run the app
```bash
python main.py
```

#### 4. Open in browser
```
http://127.0.0.1:8000/
```

Try searching for terms like:
- `pizza`
- `piazza`
- `apple`
- `python`

### 📂 Project Structure

```
.
├── main.py          ← FastAPI app with both versions
└── templates/
    ├── home.html    ← Input forms
    └── result.html  ← Displays search results
```

### 📎 Built with

- [FastAPI](https://fastapi.tiangolo.com/)
- [Wikipedia API (python-wikipedia)](https://pypi.org/project/wikipedia/)
- [Jinja2](https://jinja.palletsprojects.com/)

### 🤔 Ideas for extension

- Add language selection (e.g., DE, FR, FA)
- Let users choose from disambiguation options
- Track search analytics or build a mini dashboard

### 🙌 Contributing

PRs and suggestions welcome. This is a learning-first project — clean, clear, and beginner-friendly.

### 🧠 License

MIT – use it, build on it, remix it.

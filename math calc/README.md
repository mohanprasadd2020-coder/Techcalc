# Simple static HTML server (Flask)

This small Flask app serves `index.html` at `/` and exposes a `/files` page that links to all `.html` files found in the project root.

Prerequisites

- Python 3.7+
- (optional) virtual environment

Quick start (PowerShell on Windows):

```powershell
# from project root (where index.html lives)
python -m venv .venv; .\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
python app.py
```

Open http://127.0.0.1:5000/ in your browser to see `index.html` or visit http://127.0.0.1:5000/files to see a list of links to all HTML files.

Notes

- This is a tiny development helper. Do not use this server in production as-is.
- The server prevents basic path traversal and only serves `.html` files found in the project root.

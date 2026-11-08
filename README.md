# MailSentra Documentation

Public user documentation for the MailSentra WordPress plugin.

## Preview locally

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python -m mkdocs serve
```

Open the local URL printed by MkDocs. Build the site with:

```powershell
python -m mkdocs build --strict
```

GitHub Actions deploys the site to GitHub Pages when changes are pushed to `main`.
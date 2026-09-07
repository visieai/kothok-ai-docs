# Kothok AI Documentation

Customer documentation for **Kothok AI**, the shopping assistant for online stores.
Built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) and
published to GitHub Pages.

**Live site:** <https://docs.kothok.ai/>

## What's in here

| Path | What it holds |
|------|---------------|
| `docs/` | All page content, as plain Markdown |
| `mkdocs.yml` | Site config and the left-hand navigation (`nav:`) |
| `requirements.txt` | Python dependency (`mkdocs-material`) |
| `.github/workflows/deploy.yml` | Builds and deploys to GitHub Pages on push to `main` |
| `docs/CNAME` | Custom domain; copied to the site root at build time |

### Page structure

```
docs/
├── index.md                     # landing page
├── getting-started/             # for shop owners: onboarding → go-live
│   ├── overview.md
│   ├── connect-your-store.md
│   ├── go-live-checklist.md
│   └── keeping-current.md
├── assistant/                   # how the assistant behaves
│   ├── what-it-does.md
│   ├── channels.md
│   └── limitations.md
├── developer/                   # for developers: import API + widget
│   ├── overview.md
│   ├── import-methods.md
│   ├── push-api.md
│   ├── product-fields.md
│   ├── feed-csv-columns.md
│   ├── widget.md
│   └── testing.md
├── faq.md
├── roadmap.md
└── support.md
```

## Edit the docs

1. Content is plain Markdown in `docs/`. Edit a file, or add a new `.md` file.
2. If you add a page, add it to the `nav:` list in `mkdocs.yml`, or it won't appear
   in the sidebar.
3. Commit and push to `main`. The site rebuilds and redeploys automatically.

## Preview locally

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve
```

Open <http://127.0.0.1:8000>. The preview reloads as you edit.

Before pushing, it's worth running the same strict build the CI runs, which fails on
a broken link or a page missing from `nav:`:

```bash
mkdocs build --strict
```

## How publishing works

Push to `main` → the workflow in `.github/workflows/deploy.yml` builds the site with
`mkdocs build --strict` and deploys it to GitHub Pages.

The following are already set up and do not need to be repeated:

- **Pages source:** GitHub Actions (Settings → Pages).
- **Custom domain:** `docs.kothok.ai`, set via `docs/CNAME` and repo settings, with a
  `CNAME` DNS record pointing `docs` → `visieai.github.io`.
- **Repo visibility:** public (GitHub Pages needs this, or a paid plan for a private
  repo).

## Placeholders to replace

A few stand-in values live in the content. Search and replace them with the real
ones before sharing the site widely:

- `YOUR-WIDGET-HOST` and `THE_SHOPS_PUBLIC_KEY` — in `docs/developer/widget.md`
- `support@example.com` — in `docs/support.md`

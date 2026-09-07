# Kothok AI Documentation

Customer documentation for Kothok AI, the shopping assistant for online stores.
Built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) and
published to GitHub Pages.

## Read it

Once published, the site is at:

```
https://docs.kothok.ai/
```

> **Note on GitHub Pages and private repos.** GitHub Pages on a private repo needs a
> paid GitHub plan (Pro, Team, or Enterprise). On the free tier, make the repo
> public to publish.

## Edit it

The content is plain Markdown in `docs/`. The site structure (the left-hand nav) is
the `nav:` list in `mkdocs.yml`.

To add a page: create a Markdown file under `docs/`, then add it to `nav:`.

## Preview it locally

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve
```

Then open http://127.0.0.1:8000. The preview reloads as you edit.

## Publish it

Push to `main`. A GitHub Actions workflow
(`.github/workflows/deploy.yml`) builds the site and deploys it to GitHub Pages.

One-time setup in the repo: **Settings → Pages → Build and deployment → Source:
GitHub Actions**.

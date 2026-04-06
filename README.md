# BetterSEQTA+ documentation

This repository contains the **BetterSEQTA+** documentation site, generated with **[Zensical](https://zensical.org/)** from Markdown. Pages under `docs/` consolidate user guides and material aligned with **[BetterSEQTA-Plus/docs](https://github.com/BetterSEQTA/BetterSEQTA-Plus/tree/main/docs)** on GitHub; update this site when upstream docs change significantly.

## Important: set your `site_url` before publishing

If you **clone or fork** this repo, you must edit **`zensical.toml`** and set **`[project].site_url`** to the real base URL where your built site will be published.

1. Open **`zensical.toml`** in the repository root.
2. Find **`site_url`** (under **`[project]`**).
3. Replace the placeholder with your GitHub Pages URL, for example:

   `https://YOUR_GITHUB_USERNAME.github.io/YOUR_REPO_NAME/`

   Use your actual GitHub username and the repository name that hosts these docs. Include the trailing slash unless your host expects otherwise.

**Why this matters:** Zensical uses `site_url` for canonical links, **instant navigation**, **sitemap**, and related features. Wrong or placeholder values break those behaviors when the site is deployed. See the [Zensical `site_url` documentation](https://zensical.org/docs/setup/basics/#site_url).

## Local setup

Python 3.10+ is required.

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

On macOS or Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Preview

```bash
zensical serve
```

Open [http://localhost:8000](http://localhost:8000) (or the address shown in the terminal).

## Build static site

```bash
zensical build --clean
```

Output is written to the **`site/`** directory by default.

## GitHub Pages

The workflow in **`.github/workflows/docs.yml`** installs Zensical, runs **`zensical build --clean`**, and deploys the **`site`** folder to GitHub Pages. Ensure **`site_url`** in **`zensical.toml`** matches your GitHub Pages URL after you enable Pages for the repository.

## About BetterSEQTA+

BetterSEQTA+ is an open source browser extension for [SEQTA Learn](https://www.seqta.com.au/seqta-learn). Project home: [betterseqta.org](https://betterseqta.org/). Source code: [BetterSEQTA/BetterSEQTA-Plus](https://github.com/BetterSEQTA/BetterSEQTA-Plus).

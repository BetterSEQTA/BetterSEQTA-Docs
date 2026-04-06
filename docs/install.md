---
description: Where and how to install BetterSEQTA+ for users and developers.
---

# Install

Official download and store links are maintained on **[betterseqta.org/download](https://betterseqta.org/download)**. Use that page for the latest builds and platform-specific installers.

## Browsers (quick reference)

- **Chromium-based** (Chrome, Edge, Brave, Opera, and similar): install from the Chrome Web Store or equivalent channel linked on the download page.
- **Firefox**: the extension is published on [Mozilla Add-ons](https://addons.mozilla.org/en-US/firefox/addon/betterseqta-plus/).
- **Safari**: described upstream as experimental; not recommended for general use. Availability may require building from source; see the [BetterSEQTA+ repository](https://github.com/BetterSEQTA/BetterSEQTA-Plus) for current notes.

## Desktop and mobile

**DesQTA** and other desktop or Android options, when available, are listed on **[betterseqta.org](https://betterseqta.org/)** alongside the browser extensions.

## After installing

1. Open SEQTA Learn in the browser where you installed the extension.
2. Open the extension’s options or popup if prompted to complete setup.
3. Sign in to SEQTA as usual; BetterSEQTA+ enhances pages after they load.

If something fails, see [Troubleshooting](troubleshooting.md).

---

## Detailed installation and setup

The following sections mirror the upstream project documentation for **store installs** and **development setup**.

### Prerequisites (development)

Before developing BetterSEQTA+, install:

- [npm](https://www.npmjs.com/) (v7 or higher) or [Bun](https://bun.sh/) (recommended)
- A modern web browser (Chrome, Firefox, Edge, etc.)

### For users: browser extension

BetterSEQTA+ is available as a browser extension for Chrome, Firefox, and Edge.

#### Chrome / Edge

1. Visit the [Chrome Web Store page for BetterSEQTA+](https://chrome.google.com/webstore/detail/betterseqta/afdgaoaclhkhemfkkkonemoapeinchel) (or use [betterseqta.org/download](https://betterseqta.org/download)).
2. Click **Add to Chrome** (or equivalent).
3. Confirm the installation when prompted.

#### Firefox

1. Visit the [Firefox Add-ons page for BetterSEQTA+](https://addons.mozilla.org/en-US/firefox/addon/betterseqta-plus/).
2. Click **Add to Firefox** and confirm.

### For developers: development environment

Clone the repository and run the dev build:

#### 1. Clone the repository

```bash
git clone https://github.com/BetterSEQTA/BetterSEQTA-Plus.git
cd BetterSEQTA-Plus
```

#### 2. Install dependencies

Using npm:

```bash
npm install --legacy-peer-deps
```

Using Bun (recommended):

```bash
bun install
```

#### 3. Environment variables (optional)

Only required for pushing to extension stores from the command line. Copy the example env file if your workflow needs it:

```bash
cp .env.submit.example .env
```

Edit `.env` with your credentials as documented in the repository.

#### 4. Start the development server

```bash
npm run dev
```

Or with Bun:

```bash
bun run dev
```

#### 5. Load the extension in the browser

**Chrome / Edge**

1. Open `chrome://extensions` or `edge://extensions`.
2. Enable **Developer mode**.
3. Click **Load unpacked** and select the **`dist`** folder in your BetterSEQTA+ directory.

**Firefox**

1. Open `about:debugging#/runtime/this-firefox`.
2. Click **Load Temporary Add-on…** and select **`manifest.json`** inside **`dist`**.

#### 6. Reload after changes

After code changes, rebuild if needed and use the **reload** action on the extension page.

### Troubleshooting installation

**“Cannot find module” errors**

```bash
rm -rf node_modules
npm install --legacy-peer-deps
```

**Extension not appearing on SEQTA**

- Ensure you are on a SEQTA Learn page, the extension is enabled, and you refreshed the page.

**Development build not updating**

Stop the dev server, clear the browser cache, remove and reload the extension, then rebuild.

### Updating

**Users:** Extensions usually update automatically; check **Manage extensions** in your browser for manual updates.

**Developers:**

```bash
git pull
npm install --legacy-peer-deps
npm run dev
```

(Or use `bun install` / `bun run dev`.)

## Next steps

- [Plugin development](plugin-development.md) — create and register plugins
- [Contributing](contributing.md) — how to contribute to the project

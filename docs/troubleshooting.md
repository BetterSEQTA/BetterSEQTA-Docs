---
description: Common issues with BetterSEQTA+ and SEQTA Learn, plus developer troubleshooting.
---

# Troubleshooting

## Extension does not appear to run on SEQTA

- Confirm you are on a **SEQTA Learn** page in a **supported browser** ([Install](install.md)).
- Check that the extension is **enabled** in the browser’s extension management page.
- Try **reloading the extension** after an update (the upstream README notes this is required in some cases outside dev mode).

## School or organization restrictions

Some schools manage browsers or block extensions. If you cannot install extensions, you may need to use a **personal device** or ask IT whether policy allows the extension.

## Sign-in or timetable issues

BetterSEQTA+ **does not replace** SEQTA authentication. Problems logging in, missing lessons, or wrong timetable data usually come from **SEQTA or school configuration**, not from the extension. Contact your school’s IT or SEQTA support for account issues.

## Themes or layout look wrong after an update

- Open the extension **settings** and re-select your theme or reset options.
- If you use **custom themes**, check for updates from the theme author or the [theme documentation](customization.md) and [Theme creation](theme-creation.md).

## Where to report bugs

Open an issue on **[BetterSEQTA+ GitHub](https://github.com/BetterSEQTA/BetterSEQTA-Plus/issues)** with steps to reproduce, browser and extension version, and (if possible) a screenshot. For quick questions, the **[Discord](https://discord.gg/YzmbnCDkat)** community may help.

## FAQ

**Does BetterSEQTA+ send my password or data to third parties?**  
Review the extension’s privacy disclosures in the store listing and repository. This documentation site does not define the extension’s data practices; rely on official sources for your version.

**Is this endorsed by SEQTA or my school?**  
BetterSEQTA+ is a community project. It is not necessarily endorsed by SEQTA Pty Ltd or your institution—check local rules before use.

---

## Developer troubleshooting

Having issues with BetterSEQTA+ **development**? The sections below cover common problems when building the extension or writing plugins.

### Table of contents (developers)

- [Installation issues](#installation-issues)
- [Development server issues](#development-server-issues)
- [Browser extension issues](#browser-extension-issues)
- [Plugin development issues](#plugin-development-issues)
- [Build issues](#build-issues)
- [Still stuck?](#still-stuck)

### Installation issues

#### "npm install" fails with peer dependency errors

**Solution:**

```bash
rm -rf node_modules package-lock.json
npm install --legacy-peer-deps
```

#### "Cannot find module" errors

1. Clear and reinstall:

   ```bash
   rm -rf node_modules
   npm install --legacy-peer-deps
   ```

2. Check Node.js version: `node --version` (v16+ recommended).

3. Try: `npm cache clean --force` then `npm install --legacy-peer-deps`.

#### Permission errors on macOS/Linux

```bash
sudo chown -R $(whoami) ~/.npm
sudo chown -R $(whoami) /usr/local/lib/node_modules
```

### Development server issues

#### "npm run dev" fails

1. Check if the dev port is in use and free it.
2. Clear the build output: `rm -rf dist` then `npm run dev`.
3. Check TypeScript: `npx tsc --noEmit`.

#### Changes not reflecting in browser

1. Reload the extension on `chrome://extensions` (or equivalent).
2. Confirm the dev server shows a successful build.
3. Hard-refresh the SEQTA tab (`Ctrl+Shift+R` / `Cmd+Shift+R`).

### Browser extension issues

#### Extension doesn't load in Chrome

1. Check **Errors** on the extension card in `chrome://extensions`.
2. Ensure `dist/manifest.json` exists after a build.
3. Confirm **Site access** allows SEQTA domains if required.

#### Extension doesn't appear on SEQTA pages

1. Confirm the URL is a SEQTA Learn page.
2. Open DevTools → Console and look for BetterSEQTA+ messages.
3. Test on a real school SEQTA instance.

#### Settings page won't open

Inspect the extension popup for errors; try clearing extension storage from the console if documented in your build; reload the extension.

### Plugin development issues

#### Plugin doesn't appear in settings

1. Ensure the plugin is imported in `src/plugins/index.ts` and registered as expected.
2. Validate required plugin fields (`id`, `name`, `version`, `run`, etc.).
3. Check the browser console for load errors.

#### Plugin settings not saving

Use the settings helpers and `await api.settings.loaded` as described in [Plugin development](plugin-development.md).

#### Plugin API not behaving as expected

Prefer specific selectors, use `onPageChange` when navigation matters, and see [Plugin API](plugin-api.md).

### Build issues

#### "npm run build" fails

Run `npx tsc --noEmit`, then try a clean install and `npm run build` after `rm -rf dist node_modules`.

#### Built extension doesn't work

Load `dist` unpacked, compare with dev behavior, and inspect `dist/manifest.json`.

### Common error messages

| Message | Notes |
|---------|--------|
| Cannot access contents of the URL | Check extension site access / permissions. |
| Extension context invalidated | Reload the SEQTA tab after reloading the extension. |
| `browser is not defined` | Ensure webextension polyfill usage matches the project. |
| Module not found `@/...` | Check `tsconfig` and Vite path aliases. |

### Performance

If SEQTA feels slow, profile with DevTools, reduce listeners, and test with plugins disabled to isolate the cause.

### Still stuck?

1. Search [GitHub Issues](https://github.com/BetterSEQTA/BetterSEQTA-Plus/issues).
2. Ask on [Discord](https://discord.gg/YzmbnCDkat).
3. Open a new issue with OS, Node and browser versions, errors, and steps to reproduce.

For verbose logging and background-page debugging, use the browser’s extension developer tools as described in the upstream troubleshooting material.

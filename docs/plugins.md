---
description: Plugin system overview and links to full guides on this site.
---

# Plugins

BetterSEQTA+ extends [SEQTA Learn](https://www.seqta.com.au/seqta-learn) with a **plugin system**: self-contained modules that can add UI, react to pages, and store settings. Loaders under `src/plugins` in the [main repository](https://github.com/BetterSEQTA/BetterSEQTA-Plus) register built-in and user-facing plugins.

## Guides on this site

| Guide | Description |
|-------|-------------|
| [Plugin development](plugin-development.md) | Full beginner-oriented guide: first plugin, structure, APIs in prose |
| [Plugin API reference](plugin-api.md) | Technical API reference for plugin authors |
| [Example plugin](example-plugin.md) | Copy-paste template and walkthrough |

Start with **Plugin development**, use **Plugin API** when you need exact types and methods, and open **Example plugin** for a concrete pattern.

## Also see

- [Architecture](architecture.md) — how the extension is structured
- [Contributing](contributing.md) — sending changes to the main repo
- [Troubleshooting](troubleshooting.md) — when plugins or builds misbehave

Upstream copies of these guides live under [`docs/plugins/`](https://github.com/BetterSEQTA/BetterSEQTA-Plus/tree/main/docs/plugins) in the BetterSEQTA+ repository if you prefer reading on GitHub.

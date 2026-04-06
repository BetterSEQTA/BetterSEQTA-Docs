---
description: Themes, backgrounds, and related customization for BetterSEQTA+.
---

# Customization

## Themes and backgrounds

BetterSEQTA+ supports **dark mode**, **custom backgrounds**, and **themes**. You can use built-in options, community themes, and the official theme store (see [Features](features.md)).

## Theme creation

The **BetterSEQTA+ Theme System** lets you tailor SEQTA Learn: custom colour schemes, images and backgrounds, layout tweaks, and (when you need it) **CSS** for fine-grained control. You can share themes with others through the **theme store** (see the [GitBook introduction](https://betterseqta.gitbook.io/betterseqta-docs)).

Authoritative instructions live in two places below—not every detail is duplicated here.

### 1. Official documentation (GitBook)

Use **[BetterSEQTA+ documentation on GitBook](https://betterseqta.gitbook.io/betterseqta-docs)** as your starting point. The introduction describes the theme system and walks through basic options, images, and CSS.

**Getting started (from the docs):**

1. Open BetterSEQTA+ **settings**.
2. Go to the **Themes** tab.
3. Scroll to the bottom and use **Create Theme** to open the **Theme Creator** and begin customising.

Follow the rest of GitBook for step-by-step guidance in the UI.

### 2. Theme Creation Guide (full reference on this site)

The complete **Theme Creation Guide** is **[Theme creation](theme-creation.md)** in this documentation (aligned with [`docs/THEME_CREATION.md`](https://github.com/BetterSEQTA/BetterSEQTA-Plus/blob/main/docs/THEME_CREATION.md) in the repository). It covers:

- What a theme is made of (custom CSS, images, metadata, theme settings such as forcing light/dark mode)
- **CSS variables** (for example `--background-primary`, `--text-primary`, BetterSEQTA-specific variables like `--better-main`)
- **Selectors and classes** (layout IDs such as `#container`, dark mode `html.dark`, SEQTA/BetterSEQTA classes, CSS modules)
- **Custom images** and how they are exposed to CSS
- **Theme settings**, **best practices**, and **examples**

Use GitBook for the **Theme Creator workflow**; use **[Theme creation](theme-creation.md)** when you need variable names, selectors, or structure while writing CSS.

The upstream **[README](https://github.com/BetterSEQTA/BetterSEQTA-Plus/blob/main/README.md#creating-custom-themes)** also points theme authors at GitBook first; follow that link for the short version.

### 3. Iterate and test

1. Work in **settings → Themes** and the **Theme Creator** as described on GitBook.
2. Reload SEQTA Learn and check pages you care about (dashboard, timetable, notices, etc.).
3. For advanced styling, cross-check variables and selectors in **[Theme creation](theme-creation.md)** so your CSS matches what BetterSEQTA+ exposes.

Use [Contributing](contributing.md) only if you are changing the **extension** itself, not when you are only building a theme.

### 4. Share themes and get help

Sharing and the **theme store** are described in GitBook and on **[betterseqta.org](https://betterseqta.org/)**. For questions, use the **[Discord](https://discord.gg/YzmbnCDkat)** and mention what you tried (GitBook section, browser, and whether you used variables from THEME_CREATION.md).

!!! note "Scope of this documentation"

    **Selectors, variables, and store rules** can change between releases. Treat **[GitBook](https://betterseqta.gitbook.io/betterseqta-docs)** and **[Theme creation](theme-creation.md)** as the sources of truth for specifics.

## Extension settings

Use the extension’s **settings** UI to turn features on or off, pick themes, and adjust behavior. Exact options depend on your installed version; explore the settings panel after installation.

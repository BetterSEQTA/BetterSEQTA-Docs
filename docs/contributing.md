---
description: How to contribute to BetterSEQTA+ and to this documentation site.
---

# Contributing

## This documentation site

This site is built with **[Zensical](https://zensical.org/)**. To propose changes to these docs:

1. Clone the repository that hosts this documentation.
2. Edit Markdown under `docs/`.
3. Run `zensical serve` locally to preview (see the repository README).
4. Open a pull request.

If the documentation repository is separate from BetterSEQTA+, mention both when a change spans extension behaviour and documentation.

---

## BetterSEQTA+ extension

The extension is open source under the **MIT License**. Use the sections below: **repository guidelines** (quick norms), **getting started** (first-time setup), then **extended guidelines** (code of conduct, branches, reviews).

**Useful pages on this site:** [Install](install.md) (including development setup), [Architecture](architecture.md), [Plugin development](plugin-development.md), [Troubleshooting](troubleshooting.md). **Community:** [Discord](https://discord.gg/YzmbnCDkat).

---

## Repository guidelines

Short norms from the main repository. For your first setup, skip to **[Getting started as a contributor](#getting-started-as-a-contributor)** below.

**Never contributed to an open source project before?** You can:

- Follow **[Getting started as a contributor](#getting-started-as-a-contributor)** on this page for a full walkthrough.
- Read the [Architecture](architecture.md) guide and [Troubleshooting](troubleshooting.md) when something breaks.

We have lots of [`good first issue`](https://github.com/BetterSEQTA/BetterSEQTA-Plus/labels/good%20first%20issue) labels that are perfect for beginners!

## Discussion Before Contributing

For significant changes, please first discuss what you'd like to change via:
- Opening an issue
- Joining our Discord server
- Emailing the maintainers

This helps ensure your contribution aligns with the project's goals and saves you time!

## Community

Join our community channels to discuss the project, get help, and connect with other contributors:

- **Discord Server**: [Join our Discord](https://discord.gg/YzmbnCDkat)
- **GitHub Discussions**: For longer-form conversations
- **GitHub Issues**: For bug reports and feature requests

## Creating Plugins

If you're interested in creating plugins for BetterSEQTA+, check out our plugin development guides:

- [Creating Your First Plugin](plugin-development.md)
- [Plugin API Reference](plugin-api.md)

## Pull Request Process

1. It is recommended to start by opening an issue to discuss the change you wish to make. This will allow us to discuss the change and ensure it is a good fit for the project.
2. Fork the repo and create your branch from `main`.
3. When writing your pull request, make sure to use the pull request template.

### Pull Request Template

```
## Description

Please include a summary of the change and which issue is fixed. Please also include relevant motivation and context. List any dependencies that are required for this change.

Fixes # (issue)

## Type of change

Please delete options that are not relevant.

- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] New feature (non-breaking change which adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] This change requires a documentation update
```

### Issues

#### Create a new issue

If you spot a problem with the readme or code, [search if an issue already exists](https://github.com/BetterSEQTA/BetterSEQTA-Plus/issues). If a related issue doesn't exist, you can open a new issue using a relevant [issue form](https://github.com/BetterSEQTA/BetterSEQTA-Plus/issues/new).

#### Solve an issue

Scan through our [existing issues](https://github.com/BetterSEQTA/BetterSEQTA-Plus/issues) to find one that interests you. You can narrow down the search using `labels` as filters. As a general rule, we donâ€™t assign issues to anyone. If you find an issue to work on, you are welcome to open a PR with a fix.


---

## Getting started as a contributor

Welcome to BetterSEQTA+! This guide will walk you through making your first contribution, even if you're completely new to the project.

## Table of Contents

- [Before You Start](#before-you-start)
- [Your First 30 Minutes](#your-first-30-minutes)
- [Making Your First Contribution](#making-your-first-contribution)
- [Types of Contributions](#types-of-contributions)
- [Finding Something to Work On](#finding-something-to-work-on)
- [Development Workflow](#development-workflow)
- [Getting Help](#getting-help)

## Before You Start

### What You'll Need
- **Node.js** (v16 or higher) - [Download here](https://nodejs.org/)
- **Git** - [Download here](https://git-scm.com/)
- **A code editor** - We recommend [VS Code](https://code.visualstudio.com/)
- **A Chromium browser** (Chrome, Edge, Brave) for testing (recommended, however you can use firefox although it requires being built every time you make a change)

### Helpful Background (but not required!)
- Basic JavaScript/TypeScript knowledge
- Some familiarity with HTML/CSS
- Understanding of browser extensions (we'll teach you!)

**Don't worry if you're missing some of these!** We're happy to help you learn. ðŸ¤—

## Your First 30 Minutes

Let's get you up and running quickly:

### 1. Get the Code (3 minutes)
```bash
# Fork the repository on GitHub first, then:
git clone https://github.com/YOUR_USERNAME/BetterSEQTA-Plus.git
cd BetterSEQTA-Plus
```

### 2. Install Dependencies (3 minutes)
```bash
npm install --legacy-peer-deps
```

### 3. Start Development Server (2 minutes)
```bash
npm run dev
```

### 4. Load Extension in Browser (4 minutes)
1. Open Chrome and go to `chrome://extensions`
2. Enable "Developer mode" (toggle in top right)
3. Click "Load unpacked"
4. Select the `dist` folder in your project
5. Visit a SEQTA Learn page to see BetterSEQTA+ in action!

### 5. Make a Tiny Change (5 minutes)
Let's prove everything works:
1. Open `src/SEQTA.ts`
2. Find the line that says `"[BetterSEQTA+] Successfully initialised"`
3. Change it to `"[BetterSEQTA+] Successfully initialised - Hello [YOUR_NAME]!"`
4. Save the file
5. Go to `chrome://extensions`, click the refresh icon on BetterSEQTA+
6. Refresh a SEQTA page and check the browser console (F12) - you should see your message!

### 6. Reset Your Change (3 minutes)
```bash
git checkout -- src/SEQTA.ts
```

**Congratulations! ðŸŽ‰ You've successfully set up BetterSEQTA+ for development!**

## Making Your First Contribution

### Easy First Contributions

Here are some great starter contributions:

1. **Fix a typo in documentation** - Super easy and always appreciated!
2. **Improve error messages** - Make them more helpful
3. **Add comments to code** - Help other contributors understand
4. **Create a simple plugin** - Follow our plugin guide
5. **Fix a bug you found** - If you found a bug, fix it!

### Step-by-Step: Your First Pull Request

#### Step 1: Pick an Issue
- Go to our [Issues page](https://github.com/BetterSEQTA/BetterSEQTA-Plus/issues)
- Look for labels like:
  - `good first issue` - Perfect for beginners
  - `help wanted` - We'd love help with these
  - `documentation` - Improve our docs
  - `bug` - Fix something broken

#### Step 2: Claim the Issue
Comment on the issue saying "I'd like to work on this!" We'll assign it to you.

#### Step 3: Create a Branch
```bash
git checkout -b fix-issue-123  # Replace 123 with the issue number
```

#### Step 4: Make Your Changes
- Follow the patterns you see in existing code
- Test your changes thoroughly
- Keep changes focused and small

#### Step 5: Test Everything
```bash
# Test the extension still loads
npm run dev

# Test in browser
# 1. Reload extension at chrome://extensions
# 2. Visit SEQTA page
# 3. Verify everything still works
```

#### Step 6: Commit Your Changes
```bash
git add .
git commit -m "Fix issue #123: Brief description of what you fixed"
```

#### Step 7: Push and Create Pull Request
```bash
git push origin fix-issue-123
```

Then go to GitHub and create a pull request with:
- **Clear title**: "Fix issue #123: Brief description"
- **Description**: Explain what you changed and why
- **Testing**: Describe how you tested it

## Types of Contributions

### ðŸ› Bug Fixes
- Fix broken features
- Improve error handling
- Resolve compatibility issues

**Example**: "The theme selector doesn't work on Firefox"

### âœ¨ New Features
- Add new plugins
- Enhance existing functionality
- Improve user experience

**Example**: "Add keyboard shortcuts for common actions"

### ðŸ“š Documentation
- Fix typos and unclear explanations
- Add examples and tutorials
- Improve code comments

**Example**: "Add more examples to the plugin guide"

### ðŸŽ¨ Design & UI
- Improve the settings interface
- Make things more user-friendly
- Add animations and polish

**Example**: "Make the theme creator more intuitive"

### ðŸ”§ Technical Improvements
- Refactor code for clarity
- Add tests
- Improve performance

**Example**: "Simplify the plugin loading logic"

## Finding Something to Work On

### Browse Issues by Label
- [`good first issue`](https://github.com/BetterSEQTA/BetterSEQTA-Plus/labels/good%20first%20issue) - Perfect for beginners
- [`help wanted`](https://github.com/BetterSEQTA/BetterSEQTA-Plus/labels/help%20wanted) - We need help with these
- [`documentation`](https://github.com/BetterSEQTA/BetterSEQTA-Plus/labels/documentation) - Improve our docs
- [`bug`](https://github.com/BetterSEQTA/BetterSEQTA-Plus/labels/bug) - Fix something broken
- [`enhancement`](https://github.com/BetterSEQTA/BetterSEQTA-Plus/labels/enhancement) - Add new features

### Create Your Own Issue
Found a bug or have an idea? Create an issue first to discuss it!

### Plugin Ideas
Want to create a plugin? Here are some ideas:
- **Study Timer**: Track study time across SEQTA pages
- **Grade Tracker**: Better visualization of grades over time
- **Quick Notes**: Add notes to any SEQTA page
- **Homework Reminder**: Smart notifications for upcoming due dates
- **Custom Shortcuts**: User-defined keyboard shortcuts

## Development Workflow

### Daily Development
```bash
# Start working
git pull origin main
npm run dev

# Make changes, test, commit
git add .
git commit -m "Descriptive commit message"

# Push when ready
git push origin your-branch-name
```

### Before Submitting PR
1. **Test thoroughly** - Make sure nothing breaks
2. **Check console** - No new errors
3. **Test in different browsers** - Chrome and Firefox
4. **Update documentation** - If you changed how something works

### Code Style
- Use TypeScript where possible
- Follow existing naming conventions
- Add comments for complex logic
- Keep functions small and focused

## Getting Help

### Stuck? Here's How to Get Unstuck

1. **Check the docs** - [Architecture guide](architecture.md) explains everything
2. **Search existing issues** - Someone might have had the same problem
3. **Ask in Discord** - Our community is super helpful
4. **Create an issue** - If you found a bug or need help

### Discord Community
Join our [Discord server](https://discord.gg/YzmbnCDkat) for:
- Real-time help and discussion
- Collaboration on features
- Sharing ideas and feedback
- Getting to know the community

### Code Review Process
- All contributions need code review
- We'll provide helpful feedback
- Don't worry about making mistakes - we're here to help!
- Reviews usually happen within 24-48 hours

## Common Questions

**Q: I'm new to browser extensions. Is this too advanced for me?**
A: Not at all! We have lots of beginner-friendly issues, and our plugin system makes it easy to add features without understanding all the browser extension complexities.

**Q: How long does it take to get my first PR merged?**
A: For simple fixes, usually 1-3 days. For larger features, it might take a week or two as we discuss the best approach.

**Q: I made a mistake in my PR. What do I do?**
A: No worries! Just push more commits to the same branch and they'll be added to your PR automatically.

**Q: Can I work on multiple issues at once?**
A: It's better to focus on one issue at a time, especially when starting out. This makes code review easier and reduces conflicts.

**Q: What if I start working on something and get stuck?**
A: Ask for help! Create a draft PR with what you have so far, and we'll help you figure out the next steps.

## Recognition

All contributors get:
- Recognition in our README
- Contributor badge in Discord
- Our eternal gratitude! ðŸ™

Significant contributors may also get:
- Special Discord roles
- Input on project direction
- Maintainer status

## Next Steps

Ready to contribute? Here's what to do:

1. âœ… **Set up your development environment** (follow the 30-minute guide above)
2. ðŸ” **Find an issue to work on** (check the "good first issue" label)
3. ðŸ’¬ **Join our Discord** and introduce yourself
4. ðŸš€ **Make your first contribution** and submit a PR

Remember: **Every expert was once a beginner!** We're excited to help you learn and grow as a contributor. Welcome to the team! ðŸŽ‰

---

*Questions? Suggestions for improving this guide? Open an issue or message us on Discord!* 

---

## Extended contributing guidelines

The following sections provide detailed policies (code of conduct, branching, reviews, and more).

### Table of Contents (extended)

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
  - [Setting Up Your Development Environment](#setting-up-your-development-environment)
  - [Project Structure](#project-structure)
- [Contributing Code](#contributing-code)
  - [Branching Strategy](#branching-strategy)
  - [Pull Request Process](#pull-request-process)
  - [Coding Standards](#coding-standards)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Features](#suggesting-features)
- [Writing Documentation](#writing-documentation)
- [Community](#community)

## Code of Conduct

BetterSEQTA+ is committed to providing a welcoming and inclusive environment for all contributors. We expect all participants to adhere to our Code of Conduct, which promotes respectful and harassment-free interaction.

Key points:

- Be respectful and inclusive
- Focus on what is best for the community
- Show empathy towards other community members
- Be open to constructive feedback

## Getting Started

### Setting Up Your Development Environment

1. **Fork the Repository**

   Start by forking the BetterSEQTA+ repository to your GitHub account.

2. **Clone Your Fork**

   ```bash
   git clone https://github.com/yourusername/BetterSEQTA-Plus.git
   cd BetterSEQTA-Plus
   ```

3. **Install Dependencies**

   ```bash
   npm install
   ```

4. **Set Up Development Environment**

   ```bash
   npm run dev
   ```

5. **Install in Chrome/Firefox**

   Follow [Install](install.md) to load the development version into your browser.

### Project Structure

Understanding the project structure will help you navigate the codebase:

```
betterseqta-plus/
â”œâ”€â”€ src/                  # Source code
â”‚   â”œâ”€â”€ plugins/          # Plugin system
â”‚   â”‚   â”œâ”€â”€ built-in/     # Built-in plugins
â”‚   â”‚   â”œâ”€â”€ core/         # Plugin core functionality
â”‚   â”œâ”€â”€ settings/         # Settings system
â”‚   â”œâ”€â”€ utils/            # Utility functions
â”‚   â”œâ”€â”€ extension/        # Browser extension code
â”œâ”€â”€ docs/                 # Documentation
â”œâ”€â”€ test/                 # Test files
â”œâ”€â”€ dist/                 # Build output (generated)
â”œâ”€â”€ package.json          # Project dependencies
â”œâ”€â”€ tsconfig.json         # TypeScript configuration
â””â”€â”€ README.md             # Project README
```

## Contributing Code

### Branching Strategy

We follow a simple branching strategy:

- `main` - The main development branch
- `feature/*` - Feature branches
- `bugfix/*` - Bug fix branches
- `docs/*` - Documentation branches

Always create a new branch for your changes:

```bash
git checkout -b feature/my-new-feature
```

### Pull Request Process

1. **Keep PRs Focused**

   Each pull request should address a single concern. If you're working on multiple features, create separate PRs for each.

2. **Write Clear Commit Messages**

   Follow the conventional commits format:

   ```
   feat: add new feature
   fix: resolve bug with timetable
   docs: update installation instructions
   ```

3. **Update Documentation**

   If your changes require documentation updates, include them in the same PR.

4. **Run Tests**

   Make sure all tests pass before submitting your PR:

   ```bash
   npm test
   ```

5. **Submit Your PR**

   When you're ready, push your branch and create a pull request on GitHub.

6. **Code Review**

   All PRs will be reviewed by maintainers. Be responsive to feedback and make requested changes.

7. **Merge**

   Once approved, a maintainer will merge your PR.

### Coding Standards

We follow TypeScript best practices and have a consistent code style:

1. **Use TypeScript**

   All new code should be written in TypeScript with proper typing.

2. **Follow Existing Patterns**

   Match the coding style of the existing codebase.

3. **Write Tests**

   Add tests for new features and bug fixes.

4. **Document Your Code**

   Add comments for complex logic and JSDoc comments for functions.

5. **Use Linters**

   We use ESLint and Prettier. Run them before submitting your PR:

   ```bash
   npm run lint
   npm run format
   ```

## Reporting Bugs

If you find a bug, please report it by creating an issue on GitHub:

1. **Search Existing Issues**

   Check if the bug has already been reported.

2. **Use the Bug Report Template**

   Fill in all sections of the bug report template:

   - Description
   - Steps to reproduce
   - Expected behavior
   - Actual behavior
   - Screenshots (if applicable)
   - Environment (browser, OS, etc.)

3. **Be Specific**

   The more details you provide, the easier it will be to fix the bug.

## Suggesting Features

We welcome feature suggestions! To suggest a new feature:

1. **Search Existing Suggestions**

   Check if your idea has already been suggested.

2. **Use the Feature Request Template**

   Fill in all sections of the feature request template:

   - Description
   - Use case
   - Potential implementation
   - Alternatives considered

3. **Be Patient**

   Feature requests are evaluated based on alignment with project goals, feasibility, and maintainer bandwidth.

## Writing Documentation

Good documentation is crucial for the project. To contribute to documentation:

1. **Identify Gaps**

   Look for areas where documentation is missing or unclear.

2. **Follow Documentation Style**

   Maintain a consistent style and format.

3. **Use Clear Language**

   Write in simple, clear English. Avoid jargon when possible.

4. **Include Examples**

   Code examples and screenshots help users understand.

5. **Submit a PR**

   Follow the same process as code contributions, but create a branch with a `docs/` prefix.

## Community

Join our community channels to discuss the project, get help, and connect with other contributors:

- **Discord Server**: [Join our Discord](https://discord.gg/YzmbnCDkat)
- **GitHub Discussions**: For longer-form conversations
- **GitHub Issues**: For bug reports and feature requests

## Creating Plugins

If you're interested in creating plugins for BetterSEQTA+, check out our plugin development guides:

- [Creating Your First Plugin](plugin-development.md)
- [Plugin API Reference](plugin-api.md)

## Recognition

Contributors are recognized in several ways:

1. **CONTRIBUTORS.md**: All contributors are listed in this file
2. **Release Notes**: Significant contributions are highlighted in release notes
3. **Community Recognition**: Regular shout-outs in community channels

## Questions?

If you have any questions about contributing, please:

1. Check the documentation
2. Ask in the Discord server
3. Open a GitHub Discussion

Thank you for contributing to BetterSEQTA+! Your efforts help make SEQTA better for students and teachers everywhere.


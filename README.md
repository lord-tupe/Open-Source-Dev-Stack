# Developer Stack Canvas

**An interactive architecture command center for modern open-source developer tools.**

Map tools, build stacks, and plan DevSecOps workflows, all in a single, self-contained HTML file.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#contributing)
[![No Build Step](https://img.shields.io/badge/build-none-blue.svg)](#tech-stack)
[![Single File](https://img.shields.io/badge/deploy-single%20HTML-orange.svg)](#getting-started)

**Topics:** `developer-tools` · `architecture` · `devsecops` · `open-source` · `stack-builder` · `baas` · `ai-coding`

---

## Table of Contents

- [Overview](#overview)
- [Why This Exists](#why-this-exists)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Usage Guide](#usage-guide)
- [Keyboard Shortcuts](#keyboard-shortcuts)
- [Project Structure](#project-structure)
- [Customizing the Data](#customizing-the-data)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [Roadmap](#roadmap)
- [FAQ](#faq)
- [License](#license)
- [Acknowledgements](#acknowledgements)

---

## Overview

**Developer Stack Canvas** is a comprehensive, interactive map of the open-source development ecosystem. It helps developers, architects, and teams evaluate tools, plan architecture, and assemble coherent technology stacks, grounded in real trade-offs rather than hype.

Everything lives in one self-contained `index.html` file. There are no build steps, no package managers, no backend servers, and no dependencies to install. Clone it, open it, use it.

---

## Why This Exists

The developer tooling landscape changes weekly. New AI coding agents, BaaS platforms, and DevSecOps utilities appear faster than most teams can evaluate them. Meanwhile, most "awesome lists" are flat, unopinionated, and tell you *what* exists without helping you decide *what to use*.

This project takes a different approach:

- **Decision-oriented, not directory-oriented.** Every section is designed to help you make a choice, not just browse.
- **Trade-offs over trends.** Architecture patterns and self-hosting matrices document the costs, not just the benefits.
- **Licensing honesty.** Open-source, source-available, and open-core models are clearly distinguished, because they matter.
- **Constraint-aware.** Practical guidance for teams working with limited bandwidth, compute, or budget.

---

## Key Features

### 🔍 Tool Directory

Search and filter over **40 curated developer tools** by category, license, and hosting model. Every entry includes licensing, capabilities, and SDLC coverage data.

### 🤖 AI Landscape

Map the rapidly evolving AI coding ecosystem: inline assistants, IDE agents, terminal agents, and autonomous engineering tools, so you can see where each fits in your workflow.

### 🧱 Stack Builder

Review pre-configured technology stacks for common scenarios:

- SaaS products
- Rapid MVPs
- Enterprise systems

Each stack is a coherent, opinionated starting point rather than a random list of tools.

### 🏗️ Architecture Patterns

Compare **monoliths, microservices, BaaS, and serverless** patterns side by side, with clear trade-offs around complexity, cost, operational burden, and scalability.

### 🌳 Decision Tree

Get practical, constraint-driven guidance on which tools to use based on your specific project situation: team size, budget, hosting preference, and compliance needs.

### 🔐 DevSecOps Pipeline

Visualize security and quality gates across the entire delivery lifecycle, from pre-commit hooks through to production deployment.

### 🖥️ Self-Hosting Matrix

Understand the operational reality of self-hosting various platforms: resource requirements, maintenance burden, and what "self-hosted" actually costs you.

### ⚖️ License Matrix

Verify and compare open-source, source-available, and open-core licensing models at a glance, so you don't get surprised later.

### 📶 Low-Resource Context

Practical architecture advice for constrained environments: limited bandwidth, low compute, offline-first, or edge deployments.

### 💾 Persistent Preferences

Your saved tools, theme selection, and preferences are stored in **local storage**. Nothing leaves your browser.

---

## Tech Stack

| Layer | Technology |
| --- | --- |
| **Frontend** | React 18 (loaded via CDN) |
| **Styling** | Custom CSS with CSS variables for seamless dark and light themes |
| **Icons** | Font Awesome 6 |
| **Typography** | Inter (via Google Fonts) |
| **Build Tool** | None (a single `index.html` file) |

No npm. No bundler. No transpiler. No `node_modules`.

---

## Getting Started

### Prerequisites

A modern web browser. That's it.

### Installation

There is no build process required.

1. **Clone the repository** (or simply download `index.html`):

   ```bash
   git clone https://github.com/<your-username>/developer-stack-canvas.git
   cd developer-stack-canvas
   ```

2. **Open the file directly in your browser:**

   ```bash
   # macOS
   open index.html

   # Linux
   xdg-open index.html

   # Windows
   start index.html
   ```

That's the whole setup. The application runs entirely in the browser.

### Optional: Serve Locally

If you prefer serving over HTTP (useful for testing, or if your browser restricts `file://` behavior):

```bash
# Python 3
python -m http.server 8000

# Node.js (if you have it)
npx serve .
```

Then visit `http://localhost:8000`.

> **Tip:** If you use VS Code, the **Live Server** extension gives you instant reload on save.

---

## Usage Guide

| Section | What you can do |
| --- | --- |
| **Tool Directory** | Search by name, filter by category / license / hosting model, and save tools to your shortlist. |
| **AI Landscape** | Compare AI assistants and agents by where they operate (inline, IDE, terminal, autonomous). |
| **Stack Builder** | Load a preset stack for SaaS, MVP, or enterprise, then adapt it to your needs. |
| **Architecture Patterns** | Read side-by-side trade-offs before committing to a pattern. |
| **Decision Tree** | Answer a few questions about your constraints and get a recommended path. |
| **DevSecOps Pipeline** | Walk the pipeline stage by stage to see which gates apply where. |
| **Self-Hosting Matrix** | Check resource requirements and maintenance burden before self-hosting. |
| **License Matrix** | Confirm the licensing model of any tool before adopting it. |
| **Low-Resource Context** | Find architecture advice tuned for constrained environments. |

---

## Keyboard Shortcuts

| Shortcut | Action |
| --- | --- |
| `Ctrl + K` / `Cmd + K` | Focus the global search bar |
| `Esc` | Close modals, tool drawers, and mobile navigation |

---

## Project Structure

Since this is a single-file application, the structure is straightforward:

```text
.
├── index.html      # Contains all HTML, CSS, and React/JSX logic
└── README.md       # This file
```

All application data (including the tool registry, architecture patterns, and stack presets) is defined in **JavaScript arrays at the top of the `<script>` block** inside `index.html`.

---

## Customizing the Data

Want to make this your own? Everything is data-driven and lives in plain JavaScript objects near the top of the `<script>` block.

### Adding a Tool

Locate the `TOOLS` array and append a new entry following the existing schema. Each tool should include:

- **Name** and short description
- **Category** (e.g. CI/CD, observability, BaaS, AI coding)
- **License** model (open-source, source-available, open-core)
- **Hosting model** (self-hosted, cloud, hybrid)
- **Capabilities** and **SDLC coverage** data

### Adding a Stack Preset

Add an entry to the stack presets array with a name, target scenario, and the list of tools that compose it.

### Adding an Architecture Pattern

Add an entry to the patterns array with the pattern name, a description, and its trade-offs (pros, cons, and best-fit scenarios).

> **Note:** Keep entries accurate. Incorrect licensing or capability data undermines the entire point of the project.

---

## Deployment

Because it's a single static HTML file, deployment is trivial. Any static host works:

- **GitHub Pages:** push to `main` and enable Pages in repository settings
- **Netlify / Vercel / Cloudflare Pages:** drag and drop the folder, or connect the repo
- **Any web server:** copy `index.html` to your document root
- **Local file:** just open it

No environment variables, no server configuration, no runtime.

---

## Contributing

Contributions are welcome! If you want to add a new tool, fix a bug, or improve the architecture patterns, please open a pull request.

### How to Contribute

1. **Fork** the repository
2. **Create a branch** for your change:

   ```bash
   git checkout -b feature/add-tool-name
   ```

3. **Make your changes** to `index.html`
4. **Test in a browser:** verify both dark and light themes, and check that search/filtering still works
5. **Commit** with a clear message:

   ```bash
   git commit -m "Add <tool-name> to TOOLS array"
   ```

6. **Push** and open a **Pull Request**

### Guidelines for Adding Tools

When adding a new tool, ensure you update the `TOOLS` array in the script section with **accurate** licensing, capabilities, and SDLC coverage data. Specifically:

- ✅ Verify the license on the project's own repository; don't rely on secondhand claims
- ✅ Distinguish clearly between open-source, source-available, and open-core
- ✅ Be honest about self-hosting difficulty; "you can self-host it" does not mean "it's easy to self-host"
- ✅ Keep descriptions concise and free of marketing language
- ✅ Avoid duplicates; search the existing array first

### Reporting Issues

Found a bug or an inaccurate data point? Please open an issue with:

- A clear description of the problem
- Steps to reproduce (for bugs)
- The correct information and a source link (for data corrections)

---

## Roadmap

Ideas under consideration (feedback welcome):

- [ ] Export and import saved stacks as JSON
- [ ] Shareable stack permalinks
- [ ] Comparison view for side-by-side tool evaluation
- [ ] Additional architecture patterns (event-driven, CQRS, modular monolith)
- [ ] Expanded low-resource and offline-first guidance
- [ ] Optional PWA support for offline use

> Have a suggestion? Open an issue and make the case.

---

## FAQ

**Do I need Node.js or npm installed?**  
No. There is no build step. React is loaded from a CDN.

**Does this send any data anywhere?**  
No. The app runs entirely in your browser, and all preferences are stored in local storage.

**Can I use this offline?**  
Yes, once loaded, though CDN-hosted assets (React, Font Awesome, Google Fonts) require a connection on first load. If you need true offline support, vendor those assets locally.

**Can I use this commercially or in my own project?**  
Yes. It's MIT licensed. See [License](#license).

**How do I add a tool that isn't listed?**  
See [Contributing](#contributing). The `TOOLS` array is plain JavaScript and easy to extend.

**Why a single HTML file instead of a proper build setup?**  
Portability and zero friction. Anyone can open it, fork it, or host it anywhere without tooling. It's a deliberate trade-off favoring accessibility over modularity.

---

## License

This project is open source and available under the [MIT License](LICENSE).

You are free to use, modify, and distribute it, including for commercial purposes, provided the license notice is preserved.

---

## Acknowledgements

- [React](https://react.dev/) for the UI library
- [Font Awesome](https://fontawesome.com/) for the icons
- [Inter](https://fonts.google.com/specimen/Inter) for the typography
- The open-source maintainers behind every tool documented in this canvas. This project exists to make their work easier to find and evaluate.

---

<p align="center">
  <strong>Built for developers who want to choose tools deliberately, not by default.</strong>
</p>

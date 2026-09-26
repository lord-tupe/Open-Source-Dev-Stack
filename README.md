# Repository Metadata

**About (Description):**
> Interactive open-source developer stack canvas and architecture command center. Map tools, build stacks, and plan DevSecOps workflows.

**Topics:**
`developer-tools` `architecture` `devsecops` `open-source` `stack-builder` `baas` `ai-coding`

---

# Developer Stack Canvas

An interactive architecture command center for modern open-source developer tools.

## Overview

This project provides a comprehensive map of the open-source development ecosystem. It helps developers and teams evaluate tools, plan architecture, and build coherent technology stacks without relying on hype.

It is built as a single, self-contained HTML file. You can run it locally without any build steps, package managers, or backend servers.

## Key Features

* **Tool Directory:** Search and filter over 40 curated developer tools by category, license, and hosting model.
* **AI Landscape:** Map inline assistants, IDE agents, terminal agents, and autonomous engineering tools.
* **Stack Builder:** Review pre-configured technology stacks for common scenarios like SaaS, MVPs, and enterprise systems.
* **Architecture Patterns:** Compare monoliths, microservices, BaaS, and serverless patterns with clear trade-offs.
* **Decision Tree:** Get practical guidance on which tools to use based on your specific project constraints.
* **DevSecOps Pipeline:** Visualize security and quality gates from pre-commit hooks to production deployment.
* **Self-Hosting Matrix:** Understand the operational reality and resource requirements of self-hosting various platforms.
* **License Matrix:** Verify open-source, source-available, and open-core licensing models.
* **Low-Resource Context:** Practical architecture advice for constrained environments with limited bandwidth or compute.

## Tech Stack

* **Frontend:** React 18 (loaded via CDN)
* **Styling:** Custom CSS with CSS variables for seamless dark and light themes
* **Icons:** Font Awesome 6
* **Typography:** Inter (via Google Fonts)
* **Build Tool:** None. It is a single `index.html` file.

## Getting Started

There is no build process required.

1. Clone the repository or download the `index.html` file.
2. Open the file directly in any modern web browser.

The application runs entirely in the browser. It stores your preferences, saved tools, and theme selection in local storage.

## Keyboard Shortcuts

* `Ctrl + K` (or `Cmd + K` on Mac): Focus the global search bar.
* `Esc`: Close modals, tool drawers, and mobile navigation.

## Project Structure

Since this is a single-file application, the structure is straightforward:

```text
.
├── index.html      # Contains all HTML, CSS, and React/JSX logic
└── README.md       # This file

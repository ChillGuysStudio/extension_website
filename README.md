<div align="center">

<h1>Clipboard Manager Extension — Website</h1>

<p>Marketing site for the Firefox extension that looks like a clipboard manager.<br>Built with <a href="https://astro.build">Astro</a> · Deployed as a static site · Zero dependencies at runtime.</p>

[![Astro](https://img.shields.io/badge/Astro-6.x-FF5D01?logo=astro&logoColor=white)](https://astro.build)
[![Bun](https://img.shields.io/badge/Bun-1.x-black?logo=bun&logoColor=white)](https://bun.sh)
[![Node](https://img.shields.io/badge/Node-%3E%3D22.12-339933?logo=node.js&logoColor=white)](https://nodejs.org)
[![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)

**Extension repo → [chillguysstudio/extension](https://github.com/chillguysstudio/extension)**

</div>

---

## What this is

This repo is the **landing page** for a Firefox browser extension. The extension presents itself as a minimal clipboard manager — and it is one — but behind a 20 px floating button lives a full AI chat assistant with multi-provider support, quiz auto-fill, image analysis, and more.

The site explains that duality: what everyone sees on the surface, and what's actually running underneath.

---

## Pages & sections

| Section | ID | Description |
|---|---|---|
| Hero | — | Tagline, install CTA, live popup replica |
| Features | `#features` | The clipboard manager face: history, one-click copy, management |
| Reveal | `#reveal` | The twist — what's actually inside the extension |
| Demo | `#demo` | Interactive chat replica embedded in the page |
| Shortcuts | `#shortcuts` | `Alt+C`, `Alt+Q`, `Alt+Shift+Q`, `/reset` |
| Hidden Mechanics | `#mechanics` | Stealth details: draggable button, auto dark mode, resize |
| Providers | `#providers` | All 7 supported AI providers and their models |
| CTA | — | Download link and closing message |

---

## Tech stack

- **[Astro](https://astro.build)** — static site generator, zero JS by default
- **[@astrojs/sitemap](https://docs.astro.build/en/guides/integrations-guide/sitemap/)** — auto-generated `sitemap.xml`
- **Bun** — package manager and dev server runner
- Pure CSS — no Tailwind, no UI libraries, hand-written component styles

---

## Project structure

```
/
├── public/
│   ├── favicon.ico
│   ├── favicon.svg
│   └── robots.txt
└── src/
    ├── components/
    │   ├── chat/               # Chat UI replica (messages, input, settings)
    │   ├── sections/           # One file per page section
    │   ├── ChatReplica.astro
    │   └── PopupReplica.astro  # Pixel-accurate extension popup mock
    ├── layouts/
    │   └── Layout.astro        # Base HTML shell, meta tags, OG
    ├── pages/
    │   └── index.astro         # Page composition — assembles all sections
    └── styles/
        ├── global.css
        └── chatbox.css
```

---

## Getting started

**Prerequisites:** [Bun](https://bun.sh) installed, or Node ≥ 22.12.

```sh
# Install dependencies
bun install

# Start dev server at localhost:4321
bun dev

# Production build → ./dist/
bun build

# Preview the production build locally
bun preview
```

---

## Commands

| Command | Action |
|---|---|
| `bun install` | Install dependencies |
| `bun dev` | Start dev server at `localhost:4321` |
| `bun build` | Build for production into `./dist/` |
| `bun preview` | Preview production build locally |
| `bun astro check` | Type-check `.astro` files |
| `bun astro add <integration>` | Add an Astro integration |

---

## The extension

The extension this site markets is a Firefox add-on that:

- **On the surface** — saves clipboard snippets from the toolbar popup, one-click copy, duplicate deduplication
- **Underneath** — runs a floating AI chat with support for 7 providers (Google AI Studio, Vertex AI, OpenAI, Anthropic, OpenRouter, Grok, OpenCode), quiz screenshot + autofill shortcuts, image analysis, markdown + LaTeX rendering, and persistent conversation history

All AI API keys are stored locally in the browser. Nothing is proxied or logged.

Install from the [latest release](https://github.com/chillguysstudio/extension/releases/latest) · Extension source on [GitHub](https://github.com/chillguysstudio/extension).

---

## License

MIT

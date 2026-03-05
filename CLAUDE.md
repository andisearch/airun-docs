# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Documentation site for **Andi AIRun** — a CLI tool that extends Claude Code with executable markdown, Unix pipes, and cross-cloud provider switching. Built on [Mintlify](https://mintlify.com).

## Commands

- **Local preview:** `mint dev` (serves at http://localhost:3000)
- **Check broken links:** `mint broken-links`
- **Install Mintlify CLI:** `npm i -g mint`

## Architecture

- **Framework:** Mintlify with Aspen theme
- **Content format:** MDX files with YAML frontmatter
- **Configuration:** `docs.json` — defines site name, colors, navbar, and all navigation structure
- **Ignored content:** `.mintignore` excludes `drafts/` and `*.draft.mdx`

### Content Structure

Navigation is organized into three tabs defined in `docs.json`:

1. **Documentation** — Get Started (`introduction`, `quickstart`, `installation`), Core Concepts (`concepts/`), Guides (`guides/`), Providers (`providers/`), Advanced (`advanced/`)
2. **CLI Reference** — Commands and Flags (`cli/`)
3. **Examples** — Script Examples and Use Cases (`examples/`)

Reusable content lives in `snippets/`. Images and logos are in `images/` and `logo/`.

## Writing Style

- Active voice, second person ("you")
- One idea per sentence
- Sentence case for headings
- Bold for UI elements (e.g., Click **Settings**)
- Code formatting for file names, commands, paths, and code references
- Lead with the goal, not the steps

## Adding Pages

New MDX pages must be added to the `navigation` section in `docs.json` to appear in the site. Place files in the appropriate content directory matching the navigation tab structure.

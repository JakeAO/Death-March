# Death March Campaign Hub

A Jekyll-based static site for the Death March TTRPG campaign, featuring a survival/apocalyptic aesthetic for a Savage Worlds road trip through the zombie apocalypse.

## Overview

This repository hosts the campaign hub for **Death March**, a Savage Worlds Adventure Edition campaign where survivors in a desperate convoy attempt to reach Rockies Haven before winter—if they can survive the journey.

## Features

- **Public Player Content:**
  - Rules & Info: Savage Worlds mechanics, survival rules, vehicle rules, and cheat sheets
  - World: Setting information, factions, and the harsh reality of the apocalypse
  - Sessions: Chronological session summaries tracking the convoy's journey
  
- **Private GM Content:**
  - Accessible via obscured URL (`/gm-vault-dm47x9/`)
  - Campaign planning and session prep
  - Hidden threats and secrets
  - Not indexed by search engines (via robots.txt)

- **Theme:**
  - Dark survival aesthetic with blood red accents
  - Post-apocalyptic/zombie apocalypse atmosphere
  - Gritty, weathered design elements
  - Mobile-responsive layout

## Local Development

### Prerequisites

- Ruby 3.1 or higher
- Bundler gem

### Setup

```bash
# Install dependencies
bundle install

# Serve locally
bundle exec jekyll serve

# Build for production
bundle exec jekyll build
```

The site will be available at `http://localhost:4000`

## Project Structure

```
.
├── _config.yml           # Jekyll configuration
├── _info/                # Rules and mechanics (public)
│   ├── mechanics/        # Savage Worlds core mechanics
│   ├── cheat-sheets/     # Quick reference sheets
│   ├── survival/         # Survival mechanics
│   └── vehicles/         # Vehicle rules
├── _world/               # Campaign world content (public)
├── _sessions/            # Session summaries (public)
├── _gm/                  # GM-only content (private URL)
├── assets/css/           # Custom styling
├── index.md              # Home page
├── info.md               # Rules landing page
├── world.md              # World landing page
├── sessions.md           # Sessions landing page
└── gm-notes.md           # GM vault landing page
```

## Adding Content

### Public Content

Create new markdown files in the appropriate collection folder:

**Rules/Info Example:**
```markdown
---
layout: page
title: Page Title
topic: Mechanics
summary: Brief description
---

# Page Title

Content here...
```

**Session Example:**
```markdown
---
layout: page
title: Session Title
index: 1
summary: Brief summary
---

# Session 1: Title

Full session summary...
```

### GM Content

Same structure, but place files in `_gm/` directory. These will be published at the obscured URL but won't appear in navigation or search engine indexes.

## Deployment

The site automatically deploys to GitHub Pages via GitHub Actions when changes are pushed to the main or master branch.

### GitHub Pages Setup

1. Go to repository Settings → Pages
2. Set Source to "GitHub Actions"
3. The workflow in `.github/workflows/pages.yml` handles the rest

## Theme Customization

The site uses Jekyll's Minima theme with extensive customization in `assets/css/style.scss`. Color scheme and styling reflect the survival/apocalyptic theme.

## Campaign Info

**System:** Savage Worlds Adventure Edition  
**Genre:** Zombie Apocalypse, Survival Horror, Road Trip  
**Setting:** Post-apocalyptic America, convoy heading west to Rockies Haven  
**Tone:** Gritty, desperate, high-stakes survival with tough choices

## Contributing

This is a private campaign repository. If you're a player, please don't peek at the `_gm/` folder—spoilers ahead!

## License

Campaign content is private. The Jekyll structure and theme are based on open-source components.

## Credits

- Built with [Jekyll](https://jekyllrb.com/)
- Theme based on [Minima](https://github.com/jekyll/minima)
- Powered by [Savage Worlds Adventure Edition](https://peginc.com/savage-settings/savage-worlds/)
- Structure inspired by the Vaultlight campaign hub

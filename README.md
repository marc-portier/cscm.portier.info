# cscm.portier.info — Veilig Zwemmen in Zee (Het 12-Stappen-Kompas)

Public educational website and coastal swimming current portal powered by **CSCM** (*Coastal Swim Current Model*), published via Hugo and GitHub Pages at **https://cscm.portier.info**.

## Architecture & Review Workflow

Each of the 12 compass points (`01-l1-*` through `12-d4-*`) plus the central compass philosophy (`13-kompas-verantwoordelijkheid`) is modularized with matching 1-to-1 filenames for text and graphics:

1. **Step Texts (`content/stappen/*.md`)**:
   - Each section lives in its own Markdown file (`01-l1-afstand.md` through `13-kompas-verantwoordelijkheid.md`).
   - Frontmatter holds `title`, `step_id`, `number`, `phase`, `phase_slug`, `keyword`, `vuistregel`, and `icon`.
2. **Matching SVG Icons & Central Compass (`static/images/icons/*.svg` & `static/images/central-overview.svg`)**:
   - Each Markdown file in `content/stappen/<slug>.md` has a matching standalone SVG icon in `static/images/icons/<slug>.svg` (`01-l1-afstand.svg` through `13-kompas-verantwoordelijkheid.svg`).
   - The hero section embeds the interactive compass (`static/images/central-overview.svg`).

## Local Development

```bash
# Start the local Hugo live-reload server (requires Hugo >= 0.159.2)
hugo server -D
```

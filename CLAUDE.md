# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build & Development Commands

```bash
# Local development server
hugo server --buildDrafts

# Build for production
hugo --gc --minify

# Update theme submodule
git submodule update --init --recursive
```

## Architecture

Hugo site using the **Book theme** for side navigation. Deployed to GitHub Pages via Actions on push to main.

Target area: North Columbus / Lewis Center region (near Chase).

### Content Structure

```
content/docs/
├── priority-scale.md          # Rating system (★ ● ◐ ○ ⛔)
├── sweetie/                   # Sweetie's preferences
│   ├── _index.md
│   ├── budget.md
│   ├── location.md
│   ├── interior.md
│   ├── exterior.md
│   └── garage.md
├── chris/                     # Chris's preferences
│   ├── _index.md
│   ├── budget.md
│   ├── location.md
│   ├── interior.md
│   ├── exterior.md
│   └── garage.md
└── houses/                    # Candidates by area
    ├── _index.md
    ├── lewis-center/
    ├── westerville-polaris/
    ├── worthington-hills/
    ├── powell/
    ├── sunbury/
    └── delaware/
```

### Priority Scale

| Rating | Meaning |
|:------:|---------|
| ★ | Deal Breaker - must exist or walk |
| ● | Must Have - required |
| ◐ | Nice to Have - desired but flexible |
| ○ | Indifferent - no preference |
| ⛔ | Reject - presence is a deal-breaker |

### Adding a House

Create a new `.md` file under the appropriate area folder (e.g., `content/docs/houses/lewis-center/123-main-st.md`) with:
- Quick stats table (price, sqft, beds, baths, taxes, year built)
- Match scores table comparing against both Sweetie's and Chris's priorities
- Link to listing

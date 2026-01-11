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

### Content Structure

- `content/docs/sweetie/` - Sweetie's house preferences by category
- `content/docs/chris/` - Chris's house preferences by category
- `content/docs/houses/` - House candidates with match scores

### Adding a House

Create a new `.md` file in `content/docs/houses/` with:
- Quick stats table (price, sqft, beds, baths, taxes)
- Match scores table comparing against both Sweetie's and Chris's wishes
- Link to listing

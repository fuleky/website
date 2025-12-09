# Jolla Theme Application

This branch applies the Jolla theme to the Quarto website.

## Changes Made

1. Updated `_quarto.yml`:
   - Added `theme: jolla` under the `website` section
   - Removed legacy theme entries (`light: flatly`, `dark: darkly`) from `format.html`
   - Preserved all other settings (custom CSS, TOC, navbar)

2. `index.qmd` - No changes needed (already properly configured)

3. `styles/site.scss` - Unchanged (preserved for custom overrides)

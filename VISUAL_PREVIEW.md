# Visual Preview of Custom Styling Implementation

## Title Slide Hero (index.qmd)

```
╔═══════════════════════════════════════════════════════╗
║                                                       ║
║                  GRADIENT BACKGROUND                  ║
║             (Deep Blue #0b3d91 → Darker)             ║
║                                                       ║
║                                                       ║
║                 Your Site Title                       ║
║              (Large, Bold, White)                     ║
║                                                       ║
║          A short subtitle or description              ║
║                  (White, 95% opacity)                 ║
║                                                       ║
║                                                       ║
║                                          ┌─────────┐  ║
║                                          │  Logo   │  ║
║                                          │ (110px) │  ║
║                                          └─────────┘  ║
╚═══════════════════════════════════════════════════════╝
```

### Key Visual Elements:

1. **Background**: Linear gradient from brand blue (#0b3d91) to darker variant
2. **Title**: Responsive font size (2rem to 5rem), bold weight, white color
3. **Subtitle**: Smaller responsive text, slightly transparent
4. **Logo**: Positioned at bottom-right, 110px width, 95% opacity
5. **Layout**: Flexbox centered, minimum 60vh height, generous padding

## Site-Wide Typography

- **Body Font**: Modern system font stack (San Francisco, Segoe UI, Roboto, etc.)
- **Headings (h1-h3)**: Slightly darker brand blue (#09357f)
- **Containers**: 2rem vertical and 1rem horizontal padding

## Color Palette

- **Primary Brand**: #0b3d91 (Deep Blue)
- **Accent**: #ffd200 (Gold/Yellow)
- **Dark Variant**: #0b2b57 (Darker Blue)
- **Text on Hero**: #ffffff (White)

## Responsive Behavior

- Title and subtitle scale smoothly with viewport using CSS `clamp()`
- Logo maintains max-width of 25% on smaller screens
- Minimum hero height ensures impactful presentation on all devices
- System font stack ensures fast loading and native feel

## File Structure

```
website/
├── _quarto.yml           # Site config + stylesheet reference
├── index.qmd             # Homepage with .title-slide hero
├── about.qmd             # About page
├── styles/
│   └── site.scss         # Custom Sass with variables & styling
└── assets/
    └── images/
        ├── logo-placeholder.svg  # Placeholder logo
        └── README.md             # Logo replacement guide
```

## How to Preview

1. Install Quarto: https://quarto.org/docs/get-started/
2. Run `quarto preview` in the project directory
3. Your browser will open showing the styled website
4. The title slide will be centered with the gradient background
5. Navigate to "About" using the navbar

## Customization Quick Reference

| What to Change | File | Lines |
|----------------|------|-------|
| Site title | `_quarto.yml` or `index.qmd` | 5, 2 |
| Brand colors | `styles/site.scss` | 2-5 |
| Logo image | `assets/images/` | Replace SVG |
| Hero height | `styles/site.scss` | 12 |
| Navbar items | `_quarto.yml` | 7-9 |


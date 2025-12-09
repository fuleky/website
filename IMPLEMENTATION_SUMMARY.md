# Quarto Website Custom Styling Implementation Summary

This PR implements custom styling for a Quarto website following the examples from [Customizing Quarto Websites](https://ucsb-meds.github.io/customizing-quarto-websites/#/title-slide).

## Files Created/Modified

### Core Configuration
- **_quarto.yml**: Quarto website configuration
  - Defines the website structure and navbar
  - References the custom SCSS stylesheet for site-wide styling
  - Configured to compile SCSS to CSS automatically

### Content Pages
- **index.qmd**: Homepage with custom hero title slide
  - Uses `.title-slide` class for centered hero layout
  - Includes title, subtitle, and logo using Quarto metadata
  - Responsive design with modern gradient background
  
- **about.qmd**: Basic About page (referenced in navbar)

### Styling
- **styles/site.scss**: Custom Sass stylesheet
  - Brand color variables (`$brand-bg`, `$brand-accent`, etc.)
  - Title slide styling with gradient background
  - Responsive typography using CSS `clamp()` functions
  - Site-wide typography improvements
  - Logo positioning (bottom-right of hero)

### Assets
- **assets/images/logo-placeholder.svg**: SVG placeholder logo
  - Simple, lightweight placeholder
  - Uses brand colors from the stylesheet
  - 110px x 110px dimensions
  
- **assets/images/README.md**: Documentation for logo replacement
  - Instructions for customizing the logo
  - Supported formats and recommendations

## Key Features

### Title Slide
- **Centered hero layout** with flexbox
- **Gradient background** using brand colors
- **Responsive typography** that scales with viewport
- **Positioned logo** at bottom-right corner
- **60vh minimum height** for impactful presentation

### Site-wide Styling
- Modern system font stack for better performance
- Brand colors applied to headings
- Responsive container padding
- Consistent visual identity

## Customization Guide

### Update Site Information
Edit `_quarto.yml` or `index.qmd` to change:
- Site title
- Subtitle/tagline
- Navbar items

### Customize Colors
Edit `styles/site.scss` variables:
```scss
$brand-bg: #0b3d91;      // Primary brand color
$brand-accent: #ffd200;  // Accent color
$bg-dark: #0b2b57;       // Dark variant
$title-color: #ffffff;   // Title text color
```

### Replace Logo
1. Add your logo file to `assets/images/`
2. Either replace `logo-placeholder.svg` or update the `src` in `index.qmd`
3. Recommended size: ~110px wide

## Building the Site

When Quarto is installed, run:
```bash
quarto render
```

This will:
1. Compile the SCSS to CSS
2. Generate the HTML pages
3. Output to the `_site/` directory

## Next Steps

1. **Install Quarto** if not already available
2. **Customize content** in `index.qmd` and `about.qmd`
3. **Add your logo** to replace the placeholder
4. **Adjust colors** in `site.scss` to match your brand
5. **Run `quarto render`** to build the site
6. **Preview** the site locally with `quarto preview`

## Reference
- [Customizing Quarto Websites Tutorial](https://ucsb-meds.github.io/customizing-quarto-websites/#/title-slide)
- [Quarto Documentation](https://quarto.org/)

---

**Security Summary**: No security vulnerabilities were identified. The implementation uses standard HTML, CSS/SCSS, and Quarto configuration without any executable code or external dependencies that could introduce security risks.

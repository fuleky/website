# Personal Website

[![Website](https://img.shields.io/badge/Website-Visit-blue?style=for-the-badge)](https://fuleky.github.io/website)

**🌐 Website:** [https://fuleky.github.io/website](https://fuleky.github.io/website)

A personal website built with [Quarto](https://quarto.org).

## Building the Website

To build this website locally, you'll need to have Quarto installed. You can download it from [quarto.org](https://quarto.org/docs/get-started/).

### Preview the site

```bash
quarto preview
```

This will start a local server and open the website in your browser. The preview will automatically reload when you make changes to the source files.

### Render the site

```bash
quarto render
```

This will generate the static HTML files in the `docs/` directory.

## Project Structure

- `_quarto.yml` - Main configuration file for the website
- `index.qmd` - Home page
- `about.qmd` - About page
- `styles.css` - Custom CSS styles
- `docs/` - Generated HTML output (created when you render the site)

## Customization

You can customize the website by:

1. Editing the content in `.qmd` files (Quarto markdown)
2. Modifying the theme and layout in `_quarto.yml`
3. Adding custom styles in `styles.css`
4. Adding new pages and updating the navigation in `_quarto.yml`

## Resources

- [Quarto Documentation](https://quarto.org/docs/)
- [Creating Quarto Websites](https://quarto.org/docs/websites/)
- [Customizing Quarto Websites](https://quarto.org/docs/output-formats/html-themes.html)

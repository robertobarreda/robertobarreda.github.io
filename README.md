# robertobarreda.es

Personal website and CV built with Hugo. Clean, minimal design with timeline-based work experience display.

## Features

- 🎨 Dark theme with emerald green (#34d399) accents
- 📱 Fully responsive design
- ⚡ No build dependencies (plain CSS, no Tailwind/npm required)
- 🔗 FontAwesome and Devicon icons via CDN
- 📄 Timeline layout for work experience
- 🎯 Modular partial-based architecture

## Quick Start

### Prerequisites

```bash
# Install Hugo (Arch Linux)
sudo pacman -S hugo

# Or download from https://gohugo.io/installation/
```

### Development

```bash
# Start development server
hugo server -D

# Open http://localhost:1313 in your browser
```

**Notes:**

- Changes to files automatically reload in browser
- Press `Ctrl+C` to stop the server
- No npm/node dependencies required

### Build for Production

```bash
# Generate static site
hugo

# Output will be in ./public/
```

## Project Structure

```
.
├── hugo.toml                  # Site configuration
├── content/
│   └── about/_index.md       # CV content with timeline
├── layouts/
│   ├── index.html            # Homepage (uses about page)
│   ├── _default/
│   │   └── baseof.html       # Base template
│   └── partials/
│       ├── about-hero.html   # Title & subtitle
│       ├── social-links.html # Contact links
│       ├── about-content.html # CV content with timeline
│       └── footer.html       # Footer
├── static/
│   ├── css/
│   │   └── main.css          # All styles (no build step)
│   ├── images/
│   │   └── profile.jpg       # Profile image
│   └── assets/
│       └── cv/
│           └── Roberto_Barreda_CV.pdf
└── README.md
```

## Customization

### Changing Colors

Edit `static/css/main.css`:

```css
:root {
  --color-accent: #34d399; /* Change accent color */
}
```

### Reordering Sections

Edit `layouts/index.html`:

```go
{{ partial "about-hero.html" $aboutPage }}
{{ partial "social-links.html" . }}
{{ partial "about-content.html" $aboutPage }}
```

Simply reorder the partial calls to change the page layout.

### Editing Content

Update `content/about/_index.md`:

- Use `---` to separate timeline entries
- Content before first `---` appears as intro sections
- Each section after `---` becomes a timeline card

### Configuration

Edit `hugo.toml` to update:

- Social links (email, LinkedIn, GitHub, etc.)
- Tech stack icons
- Site title and description
- Navigation menu

## Testing Print Styles

To test how the CV looks when printed:

1. Open the page in your browser
2. Press `Ctrl+P` (or `Cmd+P` on Mac)
3. Check formatting and readability

## Deployment

The site is static HTML/CSS/JS. Deploy `public/` folder to any static hosting:

## License

Personal CV site - all content © Roberto Barreda

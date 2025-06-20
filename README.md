# Bootstrap 5.3.7 Project

A professional, single-page Bootstrap 5.3.7 project with local files and organized SCSS structure!

## Features

- ✅ Bootstrap 5.3.7 (latest version)
- ✅ Local CSS and JS files (no CDN dependencies)
- ✅ Organized SCSS structure with partials
- ✅ Single-page design with smooth scrolling
- ✅ Responsive navigation
- ✅ Contact form with validation
- ✅ Professional folder structure
- ✅ Multiple SCSS compilation methods
- ✅ Ready for PHP integration

## Quick Start

### 1. Download Bootstrap Files
Go to: https://getbootstrap.com/docs/5.3/getting-started/download/

### 2. Replace Placeholder Files
- Replace `assets/css/bootstrap.min.css` with the downloaded Bootstrap CSS
- Replace `assets/js/bootstrap.bundle.min.js` with the downloaded Bootstrap JS

### 3. Open in Browser
Open `index.html` in your web browser - that's it!

## SCSS Development

### File Structure
```
assets/scss/
├── main.scss          # Main file (imports everything)
├── _variables.scss    # Variables and Bootstrap overrides
├── _components.scss   # Component styles (buttons, cards, forms)
├── _layout.scss       # Layout and responsive styles
└── scss-compile.md    # Detailed compilation guide
```

### Quick SCSS Compilation

#### Method 1: Sass CLI (Recommended)
```bash
# Install Sass globally
npm install -g sass

# Compile once
sass assets/scss/main.scss assets/css/style.css

# Watch for changes (auto-compile)
sass --watch assets/scss/main.scss assets/css/style.css
```

#### Method 2: VS Code Extension
1. Install "Live Sass Compiler" extension
2. Click "Watch Sass" in status bar
3. Edit SCSS files and see changes instantly

#### Method 3: Online Compiler
1. Go to https://www.sassmeister.com/
2. Paste your SCSS code
3. Copy compiled CSS to `assets/css/style.css`

### SCSS Features
- **Variables**: Custom colors, spacing, typography
- **Nesting**: Organized component styles
- **Mixins**: Reusable style patterns
- **Responsive**: Mobile-first breakpoints
- **Bootstrap Integration**: Override Bootstrap variables

## Project Structure

```
├── index.html                    # Main HTML file
├── assets/
│   ├── css/
│   │   ├── bootstrap.min.css     # Bootstrap CSS (download and replace)
│   │   └── style.css            # Compiled custom styles
│   ├── scss/
│   │   ├── main.scss            # Main SCSS file
│   │   ├── _variables.scss      # Variables and overrides
│   │   ├── _components.scss     # Component styles
│   │   ├── _layout.scss         # Layout and responsive
│   │   └── scss-compile.md      # SCSS compilation guide
│   └── js/
│       ├── bootstrap.bundle.min.js  # Bootstrap JS (download and replace)
│       └── script.js            # Custom JavaScript
├── README.md                     # This file
└── SETUP.md                      # Simple setup guide
```

## Customization

### SCSS Customization
Edit files in `assets/scss/`:

- **`_variables.scss`**: Colors, fonts, spacing
- **`_components.scss`**: Buttons, cards, forms
- **`_layout.scss`**: Page structure, responsive
- **`main.scss`**: Import order and additional styles

### CSS Customization
Edit `assets/css/style.css` directly (if not using SCSS):
- Colors and typography
- Card and button styles
- Form styling
- Responsive breakpoints

### JavaScript Features
The `assets/js/script.js` includes:
- Smooth scrolling navigation
- Form validation and submission
- Active section highlighting
- Bootstrap component initialization

## For PHP Developers

This project is perfect for PHP integration:
1. Use the HTML structure as a template
2. Convert to PHP files as needed
3. Integrate with your PHP backend
4. Use SCSS for better CSS organization

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Internet Explorer 11+

## License

MIT License - feel free to use this project for any purpose.

---

**Professional, organized, and ready to use! 🚀** 
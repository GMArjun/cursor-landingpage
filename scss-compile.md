# SCSS Compilation Guide

## Method 1: Using Sass CLI (Recommended)

### Install Sass
```bash
# Install Sass globally
npm install -g sass
```

### Compile SCSS
```bash
# One-time compilation
sass assets/scss/main.scss assets/css/style.css

# Watch for changes (auto-compile)
sass --watch assets/scss/main.scss assets/css/style.css

# Compressed output (optional)
sass --style=compressed assets/scss/main.scss assets/css/style.css
```

## Method 2: Using VS Code Extension

1. Install "Live Sass Compiler" extension
2. Click "Watch Sass" in the status bar
3. Edit SCSS files and see changes instantly

## Method 3: Using Online Compiler

1. Go to https://www.sassmeister.com/
2. Paste your SCSS code
3. Copy the compiled CSS
4. Save to `assets/css/style.css`

## SCSS File Structure

```
assets/scss/
├── main.scss          # Main file (imports everything)
├── _variables.scss    # Variables and overrides
├── _components.scss   # Component styles
├── _layout.scss       # Layout and responsive
└── bootstrap/         # Bootstrap SCSS source files
```

## Bootstrap SCSS Setup

1. Download Bootstrap SCSS from: https://getbootstrap.com/docs/5.3/getting-started/download/
2. Place the `scss` folder as `assets/scss/bootstrap/`
3. Your `main.scss` should start with:
```scss
@import "bootstrap/bootstrap";
```

## Development Workflow

1. **Edit SCSS files** in `assets/scss/`
2. **Auto-compile** using watch mode
3. **Check CSS output** in `assets/css/style.css`
4. **Refresh browser** to see changes

## Tips

- Use partial files (starting with `_`) for better organization
- Keep variables in `_variables.scss`
- Use Bootstrap's mixins and functions
- Test responsive breakpoints
- Use source maps for debugging: `sass --source-map assets/scss/main.scss assets/css/style.css` 
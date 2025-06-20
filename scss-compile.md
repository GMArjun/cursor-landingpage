# SCSS Compilation Guide

## Method 1: Using Sass CLI (Recommended)

### Install Sass
```bash
# Install Sass globally
npm install -g sass

# Or install locally in your project
npm init -y
npm install sass --save-dev
```

### Compile SCSS
```bash
# One-time compilation
sass assets/scss/main.scss assets/css/style.css

# Watch for changes (auto-compile)
sass --watch assets/scss/main.scss assets/css/style.css

# Compressed output
sass --style=compressed assets/scss/main.scss assets/css/style.css
```

## Method 2: Using Node.js Scripts

### Add to package.json
```json
{
  "scripts": {
    "sass": "sass assets/scss/main.scss assets/css/style.css",
    "sass:watch": "sass --watch assets/scss/main.scss assets/css/style.css",
    "sass:compressed": "sass --style=compressed assets/scss/main.scss assets/css/style.css"
  },
  "devDependencies": {
    "sass": "^1.69.0"
  }
}
```

### Run scripts
```bash
npm run sass        # Compile once
npm run sass:watch  # Watch for changes
npm run sass:compressed  # Compressed output
```

## Method 3: Using VS Code Extension

1. Install "Live Sass Compiler" extension
2. Open VS Code settings
3. Add configuration:
```json
{
  "liveSassCompile.settings.formats": [
    {
      "format": "expanded",
      "extensionName": ".css",
      "savePath": "/assets/css"
    }
  ],
  "liveSassCompile.settings.autoprefix": true
}
```
4. Click "Watch Sass" in VS Code status bar

## Method 4: Using Online Compiler

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
└── _utilities.scss    # Utility classes (optional)
```

## Bootstrap SCSS Setup

### Option A: Using npm (Recommended)
```bash
npm install bootstrap@5.3.7
```

Then update `main.scss`:
```scss
@import "../node_modules/bootstrap/scss/bootstrap";
```

### Option B: Manual Download
1. Download Bootstrap SCSS from: https://github.com/twbs/bootstrap/tree/main/scss
2. Place in `assets/scss/bootstrap/` folder
3. Update import in `main.scss`:
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
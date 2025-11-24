# 🎨 MkDocs Catppuccin Theme
<p align="center"><img src="mkdocs_catppuccin/assets/logo.png" width="200" alt="Catppuccin MkDocs Logo"/></p>


<p align="center">
  <img src="https://raw.githubusercontent.com/catppuccin/catppuccin/main/assets/palette/macchiato.png" width="400" alt="Catppuccin Palette"/>
</p>
<p align="center">
  <a href="https://ruslanlap.github.io/Catppuccin-MkDocs/"><img src="https://img.shields.io/badge/Demo%20Site-Visit%20Now-brightgreen?style=for-the-badge" alt="Demo site"/></a>
</p>



<p align="center">
  <strong>
    Soothing pastel theme for MkDocs based on the Catppuccin color palette
  </strong>
</p>

<p align="center">
  <a href="https://pypi.org/project/mkdocs-catppuccin">
    <img alt="PyPI" src="https://img.shields.io/pypi/v/mkdocs-catppuccin">
  </a>
  <a href="https://pypi.org/project/mkdocs-catppuccin">
    <img alt="PyPI - Python Version" src="https://img.shields.io/pypi/pyversions/mkdocs-catppuccin">
  </a>
  <a href="https://github.com/ruslanlap/Catppuccin-MkDocs/blob/main/LICENSE">
    <img alt="License" src="https://img.shields.io/github/license/ruslanlap/Catppuccin-MkDocs">
  </a>
</p>

---

## 📖 Overview

This is a [MkDocs](https://www.mkdocs.org/) theme that extends [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) with the beautiful [Catppuccin](https://catppuccin.com) color palette. It provides a comfortable and aesthetically pleasing documentation experience with carefully crafted soothing pastel colors.

## ✨ Features

- 🎨 **Four Catppuccin Flavors**: Latte (light), Frappé, Macchiato, and Mocha (dark)
- 🌈 **Complete Color Integration**: All UI elements styled with Catppuccin colors
- 🎯 **Syntax Highlighting**: Code blocks with Catppuccin-themed syntax colors
- 📱 **Fully Responsive**: Works perfectly on all devices
- 🔌 **Easy Installation**: Just `pip install mkdocs-catppuccin`
- ⚡ **Extends Material**: All Material for MkDocs features available

## 🚀 Installation

Install the theme using pip:

```bash
pip install mkdocs-catppuccin
```

Or install from source:

```bash
git clone https://github.com/ruslanlap/Catppuccin-MkDocs.git
cd Catppuccin-MkDocs
pip install -e .
```

## 📝 Step-by-Step Configuration Guide

### Step 1: Install the Theme

```bash
pip install mkdocs-catppuccin
```

### Step 2: Create Project Structure

Your MkDocs project should have this structure:

```
your-project/
├── docs/
│   ├── index.md              # Home page
│   ├── assets/               # Assets folder (optional)
│   │   └── logo.png         # Your logo
│   └── stylesheets/         # CSS folder (optional)
│       └── extra.css        # Your custom styles
└── mkdocs.yml               # Configuration file
```

### Step 3: Basic Configuration

Create or edit your `mkdocs.yml` file:

```yaml
# Basic site information
site_name: Your Project Name
site_description: Your documentation description
site_url: https://yourname.github.io/your-project/

# Catppuccin theme configuration
theme:
  name: catppuccin
  
  # Choose color scheme (pick one or multiple)
  palette:
    # Light theme - Catppuccin Latte
    - scheme: latte
      toggle:
        icon: material/weather-sunny
        name: Switch to dark mode
    
    # Dark theme - Catppuccin Mocha
    - scheme: mocha
      toggle:
        icon: material/weather-night
        name: Switch to light mode
  
  # Add your logo (optional)
  logo: assets/logo.png        # Path to your logo
  favicon: assets/logo.png     # Browser tab icon
  
  # Useful features
  features:
    - navigation.tabs          # Navigation tabs
    - navigation.sections      # Navigation sections
    - navigation.top           # Back to top button
    - search.suggest           # Search suggestions
    - search.highlight         # Highlight search results
    - content.code.copy        # Copy code button

# Your site navigation
nav:
  - Home: index.md
  - About: about.md

# Plugins
plugins:
  - search                     # Documentation search
```

### Step 4: Custom Styles (Optional)

**IMPORTANT:** The theme already includes all Catppuccin styles! You **DO NOT need** to add `extra_css` for basic usage.

Add `extra_css` **ONLY if** you want to customize something:

```yaml
# Add this ONLY if you need custom styles
extra_css:
  - stylesheets/extra.css      # Your custom styles
```

Create `docs/stylesheets/extra.css` file for your customizations:

```css
/* Example: change heading color */
.md-typeset h1 {
  color: #c6a0f6;  /* Catppuccin Mauve */
}
```

#### Changing Accent Color

By default, the theme uses **Green** as the accent color (for links, active navigation, etc.). You can change it to any Catppuccin color you prefer!

**Example: Change accent from Green to Pink**

Add this to your `docs/stylesheets/extra.css`:

```css
/* Change accent color to Pink */
[data-md-color-scheme="latte"] {
  --md-accent-fg-color: var(--ctp-latte-pink);
  --md-accent-fg-color--transparent: rgba(234, 118, 203, 0.1);
}

[data-md-color-scheme="frappe"] {
  --md-accent-fg-color: var(--ctp-frappe-pink);
  --md-accent-fg-color--transparent: rgba(244, 184, 228, 0.1);
}

[data-md-color-scheme="macchiato"] {
  --md-accent-fg-color: var(--ctp-macchiato-pink);
  --md-accent-fg-color--transparent: rgba(245, 189, 230, 0.1);
}

[data-md-color-scheme="mocha"] {
  --md-accent-fg-color: var(--ctp-mocha-pink);
  --md-accent-fg-color--transparent: rgba(245, 194, 231, 0.1);
}
```

**Available Catppuccin colors for accent:**
- `pink` - Soft pink (shown above)
- `mauve` - Purple
- `blue` - Blue
- `sapphire` - Cyan-blue
- `sky` - Light cyan
- `teal` - Teal
- `green` - Green (default)
- `yellow` - Yellow
- `peach` - Orange
- `red` - Red
- `maroon` - Dark red
- `lavender` - Light purple

Just replace `pink` with any color name from the list above in the CSS variables!

### Step 5: All 4 Color Schemes

If you want to give users a choice of all 4 Catppuccin variants:

```yaml
theme:
  name: catppuccin
  palette:
    # Light theme - Latte
    - scheme: latte
      toggle:
        icon: material/weather-sunny
        name: Switch to Frappé
    
    # Dark theme - Frappé (coolest)
    - scheme: frappe
      toggle:
        icon: material/weather-night
        name: Switch to Macchiato
    
    # Dark theme - Macchiato (warm)
    - scheme: macchiato
      toggle:
        icon: material/weather-partly-cloudy
        name: Switch to Mocha
    
    # Dark theme - Mocha (warmest)
    - scheme: mocha
      toggle:
        icon: material/weather-cloudy
        name: Switch to Latte
```

### Step 6: Complete Configuration Example

Here's a complete `mkdocs.yml` example with all features:

```yaml
site_name: My Documentation
site_description: Beautiful documentation with Catppuccin theme
site_url: https://yourname.github.io/your-project/
repo_url: https://github.com/yourname/your-project
repo_name: yourname/your-project

theme:
  name: catppuccin
  palette:
    - scheme: latte
      toggle:
        icon: material/weather-sunny
        name: Switch to Frappé
    - scheme: frappe
      toggle:
        icon: material/weather-night
        name: Switch to Macchiato
    - scheme: macchiato
      toggle:
        icon: material/weather-partly-cloudy
        name: Switch to Mocha
    - scheme: mocha
      toggle:
        icon: material/weather-cloudy
        name: Switch to Latte
  
  logo: assets/logo.png
  favicon: assets/logo.png
  
  features:
    - navigation.tabs
    - navigation.sections
    - navigation.expand
    - navigation.footer
    - navigation.top
    - navigation.tracking
    - search.suggest
    - search.highlight
    - search.share
    - content.code.copy
    - content.code.annotate

# Navigation
nav:
  - Home: index.md
  - Configuration: configuration.md

# Plugins
plugins:
  - search

# Markdown extensions
markdown_extensions:
  - admonition
  - pymdownx.details
  - pymdownx.superfences
  - pymdownx.highlight:
      anchor_linenums: true
  - pymdownx.inlinehilite
  - pymdownx.snippets
  - tables
  - toc:
      permalink: true

# Copyright
copyright: Copyright &copy; 2025 Your Name

# Additional settings
extra:
  social:
    - icon: fontawesome/brands/github
      link: https://github.com/yourname/your-project
  generator: false
```

### 📌 Important Notes

1. **Logo**: Place your `logo.png` file in the `docs/assets/` folder
2. **CSS**: The theme already includes all Catppuccin styles - `extra_css` is only needed for your own customizations
3. **Color schemes**: You can use a single scheme or all four with a toggle
4. **Testing**: Run `mkdocs serve` to preview your documentation locally

## 🎨 Color Schemes

### Light Mode - Latte 🌻
Perfect for daytime reading with warm, gentle tones:
- **Background**: `#eff1f5` (Base)
- **Text**: `#4c4f69` (Text)
- **Primary**: `#8839ef` (Mauve)
- **Accent**: `#1e66f5` (Blue)

### Dark Mode - Mocha 🌙
Cozy and comfortable for nighttime with rich, soft colors:
- **Background**: `#1e1e2e` (Base)
- **Text**: `#cdd6f4` (Text)
- **Primary**: `#cba6f7` (Mauve)
- **Accent**: `#89b4fa` (Blue)

### Syntax Highlighting

Both themes include complete syntax highlighting:
- **Keywords**: Red
- **Strings**: Green
- **Functions**: Mauve
- **Numbers**: Peach
- **Comments**: Overlay0
- **Operators**: Sky
- **Variables**: Rosewater

## 📦 What's Included

```
mkdocs-catppuccin/
├── mkdocs_catppuccin/
│   ├── __init__.py
│   ├── mkdocs_theme.yml         # Theme configuration
│   └── assets/
│       └── stylesheets/
│           └── catppuccin.css   # Catppuccin colors
├── pyproject.toml               # Package configuration
├── LICENSE                      # MIT License
└── README.md                    # This file
```

## 🔧 Development

### Setting Up Development Environment

```bash
# Clone the repository
git clone https://github.com/ruslanlap/Catppuccin-MkDocs.git
cd Catppuccin-MkDocs

# Install in editable mode
pip install -e .

# Create a test MkDocs project
mkdocs new test-site
cd test-site

# Configure to use the theme
echo "theme:
  name: catppuccin" > mkdocs.yml

# Serve the documentation
mkdocs serve
```

### Building the Package

```bash
# Install build tools
pip install build twine

# Build the package
python -m build

# The package will be in dist/
```

### Publishing to PyPI

```bash
# Upload to TestPyPI first
python -m twine upload --repository testpypi dist/*

# If everything looks good, upload to PyPI
python -m twine upload dist/*
```

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Credits

- **Catppuccin Theme**: [catppuccin.com](https://catppuccin.com) - The beautiful color palette
- **Material for MkDocs**: [squidfunk/mkdocs-material](https://github.com/squidfunk/mkdocs-material) - The base theme
- **MkDocs**: [mkdocs.org](https://www.mkdocs.org/) - The documentation framework

## 🔗 Links

- **Homepage**: [github.com/ruslanlap/Catppuccin-MkDocs](https://github.com/ruslanlap/Catppuccin-MkDocs)
- **PyPI**: [pypi.org/project/mkdocs-catppuccin](https://pypi.org/project/mkdocs-catppuccin)
- **Catppuccin**: [catppuccin.com](https://catppuccin.com)
- **Material for MkDocs**: [squidfunk.github.io/mkdocs-material](https://squidfunk.github.io/mkdocs-material)


# Catppuccin-MkDocs

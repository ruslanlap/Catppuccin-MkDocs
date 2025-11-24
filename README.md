# 🎨 MkDocs Catppuccin Theme
<p align="center"><img src="mkdocs_catppuccin/assets/logo.png" width="200" alt="Catppuccin MkDocs Logo"/></p>


<p align="center">
  <img src="https://raw.githubusercontent.com/catppuccin/catppuccin/main/assets/palette/macchiato.png" width="400" alt="Catppuccin Palette"/>
</p>

[Demo site](https://ruslanlap.github.io/Catppuccin-MkDocs/)

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

## 📝 Configuration

### 1. Enable the Theme

In your `mkdocs.yml`, set the theme name to `catppuccin`:

```yaml
theme:
  name: catppuccin
```

### 2. Configure Color Palette

You can choose from 4 Catppuccin flavors: `latte`, `frappe`, `macchiato`, or `mocha`.

#### Single Color Scheme

To use a single flavor (e.g., Macchiato):

```yaml
theme:
  name: catppuccin
  palette:
    - scheme: macchiato
```

#### Light/Dark Toggle

To enable toggling between a light (Latte) and dark (Mocha) theme:

```yaml
theme:
  name: catppuccin
  palette:
    # Light mode - Catppuccin Latte
    - scheme: latte
      toggle:
        icon: material/weather-night
        name: Switch to dark mode

    # Dark mode - Catppuccin Mocha
    - scheme: mocha
      toggle:
        icon: material/weather-sunny
        name: Switch to light mode
```

### 3. Custom CSS (Optional)

The theme comes with built-in Catppuccin styling. However, if you want to customize specific elements or override colors, you can use the provided CSS files.

1.  **`docs/stylesheets/catppuccin.css`**: This file contains the core Catppuccin color variables and theme definitions. You generally don't need to touch this unless you are developing the theme itself.
2.  **`docs/stylesheets/extra.css`**: Use this file for your own custom overrides.

To use these files, add them to `extra_css` in `mkdocs.yml`:

```yaml
extra_css:
  - stylesheets/catppuccin.css # Optional: Only if you need to manually include the base styles
  - stylesheets/extra.css      # Your custom overrides
```

### 4. Advanced Customization

You can further customize the theme using Material for MkDocs features:

```yaml
theme:
  name: catppuccin
  features:
    - navigation.tabs
    - navigation.sections
    - navigation.top
    - search.suggest
    - search.highlight
    - content.code.copy
```

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

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

## 📝 Покрокова Інструкція / Step-by-Step Guide

### Крок 1: Встановіть тему / Step 1: Install the Theme

```bash
pip install mkdocs-catppuccin
```

### Крок 2: Створіть структуру проєкту / Step 2: Create Project Structure

Ваш проєкт MkDocs повинен мати таку структуру:

```
your-project/
├── docs/
│   ├── index.md              # Головна сторінка
│   ├── assets/               # Папка для ресурсів (необов'язково)
│   │   └── logo.png         # Ваше лого
│   └── stylesheets/         # Папка для CSS (необов'язково)
│       └── extra.css        # Ваші власні стилі
└── mkdocs.yml               # Файл конфігурації
```

### Крок 3: Базова Конфігурація / Step 3: Basic Configuration

Створіть або відредагуйте файл `mkdocs.yml`:

```yaml
# Основна інформація про сайт
site_name: Назва Вашого Проєкту
site_description: Опис вашої документації
site_url: https://yourname.github.io/your-project/

# Налаштування теми Catppuccin
theme:
  name: catppuccin
  
  # Вибір кольорової схеми (оберіть одну або кілька)
  palette:
    # Світла тема - Catppuccin Latte
    - scheme: latte
      toggle:
        icon: material/weather-sunny
        name: Перемкнути на темну тему
    
    # Темна тема - Catppuccin Mocha
    - scheme: mocha
      toggle:
        icon: material/weather-night
        name: Перемкнути на світлу тему
  
  # Додайте своє лого (необов'язково)
  logo: assets/logo.png        # Шлях до вашого лого
  favicon: assets/logo.png     # Іконка для вкладки браузера
  
  # Корисні функції
  features:
    - navigation.tabs          # Вкладки навігації
    - navigation.sections      # Секції в навігації
    - navigation.top           # Кнопка "Вгору"
    - search.suggest           # Підказки при пошуку
    - search.highlight         # Підсвічування результатів пошуку
    - content.code.copy        # Кнопка копіювання коду

# Навігація вашого сайту
nav:
  - Головна: index.md
  - Про проєкт: about.md

# Плагіни
plugins:
  - search                     # Пошук по документації
```

### Крок 4: Додаткові Стилі (Необов'язково) / Step 4: Custom Styles (Optional)

**ВАЖЛИВО:** Тема вже включає всі стилі Catppuccin! Вам **НЕ потрібно** додавати `extra_css` для базового використання.

Додайте `extra_css` **тільки якщо** ви хочете змінити щось своє:

```yaml
# Додайте це ТІЛЬКИ якщо потрібні власні стилі
extra_css:
  - stylesheets/extra.css      # Ваші власні стилі
```

Створіть файл `docs/stylesheets/extra.css` для ваших змін:

```css
/* Приклад: змінити колір заголовків */
.md-typeset h1 {
  color: #c6a0f6;  /* Catppuccin Mauve */
}
```

### Крок 5: Всі 4 Кольорові Схеми / Step 5: All 4 Color Schemes

Якщо хочете дати користувачам вибір з усіх 4 варіантів Catppuccin:

```yaml
theme:
  name: catppuccin
  palette:
    # Світла тема - Latte
    - scheme: latte
      toggle:
        icon: material/weather-sunny
        name: Перемкнути на Frappé
    
    # Темна тема - Frappé (найхолодніша)
    - scheme: frappe
      toggle:
        icon: material/weather-night
        name: Перемкнути на Macchiato
    
    # Темна тема - Macchiato (тепла)
    - scheme: macchiato
      toggle:
        icon: material/weather-partly-cloudy
        name: Перемкнути на Mocha
    
    # Темна тема - Mocha (найтепліша)
    - scheme: mocha
      toggle:
        icon: material/weather-cloudy
        name: Перемкнути на Latte
```

### Крок 6: Повний Приклад Конфігурації / Step 6: Complete Example

Ось повний приклад `mkdocs.yml` з усіма можливостями:

```yaml
site_name: Моя Документація
site_description: Красива документація з темою Catppuccin
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

# Навігація
nav:
  - Головна: index.md
  - Конфігурація: configuration.md

# Плагіни
plugins:
  - search

# Розширення Markdown
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

# Копірайт
copyright: Copyright &copy; 2025 Ваше Ім'я

# Додаткові налаштування
extra:
  social:
    - icon: fontawesome/brands/github
      link: https://github.com/yourname/your-project
  generator: false
```

### 📌 Важливі Примітки / Important Notes

1. **Лого**: Покладіть ваш файл `logo.png` у папку `docs/assets/`
2. **CSS**: Тема вже включає всі стилі Catppuccin - `extra_css` потрібен тільки для ваших власних змін
3. **Кольорові схеми**: Можете використати одну схему або всі чотири з перемикачем
4. **Тестування**: Запустіть `mkdocs serve` щоб побачити результат локально

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

# 🎨 HTML Advanced Project - Techium Website

> **Advanced HTML5 Concepts & Best Practices for a Complete Marketing Website**

![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)
![Language](https://img.shields.io/badge/Language-HTML5-E34C26?style=flat-square&logo=html5)
![School](https://img.shields.io/badge/School-Holberton-blue?style=flat-square)
![Files](https://img.shields.io/badge/Files-40-informational?style=flat-square)

---

## 📋 Table of Contents

- [🎯 Project Overview](#-project-overview)
- [📂 File Structure](#-file-structure)
- [📝 Detailed File Documentation](#-detailed-file-documentation)
- [🎨 HTML5 Semantic Elements](#-html5-semantic-elements)
- [✅ Best Practices](#-best-practices)
- [🚀 How to Use](#-how-to-use)

---

## 🎯 Project Overview

Ce projet constitue une implémentation **complète et progressive** d'un site web pour l'agence digitale **Techium**. Le site est construit avec **HTML5 sémantique pur**, sans CSS, en suivant une progression pédagogique étape par étape à travers 40 fichiers.

### Objectifs Atteints

- ✨ Maîtriser la structure HTML5 sémantique complète
- 🏗️ Utiliser les balises sémantiques pour meilleure accessibilité
- 📱 Créer un site responsive-ready avec viewport meta
- 🎯 Implémenter une navigation logique et hiérarchisée
- 🖼️ Intégrer images, vidéos, audio et iframes
- 📊 Ajouter des tableaux, listes et éléments interactifs
- ✅ Respecter les standards Holberton School

---

## 📂 File Structure

```
html_advanced/
│
├── Main Entry Point
├── index.html                # 🎯 FINAL: Homepage avec SVG social icons
├── about.html                # À propos
├── contact.html              # Contact
├── latest_news.html          # Actualités
│
├── Progressive Development (0-36)
├── 0-index.html              # Structure HTML de base
├── 1-index.html              # Attributs lang et dir
├── 2-index.html              # Meta charset, viewport, title, description, favicons
├── ... (3-10)
├── 11-styleguide.html        # 📚 Guide style: Headings (h1-h6)
├── 12-index.html             # Paragraphes dans chaque section
├── 13-styleguide.html        # Guide style: Exemples paragraphes
├── ... (14-25)
├── 26-styleguide.html        # Guide style: Listes (ul, ol, dl)
├── ... (27-35)
├── 36-index.html             # Images dans tous les sections
│
├── Final Styleguide Versions
├── 38-styleguide.html        # Guide style + Video player
├── 39-styleguide.html        # Guide style + Video + Audio player
├── styleguide.html           # Guide style COMPLET (Video + Audio + Iframe)
│
└── Documentation
    └── README.md             # Cette documentation
```

---

## 📝 Detailed File Documentation

### Phase 1: Foundation & Metadata (Files 0-10)

#### 2-index.html - Meta Tags & Favicon Setup
**Key features**:
- `<meta charset="utf-8">` - UTF-8 encoding
- `<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">` - Responsive configuration
- `<title>Homepage - Techium</title>` - Page title
- `<meta name="description" content="Techium is a digital agency">` - SEO description
- `<link rel="icon" type="image/x-icon" href="./favicon.ico">`
- `<link rel="icon" type="image/png" href="./favicon.png">`

### Phase 2: Content Structure (Files 11-36)

#### 11-styleguide.html - Heading Hierarchy
Demonstrates proper use of h1-h6 tags with semantic structure.

#### 12-index.html - Paragraph Content
Adds meaningful content to all main sections with Lorem ipsum text.

#### 14-15-index.html - Structural Organization
Implements proper div wrappers and section hierarchy.

#### 16-17-index.html - Semantic HTML5
Adds `<header>`, semantic comments for better documentation.

#### 18-index.html - Linked Branding
Converts text logo to linked element: `<a href="/"><span>Techium</span></a>`

#### 20-21-index.html - Navigation & Social Links
- Main navigation list with 7 menu items
- Social media links: Facebook, Twitter, Instagram

#### 22-23-index.html - Call-to-Action
- CTA buttons: "Get started", "Learn more about us", "Get in touch"
- Links on service/work/news headings

#### 25-index.html - Footer Navigation
Secondary navigation for legal pages: Terms of Use, Privacy Policy, Cookie Policy

#### 26-30-styleguide.html - Styleguide Elements
- Lists (unordered, ordered, definition)
- Horizontal rules
- Blockquotes and inline quotes

#### 31-36-index.html - Advanced Elements
- Address tag and author attribution
- Tables with proper scope attributes
- Details/summary interactive elements
- Image integration throughout site

### Phase 3: Media & Advanced Features (Files 38-styleguide.html)

#### index.html (Final) - SVG Social Icons
Replaces text links with scalable vector graphics (25x25px each):
```html
<svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" width="25px" height="25px">
  <!-- Icon paths -->
</svg>
```

#### 38-styleguide.html - Video Player
```html
<video controls loop poster="https://...thumbnail.jpg">
  <source src="https://...BigBuckBunny.mp4" type="video/mp4">
  Sorry, your browser doesn't support video element
</video>
```

#### 39-styleguide.html - Audio Player
```html
<audio controls>
  <source src="https://...TroubleChapter8_64kb.mp3" type="audio/mpeg">
  Sorry, your browser doesn't support audio element
</audio>
```

#### styleguide.html (Final) - Iframe Embedding
```html
<iframe title="Holberton School" width="350px" height="200px" 
        src="https://www.youtube.com/embed/41N6bKO-NVI">
  Holberton Sally
</iframe>
```

---

## 🎨 HTML5 Semantic Elements

All files implement proper semantic HTML5 with these key elements:

- `<header>` - Page and section headers
- `<nav>` - Navigation lists
- `<main>` - Primary content area
- `<section>` - Thematic groupings
- `<article>` - Self-contained content
- `<footer>` - Page footer
- `<address>` - Contact information
- `<h1-h6>` - Heading hierarchy
- `<video>` - Video player
- `<audio>` - Audio player
- `<iframe>` - Embedded content
- `<details>/<summary>` - Interactive disclosure
- `<table>` - Tabular data
- `<blockquote>` - Citations
- `<mark>` - Highlighted text
- `<pre>/<code>` - Preformatted code

---

## ✅ Best Practices

### Accessibility
- All images have descriptive `alt` attributes
- All iframes have `title` attributes
- Table headers use `scope` attributes (col/row)
- Proper heading hierarchy (h1 → h6)
- Semantic HTML for screen readers

### SEO
- Meta charset and viewport specified
- Page title and description provided
- Structured content with semantic tags
- Proper internal linking

### Code Quality
- HTML5 valid syntax throughout
- Proper indentation and formatting
- Semantic HTML structure
- Meaningful comments where needed

### Media Handling
- Fallback content for all media
- Proper MIME types specified
- Responsive image sizing
- External media from trusted CDNs

---

## 🚀 How to Use

### View the website

```bash
cd html_advanced
python3 -m http.server 8000
```

Then visit in browser:
- Homepage: http://localhost:8000/index.html
- About page: http://localhost:8000/about.html
- Contact page: http://localhost:8000/contact.html
- Latest news: http://localhost:8000/latest_news.html
- Styleguide: http://localhost:8000/styleguide.html

---

## 📊 Project Statistics

- **Total Files**: 40+ numbered files + 4 main pages
- **Styleguide Versions**: 10+ (11-39 + styleguide.html)
- **HTML5 Elements Used**: 25+
- **Images Integrated**: 11 (logo + works + about + news + testimonials)
- **Media Files**: 2 (video + audio)
- **SVG Icons**: 3 (Facebook, Twitter, Instagram)
- **Total Code Lines**: 3000+

---

## � Key Learning Outcomes

- Master HTML5 semantic markup
- Implement proper document structure
- Use media elements correctly
- Apply accessibility best practices
- Create accessible navigation
- Handle fallback content properly
- Understand heading hierarchy
- Use proper ARIA attributes
- Work with external media
- Follow semantic web standards

---

Made with ❤️ for Holberton School

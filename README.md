# Pro Residential Services Website

A static website built with Hugo using the Hermit-V2 theme.

## File Structure

```
prores-website/
├── content/
│   ├── _index.md          # Landing page / Home
│   ├── about.md           # About Us page
│   ├── contact.md         # Contact page with form
│   ├── gallery.md         # Photo gallery page
│   ├── services.md        # Services listing
│   └── posts/             # Blog posts (optional)
├── static/
│   └── images/
│       └── gallery/       # Gallery images go here
├── themes/
│   └── hermit-v2/         # Theme files
└── hugo.toml              # Site configuration
```

## Quick Start

### 1. Copy Content Files

Copy the files from the `content/` folder to your repository's `content/` folder:

```bash
# From your repository root
cp -r /path/to/these/files/content/* content/
```

### 2. Update Configuration

Replace your existing `hugo.toml` with the provided one, or merge the settings:

```bash
cp hugo.toml /path/to/your/repo/hugo.toml
```

### 3. Add Images

Place your gallery images in `static/images/gallery/` and update the `gallery.md` file to reference them.

### 4. Customize Content

Edit each `.md` file to add your actual:
- Business information
- Contact details
- Service descriptions
- Team bios
- Service area locations

### 5. Set Up Contact Form

The contact form uses Formspree. To enable it:
1. Create a free account at [formspree.io](https://formspree.io)
2. Create a new form
3. Replace `YOUR_FORM_ID` in `contact.md` with your actual form ID

### 6. Test Locally

```bash
hugo server -D
```

Visit `http://localhost:1313` to preview your site.

### 7. Build for Production

```bash
hugo
```

The built site will be in the `public/` folder.

## Customization

### Colors

Edit the theme colors in `hugo.toml`:
```toml
themeColor = "#2d5a27"    # Main theme color
accentColor = "#4a9f42"   # Accent/highlight color
```

### Menu Items

Add or remove menu items in `hugo.toml`:
```toml
[[menu.main]]
  name = "New Page"
  url = "/new-page/"
  weight = 6
```

### Featured Images

Add a featured background image to any page:
```yaml
---
title: "Page Title"
featuredImg: "/images/your-image.jpg"
---
```

## Adding Blog Posts (Optional)

Create posts in `content/posts/`:

```bash
hugo new posts/my-first-post.md
```

## Deployment

### Netlify
Already configured with `netlify.toml`. Just connect your GitHub repo to Netlify.

### GitHub Pages
Add a GitHub Action workflow or use the Hugo documentation for GitHub Pages setup.

## Need Help?

- [Hugo Documentation](https://gohugo.io/documentation/)
- [Hermit-V2 Theme](https://github.com/1bl4z3r/hermit-V2)
- [Hermit-V2 Demo & Docs](https://1bl4z3r.github.io/hermit-V2)

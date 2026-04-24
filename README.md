# Karthik's Personal Site

Hugo-powered personal site + blog. Palette: beige, gray, lilac, deep brown.

## Quick Start (Arch Linux)

```bash
# 1. Install Hugo
sudo pacman -S hugo

# 2. Preview locally
hugo server -D
# → Open http://localhost:1313

# 3. Write a new blog post
hugo new blog/my-new-post.md
# Edit content/blog/my-new-post.md, remove `draft: true` when ready

# 4. Build for production
hugo --gc --minify
# Output goes to ./public/
```

## Deploy to GitHub Pages

This repo includes a GitHub Actions workflow (`.github/workflows/hugo.yml`)
that auto-builds and deploys on every push to `main`.

### First-time setup:

1. Replace the contents of your `karthikb-dev.github.io` repo with this project
2. Go to **Settings → Pages → Source** and select **GitHub Actions**
3. Push to `main` — the site builds and deploys automatically

### Custom domain (<$10/year):

1. Buy a domain (Cloudflare Registrar, Namecheap, Porkbun — all under $10/yr for .com)
2. Add DNS records pointing to GitHub Pages:
   - `A` records: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` for `www` → `karthikb-dev.github.io`
3. Create a file `static/CNAME` containing your domain (e.g. `karthikbhattaram.com`)
4. In GitHub repo Settings → Pages, enter your custom domain
5. Enable "Enforce HTTPS"

## Project Structure

```
.
├── archetypes/default.md        # Template for new posts
├── content/
│   └── blog/                    # Blog posts (Markdown)
├── layouts/
│   ├── _default/baseof.html     # Base HTML shell
│   ├── _default/single.html     # Single post layout
│   ├── blog/list.html           # Blog listing page
│   ├── index.html               # Homepage
│   └── partials/                # Header, footer
├── static/
│   ├── css/style.css            # All styles (your palette!)
│   ├── assets/pdf/              # Resume, certs
│   └── images/                  # Site images
├── hugo.toml                    # Site config
└── .github/workflows/hugo.yml   # Auto-deploy
```

## Writing Posts

Posts are Markdown files in `content/blog/`. Front matter:

```yaml
---
title: "My Post Title"
date: 2025-04-20
summary: "Shows up on the blog listing page."
tags: ["security", "networking"]
draft: false
---

Your content here. Supports all Markdown + Hugo shortcodes.
```

## Tweaking the Palette

All colors are CSS custom properties in `static/css/style.css`:

```css
:root {
  --beige:      #F5F0EB;
  --lilac:      #B8A9C9;
  --lilac-deep: #8E7BA8;
  --brown:      #3B2A1A;
  --gray:       #9E9E9E;
}
```

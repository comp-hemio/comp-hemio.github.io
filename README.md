# Hemio - Contemporary Piano Composer Website

Official website for Hemio, featuring the Hemio Monthly Series and compositional essays.

## Setup Instructions

### Option 1: GitHub Direct Upload (Easiest)

1. Go to https://github.com/comp-hemio
2. Click "New repository"
3. Name it exactly: `comp-hemio.github.io`
4. Make it Public
5. Click "Create repository"
6. Upload all files from this folder
7. Wait 1-2 minutes
8. Visit https://comp-hemio.github.io

### Option 2: Local Development

1. Install Ruby (https://www.ruby-lang.org/en/downloads/)
2. Install Bundler:
   ```bash
   gem install bundler
   ```
3. Clone the repository:
   ```bash
   git clone https://github.com/comp-hemio/comp-hemio.github.io.git
   cd comp-hemio.github.io
   ```
4. Install dependencies:
   ```bash
   bundle install
   ```
5. Run locally:
   ```bash
   bundle exec jekyll serve
   ```
6. Open http://localhost:4000

## Customization Needed

### Essential Updates in `_config.yml`:
- Add your Spotify artist ID
- Add your Apple Music URL
- Add your YouTube channel URL
- Add your email for contact
- Upload avatar image to `/assets/images/avatar.jpg`

### Content Updates:
- Replace placeholder images in `/assets/images/`
- Update streaming links in `/music/` page
- Add your actual compositions to the Music page
- Write new blog posts in `/_posts/` folder

### Images Needed:
- `/assets/images/avatar.jpg` - Your profile photo
- `/assets/images/header-piano.jpg` - Homepage header
- `/assets/images/music-header.jpg` - Music page header
- `/assets/images/writing-header.jpg` - Writing page header
- `/assets/images/water-memories-cover.jpg` - Album art
- Album art for each release

## Adding New Content

### New Blog Post:
Create a file in `/_posts/` with format: `YYYY-MM-DD-title.md`

```yaml
---
layout: single
title: "Your Title"
date: 2025-12-15
categories:
  - composition
tags:
  - minimalism
excerpt: "Brief description"
---

Your content here...
```

### New Music Release:
Edit `/_pages/music.md` and add your new release following the existing format.

## Multilingual Support (Future)

To add Korean, Japanese, Spanish versions:
1. Create folders: `/ko/`, `/ja/`, `/es/`
2. Duplicate pages in each language folder
3. Update `_config.yml` with multilingual plugin
4. Add language switcher to navigation

## Domain Setup (Optional)

To use a custom domain like `hemio.com`:
1. Buy domain from registrar (Namecheap, GoDaddy, etc.)
2. Add CNAME file with your domain
3. Configure DNS A records to GitHub Pages IPs
4. Update `url` in `_config.yml`

## Support

- Jekyll Documentation: https://jekyllrb.com/docs/
- Minimal Mistakes Theme: https://mmistakes.github.io/minimal-mistakes/
- GitHub Pages: https://docs.github.com/en/pages

## License

All content © Hemio. All rights reserved.

# Hemio Website - Quick Start Guide

## 🚀 Step 1: Create GitHub Repository

1. Go to: https://github.com/comp-hemio
2. Click the green "New" button (or "New repository")
3. Repository name: **comp-hemio.github.io** (must be exactly this!)
4. Description: "Contemporary piano composer - Official website"
5. Select **Public**
6. **DO NOT** initialize with README
7. Click "Create repository"

## 📤 Step 2: Upload Files

### Method A: Web Upload (Easiest)
1. Download and unzip `comp-hemio-website.zip`
2. On the new repository page, click "uploading an existing file"
3. Drag and drop ALL files from the unzipped folder
4. Scroll down and click "Commit changes"

### Method B: Git Command Line
```bash
# Unzip the file first
cd path/to/unzipped/folder

# Initialize git
git init
git add .
git commit -m "Initial commit - Hemio website"

# Connect to GitHub
git remote add origin https://github.com/comp-hemio/comp-hemio.github.io.git
git branch -M main
git push -u origin main
```

## ⏱️ Step 3: Wait & Visit

Wait 1-2 minutes for GitHub Pages to build, then visit:
**https://comp-hemio.github.io**

## ✏️ Step 4: Customize Your Site

### Essential Updates:

1. **Edit `_config.yml`:**
   - Line 13: Add your Spotify artist URL
   - Line 15: Add your Apple Music URL
   - Line 17: Add your YouTube URL
   - Line 46: Add your email

2. **Add Images:**
   - Create folder: `assets/images/`
   - Upload: avatar.jpg (your photo)
   - Upload: header images
   - Upload: album art
   - See `assets/images/README.md` for specifications

3. **Update Music Page:**
   - Edit `_pages/music.md`
   - Add your actual releases
   - Add streaming links

4. **Write Blog Posts:**
   - Create files in `_posts/`
   - Format: `YYYY-MM-DD-title.md`
   - Copy format from existing post

## 🔧 Editing Files on GitHub

1. Navigate to the file (e.g., `_config.yml`)
2. Click the pencil icon (Edit)
3. Make changes
4. Scroll down, add commit message
5. Click "Commit changes"
6. Wait 30-60 seconds, refresh your site

## 📝 Adding New Content

### New Release:
1. Edit `_pages/music.md`
2. Add new section following the format
3. Update archive.md

### New Blog Post:
1. Go to `_posts` folder
2. Click "Add file" → "Create new file"
3. Name: `2025-12-15-your-title.md`
4. Copy format from existing post
5. Commit

## 🌐 Custom Domain (Optional)

If you want `hemio.com` instead of `comp-hemio.github.io`:

1. Buy domain from Namecheap/GoDaddy
2. In domain DNS settings, add:
   - Type: A, Host: @, Value: 185.199.108.153
   - Type: A, Host: @, Value: 185.199.109.153
   - Type: A, Host: @, Value: 185.199.110.153
   - Type: A, Host: @, Value: 185.199.111.153
3. Edit CNAME file, add your domain
4. In GitHub repo: Settings → Pages → Custom domain

## 🎨 Design Customization

To change theme colors, edit `_config.yml`:
- Line 24: `minimal_mistakes_skin`
- Options: "air", "aqua", "contrast", "dark", "mint", "plum"

## 🔍 SEO Setup (Later)

Once you have content:
1. Submit sitemap to Google: `https://comp-hemio.github.io/sitemap.xml`
2. Add Google Analytics (optional)
3. Submit to Spotify for Artists

## 📱 Social Media Integration

Add Open Graph images in `_config.yml` for better social sharing.

## ❓ Troubleshooting

**Site not showing?**
- Check repository name is exactly `comp-hemio.github.io`
- Wait 2-3 minutes
- Check Settings → Pages is enabled

**Images not showing?**
- Check file paths in markdown
- Make sure files are in `assets/images/`
- Image names are case-sensitive

**Changes not appearing?**
- GitHub Pages takes 30-60 seconds to rebuild
- Hard refresh browser (Ctrl+Shift+R / Cmd+Shift+R)

## 📚 Resources

- Jekyll Docs: https://jekyllrb.com/docs/
- Minimal Mistakes: https://mmistakes.github.io/minimal-mistakes/
- GitHub Pages: https://pages.github.com/
- Markdown Guide: https://www.markdownguide.org/

## 🆘 Need Help?

If you get stuck, you can:
1. Check the README.md in the zip file
2. Read GitHub Pages documentation
3. Ask me for help with specific issues

---

**Good luck with your website! 🎹**

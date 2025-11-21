# Hemio Multilingual Website

## Language Structure

The site supports 4 languages:
- **English (en)** - Default language
- **Korean (ko)** - 한국어
- **Spanish (es)** - Español
- **Japanese (ja)** - 日本語

## How It Works

### Automatic Language Detection
- When visiting the root `/`, the site detects browser language
- Automatically redirects to appropriate language (e.g., Korean speakers → `/ko/`)
- Language preference is saved in localStorage

### File Naming Convention

All content files follow this pattern:
```
filename.LANG.md
```

Examples:
- `music.en.md` - English music page
- `music.ko.md` - Korean music page
- `music.es.md` - Spanish music page
- `music.ja.md` - Japanese music page

For blog posts:
```
YYYY-MM-DD-slug.LANG.md
```

Examples:
- `2025-12-01-water-memories-essay.en.md`
- `2025-12-01-water-memories-essay.ko.md`

### Required Front Matter

Each content file must include:
```yaml
---
ref: unique-identifier  # Same across all language versions
lang: en               # Language code
permalink: /about/     # URL (language-specific for non-English)
---
```

### Language Switcher

The language switcher appears automatically on pages with multiple language versions. It uses the `ref` field to find corresponding pages in other languages.

If a translation doesn't exist, the switcher will show English as fallback.

## Adding New Content

### Creating a New Page in Multiple Languages

1. **English version** (`_pages/pagename.en.md`):
```yaml
---
layout: single
title: "Page Title"
permalink: /pagename/
ref: pagename
lang: en
---

{% include language-switcher.html %}

Your content here...
```

2. **Korean version** (`_pages/pagename.ko.md`):
```yaml
---
layout: single
title: "페이지 제목"
permalink: /ko/pagename/
ref: pagename
lang: ko
---

{% include language-switcher.html %}

한국어 콘텐츠...
```

3. **Spanish version** (`_pages/pagename.es.md`):
```yaml
---
layout: single
title: "Título de página"
permalink: /es/pagename/
ref: pagename
lang: es
---

{% include language-switcher.html %}

Contenido en español...
```

4. **Japanese version** (`_pages/pagename.ja.md`):
```yaml
---
layout: single
title: "ページタイトル"
permalink: /ja/pagename/
ref: pagename
lang: ja
---

{% include language-switcher.html %}

日本語のコンテンツ...
```

### Creating a New Blog Post in Multiple Languages

1. Create files: `_posts/YYYY-MM-DD-slug.LANG.md`
2. Use same `ref` value across all versions
3. Use `lang` code for each language

### Fallback Behavior

If a translation is missing:
- The language switcher will only show available languages
- Users clicking a missing language will see English (default)

## URL Structure

- English: `/pagename/`
- Korean: `/ko/pagename/`
- Spanish: `/es/pagename/`
- Japanese: `/ja/pagename/`

## Navigation Updates

To add language-specific navigation, edit `_data/navigation.yml` or create language-specific navigation files.

## SEO Considerations

Each language version has its own:
- Title and meta description
- URL structure
- hreflang tags (automatic via Jekyll)

## Testing Locally

```bash
bundle exec jekyll serve
```

Visit:
- http://localhost:4000/ (auto-detects language)
- http://localhost:4000/ko/ (Korean)
- http://localhost:4000/es/ (Spanish)
- http://localhost:4000/ja/ (Japanese)

## Tips

1. **Keep `ref` consistent** - This is how language versions are linked
2. **Translate everything** - Title, content, excerpts
3. **Update all versions** - When updating content, update all language versions
4. **Test language switcher** - Make sure all versions are linked correctly

## Example Workflow

When releasing a new song with blog post:

1. Update music pages:
   - `_pages/music.en.md`
   - `_pages/music.ko.md`
   - `_pages/music.es.md`
   - `_pages/music.ja.md`

2. Create blog posts:
   - `_posts/2025-12-15-new-song.en.md`
   - `_posts/2025-12-15-new-song.ko.md`
   - `_posts/2025-12-15-new-song.es.md`
   - `_posts/2025-12-15-new-song.ja.md`

3. All use same `ref: new-song`

4. Language switcher automatically appears and connects all versions

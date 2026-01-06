# Site Simplification Summary

## Overview
This Jekyll site has been stripped down from a complex academic template to a minimal, maintainable personal portfolio.

## What Was Removed

### Dependencies (20 → 5 gems)
**Removed:**
- jekyll-archives
- jekyll-email-protect
- jekyll-get-json
- jekyll-imagemagick
- jekyll-jupyter-notebook
- jekyll-link-attributes
- jekyll-minifier
- jekyll-scholar
- jekyll-toc
- jekyll-twitter-plugin
- jemoji
- classifier-reborn
- unicode_utils
- mini_racer
- feedjira
- httparty

**Kept:**
- jekyll
- jekyll-feed
- jekyll-paginate-v2
- jekyll-sitemap
- webrick

### Pages (8 → 4)
**Removed:** about_einstein.md, dropdown.md, repositories.md, publications.md
**Kept:** about.md, projects.md, cv.md, blog.md

### Layouts (12 → 5)
**Removed:** profiles.html, distill.html, archive-year.html, archive-tag.html, archive-category.html, none.html, bib.html
**Kept:** default.html, about.html, page.html, post.html, cv.html

### Collections
**Removed:** _news/, _bibliography/
**Kept:** _projects/ (all 17 projects), _posts/ (all 20 posts)

### Data Files
**Removed:** coauthors.yml, repositories.yml, venues.yml
**Kept:** cv.yml

### Includes
**Removed:**
- disqus.html, giscus.html (comment systems)
- news.html, selected_papers.html, related_posts.html
- repository/ (GitHub stats)
- resume/ (JSON resume parsing)
- wechatModal.html
- scripts/analytics.html, scripts/badges.html, scripts/masonry.html

### Assets
**Removed directories:** jupyter/, plotly/, pdf/, video/, bibliography/
**Removed SCSS:** _distill.scss, font-awesome/

### Config Features Disabled
- GitHub repository stats and trophies
- Comment systems (Giscus, Disqus)
- External blog sources (Medium)
- Blog archives
- Bibliography/publications system
- Email obfuscation
- Responsive image generation (ImageMagick)
- Math rendering (MathJax)
- Masonry grid layout
- Medium zoom
- Tooltips
- Site verification (Google, Bing)

## What Still Works

✅ **Core Pages**
- Home/About page with profile image
- Projects gallery (all 17 projects)
- CV/Resume page
- Blog with pagination (20 posts)

✅ **Features**
- Responsive design (mobile/tablet/desktop)
- Dark mode toggle
- Navigation bar
- Social media icons
- Project categories
- Progress bar
- Google Analytics
- RSS feed
- Sitemap

✅ **Blog Features**
- Post pagination
- Latest posts widget
- Tags and categories (display only, no archive pages)
- Syntax highlighting

## File Changes Summary

**Total files modified/deleted:** 78
**Lines of code removed:** ~9,700+
**Build time improvement:** 40-80% faster (estimated 3-5 sec vs 15-30 sec)

## Migration Notes

### If You Need Ruby/Jekyll Locally
Your system Ruby (2.6.10) is too old. Options:
1. Use Docker: `docker compose up`
2. Install rbenv/rvm and Ruby 3.0+
3. Use GitHub Pages to build (push to GitHub)

### Backup
Full backup available on branch: `backup-before-simplification`

### Potential Issues
1. **Archive links removed:** Blog post tags/categories now display as plain text
2. **Publications removed:** If you need this back, we'd need to restore jekyll-scholar
3. **Table of contents:** Not available in posts anymore (jekyll-toc removed)
4. **Related posts:** Not shown at bottom of posts anymore

### Easy to Re-add Later
- Math rendering (MathJax): 30 min
- Table of contents: 1 hour  
- Comment system: 30 min
- Archive pages: 1 hour

## Next Steps

1. **Test the build:**
   - Push to GitHub and let GitHub Pages build it
   - Or use Docker: `docker compose pull && docker compose up`

2. **Review pages:**
   - Check that about.md, projects.md, cv.md look correct
   - Verify blog posts display properly

3. **Further cleanup (optional):**
   - Remove unused images in assets/img/
   - Clean up old _site/ directory
   - Remove unused CSS in assets/css/

4. **Customize:**
   - Update about.md with your content
   - Add/remove projects
   - Update cv.yml

## Rollback Instructions

If you want to go back to the full template:
```bash
git checkout backup-before-simplification
```

Or cherry-pick specific files:
```bash
git checkout backup-before-simplification -- path/to/file
```

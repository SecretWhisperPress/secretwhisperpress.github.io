[README.md](https://github.com/user-attachments/files/25533481/README.md)
# Secret Whisper Press — Website

**secretwhisperpress.com** · Est. 2026

Books for the Quiet Architects.

---

## File Structure

```
secretwhisperpress/
├── index.html                          ← Main site (all HTML/CSS/JS)
├── feel-the-horizon-within-cover.jpg   ← Book cover image
├── the-quiet-architects-cover.jpg
├── before-needed-cover.jpg
├── invisible-atm-cover.jpg
└── README.md
```

---

## Setup & Deployment

### 1. Push to GitHub

```bash
# From inside the project folder
git init
git add .
git commit -m "Initial commit — Secret Whisper Press website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/secretwhisperpress.git
git push -u origin main
```

### 2. Add a New Book

In `index.html`, find the `books-grid` div and copy this block:

```html
<div class="fade-up" style="transition-delay: 0.Xs;">
  <a href="https://secretwhisperpress.gumroad.com/l/YOUR-SLUG" class="book-card" target="_blank" rel="noopener">
    <div class="book-cover-wrap">
      <img src="your-cover.jpg" alt="Book Title cover" loading="lazy"
           onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';" />
      <div class="book-cover-placeholder" style="display:none;">
        <div class="ph-rule"></div>
        <div class="ph-title">Your Book Title</div>
        <div class="ph-rule"></div>
        <div class="ph-author">Mehdi Zaki</div>
      </div>
    </div>
    <div class="book-meta">
      <p class="book-format">eBook · PDF</p>
      <h3 class="book-title">Your Book Title</h3>
      <p class="book-author">by Mehdi Zaki</p>
      <p class="book-desc">Your description here.</p>
      <span class="book-buy">$XX.XX — Buy Now →</span>
    </div>
  </a>
</div>
```

Replace the `transition-delay` value: 0s, 0.1s, 0.2s, 0.3s... (stagger by 0.1s per card).

### 3. Update Gumroad Links

All Gumroad links follow the pattern:
```
https://secretwhisperpress.gumroad.com/l/PRODUCT-SLUG
```

Update the slug in both the book card `href` and the footer links.

---

## Hosting

This is a **static HTML site** — one file, no dependencies, no build step.

**Recommended hosts (free tier available):**
- **Netlify** — drag and drop the folder, done
- **GitHub Pages** — enable in repo Settings → Pages → `main` branch
- **Vercel** — connect GitHub repo, auto-deploys on push

If your domain is already pointing to a host, just replace `index.html` and the cover images.

---

## Updating Cover Images

1. Export/save cover as JPG, width 600–900px
2. Name it to match exactly what's in the `<img src="...">` tag
3. Drop it in the root folder alongside `index.html`
4. Commit and push

---

## Current Books & Gumroad Slugs

| Title | Slug | Price |
|---|---|---|
| Feel the Horizon Within | `feel-the-horizon-within` | $17.99 |
| The Quiet Architects | `quiet-architects` | $19.99 |
| Before You Were Needed | `before-needed` | $17.99 |
| The Invisible ATM | `invisible-atm` | $21.99 |

---

*The soil is the self. Tend to that first.*

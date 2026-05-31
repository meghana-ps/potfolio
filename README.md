# Portfolio — Editing Guide (VS Code)

A quick reference so you can confidently update any part of your portfolio without breaking anything.

---

## File Structure

```
portfolio/
├── index.html         ← All content lives here
├── style.css          ← All styling lives here
├── README.md          ← This file
└── assets/
    ├── profile.jpg            ← Your profile photo
    ├── Meghana_Paladi_Shekar_CV.pdf  ← Your CV
    ├── project_greenhouse.png
    ├── project_obesity.png
    └── project_global.png
```

---

## How to Edit Content (index.html)

Every section in `index.html` starts with a block comment like this:

```html
<!-- ============================================================
     HERO SECTION
     Edit: ...
============================================================ -->
```

Follow those inline `<!-- EDIT: ... -->` hints. You only need to change text **between** `>` and `<` tags.

### Change your name or title
Search for `hero-name` in index.html. Edit the two lines inside:
```html
<h1 class="hero-name">Meghana<br><em>Paladi Shekar</em></h1>
```

### Update the hero description
Search for `hero-desc` and edit the paragraph text.

### Update your stats (numbers)
Search for `hero-stats` and edit the three `stat-num` values.

### Add a new Experience entry
Find the `<!-- JOB 3 -->` comment. Copy the entire `<div class="exp-item">` block below it and fill in your details.

### Add a new Project card
Find `<!-- PROJECT 4 -->`. Copy the `<div class="proj-card">` block and edit:
- `proj-tag` → category label
- `h3` → project title
- `p` → description
- `proj-tech-row span` → tech tags
- `a href` → live URL and GitHub URL
- `img src` → put your image in `assets/` and update the path

### Update Contact links
Search for `contact-links` — update the `href=""` values for email, LinkedIn, phone, and GitHub.

---

## How to Edit Colours (style.css)

Open `style.css` and find the `:root { }` block at the very top. Change any variable:

```css
:root {
    --accent: #4fd1b5;   /* ← change this to any colour */
    --bg:     #0d1117;   /* ← page background */
    ...
}
```

---

## How to Add Your Profile Photo

1. Name your photo `profile.jpg` (or `.png`)
2. Drop it into the `assets/` folder
3. The `<img src="./assets/profile.jpg">` in the Hero section will pick it up automatically

For best results: square or slightly portrait crop, minimum 600×700px.

---

## How to Add Project Images

1. Drop images into `assets/` (PNG or JPG, ~800px wide is fine)
2. In `index.html`, find the project card and update the `img src`:
```html
<img src="./assets/your-image-name.png" alt="Project Name">
```

---

## Deploying (free options)

| Service | How |
|---------|-----|
| **GitHub Pages** | Push to a repo, enable Pages in Settings → Pages |
| **Netlify** | Drag-and-drop the `portfolio/` folder at netlify.com |
| **Vercel** | Import the repo, zero config needed |

---

## Quick checklist before publishing

- [ ] Add your profile photo to `assets/profile.jpg`
- [ ] Add your CV PDF to `assets/`
- [ ] Replace placeholder GitHub links (`href="#"`) with real URLs
- [ ] Replace project image placeholders with real screenshots
- [ ] Update the ChemALLM project links when ready
- [ ] Check the CV download button points to the right PDF filename

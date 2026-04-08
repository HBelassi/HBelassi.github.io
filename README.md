# Hana Belassi — Portfolio Website

A static HTML/CSS portfolio site that's completely free to host.
No platform subscriptions needed — just pay for your domain (~€12/year).

---

## File Structure

```
/
├── index.html              ← Homepage (project grid + filter)
├── about.html              ← About Me page
├── stayfit.html            ← StayFit project page
├── text-enlargement.html   ← Text Enlargement project page
├── consumer-app-vi.html    ← Password-protected project
├── consumer-app-vii.html   ← Password-protected project
├── consumer-app-viii.html  ← Password-protected project
├── style.css               ← All styles (edit this for design changes)
└── images/                 ← Create this folder and add your images here
```

---

## How to Add a New Project

### Step 1 — Add a card to the homepage (index.html)

Find the `<!-- PROJECT GRID -->` section and copy this block:

```html
<a class="project-card" href="your-project.html" data-category="ux">
  <img src="images/your-thumbnail.jpg" alt="Project name">
  <div class="overlay">
    <span class="project-tag">UXR / UX</span>
    <span class="project-name">Your Project Name</span>
    <span class="project-arrow">→</span>
  </div>
</a>
```

- Change `href` to your new project filename
- Change `data-category` to `"ux"` or `"industrial"`
- Replace the `img src` with your thumbnail image path
- Update the project name and tag

### Step 2 — Create the project page

Copy `stayfit.html`, rename it to `your-project.html`, and edit:
- The `<title>` in `<head>`
- The year in `.year`
- The `<h1>` title
- The `.hero-subtitle` text
- The meta row (role, year, type)
- The project body content

### Step 3 — Add your images

Put your thumbnail image in the `images/` folder, then reference it:
```html
<img src="images/your-thumbnail.jpg" alt="Your project">
```

---

## How to Change a Password (for protected projects)

Open the relevant HTML file (e.g., `consumer-app-vi.html`) and find:

```javascript
const PROJECT_PASSWORD = 'yourpassword'; // ← CHANGE THIS
```

Replace `yourpassword` with whatever you want.

---

## How to Update Your About Page

Open `about.html` and edit the text directly in the HTML.
Look for comments like `<!-- Add your content here -->` as guides.

To add your photo:
```html
<!-- Find this line: -->
<div class="photo-placeholder">Your photo here</div>

<!-- Replace it with: -->
<img src="images/hana-photo.jpg" alt="Hana Belassi">
```

---

## Hosting on GitHub Pages (Free)

1. Go to https://github.com and create a free account
2. Click "New repository" → name it `hana-portfolio` → set to Public
3. Upload all these files to the repository
4. Go to Settings → Pages → Source: Deploy from branch → main → Save
5. Your site will be live at: `https://yourusername.github.io/hana-portfolio`

### Connecting your domain (hanabelassi.com)

1. In the GitHub Pages settings, enter `www.hanabelassi.com` in "Custom domain"
2. Go to your domain registrar (wherever you bought hanabelassi.com)
3. Add these DNS records:
   - Type: `A`, Name: `@`, Value: `185.199.108.153`
   - Type: `A`, Name: `@`, Value: `185.199.109.153`
   - Type: `A`, Name: `@`, Value: `185.199.110.153`
   - Type: `A`, Name: `@`, Value: `185.199.111.153`
   - Type: `CNAME`, Name: `www`, Value: `yourusername.github.io`
4. Wait 24-48 hours for DNS to propagate
5. Enable "Enforce HTTPS" in GitHub Pages settings

---

## Alternative: Netlify Drop (Even Easier)

1. Go to https://app.netlify.com/drop
2. Drag your entire project folder onto the page
3. It's instantly live with a random URL
4. Go to Site Settings → Domain Management → Add custom domain
5. Follow their DNS instructions (same concept as above)
6. Free tier is more than sufficient for a portfolio

---

## Cost Summary

| What              | Cost         |
|-------------------|--------------|
| GitHub Pages      | **Free**     |
| Netlify (free)    | **Free**     |
| Your domain       | ~€12/year    |
| **TOTAL**         | **~€12/year**|

vs. Squarespace: ~€115/year (hosting + domain)

**Saving: ~€100/year**

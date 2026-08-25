# Heaveans Creative Labs — Portfolio Website

A multipage portfolio site built with vanilla HTML, CSS, and JavaScript — no build step, no dependencies. Deep navy + orange palette, smooth animations, custom cursor, project filtering, and a contact form.

## File Structure

```
heaveans-creative-labs/
├── index.html              (Redirect to pages/index.html)
├── pages/
│   ├── index.html          (Home page - hero section)
│   ├── about.html          (Creative services/capabilities)
│   │                         (Creative landing page)
│   ├── creative-work.html  (Creative Work practice page)
│   ├── graphics-portfolio.html (Graphics Portfolio page)
│   ├── web-design.html     (Web Design portfolio page)
│   ├── creative-detail.html (Creative portfolio case-study view)
│   ├── engineering.html    (Engineering capabilities and approach)
│   ├── labs.html            (Lab research and experimentation)
│   ├── about-us.html       (Studio overview and values)
│   ├── projects.html       (Featured projects with filtering)
│   ├── project-detail.html  (Dynamic detail view for each project)
│   └── start-project.html  (Contact/Lab form)
├── css/
│   └── shared.css          (Global styles - navbar, footer, animations, colors, fonts)
├── js/
│   └── shared.js           (Shared JS - cursor, navbar scroll, mobile menu, page detection)
├── admin/
│   ├── index.html          (Decap CMS interface)
│   └── config.yml          (CMS configuration)
└── README.md
```

## Design System

### Font Stack
- **Headings** (`<h1>`–`<h6>`): **Geist** (modern, geometric, clean)
- **Body Text**: **Inter** (highly readable, balanced proportions)

### Color Palette
- **Navy**: `#0a1628` (primary background)
- **Orange**: `#ff6b35` (accent, CTAs)
- **White/Gray**: Various opacities for contrast

### Responsive Breakpoints
- **768px**: Mobile menu activates, grid layouts stack to single column
- **1024px**: Lab form sections change to single column
- Custom cursor hides on mobile automatically

## Navigation & Footer

All pages share a fixed navbar with links to:
- **Home** → `pages/index.html`
- **Creative** → `pages/about.html` (services)
- **Creative Work** → `pages/creative-work.html` (creative practice)
- **Graphics Portfolio** → `pages/graphics-portfolio.html` (graphic and editorial work)
- **Web Design** → `pages/web-design.html` (website portfolio)
- **Engineering** → `pages/engineering.html` (engineering capabilities)
- **Labs** → `pages/labs.html` (research and experimentation)
- **About Us** → `pages/about-us.html` (studio overview)
- **Projects** → `pages/projects.html` (image-led portfolio with filtering)
- **Project details** → `pages/project-detail.html?project=gridsense` (deep project view)
- **Contact Us** → `pages/start-project.html` (project inquiry form)
- **Lab** → `pages/start-project.html` (contact form)

Footer includes social links to:
- X/Twitter
- Facebook
- YouTube
- TikTok

## Deploy on GitHub Pages

1. Create a **public** GitHub repository:
   ```bash
   git init
   git add .
   git commit -m "Multipage portfolio launch"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/heaveans-creative-labs.git
   git push -u origin main
   ```

2. Go to **Settings → Pages** in your repository.

3. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)`

4. Save. Your site will be live at:
   ```
   https://YOUR_USERNAME.github.io/heaveans-creative-labs/
   ```

## Customizing

### Colors
Edit CSS variables in `css/shared.css` under `:root`:
```css
--navy-900: #0a1628;        /* Main background */
--orange-500: #ff6b35;      /* Primary accent */
--white: #ffffff;           /* Primary text */
```

### Content
- **Home Hero**: Edit `pages/index.html` — title, subtitle, CTA buttons
- **Services**: Edit `pages/about.html` — service cards, descriptions, tags
- **Projects**: Edit `pages/projects.html` — replace gradients with real `<img>` tags, update titles/categories/descriptions
- **Contact Info**: Edit `pages/start-project.html` — email, phone, location
- **Social Links**: Update all footer `<a>` hrefs in each page

### Fonts
To change fonts globally:
1. Edit the Google Fonts import link in each page's `<head>` (currently `Geist + Inter`)
2. Update font-family references in `css/shared.css`

## Features

✓ **Multipage Architecture** — Clean page separation with shared navbar/footer  
✓ **Fully Responsive** — Desktop, tablet, mobile (768px breakpoint)  
✓ **Mobile Menu** — Slide-in navigation for screens < 768px  
✓ **Custom Cursor** — Animated dual-circle cursor (auto-disables on mobile)  
✓ **Project Filtering** — Filter by category (Branding, Web, App)  
✓ **Smooth Animations** — CSS keyframes + scroll triggers  
✓ **Contact Form** — Client-side simulation (ready to wire to Formspree/Getform)  
✓ **Git-Based CMS** — Decap CMS ready (see below)  
✓ **No Build Step** — Pure HTML, CSS, JS

## CMS Setup (Optional)

### Decap CMS (Git-Based, Recommended)

**Simple Setup (Local Only):**
- Edit `admin/config.yml` to point to your content files
- Access locally at `/admin/` for editing

**Production Setup (Remote Editing):**
1. Create free [Netlify](https://www.netlify.com/) account
2. Connect GitHub repo to Netlify (Netlify provides auth)
3. Enable **Identity** and **Git Gateway** in Netlify dashboard
4. Invite yourself as a user
5. Visit `https://YOUR_USERNAME.github.io/heaveans-creative-labs/admin/` to edit
6. Site stays on GitHub Pages; Netlify handles auth only

**Alternative:** [Tina CMS](https://tina.io/) (GitHub-native auth, no Netlify)

## Advanced Customization

### Project Filtering
In `pages/projects.html`, filter cards by `data-category` attribute — add/remove categories as needed.

### Form Submission
Contact form currently simulates submission. To receive real emails:
1. **Formspree** or **Getform**: Update form `action` attribute to their endpoint
2. **Custom Backend**: Post to your own API

### Animations
CSS keyframes in `css/shared.css`: `fadeInUp`, `bounce`, `spin`. Adjust timing as needed.

## Notes

- **No Dependencies** — Runs natively in browser
- **Mobile Cursor** — Automatically hidden on touch devices
- **Page Navigation** — Traditional `.html` file links (not hash-based)
- **GitHub Pages Compatible** — Fully static hosting ready

---

Built with ❤️ by Heaveans Creative Labs

# CHRONOS | Perpetual 41 — Horological Scroll Experience

An Apple-style, 60 FPS scroll-driven interactive watch advertisement website. As the user scrolls, the watch seamlessly rotates and mechanically explodes into its internal movement, gears, escapement, and Oyster casing.

Designed with a Rolex-inspired luxury aesthetic, Swiss typography, circular SVG frame preloader, glassmorphic navigation, and responsive editorial storytelling sections.

---

## ✨ Features

- **🎞️ 240-Frame Canvas Sequence:** Smooth scroll-linked frame progression rendered onto an HTML5 canvas with zero jank.
- **⚡ 60 FPS `requestAnimationFrame` Pipeline:** Decoupled scroll listener and draw loop that skips redundant repaints.
- **📱 Fully Mobile-Optimized:**
  - Dynamic viewport units (`100dvh` / `100vh`) to eliminate mobile browser address bar jump on iOS Safari & Chrome Android.
  - Adaptive frame stepping: loads every 2nd frame on mobile devices (<768px) to reduce bandwidth and memory by 50%.
  - Native touch physics with `touch-action: pan-y` and `-webkit-overflow-scrolling: touch`.
  - Apple Web App & Notch support with `viewport-fit=cover` and safe-area insets.
- **💎 Luxury Design System:**
  - Gold SVG circular frame preloader with real-time percentage counter.
  - Glassmorphic sticky navigation bar (`backdrop-filter: blur(20px)`).
  - Editorial Craftsmanship, Technical Specifications (3×2 grid), Heritage story, and interactive CTA.
  - IntersectionObserver scroll reveals.
- **🚀 Zero External Runtime Dependencies:** Pure HTML5, CSS3 Custom Properties, and Vanilla JavaScript.

---

## 🚀 Deploying to Vercel via GitHub

### Step 1: Create a GitHub Repository
1. Go to [github.com/new](https://github.com/new).
2. Name your repository (e.g. `chronos-watch-experience`).
3. Leave it public or private, and **do not** initialize with a README (one is already prepared).

### Step 2: Push Your Code to GitHub
In your project folder, run the following commands:

```bash
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git branch -M main
git push -u origin main
```

### Step 3: Deploy with Vercel (1-Click)
1. Go to [vercel.com](https://vercel.com) and log in with your GitHub account.
2. Click **"Add New..."** → **"Project"**.
3. Select your `chronos-watch-experience` repository from the list.
4. Click **"Deploy"** (Vercel will automatically detect the static project and apply `vercel.json` edge-caching headers).

Your website is now live worldwide with instant edge caching! 🎉

---

## 💻 Local Development

To run the site locally:

```bash
# Using npx serve
npx serve -l 3456
```

Then open `http://localhost:3456` in your browser.

---

## ⚙️ Customization

### Adjusting Animation Speed
The scroll speed is controlled by the height of `.scroll-container` in `index.html`:

```css
/* Increase height for slower, more granular scrolling (e.g. 500vh - 600vh) */
/* Decrease height for faster scrolling (e.g. 250vh - 300vh) */
.scroll-container { 
  height: 400vh; 
  position: relative; 
}
```

### Customizing Colors & Brand
Edit the CSS custom properties in the `:root` block of `index.html`:

```css
:root {
  --color-gold: #c5a44e;       /* Luxury gold accent */
  --color-gold-light: #d4b96a; /* Highlight gold */
  --color-green: #006039;      /* Rolex emerald accent */
  --color-black: #000000;      /* Background */
  --color-cream: #f7f4ef;      /* Specs section background */
}
```

---

## 📄 License
MIT License. Free to use for personal and commercial projects.

# Birthday Wishes Website

A full-screen, scrollable birthday celebration website built with **pure HTML and CSS** (no JavaScript needed).

## Quick Start

1. Open `index.html` in your web browser
2. Scroll through all 5 sections
3. Click the navigation links at the top to jump to any section
4. Share with a friend to celebrate!

---

## 📁 File Structure

```
birthday/
├── index.html      ← Main HTML structure (5 sections)
├── style.css       ← All styling and animations (1500+ lines with comments)
├── CNAME          ← Domain configuration file
└── README.md      ← This file
```

---

## 🎨 The 5 Sections

### 1. **HERO** - Opening Scene
- Large "Happy Birthday" heading with glowing effect
- Welcome message explaining the site
- Two buttons: "Start the story" & "Jump to the finale"
- Decorative sparks and gift boxes
- Scroll indicator animation

### 2. **MEMORIES** - Story Cards
- Three glassmorphic cards with numbered badges
- Tilt effect for visual interest
- Text explaining memorable moments
- 2-column layout (stacks on mobile)

### 3. **BALLOONS** - Floating Decoration
- Four animated balloons floating up and down
- Each balloon has its own timing and color
- Strings attached to each balloon
- Glowing background container

### 4. **CAKE** - Birthday Centerpiece
- Three-layered chocolate cake (CSS-drawn, not an image)
- Three animated candle flames with unique timing
- Frosting drips for detail
- Glowing plate and halo effects

### 5. **FINAL MESSAGE** - Celebration Finale
- Confetti particles falling with rotation
- Glowing goodbye message
- "Back to top" button

---

## 🎯 How to Customize

### Change Colors
Edit the `:root` variables in [style.css](style.css) (around line 30):

```css
:root {
  --gold: #ffd584;      /* Primary accent color */
  --rose: #ff8fa3;      /* Pink accent */
  --sky: #a8d5ff;       /* Blue accent */
  --mint: #8ceccb;      /* Green accent */
}
```

### Change Text
All text is in [index.html](index.html):
- Hero title: Line 26
- Section headings: Lines 36, 56, 72, 89
- Memory card text: Lines 48-54
- Final message: Line 100

### Adjust Animations
In [style.css](style.css), find the `@keyframes` section (around line 1000):

- **Balloons**: Change `animation: balloonFloat` duration and `translateY` amount
- **Flames**: Adjust `@keyframes flame` scale values
- **Confetti**: Modify `@keyframes confettiFall` distance and speed
- **General**: Look for `animation-duration` values (measured in seconds, like `7.5s`)

### Change Layout Spacing
Look for these CSS properties:
- `gap:` - Distance between elements
- `padding:` - Inner space
- `width:` / `height:` - Sizing
- `margin:` - Outer space

### Mobile Responsive Breakpoints
Adjustments happen automatically at:
- **980px** - Tablet: Single column, smaller sizes
- **640px** - Mobile: Vertical nav, adjusted padding
- **420px** - Small phone: Minimal spacing, compact layout

---

## 🎬 CSS Organization

The `style.css` file is organized into clear sections (look for comments with `=====`):

1. **Global Settings & Color Variables** - Reusable colors and values
2. **Body & Background** - Page background and atmosphere
3. **Typography** - All text styling (headings, paragraphs)
4. **Navigation Bar** - Fixed header with links
5. **Page & Section Layout** - Container structure
6. **Button Styles** - Primary and secondary buttons
7. **Hero Section** - Opening area with text and art
8. **Memories Section** - Card grid layout
9. **Balloons Section** - Floating animation container
10. **Cake Section** - CSS-drawn cake and candles
11. **Final Message** - Closing section
12. **Confetti Animation** - Falling particles
13. **Animations & Keyframes** - All animation definitions
14. **Responsive Design** - Mobile/tablet adjustments
15. **Accessibility** - Reduced motion preferences

---

## 🧩 HTML Structure

The HTML is simple and semantic:

```html
<header class="topbar">
  <!-- Navigation bar (fixed at top) -->
</header>

<main class="page">
  <section id="hero" class="panel hero">
    <!-- Hero section -->
  </section>
  
  <section id="memories" class="panel memories">
    <!-- Memories section -->
  </section>
  
  <!-- ...more sections... -->
</main>
```

Each section:
- Uses `id=""` for anchor links (e.g., `href="#cake"`)
- Has `class="panel"` for shared styling
- Uses semantic HTML (`<section>`, `<article>`, `<nav>`)
- Includes `aria-hidden="true"` on decorative elements for accessibility

---

## ✨ CSS Features Used

- **CSS Grid** - Layout and alignment
- **Flexbox** - Flexible spacing and direction
- **CSS Variables** - Reusable color tokens (`--gold`, `--text`, etc.)
- **Gradients** - Layered radial and linear gradients for atmosphere
- **backdrop-filter** - Glassmorphism effect on cards (22-24px blur)
- **CSS Animations** - Smooth floating, twinkling, and falling effects
- **Media Queries** - Responsive design at 3 breakpoints
- **Pseudo-elements** (::before, ::after) - Decorative elements without extra HTML
- **Box-shadow** - Depth, glow, and layered shadow effects
- **clip-path** - (Could be used for decorative shapes)

---

## 🎭 Animation Timing

All animations use `cubic-bezier(0.25, 0.46, 0.45, 0.94)` easing for smooth, natural motion:

- **Balloons**: 7.5-8.6 seconds (staggered)
- **Flames**: 2.2 seconds (staggered)
- **Confetti**: 7.5 seconds (staggered)
- **Scroll indicator**: 2 seconds (infinite)
- **Memory cards hover**: 260ms (instant feedback)

---

## 📱 Browser Support

Works in all modern browsers:
- Chrome/Edge (90+)
- Firefox (88+)
- Safari (14+)
- Mobile browsers (iOS Safari, Chrome Mobile)

---

## ♿ Accessibility

- Semantic HTML structure
- Alt text on decorative elements (`aria-hidden="true"`)
- `prefers-reduced-motion` media query (disables animations for users who request it)
- Proper heading hierarchy (h1 → h2 → h3)
- Navigation links with `aria-label`

---

## 🚀 Deployment

1. Upload all three files to a web server
2. Or use GitHub Pages:
   - Push files to a GitHub repository
   - Enable GitHub Pages in repository settings
   - Use `CNAME` file if you have a custom domain

---

## 💡 Tips for Customization

### Make it Personal
- Replace section headings with custom text
- Change balloon colors to recipient's favorites
- Update memory card descriptions

### Adjust the Mood
- Change `--bg` to a lighter color for daytime feel
- Reduce blur values for sharper glass effect
- Speed up animations by reducing duration values

### Add Your Own Sections
- Copy a `<section>` block
- Give it a unique `id=""` and `class="panel"`
- Add a navigation link to the header
- Adjust responsive sizes in the media queries

---

## 📝 Notes

- All animations are pure CSS (no JavaScript)
- Smooth scrolling works automatically with `scroll-behavior: smooth`
- Navigation links use hash anchors (`#hero`, `#memories`, etc.)
- Decorative elements don't interfere with text selection or interaction
- Works offline - just open `index.html` in a browser

---

## 🎉 Have Fun!

This is your template. Customize it, make it special, and enjoy sharing it with someone you care about!

For questions about specific CSS properties or animations, check the detailed comments in [style.css](style.css).

---
name: Pretzel Pizza Design System
colors:
  surface: '#fff8f6'
  surface-dim: '#edd5ca'
  surface-bright: '#fff8f6'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#fff1eb'
  surface-container: '#ffeae0'
  surface-container-high: '#fce3d8'
  surface-container-highest: '#f6ded2'
  on-surface: '#251912'
  on-surface-variant: '#584236'
  inverse-surface: '#3c2d26'
  inverse-on-surface: '#ffede5'
  outline: '#8c7164'
  outline-variant: '#e0c0b0'
  surface-tint: '#9c4500'
  primary: '#9c4500'
  on-primary: '#ffffff'
  primary-container: '#f97306'
  on-primary-container: '#562300'
  inverse-primary: '#ffb68e'
  secondary: '#7e5700'
  on-secondary: '#ffffff'
  secondary-container: '#fdbb3f'
  on-secondary-container: '#6f4c00'
  tertiary: '#00629d'
  on-tertiary: '#ffffff'
  tertiary-container: '#00a1fd'
  on-tertiary-container: '#003558'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#ffdbca'
  primary-fixed-dim: '#ffb68e'
  on-primary-fixed: '#331200'
  on-primary-fixed-variant: '#773300'
  secondary-fixed: '#ffdeac'
  secondary-fixed-dim: '#fdbb3f'
  on-secondary-fixed: '#281900'
  on-secondary-fixed-variant: '#604100'
  tertiary-fixed: '#cfe5ff'
  tertiary-fixed-dim: '#99cbff'
  on-tertiary-fixed: '#001d34'
  on-tertiary-fixed-variant: '#004a78'
  background: '#FAF7F1'
  on-background: '#251912'
  surface-variant: '#f6ded2'
  foreground: '#26201A'
  card: '#FDFBF7'
  muted: '#EDE6DC'
  muted-foreground: '#7A7068'
  accent-red: '#DF2020'
  border: '#E3DBD0'
  warm-tint: '#FBF1E6'
  golden: '#F8C123'
  destructive: '#EF4444'
  dark-background: '#1F1812'
  dark-card: '#2A221C'
typography:
  h1-hero:
    fontFamily: Noto Serif
    fontSize: 60px
    fontWeight: '900'
    lineHeight: '1.1'
  h2-section:
    fontFamily: Noto Serif
    fontSize: 30px
    fontWeight: '700'
    lineHeight: '1.2'
  h3-card:
    fontFamily: Noto Serif
    fontSize: 24px
    fontWeight: '700'
    lineHeight: '1.3'
  body-lead:
    fontFamily: Plus Jakarta Sans
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-default:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.5'
  nav-link:
    fontFamily: Plus Jakarta Sans
    fontSize: 14px
    fontWeight: '500'
    lineHeight: '1'
  pill-badge:
    fontFamily: Plus Jakarta Sans
    fontSize: 14px
    fontWeight: '600'
    lineHeight: '1'
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  container-max: 1400px
  section-py-desktop: 6rem
  section-py-mobile: 4rem
  gutter-grid: 1.5rem
  hero-gap: 2.5rem
  nav-height: 4rem
---

# Pretzel Pizza — Complete Design & Content Specification

## 🎨 Color Palette (Exact Values)

### Light Mode
| Token | HSL | HEX | Usage |
|---|---|---|---|
| Background | `hsl(40, 33%, 97%)` | `#FAF7F1` | Main page background (warm off-white) |
| Foreground | `hsl(20, 25%, 12%)` | `#26201A` | Primary text (warm dark brown) |
| Card | `hsl(40, 30%, 99%)` | `#FDFBF7` | Card surfaces |
| **Primary (Orange)** | `hsl(25, 95%, 50%)` | `#F97306` | Buttons, links, brand logo, accents |
| Secondary (Amber) | `hsl(38, 80%, 55%)` | `#E8A82C` | Secondary actions |
| Muted | `hsl(35, 25%, 92%)` | `#EDE6DC` | Subtle background sections |
| Muted foreground | `hsl(20, 10%, 45%)` | `#7A7068` | Subtitles, descriptions |
| Accent (Red) | `hsl(0, 75%, 50%)` | `#DF2020` | Pizza-red accent |
| Border / Input | `hsl(35, 20%, 88%)` | `#E3DBD0` | Borders |
| Warm | `hsl(30, 60%, 96%)` | `#FBF1E6` | Hero background tint |
| Golden | `hsl(43, 96%, 56%)` | `#F8C123` | Highlight golden tone |
| Destructive | `hsl(0, 84%, 60%)` | `#EF4444` | Errors / remove |

### Dark Mode
| Token | HSL | HEX |
|---|---|---|
| Background | `hsl(20, 20%, 8%)` | `#1F1812` |
| Foreground | `hsl(40, 20%, 92%)` | `#EDE7DC` |
| Card | `hsl(20, 18%, 12%)` | `#2A221C` |
| Primary | `hsl(25, 95%, 55%)` | `#FA851A` |
| Secondary | `hsl(38, 70%, 40%)` | `#AE7B1F` |
| Muted | `hsl(20, 15%, 18%)` | `#352B25` |
| Accent | `hsl(0, 70%, 55%)` | `#DC3535` |
| Border | `hsl(20, 15%, 20%)` | `#3B3029` |

**Border radius:** `0.75rem` (12px) base — buttons `0.5rem`, cards `0.75rem`, hero image `1rem` (rounded-2xl).

---

## 🔤 Typography

- **Display font (H1–H4):** `Playfair Display`, serif — weights 700, 800, 900 (Google Fonts)
- **Body font:** `DM Sans`, sans-serif — weights 400, 500, 600, 700
- **Logo:** Playfair Display, bold, ~20px, primary orange, prefixed with 🥨

**Sizes (responsive):**
| Element | Mobile | Desktop |
|---|---|---|
| H1 hero | text-4xl (36px) | text-6xl (60px), font-black (900), leading-tight |
| H2 section | text-3xl (30px) | font-bold (700) |
| H3 card | text-lg–text-2xl | font-bold |
| Body lead | text-lg (18px) | muted-foreground |
| Body default | text-sm–text-base (14–16px) | |
| Nav links | text-sm (14px) | font-medium (500) |
| Pill badge | text-sm (14px) | font-semibold (600) |

---

## 📐 Layout & Spacing

- **Container:** centered, `padding: 2rem`, max-width `1400px` at 2xl
- **Section vertical padding:** `py-16` (64px), `py-24` (96px) for hero
- **Grid gaps:** `gap-6` (24px) cards, `gap-8`–`gap-10` hero
- **Featured grid:** `grid-cols-1 sm:grid-cols-2 lg:grid-cols-4`
- Generous, airy, editorial spacing rhythm

---

## 🧩 Page Sections (Home `/`)

### 1. Sticky Navbar (h-16)
- `bg-background/80` + `backdrop-blur-md`, bottom border
- Left: 🥨 + "Pretzel Pizza" (Playfair bold, primary orange)
- Center (desktop): Home, Menu, Build Your Own — muted, primary on hover/active
- Right: dark-mode toggle, user icon, cart icon with circular orange badge (20×20px, 10px bold white text)
- Mobile: hamburger drawer

### 2. Hero (`bg-warm`, py-16 md:py-24)
- 2-column grid (md:grid-cols-2)
- Left:
  - Pill: "🥨 New Concept" — `bg-primary/10`, rounded-full, px-4 py-1.5, primary text
  - H1: **"Pretzel Meets Pizza."** — "Pizza." in primary orange
  - Paragraph (muted, max-w-md): *"Handcrafted soft pretzel crust topped with gourmet pizza ingredients. A twist on two classics you never knew you needed."*
  - CTAs: "Order Now →" (solid orange) + "Build Your Own" (outline)
- Right: pretzel pizza photo, `rounded-2xl shadow-2xl`, with absolute glow `-inset-4 rounded-full bg-primary/10 blur-3xl` behind

### 3. How It Works (py-16)
- Centered H2: "How It Works"
- 3-column grid, each item:
  - Icon container `h-14 w-14 rounded-2xl bg-primary/10`, primary icon h-7 w-7
  - H3 (Playfair bold) + small muted description
- Items:
  1. **ChefHat** — "Choose Your Style" — *Pick from our menu or build your own creation*
  2. **Clock** — "Freshly Made" — *Each pretzel pizza is baked to golden perfection*
  3. **Truck** — "Fast Delivery" — *Hot and fresh, delivered right to your door*

### 4. Fan Favorites (`bg-muted/40`, py-16)
- Header row: H2 "Fan Favorites" + subtitle "Our most popular pretzel pizzas" (left); "View All →" link (right)
- 4-column responsive MenuCard grid

### 5. CTA (py-16, centered)
- H2: "Ready to Try Something New?"
- *Build your perfect pretzel pizza with our interactive customizer.*
- Primary button: "Start Building →"

### 6. Footer
- Multi-column footer with brand, links, copyright

---

## 🃏 UI Components

### Buttons (shadcn/ui + cva)
- Base: `inline-flex rounded-md text-sm font-medium transition-colors`, focus ring
- Variants:
  - default: `bg-primary text-primary-foreground hover:bg-primary/90`
  - outline: `border border-input bg-background hover:bg-accent`
  - ghost: transparent, hover muted
  - link: orange underline on hover
- Sizes: default (h-10 px-4), sm (h-9), lg (h-11 px-8), icon (10×10)
- Icon+label gap: gap-2

### Cards
- `rounded-lg border bg-card shadow-sm`
- Image top, p-6 padding, CardTitle (2xl semibold), muted description, price + "Add to Cart" footer
- Subtle hover lift/shadow

### Pill Badges
- `rounded-full bg-primary/10 px-4 py-1.5 text-sm font-semibold text-primary`

### Inputs
- `h-10 rounded-md border border-input bg-background px-3 py-2`, focus ring

---

## ✨ Effects & Motion
- `animate-fade-in`: opacity 0→1 + translateY 10px→0, 0.5s ease-out
- Smooth `transition-colors` everywhere
- Backdrop blur on sticky navbar
- Soft glow halo behind hero (blur-3xl + 10% primary)
- shadow-2xl on hero image, shadow-sm on cards

---

## 🎯 Overall Design Style

Warm, editorial, artisanal foodie — modern bakery brand vibe. Playfair Display (serif elegance) paired with DM Sans (clean geometric) for a "premium street food" feel. Orange + amber + red palette evokes baked pretzels and pizza ovens. Generous whitespace, rounded-2xl shapes, soft shadows, 10%-opacity color tints (`bg-primary/10`) for warmth without heaviness. Mobile-first, responsive, polished dark mode preserving warm hue. Brand mark: 🥨.

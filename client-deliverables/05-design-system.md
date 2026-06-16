# Design System & Brand Guidelines

**Project:** Coin Care Capital  
**Date:** [Insert Date]  
**Version:** 1.0

---

## 1. Brand Identity

### Logo

The Coin Care Capital logo should be used consistently across the website. The following versions exist:

| Version | Usage | File |
|---|---|---|
| Primary (full color) | Light backgrounds (navbar, cards) | `coincare-1.svg` |
| Original | Alternative usage | `coincare_logo.svg` |
| Compact | Small spaces | `coincare_logo_new.svg` |

**Logo Rules:**
- ✅ Always maintain the original aspect ratio
- ✅ Minimum clear space around the logo = height of the logo "coin" icon
- ❌ Do not stretch, rotate, or alter the colors
- ❌ Do not place the logo on a busy, low-contrast background without a container

---

## 2. Color Palette

### Primary Colors

| Name | Hex | Usage |
|---|---|---|
| **Brand Blue (Dark)** | `#1e3a8a` (blue-900) | Primary buttons, navbar accents, headings, hero background |
| **Brand Blue (Deep)** | `#172554` (blue-950) | Dark sections (Requirements, hero gradient) |
| **Brand Blue (Medium)** | `#3b82f6` (blue-500) | Interactive highlights, hover states |
| **Brand Blue (Light)** | `#dbeafe` (blue-100) | Text on dark backgrounds, subtle accents |

### Neutral Colors

| Name | Hex | Usage |
|---|---|---|
| **Slate 900** | `#0f172a` | Primary text |
| **Slate 500** | `#64748b` | Body text, descriptions |
| **Slate 400** | `#94a3b8` | Captions, labels |
| **Slate 100** | `#f1f5f9` | Card borders, dividers |
| **Slate 50** | `#f8fafc` | Page background |
| **White** | `#ffffff` | Card backgrounds, sections |

### Accent Colors

| Name | Hex | Usage |
|---|---|---|
| **Emerald 400** | `#34d399` | Success indicators, stat borders, trust badges |
| **WhatsApp Green** | `#25D366` | WhatsApp CTA buttons |
| **Green 400** | `#4ade80` | "Online" pulse dot, active indicators |

---

## 3. Typography

### Font Family

**Primary Font:** [Outfit](https://fonts.google.com/specimen/Outfit) (Google Fonts)

A modern geometric sans-serif that conveys professionalism and approachability. Loaded via `next/font/google` for optimal performance.

**Fallback Stack:** `ui-sans-serif, system-ui, sans-serif`

### Type Scale

| Element | Size (Desktop) | Size (Mobile) | Weight | Tracking |
|---|---|---|---|---|
| H1 (Hero) | 4.5rem (72px) | 3rem (48px) | 900 (Black) | Tight (-0.025em) |
| H2 (Section) | 3rem (48px) | 1.875rem (30px) | 900 (Black) | Tight |
| H3 (Card Title) | 1.25rem (20px) | 1.125rem (18px) | 900 (Black) | Normal |
| Body (Large) | 1.125rem (18px) | 1rem (16px) | 400 (Regular) | Normal |
| Body | 1rem (16px) | 0.875rem (14px) | 400 (Regular) | Normal |
| Caption / Label | 0.75rem (12px) | 0.75rem (12px) | 700 (Bold) | Wide (0.05em) |
| Nav Links | 0.875rem (14px) | 1.125rem (18px) | 700 (Bold) | Normal |

---

## 4. Spacing & Layout

### Container
- **Max width:** `max-w-7xl` (1280px)
- **Horizontal padding:** `px-4` (16px) on mobile, `px-6` on tablet, `px-8` on desktop

### Section Spacing
- **Vertical padding:** `py-24` (96px) per section
- **Between heading and content:** `mb-16` (64px)
- **Between cards in a grid:** `gap-6` (24px)

### Border Radius Scale
| Element | Radius |
|---|---|
| Small buttons, inputs | `rounded-lg` (8px) |
| Cards, modals | `rounded-2xl` (16px) |
| Large feature cards | `rounded-[2rem]` (32px) |
| Hero image, about image | `rounded-[3rem]` (48px) |
| Pill badges, tabs | `rounded-full` (9999px) |

---

## 5. Component Patterns

### Buttons

| Type | Style | Usage |
|---|---|---|
| **Primary** | `bg-blue-900 text-white rounded-xl font-bold` | Main CTAs ("Apply Now") |
| **Primary (Hero)** | `bg-white text-blue-900 rounded-2xl font-black` + glow shadow | Hero section only |
| **WhatsApp** | `bg-[#25D366] text-white rounded-2xl font-black` | WhatsApp CTAs |
| **Secondary** | `bg-slate-900 text-white rounded-xl font-black` | B2B section CTA |
| **Text Link** | `text-blue-900 font-bold` + arrow icon | "See Our Process →" style links |

**All buttons** use the `.btn-press` class for a physical press feedback effect:
```css
.btn-press:active {
  transform: scale(0.97);
}
```

### Cards

- White background with subtle border (`border-slate-100`)
- Generous padding (`p-8`)
- Hover state: elevated shadow + border color shift to blue
- Rounded corners: `rounded-[2rem]`

### Badges / Pills

- Semi-transparent background (`bg-white/10 backdrop-blur-md`)
- Rounded full (`rounded-full`)
- Small text, bold weight
- Often include a status dot or icon

---

## 6. Animation & Motion

We follow **Emil Kowalski's motion design principles** for a premium, polished feel.

### Easing Curves

| Name | Value | Usage |
|---|---|---|
| `easeOut` | `cubic-bezier(0.23, 1, 0.32, 1)` | Enter animations (elements appearing) |
| `easeInOut` | `cubic-bezier(0.77, 0, 0.175, 1)` | Expand/collapse (accordion, modals) |

### Animation Patterns

| Pattern | Duration | Description |
|---|---|---|
| **Fade up** | 400–600ms | Elements fade in and slide up 10–12px on scroll |
| **Stagger** | 80ms delay per item | Sequential reveal of grid items |
| **Scale in** | 500ms spring | Modals and success states |
| **Tab switch** | 300ms | Content swaps with fade + slide |
| **Accordion** | 300ms | Height animation for FAQ expand/collapse |
| **Hover scale** | 300ms | Cards scale to 1.02, images scale to 1.05 |

### Key Rules
1. **Asymmetric timing:** Enter animations are slower/springy, exits are snappy and fast
2. **Once-only viewport triggers:** Scroll animations fire once, never re-trigger
3. **Subtle over dramatic:** No spinning, bouncing, or attention-grabbing animations
4. **Physical feel:** Button presses shrink slightly, creating tactile feedback

---

## 7. Iconography

**Library:** [Lucide React](https://lucide.dev/)  
**Default size:** 18–24px for inline, 32px for feature cards  
**Stroke width:** Default (2) for body, 1.5 for large decorative icons, 3 for bold accordion icons

### Commonly Used Icons

| Icon | Usage |
|---|---|
| `Car` | Vehicle-related content |
| `ShieldCheck` | Security, trust, compliance |
| `Clock` | Speed, timing, tenure |
| `CheckCircle` | Requirements met, trust badges |
| `MessageCircle` | WhatsApp CTA |
| `ArrowRight` | CTAs, navigation links |
| `Phone`, `Mail`, `MapPin` | Contact information |
| `Calculator` | Loan calculator |
| `Plus`, `Minus` | FAQ accordion toggle |

---

## 8. Responsive Breakpoints

| Breakpoint | Width | Target |
|---|---|---|
| Default | < 640px | Mobile phones |
| `sm` | ≥ 640px | Large phones |
| `md` | ≥ 768px | Tablets |
| `lg` | ≥ 1024px | Laptops, small desktops |
| `xl` | ≥ 1280px | Desktops |

### Key Responsive Behaviors
- **Navigation:** Full horizontal links on `lg+`, hamburger menu below
- **Grids:** 1 column on mobile → 2 on `md` → 4 on `lg` (process steps)
- **Hero text:** `text-5xl` → `text-6xl` → `text-7xl` across breakpoints
- **Images:** Full width on mobile, side-by-side on `lg+`
- **B2B tabs:** Stack vertically on mobile, horizontal on tablet+

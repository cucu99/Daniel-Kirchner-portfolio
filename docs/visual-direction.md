# Visual Direction

## Creative North Star
- **Mood:** Professional, optimistic, approachable. Inspired by minimal personal portfolio references in `docs/design/` with clean layouts, generous whitespace, and subtle depth.
- **Keywords:** Crisp, modern, trustworthy, growth-oriented.
- **Inspiration set:** Uploaded mockups (`design/daniel_kirchner's_portfolio_homepage`, `design/about_me_page_2`, `design/blog_post_listing_*`, `design/project_showcase`). The build should replicate their hierarchy, spacing, and use of photography/illustration over gradients.

## Color System
Derived from Tailwind variables in the design HTML exports.

| Token | Hex | Usage |
| --- | --- | --- |
| `primary` | `#1173D4` | Buttons, active states, links, icon accents |
| `primary-hover` | `#0F64B6` | Darker hover state for primary CTA |
| `background-light` | `#F5F6F8` | Section backgrounds, cards (`bg-gray-50` analogue) |
| `surface` | `#FFFFFF` | Cards, content surfaces |
| `text-primary` | `#111418` | Headlines and body copy |
| `text-secondary` | `#4A5568` | Supporting text, nav items |
| `accent-muted` | `#C7CED9` | Dividers, subtle borders |
| `footer-bg` | `#1F2933` | Footer background, dark callout contrasts |

> Map these to Tailwind theme tokens (`colors.primary.DEFAULT`, `colors.primary.hover`, etc.) and ensure WCAG contrast. For dark mode, invert backgrounds and use `#0B1726` with the same primary.

## Typography
- **Primary typeface:** Inter (Google Fonts). Use `next/font` to self-host weights 400, 500, 700, 900 to match headings in mockups.
- **Scale:**
  - `display` (hero name): clamp between 3rem–4.5rem (`font-extrabold`, tight tracking).
  - `h1`: 2.5rem bold; `h2`: 2rem semibold; `h3`: 1.5rem medium.
  - Body copy: 1rem/1.625rem leading with max-width ~65ch.
- **Accents:** Use uppercase nav labels with letter-spacing `0.02em`. Keep blog subtitles and metadata in small caps or medium weight 0.875rem.

## Layout & Spacing
- **Grid:** Max content width 1200px (`container mx-auto px-6 md:px-10`). Utilize a 12-column responsive grid for sections like blog listing/cards.
- **Spacing scale:** Emulate Tailwind defaults; hero padding `py-24`, sections `py-20`, card padding `p-6`.
- **Elevation:** Apply soft shadows (`shadow-md`, `shadow-lg`) and 12–16px corner radii. Hover states use box-shadow glow tinted with `rgba(17, 115, 212, 0.2-0.5)`.

## Imagery & Iconography
- **Hero imagery:** Full-bleed photography with blurred gradient overlay (see homepage mockup). Use `next/image` with overlay `bg-gradient-to-t from-black/60` for legibility.
- **Project/blog art:** Maintain cohesive flat-lay or geometric illustrations in teal/green palettes present in `blog_post_listing_*` assets. Establish aspect ratio (~4:3) and rounded corners.
- **Icons:** Leverage Material Symbols Outlined for skill cards and Lucide/Heroicons for navigation/CTAs; keep stroke icons at 1.5pt weight with primary color fill for emphasis.

## Component Styling Patterns
- **Navigation bar:** Sticky with translucent background (`bg-white/80` + `backdrop-blur-md`). Active link uses primary color underline or weight.
- **Buttons:** Rounded-md (8px radius) with solid primary fill; white text and bold type. Hover = 95% brightness + scale `1.03`. Focus = 2px primary ring + 2px offset.
- **Cards:** White surface, subtle border `1px solid #E2E8F0`, shadow-sm, 16px radius. On hover, lift via translateY(-4px) and glow.
- **Blog post layout:** Single-column article with max width 768px, generous line-height, blockquote style `border-l-4 primary` + `bg-gray-50`.
- **Contact banner:** Full-width primary background with inverted button.

## Interaction & Motion
- **Hover transitions:** Duration 200ms, easing `ease-out`. Buttons and cards scale subtly; links transition color without underline shift.
- **Focus states:** Always visible, using primary ring on interactive elements to meet accessibility.
- **Scroll effects:** Optionally add fade-in or slide-up for hero text using `framer-motion` but respect `prefers-reduced-motion`.

## Accessibility Guardrails
- Maintain color contrast ratio ≥ 4.5:1 for text on backgrounds. Primary (`#1173D4`) on white passes for both large and small text; lighten backgrounds if needed.
- Ensure nav and hero overlays provide readable text over imagery by enforcing gradient opacity ≥ 0.6 near text.
- Provide alternate text for all imagery and transcripts for testimonial quotes if added.

## Implementation Notes
- Capture these tokens in `tailwind.config.ts` and a dedicated `tokens.css` (if needed) before coding components.
- Add sample components (Header, Hero, Card) early to validate the system against the mockups in `docs/design/`.
- Update this document as visual refinements occur, keeping it the source of truth for design decisions.

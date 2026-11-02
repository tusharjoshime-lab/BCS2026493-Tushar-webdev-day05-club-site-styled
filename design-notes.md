# Design notes — Day 5

## Design direction
- **Site purpose and audience:** A student astronomy club website for college students who want to explore space, attend beginner-friendly events, and join a campus community.
- **Visual style / mood:** Modern, curious, welcoming, and space-inspired. Deep navy and blue create a cosmic feel; warm gold highlights important actions.

## Colour palette
| Role | Colour value | Where it is used |
|---|---|---|
| Primary | `#2458a6` | Links, small accents, icons |
| Secondary | `#173f7d` | Header, hero gradients, form sidebar |
| Accent | `#e5a93d` | Main buttons, stars, focus accents |
| Page background | `#f3f6fb` | Main page background |
| Main text | `#17243a` | Body text and headings |

## Typography
- **Google Font for headings:** Manrope
- **Google Font for body text:** DM Sans
- **Why these fonts work for the site:** Manrope gives headings a geometric, modern character, while DM Sans stays clear and readable for paragraphs, forms, and navigation. Both are loaded from Google Fonts with sans-serif fallbacks.

## CSS design tokens
| Custom property | Value | Purpose |
|---|---|---|
| `--color-primary` | `#2458a6` | Primary interactive colour |
| `--color-accent` | `#e5a93d` | Highlights and calls to action |
| `--space-3` | `1.5rem` | Common section/card spacing |
| `--font-heading` | `'Manrope', sans-serif` | Heading font stack |
| `--radius-card` | `0.75rem` | Consistent rounded cards |

## Selectors and cascade
- **Element selector:** `body`, `h1`, `table`
- **Class selector:** `.feature-card`, `.site-nav a`, `.form-card`
- **ID selector:** `#join-us`
- **Descendant selector:** `.site-nav a`, `.field label`
- **Attribute/pseudo-class selectors:** `a[aria-current="page"]`, `a:hover`, `input:focus-visible`

The stylesheet contains a commented-out DevTools exercise at the bottom. To perform it, temporarily uncomment the two test rules, add `feature-card` and `join-us` to the same test element (or use the existing CTA section and temporarily apply both test selectors), then inspect the element in browser DevTools. When both selectors match the same element and set the same property, the ID selector wins because ID specificity (1-0-0) is higher than class specificity (0-1-0). The test rules are disabled in the final stylesheet so the finished site stays visually consistent.

## DevTools debugging
- **Issue to check:** Confirm the shared stylesheet loads on all four pages and check for any horizontal overflow at narrow widths.
- **How I found it:** Use browser DevTools → Network (filter for CSS) and Elements/Computed styles; resize the viewport and inspect the page width.
- **Fix:** All root-level pages link to `css/style.css`. Responsive grids switch to one column at smaller breakpoints, navigation wraps, and event tables can scroll horizontally inside `.table-wrap`.
- **Before submission:** Perform this browser check yourself and update this section with any additional issue you actually find and fix.

## Final review
- **Pages checked:** `index.html`, `about.html`, `registration.html`, `contact.html` (source files and stylesheet links checked; please open each page in a browser at desktop and narrow widths for visual confirmation).
- **Screenshot filename:** `day05-club-site-screenshot.png` (save your own browser screenshot with this name after testing).
- **Repository URL:** `https://github.com/tusharjoshime-lab/bcs2026493-tushar-webdev-day05-club-site-styled` (create this repository on GitHub and push the project before treating the URL as live).

## Git checkpoints
Run each checkpoint from the project root, after making the corresponding changes:
1. `git add . && git commit -m "style: link stylesheet"`
2. `git add . && git commit -m "style: add selectors"`
3. `git add . && git commit -m "style: add typography and colours"`
4. `git add . && git commit -m "refactor: use css variables"`
5. `git add . && git commit -m "docs: add design notes"`

The commits are listed as a workflow guide; because the finished project is supplied as one ZIP, create the commits in sequence while completing/reviewing each checkpoint rather than trying to recreate the intermediate history from the final files.

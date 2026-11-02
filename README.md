# Day 5 — CSS Fundamentals: Orbit Club

A styled version of the Day 4 responsive four-page astronomy club website. The four HTML pages share one external stylesheet at `css/style.css`.

## Files
- `index.html` — home page
- `about.html` — club story and events
- `registration.html` — membership and volunteer forms
- `contact.html` — contact information and message form
- `css/style.css` — shared responsive design system, CSS selectors, and custom properties
- `design-notes.md` — palette, typography, tokens, selector/cascade exercise, and review checklist
- `favicon.svg` — browser icon

## Preview
Open `index.html` in a browser. All pages use relative links to `css/style.css`. Google Fonts load over the internet; fallback fonts are defined.

## DevTools exercise
The bottom of `css/style.css` contains a commented-out class-versus-ID exercise. Follow the instructions in `design-notes.md`, inspect specificity in DevTools, and leave the exercise rules disabled for the final appearance.

## Git setup and checkpoint commits
Initialize a fresh repository in this folder and make the assignment commits as you complete/review each checkpoint:
```bash
git init
git add .
git commit -m "style: link stylesheet"
# Complete/verify the selector checkpoint, then:
git add .
git commit -m "style: add selectors"
# Continue the remaining checkpoints using the messages in design-notes.md.
```
Because this ZIP contains the completed stylesheet, you may instead make a single initial commit and then create the remaining checkpoint commits while reviewing each step.

## Forms
Forms are demos using `action="#"`; they do not send information to a server. Never enter a real password or sensitive information.

## GitHub repository name
`bcs2026493-tushar-webdev-day05-club-site-styled`

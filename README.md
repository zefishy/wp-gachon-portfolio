# Portfolio — Ryan Wong

A single-page personal portfolio for **Ryan Wong**, exchange student at
Gachon University (K0126002 Web Programming · 2026 Fall · Dr. Toshpulatov).

Built as the Week 9 homework: a personal portfolio repo with a semantic
HTML page, responsive CSS themed to match my
[course library](https://github.com/zefishy/web-prog-gachon), and a
light/dark theme toggle that remembers your choice.

## What's on the page

- **Hero** — name, photo, role, and a short bio
- **Course projects** — three pieces of coursework I'm proud of:
  - [Book Search App](https://github.com/zefishy/web-prog-gachon/blob/main/week7/book_search.html) — Open Library API lab with skeleton loading cards, timeout, retries, and a cache
  - [Registration form with JS validation](https://github.com/zefishy/web-prog-gachon/blob/main/week8/week8_1/homework_registration_js_validation.html) — live per-field validation with ARIA announcements
  - [Gachon Wind website proposal](https://github.com/zefishy/web-prog-gachon/blob/main/assignment/project.html) — Team 16 club website redesign proposal
- **Skills** — markup, styling, scripting, design, and workflow
- **About** — role, field, focus, interests, and goals

## Structure

```
portfolio/
├── index.html        # the page (semantic: header, nav, main, footer)
├── css/
│   └── styles.css    # design tokens + page styles (dark default, light theme)
├── js/
│   └── main.js       # light/dark toggle, saved to localStorage
└── img/
    └── avatar.svg    # profile photo placeholder
```

## Theming

The palette is the same one as my course library — a dark green ramp
(`#092328 → #8BBB92`) by default, with a light theme behind the header
switch. The switch cross-fades the colour tokens and saves the choice in
`localStorage`, so returning visitors get the theme they picked.

## Replace the placeholder photo

`img/avatar.svg` is a stand-in (initials on the palette green). To use a
real photo, drop it in `img/` and point the hero image at it in
`index.html`:

```html
<img class="avatar" src="img/me.jpg" alt="Portrait of Ryan Wong" width="160" height="160">
```

## Deploy — GitHub Pages (Homework 2)

1. Push this repo to GitHub with the branch name `main`.
2. On the repo page: **Settings → Pages → Build and deployment →
   Source: "Deploy from a branch"**, branch `main`, folder `/ (root)` → **Save**.
3. Wait about a minute — the site goes live at
   `https://<username>.github.io/portfolio/` (the URL to submit on Cybercampus).

## Accessibility — the Homework 2 checklist

The page already meets every item; the Lighthouse score must be captured
from the **live** URL after deploying (DevTools → Lighthouse →
category *Accessibility* → Mobile → Analyze):

- [x] Semantic HTML — `header`, `nav`, `main`, `footer`, labelled `section`s
- [x] Responsive CSS — mobile-first, with narrow-phone rules at ≤ 36 rem
- [x] JS interaction — light/dark toggle with saved preference
- [x] Meaningful alt text on every image
- [x] WCAG AA contrast — computed for every text/background pair in both
      themes; worst pair is 6.8:1 (AA requires 4.5:1)
- [x] Valid HTML — passes the W3C Nu validator with zero errors
- [ ] **Lighthouse Accessibility ≥ 90** — run it on the live URL and save the
      screenshot for Cybercampus

## Viewing

Open `index.html` in any browser — no build step, no dependencies. Once
GitHub Pages is enabled on this repo, the site will also be live at
`https://<username>.github.io/portfolio/`.

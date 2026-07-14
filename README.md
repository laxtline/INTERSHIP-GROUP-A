# Internship Group A — Project Gallery

A single-page showcase website for our **Diploma in Electrical Engineering** internship (Group A).
Animated landing screen → project gallery → fullscreen image viewer, with an electrical / circuit-board theme.

## Run it

Just open `index.html` in any modern browser (double-click). No build step, no server needed.

## Project structure

```
sibu/
├─ index.html        # the whole site (HTML + CSS + JS, self-contained)
├─ images/           # project photos (project-1.jpeg … project-6.jpeg)
└─ README.md
```

## How to customize

Everything is edited in one place. Open `index.html` and find the `PROJECTS` array
near the bottom (inside `<script>`):

```js
const PROJECTS = [
  { src:"images/project-1.jpeg", name:"Project Work", alt:"…description…" },
  ...
];
```

- **Change a caption** → edit `name`.
- **Add / remove a photo** → add or delete a line (counter, dots, and lightbox update automatically).
- **Replace a photo** → drop a new file in `images/` and point `src` at it.
- `alt` is the description read by screen readers and used by search engines — keep it meaningful.

To change the group name/title, edit the `.title` / `.subtitle` in the `<header class="hero">`.

## Features

- Fully responsive (mobile → desktop), works offline.
- Keyboard support: `←` / `→` to navigate, `Esc` to close the viewer.
- Touch swipe on mobile.
- Accessible: focus management, ARIA labels, and respects `prefers-reduced-motion`.
- Graceful fallback if an image is missing.

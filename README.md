# Google Homepage Clone (Tailwind CSS)

A responsive front-end recreation of the Google homepage built using plain HTML, Tailwind CSS utilities, and minimal vanilla JavaScript.

This project focuses on layout precision, utility-first styling, and simple DOM interaction without external frameworks.

---

## Overview

The page includes:

- Header navigation (Gmail, Images, Apps icon, Sign in button)
- Centered Google logo
- Interactive search box with SVG icons
- Trending searches dropdown (visible on input focus)
- Search action buttons
- Multi-language links
- Fixed footer (localized for India)

The layout adapts across screen sizes using Tailwind’s responsive utilities.

---

## Tech Stack

- HTML5
- Tailwind CSS (compiled into `output.css`)
- Vanilla JavaScript
- Inline SVG icons

No frameworks. No CDN dependencies inside the markup.

---

## Project Structure

```
project/
│
├── index.html
├── output.css
└── images/
    └── google.png
```

---

## Features

### Responsive Layout
- Flexbox-based alignment
- Responsive widths (`w-full`, `md:w-1/2`)
- Fixed footer at bottom
- Clean spacing and hover effects

### Interactive Search Box
The search input toggles a hidden trending results container using basic DOM events:

```javascript
document.getElementById("searchbox").onfocus = function () {
    document.getElementById("resultlist").classList.toggle("hidden")
}

document.getElementById("searchbox").onblur = function () {
    document.getElementById("resultlist").classList.toggle("hidden")
}
```

Behavior:
- Focus → shows trending list
- Blur → hides trending list

### Utility-First Styling
All styling is implemented using Tailwind utility classes:
- Borders
- Rounded components
- Hover states
- Drop shadows
- Spacing utilities

No custom CSS classes were written manually.

---

## How to Run

1. Compile Tailwind (if not already compiled):

```bash
npx tailwindcss -i ./input.css -o ./output.css --watch
```

2. Open `index.html` in your browser.

---

## What This Project Demonstrates

- Layout structuring with Flexbox
- Visual UI recreation
- Tailwind responsive design patterns
- Basic DOM manipulation
- Clean component grouping inside a single HTML file

---

## Known Limitations

- The search box does not perform real queries.
- Trending results are static.
- Accessibility roles are minimal.
- No keyboard navigation support for results.

---

## Possible Improvements

- Add keyboard navigation for dropdown results
- Implement actual search functionality
- Improve accessibility with ARIA attributes
- Replace toggle logic with explicit add/remove for better state control
- Refine mobile spacing

---

## Purpose

This project was built as a front-end practice exercise to replicate a real-world interface using modern utility CSS and minimal scripting.
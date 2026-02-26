# Pipo's Hitchhiking Adventure — LAB3 (RICING)

## Project Overview

This project is an interactive narrative game inspired by classic "Choose Your Own Adventure" (CYOA) books. The game is built with **HTML and CSS only** (no JavaScript) and is designed to be served via an **NGINX** web server.

**LAB3** applies **RICING** (page theme): a set of custom styles and layout rules to give the story a consistent, readable look with typography, colors, animations, and responsive layout.

---

## What Is This Lab About?

**RICING** (from the Linux community) means customizing and tuning a system (here, a web story) to make it more aesthetic, unique, and pleasant to use. In this lab we:

- Define a **theme** with CSS variables (colors, backgrounds, typography, spacing, transitions).
- Use **CSS Grid and Flexbox** for the page layout (no float or absolute positioning for main structure).
- Style **interactive choice buttons** (default, hover, active, and keyboard focus).
- Add **animations and micro-interactions** (e.g. content fade-in, title glow, image reveal) using `@keyframes` and `transition`.

---

## How the Lab Works

- **Pages**: The story is split into multiple HTML pages under `pages/` (e.g. `pages/inicio/`, `pages/aventura/`, `pages/finales/`). Each page links to shared CSS in the `css/` folder.
- **Theme**: `css/story-theme.css` defines CSS variables (e.g. `--color-primary`, `--bg-inicio`, `--font-heading`, `--spacing-md`, `--transition-normal`) used across the site.
- **Layout**: `css/layout.css` uses a Grid layout with areas for header, content, choices, and footer, and Flexbox inside content and choices. Layout is responsive with relative units (`rem`, `%`, `vw`/`vh`).
- **Buttons**: `css/buttons.css` styles the choice links as RPG-style buttons with three visual states and `:focus-visible` for keyboard users.
- **Animations**: `css/animations.css` implements at least three animations (e.g. content fade-in, title glow, image reveal) and uses the theme’s transition variables for interactions.

---

## How to Run the Lab

1. **Using NGINX**
   - Install and run NGINX so that its document root (or a `location`) points to this project folder (the one that contains `pages/` and `css/`).
   - Open the start page in the browser, e.g.  
     `http://localhost/pages/inicio/index.html`  
     (adjust host/port/path to match your NGINX configuration.)

2. **Opening the start page**
   - Entry point: **`pages/inicio/index.html`**.
   - From there, follow the links to choose routes and reach different endings (good, neutral, bad).

3. **No server required for local file viewing**
   - You can also open `pages/inicio/index.html` directly in the browser (file://). Some features (e.g. Google Fonts) work best with a real host; running with NGINX is the intended setup for the lab.

---

## The Story: Who Is Pipo

Pipo is a young traveler with one goal: to cross the border and leave the country to start a new life. With a backpack and a sign, he hitchhikes through different scenarios. The player makes choices for Pipo; each route leads to different situations and endings (good, neutral, or bad).

---

## Repository and Rules

- The project uses **no JavaScript**.
- **No inline CSS**: all styles are in the `css/` folder and linked from each HTML file.
- HTML files are grouped in **subfolders** under `pages/` (e.g. `inicio`, `aventura`, `finales`); the project root contains no loose HTML files.
- A `.gitignore` is used to avoid committing unnecessary files. The lab expects a public Git repository with a clear history (e.g. at least one commit per day while the lab is active).

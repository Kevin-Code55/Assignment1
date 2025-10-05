# Kevin – Portfolio (HTML5 & CSS3, No Flexbox)

A simple, responsive, **four‑page** portfolio built with semantic HTML5 and CSS3 **without Flexbox**. The site demonstrates linear/angled gradients, separate stylesheets per viewport, basic accessibility, and HTML5 form validation.

## Pages
- **Home** (`index.html`) – Intro blurb and navigation.
- **About** (`about.html`) – Photo plus a intro video rendered via `<video controls poster="…">`.
- **Projects** (`projects.html`) – 4–5 short project summaries (2–3 lines each).
- **Contact** (`contact.html`) – HTML5 form (Name, Email, Phone, Submit)


## Folder Structure
```
/ (repo root)
  index.html
  about.html
  projects.html
  contact.html
  main.css
  mobile.css          # ≤ 600px
  tablet.css          # 601–900px
  desktop.css         # ≥ 901px
  /images
    myphoto.png
    video-poster.png
  /video
    websitevideo.mp4  22s, H.264 MP4
```

## Responsiveness (No Flexbox)
- Uses **separate CSS files** per breakpoint:
  - `mobile.css` → `@media (max-width: 600px)`
  - `tablet.css` → `@media (min-width: 601px) and (max-width: 900px)`
  - `desktop.css` → `@media (min-width: 901px)`
- Layout uses **floats + clearfix** (no Flexbox).
- Images and video are fluid (`max-width: 100%`, `height: auto` in mobile/tablet CSS).

## Color & Gradients
- Primary palette: **lightblue** on white/neutral text.
- Global gradient applied to `body`:
  ```css
  background: linear-gradient(135deg, lightblue, white);
  ```
- Additional accents (borders/buttons) reuse `lightblue'
- High‑contrast text ensured for readability.

## Accessibility
- Semantic landmarks: `<header>`, `<nav>`, `<main>`, `<footer>`.
- Descriptive `alt` text for images (`alt="Photo of Kevin"`). Decorative images can use `alt=""`.
- Labels explicitly associated with form inputs.
- Optional: set `aria-current="page"` on the active nav link for each page.
- (Nice to have) A “Skip to main content” link pointing to `#main`.

## Media
- **Photo:** `images/myphoto.png` (used as both small logo and About page portrait).
- **Video:** `video/websitevideo.mp4` (45–60s, MP4/H.264), referenced in About page:
  ```html
  <video controls width="400" poster="images/video-poster.png">
    <source src="video/websitevideo.mp4" type="video/mp4" />
  </video>
  ```
- Keep media **inside this repository** (avoid `C:\…` or `../` paths outside the repo).

## Contact Form (HTML5 Validation)
Fields and example constraints:
```html
<input id="name" name="name" type="text" required minlength="2" maxlength="60">

<input id="email" name="email" type="email" required>

<input id="phone" name="phone" type="tel" required


<textarea id="comments" name="comments" required minlength="10" maxlength="500"></textarea>
```

## How to Run Locally
1. Download/clone the repository.
2. Open `index.html` in your browser.
3. Navigate via the top menu to About/Projects/Contact.


External Code Help 
Nothing was copied directly used W3C website tutorials and general youtube videos as well as code from lectures and labs 

---

© 2025 Kevin.
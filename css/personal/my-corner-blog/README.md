# My Corner Blog

A small, single-page personal "about me" blog built with plain HTML and CSS. It features a two-photo-strip header (a real photo booth strip next to a chibi illustration), a few short sections about me, and a contact link. No frameworks, no JavaScript, and no external requests: even the fonts are self-hosted.

<!-- Add a screenshot named screenshot.png next to this file, then uncomment the line below:
![Screenshot of the blog](screenshot.png)
-->

## Features

- **Responsive layout.** The header sits in a row on wide screens and stacks into a column at `52rem` (about 832px) and below.
- **Design tokens with CSS variables.** All colors and fonts are defined once in `:root` and reused with `var(--name)`.
- **Fluid heading.** The `h1` scales with the window width using `clamp(2.5rem, 6vw, 4.25rem)`.
- **Photo-strip cards.** Each strip sits on a white frame with a soft shadow and a slight tilt, with the two tilted in opposite directions and staggered.
- **Self-hosted fonts.** Fredoka (headings) and Nunito (body text) load from the `fonts/` folder through `@font-face`, using `.woff2` with a `.ttf` fallback.
- **Auto-decorated email links.** Any link whose `href` starts with `mailto:` gets a small envelope icon, drawn with an attribute selector and a CSS mask so it follows the link color.
- **Semantic HTML.** `header`, `main`, `section`, `footer`, and `figure`/`figcaption` are used where they fit, with descriptive `alt` text on images.

## Built with

- HTML5
- CSS3 (flexbox, custom properties, media queries, `clamp()`, `@font-face`, pseudo-elements, CSS masks)

## Project structure

```
my-corner-blog/
├── index.html
├── styles.css
├── README.md
├── fonts/
│   ├── Fredoka.woff2
│   ├── Fredoka.ttf
│   ├── Fredoka-OFL.txt
│   ├── Nunito.woff2
│   ├── Nunito.ttf
│   └── Nunito-OFL.txt
└── images/
    ├── irl-me-pic.jpg
    ├── chibi-me-pic.jpg
    └── mail.svg
```

## Getting started

1. Download or clone the project and keep the folder structure above intact, since the HTML and CSS use relative paths.
2. Open the folder in VS Code.
3. Start a local server with the **Live Preview** or **Live Server** extension: right-click `index.html` and choose **Show Preview** or **Open with Live Server**.
4. Edit and save, and the page refreshes automatically.

> **Note:** open the page through a local server rather than double-clicking `index.html`. Browsers can block the CSS mask that draws the email icon when a page is opened straight from disk (`file://`).

## Customizing

- **Text:** edit the headings and paragraphs in `index.html`. The sections are `#about-me`, `#my-hobbies`, and `#fun-facts`.
- **Colors and fonts:** change the variables at the top of `styles.css` inside `:root`. Every rule that uses `var(--...)` updates automatically.
- **Photos:** replace `images/irl-me-pic.jpg` and `images/chibi-me-pic.jpg` with your own, keeping the same file names (or update the `src` paths in `index.html`). Tall, narrow strips work best, since each frame is `10.5rem` wide.
- **Email link:** change the `mailto:` address and link text in the footer.
- **Breakpoint:** the layout switches at `@media (max-width: 52rem)` near the bottom of `styles.css`.

## What I practiced

- Structuring a page with semantic HTML and class names that describe purpose
- Storing colors and fonts as CSS variables
- Building rows and columns with flexbox (`justify-content`, `align-items`, `gap`, `align-self`)
- Descendant selectors (`.strip-frame img`) and attribute selectors (`a[href^="mailto:"]`)
- Responsive design with a media query and `clamp()`
- Using `rem` units for text and spacing so the page respects the visitor's font settings
- Self-hosting fonts with `@font-face` and converting them to `.woff2`

## Credits and licenses

- **Fonts:** [Fredoka](https://fonts.google.com/specimen/Fredoka) and [Nunito](https://fonts.google.com/specimen/Nunito) are licensed under the [SIL Open Font License 1.1](https://openfontlicense.org). The license text for each is included in the `fonts/` folder.
- **Email icon:** `mail.svg` came from [SVG Repo](https://www.svgrepo.com). Check the license shown on the icon's page there if you reuse or redistribute it.
- **Photos and illustration:** personal images of the author. Add your preferred usage terms here.
- **Code:** add a license here (for example MIT) if you want others to reuse it.

## Ideas for next steps

- Add a small-phone rule (around `26rem`) that shrinks the strips so two of them fit on very narrow screens without side scrolling
- Add a navigation menu with jump links to each section (`#about-me`, `#my-hobbies`, `#fun-facts`)
- Turn "Things I Love" into a styled list, or use the unused `--peach` variable for card-style panels
- Publish the site for free with GitHub Pages

# Pavlos Koseoglou academic website

A simple, responsive, one-page academic website for GitHub Pages. It uses plain HTML and CSS, with no framework, database, cookies, analytics, or contact form.

## Folder structure

```text
pavlos-koseoglou-github-site/
├── index.html                 Main page and all text
├── README.md                  These instructions
├── .nojekyll                  Tells GitHub Pages not to process the site with Jekyll
└── assets/
    ├── css/
    │   └── style.css          Colors, layout, spacing, and mobile rules
    └── images/
        ├── pavlos-koseoglou.png
        └── uoa-logo.png
```

## Publish on GitHub Pages

1. Sign in to GitHub and create a new **public** repository. A clear name is `pavlos-koseoglou.github.io` if this will be your main personal site.
2. Upload **the contents of this folder**, not the outer ZIP file. `index.html` must be at the top level of the repository.
3. Open the repository's **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch **main**, folder **/(root)**, and click **Save**.
6. GitHub normally publishes the site within a few minutes. If the repository is named `pavlos-koseoglou.github.io`, the address will be `https://pavlos-koseoglou.github.io/`. For another repository name, it will normally be `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`.

## Where to edit things

Open `index.html` in a plain-text editor such as Visual Studio Code, Notepad++, or GitHub's built-in editor. The file contains large comments beginning with `<!-- ===`. These clearly mark each section.

### Name and academic title

Near the top of `index.html`, edit these lines:

```html
<span class="brand-name">Pavlos Koseoglou</span>
<span class="brand-role">Assistant Professor · Nuclear Physics</span>
```

Also update the large introduction under the `INTRODUCTION` comment.

### About text

Find the comment `ABOUT`. Edit the paragraphs inside this section. Keep the section to one or two short paragraphs for a clean page.

### Research areas

Find `RESEARCH AREAS`. Each topic is an `<article class="card">...</article>` block. To add a research area, copy one full article block and change its heading and paragraph.

### Project

Find `FEATURED PROJECT`. Change the text there. To change the external project link, edit only the address inside:

```html
href="https://radium.phys.uoa.gr/Yber/"
```

### Academic positions, education, and grants

Find `EXPERIENCE AND EDUCATION`. Each entry is one `<li>...</li>`. Add new positions at the top of the relevant `<ol class="timeline">` list.

Example:

```html
<li>
  <span>2027–present</span>
  <strong>Position title</strong>
  <small>University or research institute</small>
</li>
```

### Contact information

Find `CONTACT INFORMATION`. Edit the address, office, email, and telephone directly. There is deliberately no form.

The email is written as `pkoseoglou [at] phys.uoa.gr` to reduce automated spam collection. To make it clickable, replace that text with:

```html
<a href="mailto:pkoseoglou@phys.uoa.gr">pkoseoglou@phys.uoa.gr</a>
```

### Photograph and university logo

The images are in `assets/images/`.

- Replace `pavlos-koseoglou.png` with a new portrait using exactly the same filename.
- Replace `uoa-logo.png` in the same way if the official logo changes.
- A square image of at least 600 × 600 pixels works best for the circular portrait.

If you use another filename, also change the corresponding `src="assets/images/..."` address in `index.html`.

### Blue colors

Open `assets/css/style.css`. The first lines contain all main colors:

```css
--blue-900: #0b2f55;
--blue-700: #145da0;
--blue-600: #1f70b7;
--blue-100: #eaf4fb;
```

Changing these four values changes the color scheme across the whole site.

## Adding a publications link

A publications list was not present in the supplied files. When you have a Google Scholar, ORCID, Scopus, or institutional publications URL, add a navigation link before `Contact`:

```html
<a href="YOUR-PUBLICATIONS-URL" target="_blank" rel="noopener noreferrer">Publications</a>
```

You can also add the same link below the Research section using the `text-link` class.

## Testing before publishing

Double-click `index.html` to open it locally in a browser. Check:

- every menu item scrolls to the correct section;
- the Yber link opens correctly;
- the telephone link is correct;
- the page is readable on a narrow mobile window;
- no old or private information remains.

## Keeping it simple

For normal updates, edit only `index.html`. Do not rename folders or move `style.css`, because that would break the relative file paths. No installation or build command is required.

## Google Analytics

Google Analytics 4 is enabled on every HTML page with Measurement ID `G-2GMNB56BF7`.

The tracking code is located immediately before `</head>` in each HTML file. If the Measurement ID changes, replace every occurrence of `G-2GMNB56BF7` with the new ID. After publishing, visits may take up to 24–48 hours to appear in standard Google Analytics reports, while **Reports → Realtime** is normally the quickest place to test it.

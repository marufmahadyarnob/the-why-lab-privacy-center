# The Why Lab — Privacy Center

Static bilingual Privacy Center (English and বাংলা) for **The Why Lab**, built with plain HTML, CSS, and JavaScript for GitHub Pages.

## Files

```text
├── index.html   Semantic markup and default English policy content
├── style.css    Theme tokens, responsive layout, and print styles
├── script.js    Bengali translations, TOC observer, theme/language state, and UI actions
├── favicon.svg  Site icon
└── README.md
```

## Updating Content

- **English copy & policy:** Edit `index.html` directly. `script.js` snapshots the English DOM on load, so English text lives in one place only.
- **Bengali translations:** Update `BN_UI`, `BN_POLICY`, and `BN_FAQ` in `script.js`. Keep section `id` values (`section-1` through `section-19`) aligned with `index.html`.
- **Contact email & social links:** Edit `CONFIG` at the top of `script.js` and the matching fallback attributes in `index.html`.
- **Effective / Last Updated dates:** Update `[data-i18n="dates.effectiveValue"]` and `[data-i18n="dates.updatedValue"]` in `index.html`, and their counterparts inside `BN_UI` in `script.js`.
- **Colors:** Adjust the CSS custom properties in `:root` and `html.dark` at the top of `style.css`.

## Deploying to GitHub Pages

1. Push `index.html`, `style.css`, `script.js`, `favicon.svg`, and `README.md` to the `main` branch of a public GitHub repository.
2. Open the repository **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select **`main`** and **`/ (root)`**, and save.
4. Once GitHub Pages finishes publishing, add your live URL as a `<link rel="canonical" href="...">` tag inside `<head>` in `index.html`.

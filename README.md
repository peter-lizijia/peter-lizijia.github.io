# Zijia Li's Academic Homepage

Public site: https://peter-lizijia.github.io/

Static HTML, CSS, and JavaScript, adapted from [Ruiyu Wang's academic portfolio template](https://github.com/RuiyuWANG/ruiyuwang.github.io/tree/template), revision `3283c9835a21d9e471f7f9bb93c11ce9117028ea`. The template's MIT license is in `licenses/academic-portfolio-MIT.txt`.

## Editing

- `index.html`: homepage, biography, experience, education, projects, and honors.
- `data/site-content.json`: shared text and local editor content. Keep the matching `data-editable` text in HTML in sync so the site also works without JavaScript.
- `data/publications.json`: publication metadata. Add public paper, project, or code URLs to the `links` array when available.
- `data/research-keywords.json`: keyword labels and groups.
- `css/portfolio.css`: template styling; `css/profile.css`: personal layout adjustments.
- `favicon.svg`: the L favicon; `assets/img/avatar.png`: the portrait.
- `pdfs/Zijia_Li_CV.pdf`: downloadable CV; `images/cv-pages/cv-1.png`: its rendered preview. Refresh both when replacing the CV. Older PDF URLs in `assets/files/` are retained for existing links.

Life and Blog pages are empty and their navigation links are commented out. Services is reserved in an HTML comment. The publication entry currently states workshop acceptance and full-manuscript review separately; update its status only when confirmed.

## Preview and Build

No dependencies or local Jekyll installation are required. With Node.js installed:

```sh
npm run dev
npm run build
npm run check
```

The preview server prints its local URL and uses another port if needed. `?edit=1` enables the localhost text editor. Alternatively, preview with `python3 -m http.server 8000 --bind 127.0.0.1`.

The publication and keyword scripts generate committed HTML and JavaScript, so GitHub Pages needs no build step. Keep `.nojekyll` in the repository root. The older `index.md`, `_config.yml`, `_includes`, `_layouts`, and `_sass` are retained as legacy source and no longer control the live homepage.

Commit the changed source and generated files, then push to `main`. GitHub Pages publishes the repository root.

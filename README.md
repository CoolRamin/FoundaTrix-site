# FoundaTrix Studio Website

Public source for the product website of **FoundaTrix Studio**, a Windows desktop program by
Ramisoft Solutions for the analysis and design of rigid foundations of any shape: spread, combined,
strapped and mat foundations with any number of pedestals.

This repository's **Issues** are also the public place to report a bug in the program or ask for a
feature: see [Reporting bugs and requesting features](#reporting-bugs-and-requesting-features).

## Scope of this repository

This repository contains **only the static website** (`src/`): HTML, CSS, a small script and SVG
artwork, plus the GitHub configuration that makes its Issues usable as a public support channel.

**It does not contain, and will never contain, any FoundaTrix Studio application source code.** The
desktop program, its engine and its cloud service are developed in a separate, private repository.
Nothing here requires or exposes that source: no engine code, no project files, no cloud
configuration, no build output of the program.

## Reporting bugs and requesting features

- **Bug reports and feature requests (public):** open an [issue](../../issues/new/choose) and pick
  the template that fits.
- **Private matters** (confidential project data, licensing, security): email
  `admin@ramisoftsolutions.com`. Please do not attach a client's project to a public issue.
- **Version details:** in the program, **Help > About > Copy details** copies the version, the
  build and how the program was installed. Paste them into the issue.

## Site map

| Path | File | What it is |
|---|---|---|
| `/` | `src/index.html` | Home: what the program does, the premium capabilities, plans, download, support |
| `/features/` | `src/features/index.html` | The engineering in detail: methods, standards, data and exchange |
| `/pricing/` | `src/pricing/index.html` | Free, signed in, and premium, with a comparison table and questions |
| `/support/` | `src/support/index.html` | Where to report a bug, ask for a feature or write privately |
| `/privacy/` | `src/privacy/index.html` | Privacy policy |
| `/terms/` | `src/terms/index.html` | Terms of use, including the engineering disclaimer |
| (any 404) | `src/404.html` | Not-found page |

`styles.css` and `site.js` are shared by every page. The pages are hand-written HTML with no build
step and no framework. The site uses no cookies, analytics, trackers or third-party scripts, fonts
or images: everything it loads comes from its own folder.

**Every `href` and `src` is root-absolute** (`/styles.css`, `/images/...`, `/pricing/`). The pages
live in folders, so a relative path that works from `/` breaks from `/pricing/`, and for a
stylesheet it fails silently: the page still renders, unstyled.

## Placeholder artwork

The product pictures are **placeholders**, drawn as SVG to look like the program, until real
screenshots replace them. Each one lives in `src/images/placeholders/` and is referenced by an
`<img>` inside a `.shot` frame, so replacing one is: save the screenshot as a PNG under
`src/images/`, point the `src` at it, and update the `width`, `height` and `alt` attributes.

| Placeholder | Used on | The screenshot it stands in for |
|---|---|---|
| `studio-overview.svg` | Home (below the hero), Features | The Studio with a site of footings coloured by bearing pressure, its legend, the Model Explorer and Properties |
| `studio-modelling.svg` | Home | Drawing a footing: a snap marker, a typed dimension and the Command Line's prompt |
| `bearing-pressure.svg` | Home | One foundation's pressure map with a lifted corner and the neutral axis, beside the Results pane |
| `concrete-design.svg` | Home, Features | The Design pane's checks with their clauses, beside the swept shear and moment envelope |
| `tables.svg` | Home | The Load Combinations table beside the model |
| `wizard.svg` | Home, Features | The vertical vessel wizard: steps, questions, the drawing and the checks |
| `steel-design.svg` | Home, Features | A pipe rack coloured by AISC 360-22 utilisation, with the Steel pane |
| `calc-report.svg` | Home, Features | Two pages of the calculation report: a derivation, symbolic then substituted, and a figure |
| `bim-export.svg` | Home, Features | An exported foundation with reinforcement and anchorage in a BIM viewer |

`src/images/hero-foundation.svg` (the hero's illustration, a combined footing), `src/images/types/*.svg` (the five
foundation types) and `src/images/foundatrix-mark.svg` / `src/favicon.svg`
(the program's own mark, converted from its `Logo.xaml` and `Logo.Small.xaml`) are artwork, not placeholders.

Capture guidance that worked for the sister site: a window of about 1500 x 1000, the workspace band
rather than the whole window, fictional project, client and site names only, and a link from each
picture to its full-size file.

## Before publishing: values to confirm

| What | Where | Now |
|---|---|---|
| Download link (Microsoft Store) | `src/index.html`, `#download` section, and every "Download" button (`/#download`) | A "coming soon" Store button; replace with the listing URL and Microsoft's official badge |
| This repository's GitHub URL | Every page (search for `github.com/CoolRamin/FoundaTrix-site`) | `https://github.com/CoolRamin/FoundaTrix-site` |
| The site's domain | Add `<link rel="canonical">`, `og:url` and a `sitemap.xml` once it is known | Omitted on purpose |
| Privacy and terms URLs in the program and the Store listing | They point at `https://www.ramisoftsolutions.com/privacy/` and `/terms/` | Keep those pages, or point the program at this site's |

The privacy policy and terms of use are the same text as the pages published on
www.ramisoftsolutions.com (effective October 5, 2026). Change both together.

## Local preview

There is no build step. Because the links are root-absolute, serve `src/` with any static file
server rather than opening the files directly, for example:

```bash
python -m http.server 8080 --directory src
```

then open `http://localhost:8080/`.

## Deployment

The site is a plain static folder (`src/`) with an Azure Static Web Apps configuration
(`src/staticwebapp.config.json`: trailing slashes, the 404 page, security headers including a
content security policy). Deployment wiring is added when the hosting is set up.

## Contributing

Typo fixes and copy improvements are welcome by pull request; see [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT for the website's source and content (see [LICENSE](LICENSE)). The FoundaTrix Studio program
itself is separate, closed-source software under its own terms. "FoundaTrix Studio" and its mark
are not licensed for reuse by the MIT license.

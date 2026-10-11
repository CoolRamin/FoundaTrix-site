# FoundaTrix Studio Website

Public source for the product website of **FoundaTrix Studio**, a Windows desktop program by
RamisoftSolutions for the analysis and design of rigid foundations of any shape: spread, combined,
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

## Screenshots and artwork

The product pictures are **real screenshots** of FoundaTrix Studio 1.120, taken on 2026-10-11 from
a fictional sample ("Area 200 Foundations": two vertical vessels, two exchangers, a four-bent pipe
rack, an L-shaped combined footing and an octagonal footing, every name made up). They live in
`src/images/screens/` as WebP and sit inside a `.shot` frame, whose bar stands in for the window's
own caption, so each capture is cropped below the program's caption row.

| File | Used on | What it shows |
|---|---|---|
| `studio-overview.webp` | Home (below the hero), Features | The whole site in X-ray: bearing pressure through the concrete, verdict badges, the rack's steel colours |
| `studio-modelling.webp` | Home | An octagonal footing drawn from the command line, a pedestal being placed on its snapped centre |
| `bearing-pressure.webp` | Home | From below: an L-shaped footing with its base partly lifted, beside the Results pane |
| `concrete-design.webp` | Home, Features | The Envelope pane and the Interaction pane's strength surface |
| `tables.webp` | Home | The Loads table floating over the model |
| `wizard.webp` | Home, Features | The vertical vessel wizard's anchorage page with its dimensioned drawings |
| `deformed-rack.webp`, `deformed-tee.webp` | Home, Features | The pipe rack on its deformed shape (x100) with the steel colours; one bent in elevation |
| `steel-design.webp` | Home, Features | The rack isolated, its members coloured by AISC 360-22 utilisation |
| `calc-report.webp` | Home, Features | Two report pages: the foundation plan and the wind derivation |
| `bim-export.webp` | Home, Features | The exported IFC in a third-party viewer (its branding cropped out) |

`src/images/assistant-connector.svg` is an illustration, not a screenshot: a generic assistant
conversation (deliberately not any one assistant's interface) creating a model through the connector,
with the tool names the endpoint really exposes. `src/images/hero-foundation.svg` (the hero's
illustration, a combined footing), `src/images/types/*.svg` (the five foundation types) and
`src/images/foundatrix-mark.svg` / `src/favicon.svg` (the program's own mark, converted from its
`Logo.xaml` and `Logo.Small.xaml`) are artwork.

When replacing a screenshot: fictional project, client, equipment and site names only (never a real
project's), a dark-theme window of about 1700 x 1075 or 1700 x 1280, cropped below the caption row,
saved as WebP at quality 84 to 86; then update the `<img>` `width`, `height` and `alt`.

## Values still to settle

| What | Where | Now |
|---|---|---|
| Download link (Microsoft Store) | `src/index.html`, `#download` section, and every "Download" button (`/#download`) | A "coming soon" Store button; replace with the listing URL and Microsoft's official badge |
| Privacy and terms URLs in the program and the Store listing | Since 2026-10-11 they point at this site's `/privacy/` and `/terms/`; the copies on ramisoftsolutions.com are no longer linked by the program | Settled |

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

The site is hosted on **Azure Static Web Apps** (Free plan): the app `swa-foundatrix-site` in the
resource group `rg-lateralpile`, region West US 2. Every push to `main` publishes `src/` through
`.github/workflows/deploy.yml`, which authenticates with the repository secret
`AZURE_STATIC_WEB_APPS_API_TOKEN` (the app's deployment token). Pull requests are not deployed.
`src/staticwebapp.config.json` sets trailing slashes, the 404 page and the security headers,
including a content security policy.

| Address | DNS at GoDaddy | Role |
|---|---|---|
| `https://www.foundatrix.com` | `CNAME www` to the app's `azurestaticapps.net` host | Primary (canonical) address |
| `https://foundatrix.com` | `A @` to the app's stable inbound IP, validated by a `TXT @` token | Redirects to `www` |
| `victorious-desert-07deff81e.4.azurestaticapps.net` | (Azure's own) | Redirects to `www` once `www` is the default domain |

The canonical links, `og:url` and `sitemap.xml` all name `https://www.foundatrix.com`. If the
deployment token is ever rotated in Azure, set the repository secret again.

## Contributing

Typo fixes and copy improvements are welcome by pull request; see [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT for the website's source and content (see [LICENSE](LICENSE)). The FoundaTrix Studio program
itself is separate, closed-source software under its own terms. "FoundaTrix Studio" and its mark
are not licensed for reuse by the MIT license.

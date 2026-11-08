# FoundaTrix Studio

**FoundaTrix Studio** is professional Windows software by RamisoftSolutions for the analysis and design of rigid
foundations of any shape: spread, combined, strapped and mat foundations on any outline, carrying any number of pedestals,
under columns, vessels, heat exchangers, substation equipment and pipe supports. It solves the bearing pressure under a
rigid base exactly, a partly lifted base included, checks overturning and sliding, and designs the concrete to ACI 318-19.
The analysis, the design and the calculation report are free, with no limit on model size or time and no account required.

**Latest version: 1.168 (November 7, 2026).** [Website](https://www.foundatrix.com/) ·
[Features](https://www.foundatrix.com/features/) · [What's new](https://www.foundatrix.com/whats-new/) ·
[Changelog](CHANGELOG.md) · [Microsoft Store](https://apps.microsoft.com/detail/9PN2N2M02389)

> This README describes the program as of its latest version. The website, https://www.foundatrix.com, is the complete and
> authoritative description of what the program does, with its limits stated on the features page. This repository holds
> the website's source and the program's public issue tracker; the program's own source is private.

## What FoundaTrix Studio does

- **Rigid foundations of any type and shape**: spread, combined, strapped and mat foundations, rectangular, circular,
  octagonal or irregular, with any number of pedestals, modelled in a 3D Studio with drafting precision or typed into
  spreadsheet-style tables beside the model.
- **Bearing pressure** under a rigid base for every allowable stress combination, a partly lifted base included, solved for
  the neutral axis that puts the pressure resultant where the load acts; **overturning and sliding**.
- **Loads**: service loads combined by ASCE 7-22 (strength and allowable stress, seismic included), or your own supplied
  combinations analysed as they are.
- **ACI 318-19 design**: one-way shear and flexure from a swept envelope, the four mats and their bars, two-way shear,
  pedestal axial force and moment on a biaxial strength surface, strap footings, and cast-in anchor rods to Chapter 17.
- **Wizards** (premium) that build a complete, loaded foundation from a questionnaire: vertical vessels, horizontal vessels
  and heat exchangers, substation equipment and pipe supports, each decision recorded with the clause behind it.
- **Steel stands and racks** (premium) analysed as 3D frames by the direct analysis method and designed to AISC 360-22,
  base plates to AISC Design Guide 1, with a member detail that works every check equation by equation.
- **Foundations on piles** (premium, with a PileTrix Studio subscription or trial): pile models copied from the job's
  PileTrix Studio analyses and the rigid cap analysed on its piles under every combination.
- **Loads from StruTrix Studio** (premium, with a StruTrix Studio subscription or trial): a StruTrix Studio structure saved
  in the same cloud job gives the model its loads, its supports' reactions read by load case or as its combinations,
  placing a footing at each support or loading the pedestals there, its latest saved version taken before every run.
- **The calculation report**: a typeset PDF printing every derivation symbolically and with your numbers substituted,
  beside its clause; free, the firm's name and logo on it premium.
- **Exchange** (premium): export to IFC 4.3, and to Revit as native elements through the included Revit add-in.
- **Cloud and AI** (free account): cloud jobs shared with PileTrix Studio and StruTrix Studio, version history, a recycle
  bin, and a connector through which your own AI assistant creates foundations and runs what-if analyses that only you
  apply.

## New in version 1.168

- File > Import > From StruTrix Studio: footing loads read from a StruTrix Studio structure saved in the same cloud job.
- With nothing selected, the view turns about the centre of the model, and a pan holds the point pressed on.
- The User's Manual rearranged in seventeen sections, with a pictured tutorial.

Every release's notes are in [CHANGELOG.md](CHANGELOG.md) and on the website's
[What's new](https://www.foundatrix.com/whats-new/) page.

## Common questions

- **Can FoundaTrix Studio read loads from a structural analysis?** Yes: since version 1.168 it reads a StruTrix Studio
  structure's support reactions from the same cloud job (premium, with a StruTrix Studio subscription or trial of your own).
- **Does it model the soil?** No. The bearing pressure is solved under a rigid base; the allowable bearing pressure and the
  other geotechnical inputs are taken as given. For a foundation on piles, the piles' own soil response comes from their
  PileTrix Studio analyses.
- **Is it free?** The modelling, the bearing pressure, stability and ACI 318-19 design, and the calculation report are free,
  with no limit on model size or time, no watermark added and no account. It is professional software for real projects,
  not a student or evaluation edition. Premium capabilities are a separate set, free to try.
- **Is a pile cap's concrete designed?** Not yet: a foundation on piles is analysed and its piles judged, and the cap's
  concrete design on the piles' reactions is the next version's.

## About this repository

This repository is the public source for the product website of FoundaTrix Studio, www.foundatrix.com. Its **Issues** are
also the public place to report a bug in the program or ask for a feature: see
[Reporting bugs and requesting features](#reporting-bugs-and-requesting-features).

**With every Store release**, update together: a new card on top of `src/whats-new/index.html`, the same notes on top of
[CHANGELOG.md](CHANGELOG.md), this README's "Latest version", "What FoundaTrix Studio does", "New in version" and "Common
questions", `src/llms.txt`, and the repository's GitHub description and topics where the headline features change. AI
search tools read this README as the program's description, so a feature missing here reads to them as a feature the
program lacks.

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
| `/whats-new/` | `src/whats-new/index.html` | Release notes: each Microsoft Store release, newest first, from the "What's new" text submitted with it |
| `/support/` | `src/support/index.html` | Where to report a bug, ask for a feature or write privately |
| `/privacy/` | `src/privacy/index.html` | Privacy policy |
| `/terms/` | `src/terms/index.html` | Terms of use, including the engineering disclaimer |
| (any 404) | `src/404.html` | Not-found page |
| `/llms.txt` | `src/llms.txt` | A plain-text summary of the program for AI tools (the llms.txt convention); keep it to what the pages say |

**What's new gets a new release card on top with every Store release**: the card's text is the "What's new" the
submission carried (checked against the program's manual), the `release--latest` class and the Latest badge move to it,
and its `release__meta` names the Store package's version (display version A.BCD is package A.B.CD.0).

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
| `deformed-rack-tiers.webp` | Home, Features | A three-tier, six-bent pipe rack on its deformed shape (x30) with the steel colours, captured from 1.121 on 2026-10-11 (the "Process unit pipe rack PR-100" sample): a 1500 x 1000 window, the workspace band below the ribbon only, the empty Command Line pane cropped off |
| `steel-design.webp` | Home, Features | The rack isolated, its members coloured by AISC 360-22 utilisation |
| `calc-report.webp` | Home, Features | Two report pages: the foundation plan and the wind derivation |
| `bim-export.webp` | Home, Features | The exported IFC in a third-party viewer (its branding cropped out) |
| `breaker-from-datasheet.webp` | Home `#assistant` | A dead-tank circuit breaker an AI assistant created from the manufacturer's outline drawing, then run at the desk: the stand on its deformed shape with steel colours over the bearing pressure (the owner's capture, 2026-10-20, program 1.147). The vendor's drawing itself is NOT published: it is the manufacturer's, and the caption describes it instead |

`src/images/assistant-connector.svg` is an illustration, not a screenshot: a generic assistant
conversation (deliberately not any one assistant's interface) creating a model through the connector,
with the tool names the endpoint really exposes. `src/images/assistant-whatif.svg` (2026-10-20, program 1.147) is
its companion: the same generic conversation running what-if versions of a footing on the engineer's computer, and the
proposal in the program's Assistant Requests pane with Apply and Decline, the desktop link's real tool names on it.
`src/images/pile-cap.svg` (the same day, program 1.127 and later) illustrates a foundation on piles: a cap on nine piles
coloured by their axial ratio, generated as an isometric drawing rather than captured; a screenshot of a real pile cap
from a fictional job can replace it. `src/images/hero-foundation.svg` (the hero's
illustration, a combined footing), `src/images/types/*.svg` (the six foundation types, `type-pilecap.svg` added
2026-10-20 in the same isometric style) and
`src/images/foundatrix-mark.svg` / `src/favicon.svg` (the program's own mark, converted from its
`Logo.xaml` and `Logo.Small.xaml`) are artwork.

When replacing a screenshot: fictional project, client, equipment and site names only (never a real
project's), a dark-theme window of about 1700 x 1075 or 1700 x 1280, cropped below the caption row,
saved as WebP at quality 84 to 86; then update the `<img>` `width`, `height` and `alt`.

## Values still to settle

| What | Where | Now |
|---|---|---|
| Download link (Microsoft Store) | `src/index.html`, `#download` section, and every "Download" button (`/#download`) | Settled 2026-10-11: the button links the Store listing, `https://apps.microsoft.com/detail/9PN2N2M02389` (Store ID 9PN2N2M02389), with the site's own Store-bag button rather than Microsoft's badge image, which the strict CSP (`img-src 'self'`) would need hosting locally |
| Privacy and terms URLs in the program and the Store listing | Since 2026-10-11 they point at this site's `/privacy/` and `/terms/`; the copies on ramisoftsolutions.com are no longer linked by the program | Settled |
| Free, with no limits, for real projects | Home: the description and `og:description`, the announce bar, the hero's assurances (No size limit), the free section (its heading and text, and two tiles: No limit on model size, Made for real projects), the Free plan; `/pricing/`: the description, `og:title`, the headline, the Free plan, three questions (model size, real projects, a catch), the closing; Features: its description; `src/llms.txt`; the JSON-LD on Home (SoftwareApplication) and `/pricing/` (FAQPage) | Stated on 2026-11-07 at the owner's word, as www.strutrix.com does. Each claim was checked in the program's source that day: nothing caps the number of footings, pedestals, loads or combinations, at any tier; the free part has no time limit (it is not a trial); the free report carries no tier marking, so the site says the free version adds no watermark (the report is stamped NOT A DESIGN when its results are not a design, an engineering marking unrelated to the plan, so never write "never watermarked"); the terms of use restrict no commercial use. No model size the program was developed or timed on is claimed: that number is StruTrix Studio's. The FAQ's JSON-LD is worked from the page's own questions: change a question, change the block. Never write "free to start" |
| The premium split | Home `#premium`, `#structure-link`, `#plans`; `/pricing/`; Features | The wizards, the steel design of stands and racks, the firm's name and logo on the report, IFC and Revit export and the job map; a foundation on piles (with PileTrix Studio's subscription or trial too) and loads from a StruTrix Studio structure (with StruTrix Studio's). The calculation report itself is free for everyone since program 1.148 (first in the Store with 1.161) |
| Loads from StruTrix Studio | Home `#structure-link`; Features `#structure-link`; `/pricing/` (the Pro plan and the comparison); `/whats-new/` (1.168) | Open to every engineer with premium since program 1.164, first in the Store with 1.168 (2026-11-07); described from the manual's section 6.5. No picture yet: a screenshot of the import from a fictional job could join the Home section |

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

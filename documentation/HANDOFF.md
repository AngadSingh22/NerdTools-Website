# NERD Tools FE Handoff

## Goal

Redesign a set of browser-saved/static HTML pages for the NERD Tools Foundation assessment flow so they feel:

- clinical but also child-friendly
- suitable for schools / therapists
- airy and easy to scan
- mobile-friendly as well as desktop-friendly
- reusable as a visual system for future pages

The user explicitly said the first visual pass looked bad and then chose a clearer reference direction.

## Final Design Direction Chosen

Reference stack selected by the user:

- Primary: `Clinical Product`
- Secondary: `Warm Education`
- Tertiary: `Editorial Calm` for spacing and typography

This replaced the earlier softer/glossier direction.

## User Preferences Captured

- Tone: clinical but child-friendly
- Audience: schools / therapists
- Typography: formal + friendly
- Density: airy and easy to scan
- Landing page priority: push users to login, with a short explanation and navigation help
- Dashboard priority: children and screening status first
- Visual treatment: subtle soft tones, not overwhelming
- Mobile support: important
- UI structure: clean cards / sections rather than crude tables
- Trust elements: all welcome, but validity, age range, and language support matter most
- Copy: preserve existing wording where possible, only minimal edits when needed for layout

## What Was Found Initially

The workspace was not a full app. It originally contained only two browser-saved HTML files and their asset folders:

- `NERD Tools Foundation.html`
- `NERD Tools Foundation_dashboard.html`
- `NERD Tools Foundation_files/`
- `NERD Tools Foundation_dashboard_files/`

There was no `package.json`, no framework, and no build system.

## Raw Site Downloads Collected

Public/guest-visible originals were downloaded directly from the live site and saved into:

- `site-downloads/index.original.html`
- `site-downloads/login.original.html`
- `site-downloads/dashboard.guest.original.html`
- `site-downloads/addchild.guest.original.html`
- `site-downloads/forgotpassword.original.html`
- `site-downloads/tnc.original.html`
- `site-downloads/form_style.original.css`
- `site-downloads/logo_ntf.original.png`
- `site-downloads/home1.2.original.png`

Important limitation:

- authenticated account-specific pages were not fetchable directly from the site without a logged-in browser session
- the logged-in dashboard view came from the user’s saved HTML snapshot
- the authenticated add-child page was not supplied as a saved logged-in page, so that page is a reconstruction based on the live form structure plus the logged-in dashboard context

## Files Created / Updated

Current themed pages in the root:

- `NERD Tools Foundation.html`
- `NERD Tools Foundation_dashboard.html`
- `NERD Tools Foundation_login.html`
- `NERD Tools Foundation_addchild.html`
- `NERD Tools Foundation_forgotpassword.html`
- `NERD Tools Foundation_terms.html`
- `shared-theme.css`

## Evolution of the Work

### Phase 1

Rebuilt the two original saved pages:

- landing page
- logged-in dashboard snapshot

Introduced:

- shared `shared-theme.css`
- mobile-first layouts
- dashboard cards and badges instead of crude tables

### Phase 2

Downloaded more public pages from the live site and created themed versions for:

- login
- add child
- forgot password
- terms and conditions

### Phase 3

User disliked the visual result. The design system was then reworked around the chosen references:

- flatter clinical shell
- more restrained controls
- calmer spacing
- stronger typography hierarchy
- less “card soup”
- less pill-heavy / overly rounded styling

Fonts were changed from:

- `Fraunces + Source Sans 3`

to:

- `Newsreader + Public Sans`

## Current Visual System

Implemented in `shared-theme.css`.

Characteristics:

- light clinical background with subtle grid texture
- flatter panels with restrained shadows
- quieter nav treatment
- stronger editorial headings
- more product-like controls and forms
- subdued sage / sky palette
- reduced visual clutter
- mobile stacking rules for forms, cards, and nav

## Current Page Status

### `NERD Tools Foundation.html`

Purpose:

- landing page

Status:

- themed and rebuilt
- includes trust/overview content
- pushes login and dashboard access

### `NERD Tools Foundation_dashboard.html`

Purpose:

- authenticated dashboard based on the user’s saved logged-in snapshot

Status:

- themed and rebuilt
- focuses on child record + screening status
- includes current saved data:
  - user: `Angad Ahuja`
  - licenses: `2`
  - children added: `1`
  - child: `Angad Singh Ahuja`
  - screening records from the snapshot

### `NERD Tools Foundation_login.html`

Purpose:

- themed login page using the live site form structure

Status:

- themed and rebuilt
- keeps live form action endpoint

### `NERD Tools Foundation_addchild.html`

Purpose:

- authenticated-style add child flow

Status:

- reconstructed, not from an authenticated saved page
- uses live add-child form structure
- nav and supporting content were adapted to match logged-in dashboard context

### `NERD Tools Foundation_forgotpassword.html`

Purpose:

- themed reset password page

Status:

- rebuilt from live public page structure

### `NERD Tools Foundation_terms.html`

Purpose:

- themed legal/terms page

Status:

- rebuilt from live public page structure
- terms content was reorganized into clearer sections, but not substantively changed

## Important Constraints / Caveats

- These are static HTML files, not a real app codebase.
- No browser-based visual verification was performed from within the environment.
- `xmllint` was not available locally when checked.
- This directory is not a git repository.
- The authenticated add-child page is inferred/reconstructed rather than sourced from a logged-in browser save.

## Best Next Step For The Next Agent

Open the current HTML pages in a browser locally and do a visual QA pass.

Specifically check:

- whether the new system is actually visually better, not just structurally cleaner
- mobile layout quality
- typography scale and spacing
- CTA hierarchy on the landing page
- whether the dashboard now feels like a serious product app
- whether the add-child page feels convincingly part of the authenticated flow

## High-Value Follow-Up Tasks

1. Do a visual refinement pass after actually viewing the rendered pages.
2. If the user can provide more authenticated browser-saved pages, convert those precisely.
3. Tighten consistency between:
   - dashboard
   - add child
   - login
   - terms
4. Decide whether to keep the current reference balance or push further toward:
   - more premium/minimal
   - warmer/softer
   - more enterprise/product-like

## If More Authenticated Pages Become Available

Most useful next browser-saved pages:

- authenticated add child page
- start screening page
- report screen / report view
- any child detail / screening continuation page

Those would let the next agent make the flow materially more consistent.

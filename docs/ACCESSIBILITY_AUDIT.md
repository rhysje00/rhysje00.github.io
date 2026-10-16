# Accessibility audit — 17 October 2026

Audited the locally built personal site: About, Publications, Research,
Repositories, and CV. The main matrix covers Chromium at 1366 and 390 CSS pixels
in both light and dark modes (20 page/viewport/theme combinations). Additional
reflow checks used 683 and 320 CSS pixels. The 683-pixel viewport approximates
the layout space at 200% zoom on a 1366-pixel desktop; native browser zoom and
screen-reader testing remain outstanding.

## Applied colour scheme

Warm ivory and deep teal in light mode; green charcoal and sea-glass in dark mode.
Both explicit theme selection and system theme preference remain available.

| Role              | Light     | Dark      |
| ----------------- | --------- | --------- |
| Page              | `#FAF7F2` | `#142321` |
| Cards and code    | `#F0EBE3` | `#1E3330` |
| Body text         | `#202D2B` | `#E4EDE9` |
| Secondary text    | `#52635F` | `#ADBFBA` |
| Links and accents | `#006B60` | `#8EDBCD` |
| Hover             | `#00554C` | `#B8F0E5` |

Calculated contrast against each mode's page background:

| Pair           | Light   | Dark    |
| -------------- | ------- | ------- |
| Body text      | 13.35:1 | 13.61:1 |
| Secondary text | 5.94:1  | 8.47:1  |
| Links          | 6.01:1  | 10.19:1 |

Filled publication badges use white text on deep teal (6.42:1); existing inline
venue backgrounds retain white text. Dark-mode links on card backgrounds measure
8.38:1. These pairwise calculations do not certify the whole website.

The text thresholds are 4.5:1 for ordinary text and 3:1 for large text.
See [W3C contrast guidance](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html).
Links also need a cue that does not depend on colour alone; see
[W3C use-of-colour guidance](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html).

## Findings

### 1. Dark-mode headings have insufficient contrast — high, fixed

- **Evidence:** Publications year headings and Research category headings used
  `#595959` on `#1C1C1D`: 2.43:1 at 32px, below 3:1. Reproduced at both main widths.
  Selectors: `.publications h2.bibliography`, `.projects h2.category`.
- **User/accessibility impact:** Section labels are hard to distinguish; WCAG 1.4.3 failure.
- **Recommendation and implementation:** Use the mode's secondary-text token.
  Applied in `assets/css/main.scss`, the existing personal-site stylesheet override.

### 2. Dark-mode publication badges have insufficient contrast — high, fixed

- **Evidence:** White 12px links on the inherited cyan `#2698BA` measured 3.34:1.
  One affected badge on About and six on Publications, at each main width.
- **User/accessibility impact:** Journal abbreviations are difficult to read; WCAG 1.4.3 failure.
- **Recommendation and implementation:** Give filled badges a separate dark teal
  background and white foreground. Applied in `assets/css/main.scss` without
  replacing existing venue colours in the bibliography data.

### 3. Some prose/footer links rely on colour alone — high, fixed

- **Evidence:** Dark-mode links inside About's `dd` and the footer lacked an
  underline and had only 2.72:1 contrast against neighbouring text. Axe reported
  eight affected links on About and three on each other sampled page.
- **User/accessibility impact:** Readers may not recognise links; WCAG 1.4.1 failure.
- **Recommendation and implementation:** Extend permanent underlines to definition
  descriptions, list items, and footer links. Applied in `assets/css/main.scss`.

### 4. Narrow layouts overflow — medium, outstanding

- **Evidence:** At 320px, CV document width was 350px and Repositories was 391px.
  CV's contact table and Repositories' trophy image extend beyond the viewport.
  Repositories also overflowed in a 390px baseline capture. No document overflow
  was observed on these pages at 683px.
- **User/accessibility impact:** Readers on narrow screens or at high zoom may
  need horizontal scrolling. Treat this as a reflow issue requiring follow-up;
  check table exceptions and image containment before assigning WCAG conformance.
- **Recommendation:** Allow contact values to wrap and constrain repository-card
  images to their containers; avoid clipping content to conceal overflow.
- **Implementation scope:** CV table styling in `al_folio_cv`; repository card
  templates/styling in `al_folio_core`. Personal-site overrides are supported;
  no new runtime override was added during this colour change.

### 5. Portrait alternative text is a filename — medium, outstanding

- **Evidence:** About renders `<img alt="Evans.jpg">`.
- **User/accessibility impact:** The alternative text does not identify the person
  pictured; assistive-technology users receive an unhelpful filename.
- **Recommendation:** Use "Rhys J. Evans" as the portrait's alternative text,
  passed through the image renderer's supported interface.
- **Implementation scope:** Profile image rendering in the existing
  `_layouts/about.liquid` override; inspect the `al_img_tools` interface first.

### 6. No skip-to-content link — medium, outstanding

- **Evidence:** Keyboard traversal on About begins with the navigation links,
  search and theme controls, then reaches the body. No skip link was found on
  any sampled page. A main landmark is present.
- **User/accessibility impact:** Keyboard users repeatedly traverse the header.
  Absence of a skip link alone does not establish a WCAG 2.4.1 failure because
  other bypass mechanisms, including landmarks, must be considered.
- **Recommendation:** Add a first-focusable skip link and a focusable main target.
- **Implementation scope:** Shared header/layout in `al_folio_core`, or a tracked
  personal-site override. Retain the existing main landmark.

## Verification and limits

- Final built site: **zero axe violations and zero incomplete results across all
  20 page/viewport/theme runs**, with the expected computed palette in each mode.
  This result covers the sampled default page states, not every interactive state.
- Baseline: the five light-mode axe scans found no violations. Explicit dark-mode
  testing found the contrast and link-identification problems above. The stock
  audit helper samples light mode only, so its clean report was insufficient.
- The colour change also adds a 3px visible keyboard focus outline, offset by 4px.
- Inspected desktop/mobile screenshots in both modes, headings and landmarks,
  initial keyboard order, and mobile navigation. The menu exposes its expanded
  state and opens with Enter. Automated checks cannot assess alternative-text
  quality, reading experience, or all interaction states.
- This is a sampled audit, not WCAG certification. It excludes downloadable PDFs,
  every project detail page, assistive-technology testing, and exhaustive search
  dialog testing. Image-based third-party widgets need separate visual review.
- The final Jekyll build passes. Browser tooling's bundled Node runtime was added
  to the command PATH because this shell initially had no JavaScript runtime.
- The starter style-contract check rejects existing `_includes` and `_layouts`.
  Both were already tracked on the base branch; this change adds neither. The
  personal-site exception is documented in `docs/ARCHITECTURE.md`.
- Full Prettier checking reports an existing duplicate `vorobev` key in
  `_data/coauthors.yml` and formatting warnings in unrelated content. Those files
  were not changed. Changed-file formatting and `git diff --check` are checked
  separately.
- The stylesheet override was audited and its acknowledgement updated in
  `.al-folio-overrides.yml`. The audit also reports a pre-existing changed About
  override; its acknowledgement was left untouched.

Temporary evidence is under `/tmp/rhys-audit/`: `details.json` (baseline),
`applied-results.json` (final matrix), `reflow.json`, `contrast.json`, screenshots,
and formatting logs. The final site is served at `http://127.0.0.1:8907/`.
The user approved its appearance in conversation; no commit, push, or deployment
was requested or performed.

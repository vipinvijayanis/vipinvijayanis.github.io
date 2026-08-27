# Portfolio site design principles

This document is the source of truth for future pages on this portfolio. Read it before changing an existing page or creating a new one.

The goal is not to make every page identical. The goal is to make every page feel like it belongs to the same clear, restrained portfolio.

## 1. Core philosophy

### Less is more

- Start with the minimum content needed to understand the page.
- Remove decorative labels, repeated explanations and duplicate calls to action.
- Prefer one strong headline over a headline plus a generic subheader.
- Let spacing, type and real work create the visual interest.
- Add an element only when it improves comprehension, credibility or navigation.

### Evidence over adjectives

- Show working products, real outcomes and specific decisions.
- Use concrete numbers where they are meaningful and defensible.
- Avoid vague phrases such as “innovative,” “world-class,” “passionate” or “results-driven.”
- Keep claims factual and consistent with the résumé and case-study source material.

### Working examples over presentation theatre

- Portfolio tiles should open the actual project or case study.
- The entire project tile is the link. Do not add redundant “Open demo” or “Read case study” buttons inside it.
- Use real screenshots, recordings and interactive demonstrations when they materially improve the story.
- Do not add ornamental mockups when the working product is available.

## 2. Visual system

All portfolio pages use the same base tokens:

```css
:root {
  --black: #080808;
  --panel: #111111;
  --white: #f5f5f0;
  --muted: #999994;
  --line: #292929;
  --accent: #ff4f5e;
  --max: 1240px;
}
```

### Colour

- Use `--black` as the page background.
- Use `--panel` sparingly for grouped content such as project tiles, metrics or media stages.
- Use `--white` for primary text and `--muted` for supporting text.
- Use `--line` for quiet structure instead of shadows or heavy containers.
- Use `--accent` for one or two high-value moments: the primary word in a hero, a key state, or the primary contact action.
- Company logos retain their official brand colours.
- Do not introduce additional page-level accent colours without a clear semantic need.

### Typography

- Use the self-hosted Geist variable font for portfolio and narrative case-study pages, with the system sans-serif stack as fallback.
- Keep the font asset inside `assets/fonts/` so GitHub Pages does not depend on an external font service.
- Headlines are large, direct and tightly spaced.
- Body copy is readable, restrained and normally no wider than 720px.
- Use uppercase, letter-spaced labels only for genuine orientation such as “Product case study” or “The problem.”
- Do not use small labels to repeat information already conveyed by a title.

Recommended headline treatment:

```css
font-weight: 650–700;
line-height: 0.9–1;
letter-spacing: -0.05em to -0.07em;
```

### Layout

- Maximum content width: `1240px`.
- Desktop page gutter: `24px` on each side; mobile gutter: `14px`.
- Use generous vertical spacing and thin dividers to separate ideas.
- Prefer one- or two-column layouts. Avoid dense dashboards on narrative pages.
- Cards should be flat: one-pixel border, no rounded corners, no ornamental shadow.
- Responsive layouts must collapse cleanly to one column.

## 3. Shared page anatomy

### Header

- Omit a repeated name or wordmark and right-align only the essential links—Work, Résumé and Contact.
- Use the same height, typography and border treatment across pages.
- Project pages should use relative links so they work locally and on GitHub Pages.

### Hero

- Use one short orientation label.
- Use one strong headline.
- Supporting copy should normally be one or two concise sentences.
- Keep role, focus areas and supporting profile copy together in one left-aligned hierarchy.
- A portrait may anchor the opposite side when it is monochrome, restrained and secondary to the headline. Align its lower edge with the final supporting line and fade it into the background rather than placing it inside a visible frame.
- Avoid pill collections, multiple hero buttons and repeated project metadata.
- One accent-coloured word or phrase is enough.

### Company proof

- Show company logos prominently and give them equal visual weight.
- Use official assets with sufficient contrast.
- Do not imply endorsement, partnership or sponsorship. The context is employment history.

### Project tiles

- Each tile contains the project title only unless an extra line is essential to distinguish two similar projects.
- The complete tile is clickable.
- A tile may use one topic-specific image when it makes the work easier to understand at a glance.
- Keep imagery secondary to typography: use a strong black overlay, preserve clear title contrast and avoid generic stock photography.
- Use a subtle border change or small movement for hover feedback.
- Do not add category ribbons, descriptions and separate calls to action by default.

### Case-study sections

- Structure the story around a small number of meaningful beats, such as outcome, product, problem and build.
- Preserve substantive evidence while simplifying its presentation.
- Use metrics only once; do not repeat the same numbers in the hero and later sections.
- Prefer a simple list or timeline to a collection of decorative process cards.
- End with one clear next action or adjacent project.

### Contact and footer

- Use email as the primary contact action.
- Résumé and LinkedIn are secondary actions.
- Centre the closing statement and its compact action group as one composition.
- Keep the footer compact.
- Do not repeat the full navigation or biography in the footer.

## 4. Writing rules

- Lead with the point.
- Use short sentences and concrete nouns.
- Remove throat-clearing phrases such as “This is an example of” or “I am passionate about.”
- Prefer active voice: “I planned and built” instead of “The solution was planned and built.”
- Explain specialist terms when an external reader may not know them.
- Keep headings specific. “Remove the detour” is stronger than “The customer problem.”
- Use Australian English consistently unless quoting a product or market term.
- Preserve material nuance; concise does not mean incomplete or misleading.

## 5. Technical principles

- Prefer portable static HTML and CSS for portfolio and case-study pages.
- Add JavaScript only when the page has a real interaction that HTML and CSS cannot provide.
- Keep each project in its own folder with an `index.html` so it has a clean URL.
- Keep media beside the page that uses it, or in a clearly named local asset folder.
- Do not embed large images, videos or datasets into HTML. Reference separate repository files.
- Use relative internal URLs.
- Give every meaningful image an accurate `alt` attribute.
- Give video a poster, controls, `playsinline` and an accessible label.
- Provide visible keyboard focus states.
- Respect `prefers-reduced-motion`.
- Make the mobile experience intentional, not merely scaled down.

## 6. Repository structure

```text
/
├── index.html                    # Portfolio landing page
├── SITE-DESIGN-PRINCIPLES.md     # This source of truth
├── assets/
│   └── logos/
├── resume/
│   └── index.html
├── checkout-funnel-demo/
│   ├── index.html
│   └── data/
└── promo-code-demo/
    ├── index.html
    ├── promo-code-checkout-recording-poster.jpg
    └── promo-code-checkout-recording.mp4
```

## 7. New-page checklist

Before considering a page complete, confirm:

- The page has one clear purpose.
- The headline communicates that purpose without a generic subheader.
- Supporting copy is as short as it can be without losing meaning.
- The black, panel, white, muted, line and coral tokens match this document.
- Navigation matches the rest of the portfolio.
- Repeated metrics, labels and calls to action have been removed.
- Every tile or card has a reason to exist.
- Internal links work from the page’s deployed folder.
- Images, video and data are separate files rather than embedded payloads.
- The page works at desktop and mobile widths.
- Keyboard focus is visible and reduced-motion preferences are respected.
- The root page, résumé and both existing demos still load.
- Changes have been reviewed locally before any push to `main`.

## 8. Decision rule for future agents

When uncertain, choose the simpler version. Preserve the evidence, remove the presentation clutter.

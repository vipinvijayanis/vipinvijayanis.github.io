# Repository working agreement

These instructions apply to the entire repository. Read this file and `SITE-DESIGN-PRINCIPLES.md` before changing any page.

## Purpose

This repository is Vipin Vijayan's static portfolio, published through GitHub Pages. It has four public surfaces:

- `/` — the portfolio landing page.
- `/resume/` — the HTML résumé.
- `/checkout-funnel-demo/` — the checkout conversion dashboard.
- `/promo-code-demo/` — the promo-code case study.

Preserve all four routes and their relative internal links.

## Sources of truth

- `SITE-DESIGN-PRINCIPLES.md` defines the visual system, content philosophy, page anatomy and technical standards.
- The current page copy and project evidence are authoritative. Do not invent employers, metrics, outcomes or product claims.
- Repository assets are authoritative for logos, imagery, video and fonts. Prefer them over new dependencies or remote assets.
- `main` is the public GitHub Pages branch.

If instructions conflict, protect factual accuracy and working routes first, then choose the simpler presentation.

## Product and design rules

- Less is more. Remove repetition before adding another element.
- Use the established black, white, muted, line and hot-coral colour tokens.
- Use the self-hosted Geist variable font with the existing system fallback stack.
- Keep layouts flat and restrained: square corners, thin dividers, no ornamental shadows or decorative containers.
- Use large direct headlines and concise supporting copy.
- Keep the root page focused on product leadership, regulated consumer-product launches and hands-on AI work.
- The root page does not need a standalone navigation bar. Keep Résumé and LinkedIn as lightweight utility links.
- Company logos should remain unboxed, left-grouped and secondary to the profile headline.
- Project tiles are fully clickable. Keep their imagery dark enough for accessible title contrast.
- Factual live-status labels are allowed when they add evidence. Do not add decorative category labels.
- Frame the final contact section as a hiring conversation, not a freelance-services pitch.
- Keep the promo-code case study visually aligned with the root page unless its narrative requires a specific variation.

## Content rules

- Lead with the material fact.
- Use short sentences, concrete nouns and Australian English.
- Prefer evidence over adjectives.
- Do not repeat the same metric or message in multiple sections.
- Do not turn the landing page into a résumé transcript.
- Do not change claims such as customer reach, live status or employment context without evidence or explicit direction from Vipin.
- Preserve the distinction between the live internal dashboard and the live customer-facing promo-code feature.

## Technical rules

- Prefer portable static HTML and CSS. Add JavaScript only for real interaction needs.
- Keep each public page in its existing folder with an `index.html`.
- Use relative internal URLs so the site works locally and on GitHub Pages.
- Keep large media and datasets as separate files; never embed them into HTML.
- Reuse local fonts and assets. Do not add a framework, build step or package manager for a small page change.
- Maintain accurate `alt` text, keyboard focus states, mobile layouts and `prefers-reduced-motion` support.
- Avoid model-authored SVG illustrations. Preserve official company-logo assets.
- Make task-relevant edits only. Do not overwrite unrelated user work.

## Working process

1. Read the relevant page and `SITE-DESIGN-PRINCIPLES.md` before editing.
2. Check the working tree and preserve unrelated changes.
3. Implement the smallest coherent change.
4. Preview locally with a static server, normally at `http://127.0.0.1:8765/`.
5. Validate `index.html`, `/resume/`, `/checkout-funnel-demo/` and `/promo-code-demo/` when shared structure or navigation changes.
6. Run `git diff --check` and inspect the final diff before committing.
7. Update `SITE-DESIGN-PRINCIPLES.md` when a durable design decision changes.

Do not perform screenshot-based or interactive browser QA unless Vipin requests it. A lightweight local response check is sufficient for ordinary copy and spacing changes.

## Git and publishing rules

- Obtain fresh explicit approval before every push, deployment, force-push, rebase, deletion or other shared/irreversible action.
- Synchronise with the latest remote `main` before publishing and preserve remote work.
- Never force-push this repository.
- Use a concise commit message that describes the user-visible result.
- After pushing, verify that the remote commit exists and report whether GitHub Pages may still be propagating.

## Completion checklist

- The requested change is visible and concise.
- The root, résumé and both demos still load.
- Internal links and local media paths work.
- Desktop and mobile CSS remain intentional.
- Accessibility behaviour is preserved.
- Design decisions remain consistent with `SITE-DESIGN-PRINCIPLES.md`.
- Nothing was pushed without fresh approval.

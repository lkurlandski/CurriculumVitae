# CV repository

Luke's academic CV: `cv.tex` (layout, hand-written sections) + `publications.bib` (papers and posters), built with `./make.sh`.

## Purpose

- `cv.tex` is a **long-term master record** of experience and accomplishments. Do not cut content just to save space; page count is not a constraint for this version.
- When a page-limited version is needed (e.g., a 2-page resume), comment out entries or sections (`%` or `\iffalse ... \fi`) rather than deleting them, so the record stays in the source.
- Primary audience: industry research labs at the intersection of machine learning and security (research-scientist roles with an emphasis on research and publishing). Order and phrase content for that reader: research and publications first.
- Before removing anything from the record, run it by Luke first.

## Conventions

- **Publications and posters live in `publications.bib`**, selected by `keywords`:
  - `conference`, `journal` → "Conference & Journal Papers"
  - `workshop` → "Workshop Papers"
  - `underreview` → "Under Review" (`@unpublished`, `note = {Under review}`, no venue named)
  - `poster` → "Posters & Talks" (`@misc`, venue in `howpublished`)
  - `minortalk` → internal/coursework talks (e.g., RPA, capstone); printed only with `\extrastrue`
- **Research statement** is modular: variants are defined as macros near the top of `cv.tex` (e.g., `\statementGeneral`) and `\researchstatement` selects one. Add a variant to tailor the CV for a role rather than editing the general one.
- **`\ifextras` toggle** (set near the top of `cv.tex`, default `\extrasfalse`): hides content kept for the record but judged to weaken a research-lab CV (the `minortalk` entries and the small-projects section). Use `\extrastrue` for a complete or engineering-leaning version.
- When a paper is accepted, change it from `@unpublished`/`underreview` to `@inproceedings`/`@article` with the right keyword and venue.
- Never list a venue for a paper that is only under review.
- **Award dollar amounts** are recorded as `%` comments next to each entry in `cv.tex`. Show an amount in the rendered CV only for grants raised through a proposal Luke wrote (e.g., the AI Seed Fund); leave amounts off named fellowships and prizes.
- Don't retroactively rename awards (e.g., the TCNJ merit scholarship was unnamed when awarded, so it is not listed as the "Presidential Scholarship").
- Use job titles that match the actual arrangement: "Undergraduate Researcher" for unpaid, for-credit work; "Research Assistant" only for funded positions.

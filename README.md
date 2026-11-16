# Claude Skills

## paper-deep-read-slides

Turns an academic paper (PDF) into a paragraph-by-paragraph, bilingual close-reading slide deck:

- Every paragraph: English original + translation + commentary; long paragraphs are split at complete units of meaning
- Every figure: annotated directly on the image (shaded regions, arrows, numbered markers) with step-by-step "how to read this figure" notes
- At the end: a synthesis of the whole paper, the causal chain, a claims-to-evidence table, background, critical reading, and a key-numbers cheat sheet
- After publishing, supplementary explainer slides can be added in response to comments

### Usage

Put the `paper-deep-read-slides/` folder into Claude's skills directory (or upload the skill in Claude), then upload a paper PDF and ask for a close reading as slides.

### Files

- `paper-deep-read-slides/SKILL.md`: the skill instructions (workflow, slide types, figure-annotation method, checks, and iteration rules)
- `paper-deep-read-slides/figure-guides/`: a library of reading guides for figures common in electrochemistry / battery papers, one file per figure type:
  CV/LSV, RDE/Levich/K–L, Tafel, EIS/DRT, XPS, XRD (including 2D-XRD and texture), SEM, plating/stripping Coulombic efficiency, full-cell performance.
  Each guide covers: what it measures, axes, reading steps, a feature → meaning table, annotation suggestions, common pitfalls, and a case library.
  After reading a new paper, append what you learned to the matching guide's case library; create guides for new figure types from `_TEMPLATE.md`.

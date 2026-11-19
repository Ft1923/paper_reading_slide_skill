---
name: paper-deep-read-slides
description: Turn an academic paper PDF into a paragraph-by-paragraph bilingual close-reading slide deck — original + translation + commentary, annotated figures with reading steps, and a full-paper synthesis with background. Use when a user uploads a paper and asks for a close reading, explanation, or slides.
---

# Paper close-reading slides (bilingual + annotated figures + synthesis)

Goal: with this deck in hand, the reader can understand the paper paragraph by paragraph without opening the original, understand every figure, and know what story the whole paper tells and where it sits in its field.

## 0. Deliverable
- Default to a Slides-type presentation (exportable to .pptx / PDF). Use the pptx skill only when the user explicitly asks for a .pptx file.
- 16:9, 1920×1080; all text ≥ 24px.
- Language: commentary and translation in the user's language (e.g. Chinese); the original text stays in English.

## 1. Read the paper (finish reading before building)
0. Get the Supplementary Information (SI PDF, and the Source Data file if there is one) before you start. If the user only gave the main text, ask for the SI or fetch it from the publisher page.
1. `pdfinfo` for the page count; skim the whole paper once with `pdftotext -layout`.
2. For two-column papers, **extract column by column** (`pdftotext -x -y -W -H` on the left and right columns), otherwise paragraphs interleave. Reassemble paragraphs in the correct order.
3. Render every page with `pdftoppm -r 200` and look at each one: locate every figure, table, scheme, and equation; watch for equations missing from the PDF (if any, supply the standard form and say so on the slide).
4. Outline the paper: abstract, each introduction paragraph, each results subsection (with subheadings), conclusions; one-sentence claim per paragraph; each figure's panels and the claim each one supports.

## 2. Splitting rules
- Follow the original paragraph order, one paragraph per slide.
- If a paragraph is too long (English > ~180 words, or the translation does not fit), **split at complete units of meaning** into 2–3 slides, with a header like "Paragraph n · 1/2". Split at turns in the argument (observation → explanation, method → conclusion), never mid-sentence.
- Remove citation superscripts; convert `<sup>/<sub>` to Unicode super/subscripts (write ^() / _ forms when no Unicode character exists).

## 3. Slide types (in order)
1. **Cover**: journal / year / pages, English title, translated title, authors and affiliations, three tags (paragraph-by-paragraph / annotated figures / synthesis).
2. **One-page overview**: three columns — problem / finding / solution — plus a note on how to use the deck.
3. **Glossary, 1–2 slides**: the 6–12 concepts needed to read this paper (materials, phenomena, methods), each in 1–2 plain-language sentences.
4. **Section dividers**: dark background, number + section name + one sentence on "what question this section answers".
5. **Paragraph slides** (the bulk):
   - Header: section pill tag + "Paragraph n · x/y";
   - Title: one sentence stating the paragraph's **claim** (not an empty "Paragraph 3"); get the causality right;
   - Left column: English original (serif); right column: translation (key conclusions bold and colored);
   - Bottom "Commentary" bar: analogies, why it matters, links to what comes before and after, the authors' hedges ("tentatively", etc.).
   - When the right column has empty space, add a "reference box" there (equation, chain of reasoning, definition).
   - **Figures follow the paragraph that cites them.** The slide right after a paragraph shows the figure(s) it cites, in citation order, with reading steps written for *that paragraph's* claim; never batch a section's figures at its end. A figure cited by several paragraphs gets one slide after each, each highlighting the part that paragraph uses (explain the axes the first time only). Equation slides go after the figure slides. Check the "paragraph → next slide" mapping with a script.
   - **Supplementary figures too**: when a paragraph's argument rests on Supplementary Figs./Tables that the main figures do not show, put those right after it as well, under the same rules. Figures mentioned only in passing can be skipped.
   - **"Find the data in the SI and analyse it"**: pull the authors' Source Data and recompute instead of restating the claim. Prefer ratios within one spectrum/sample over absolute intensities, check replicate consistency, and do an order-of-magnitude balance (e.g. monolayer capacity vs bulk change). Close with a table: author's claim / what the data show / verdict.
6. **Equation slides**: a dark equation bar (the equation + one line per symbol/trend) + bilingual text + commentary.
   - **Every displayed formula is typeset from LaTeX** — on equation slides, explainers and supplementary sections. Slides cannot render LaTeX, so convert it to SVG with MathJax (`mathjax-full`, `fontCache: 'none'`; light glyphs on dark bars, dark on light), upload it and place it with `<img>`. Symbols inside self-drawn schematics use matplotlib mathtext. Formulas in comment replies are written as `$...$`. Inline symbols in running text may stay as Unicode (section 2).
7. **Figure slides**: cover every panel. Choose the layout by aspect ratio: single image on the left + steps on the right; two or three images in a row + 2×2 steps below. Fixed content:
   - "How to read it" in 4 steps (what the axes are → what each line/color means → where the key features are → which sentence in the text it supports);
   - a dark "Takeaway" bar with one sentence.
8. **Full-paper synthesis (8–10 slides)**:
   - one-sentence thesis (full-bleed accent-color slide);
   - causal-chain diagram (two contrasting pathways in arrow boxes);
   - claim → evidence → source table;
   - core concept comparison table (e.g. "classical theory vs this paper");
   - background, 2 slides (state of the field and its pain points; timeline of the theory);
   - experimental design worth learning from;
   - critical reading (the authors' own caveats, data points the text does not discuss, methodological questions);
   - key-numbers cheat sheet;
   - the paper retold in three sentences (closing slide).

## 4. Figure annotation ("drawing on the figures")
0. **Check the guide library first**: `figure-guides/` has one reading guide per figure type (CV/LSV, RDE/Levich, Tafel, EIS/DRT, XPS, XRD, SEM, plating Coulombic efficiency, full cell). Before writing the reading steps, drawing annotations, or raising questions, open the matching file and consult its case library. For a figure type not in the library, create a new guide from `figure-guides/_TEMPLATE.md`. After finishing a paper, append the new experience to the matching guide's case library.
1. Render figure pages with `pdftoppm -r 300` and crop each panel (estimate coordinates on the 200 dpi render, then convert). **Crops must be complete**: keep the panel letter, every tick label, every axis title (including a right-hand second axis), colour bars and legends.
2. **Positioning trick**: overlay a numbered 10×10 grid on a copy of each cropped panel and read the grid image to get relative coordinates (0–1) for annotations; then draw on the clean image.
3. Draw with PIL: semi-transparent shaded regions, arrows, dashed boxes / ellipses, numbered circles, bordered text labels.
   - Fonts: Noto Sans CJK for CJK text; fall back per character to DejaVu Sans for glyphs the CJK font lacks (super/subscript digits, ⁻, ₀, etc.), otherwise they render as boxes.
   - Do not cover data curves with labels; if there is no room, pad the image (top/bottom/right) and write there.
   - Use a fixed set of 4–5 colors, consistent with the colors used for regions/pathways in the commentary.
4. Assemble a contact sheet of all annotated panels and check for overlaps, misplacements, and labels running off the edge. Also scan a ~3 px border of every raw crop for dark pixels and inspect each edge that touches content; if an axis label is cut, widen the crop and rescale the 0–1 annotation coordinates. If the source figure itself is clipped, say so on the slide.
5. Upload as assets and reference them in slides by the returned `/_blob/<id>`.

## 5. Visual style
- One shared CSS: a dark color (e.g. #14213D), two light backgrounds (paragraph slides / figure slides), one accent (e.g. #C4561F), one secondary (e.g. #1F6F8B).
- Fonts: Noto Sans SC for Chinese body text, Noto Serif SC for Chinese headings, EB Garamond for the English original.
- A fixed type scale of 4–5 sizes; page number and citation as a 24px footer.
- Generate slides with a script (content as structured data: paragraph / figure / custom slides) so one change applies everywhere.

## 6. Checks (required before publishing)
- Render every slide locally with a headless browser and check by script: content bottom beyond ~1000px, and cards with `scrollHeight > clientHeight` (text overflow).
- Spot-check screenshots of the cover, long paragraph slides, each figure layout, and the synthesis slides.
- On overflow: tighten wording → shrink single-image height → split the slide. Never drop text below 24px.
- Verify every number, potential, and unit against the original; keep the authors' hedges ("tentatively", "qualitative").

## 7. Follow-up questions after publishing (comment-driven iteration)
Users often ask about basic concepts in comments on a slide. **By default every answer goes into the deck as well as the comment thread**; only when the user says "just answer" (只回答) do you reply in the thread alone and leave the deck unchanged. Handle them as follows:
- **Concept questions** ("what is X, how is it measured"): insert a supplementary explainer slide after that slide, with a schematic drawn in matplotlib or PIL (apparatus, layered concentration profile, equation curves, energy-level diagram), "how to read it" steps, and a one-line takeaway. Cover the definition, units, physical meaning, how to read it, what it reveals, when it applies and its limits, and — for a method — how to do it yourself (steps and parameters). Put large background concepts, or anything the user asks to have "at the end", in a "supplementary section" (divider + several slides) at the end of the deck.
- **"How was this figure obtained"**: the slide right after that figure (method, equation, caveats).
- **"Draw it" / "write it here"**: "draw a picture" means a self-drawn schematic, not prose; "draw it on this figure" or "write it in the empty space" means changing that same slide (annotation, or a reference box in the empty right column), not adding a new one.
- **Challenge questions**: answer directly and honestly (what the authors did, what they did not prove, what experiment would settle it) and add the analysis to the deck after that slide or to the critical-reading slide.
- If you find that one of your own titles or commentaries had the causality wrong, fix it and say so in the reply.
- Each time, re-read the file you will change to confirm its version and publish only the changed files; reply in the comment thread and keep the session message to one line.

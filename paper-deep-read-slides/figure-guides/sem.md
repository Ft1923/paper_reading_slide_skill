# Reading guide: SEM morphology images (including EDX)

## What this figure measures
An electron beam scans the sample surface to show morphology and the size and arrangement of particles / grains. In battery papers it is mainly used to compare metal deposits or SEI morphology across conditions. EDX gives elemental distribution.

## Axes and common forms
- No axes: **read the scale bar** (the bar at the lower left / right).
- Common layouts: one row per condition, magnifying from left to right (e.g. 10 μm → 2 μm → 200 nm); or one column of top views + one column of cross sections.

## Reading steps
1. Read every scale bar first to know the field of view and the magnification relationship within a row.
2. Low magnification for the overall picture: uniform coverage? flat or undulating? cracks / holes?
3. High magnification for the building blocks: platelets / needles / particles / dendrites; platelet orientation (lying flat or standing up); dense or porous.
4. Compare across conditions at the same magnification, row by row, to find the trend.
5. With EDX, use the element maps to tell metal from by-products (S- and O-rich regions are often sulfates / oxides).

## Key features → meaning (metal anodes)
| Feature in the figure | Physical meaning |
|---|---|
| Hexagonal platelets lying flat, stacked layer on layer | (002)-oriented deposit, dense, good reversibility |
| Platelets standing up, randomly oriented, porous | Mossy deposit, high surface area, more side reactions |
| Sharp needles / branches | Dendrites, may pierce the separator |
| Surface covered by fine nanosheets | SEI / by-products (e.g. ZHS) |
| Bright/dark contrast differences | Differences in composition or conductivity (metal is bright; insulating by-products charge easily) |

## Annotation suggestions
- Label the condition on the left of each row (potential, current, cycle number) and summarize the morphology in one sentence on the right.
- On high-magnification images, separate regions with dashed lines (e.g. "left: Zn / right: needle-like SEI").
- Point to representative features with arrows (upright platelets, flat platelets, holes).

## Common pitfalls / questions to ask
- Representativeness: does one image represent the whole electrode? Are several regions or a low-magnification overview shown?
- Sample preparation: disassembly, washing, drying, and air exposure can change morphology or dissolve by-products.
- Top views alone do not show thickness or porosity; cross sections are better.
- "Denser" and "flatter" are qualitative; ask whether roughness or porosity was quantified.

## Case library

### Baffour et al. 2026, JACS — Figure 4 (morphology at four potentials)
- System: potentiostatic deposition on stainless steel at −1000 / −1050 / −1075 / −1300 mV vs Ag/AgCl.
- What the figure shows: at −1000 and −1050 mV (before Zn deposits), SEI platelets stand up randomly and become increasingly disordered; at −1075 mV, Zn clusters mix with SEI platelets, and Zn nucleates along SEI crystals; at −1300 mV, only dense, flat-lying hexagonal Zn platelets are visible.
- Authors' interpretation: the SEI itself also undergoes "overlimiting" instability; Zn nucleating on the SEI causes loss of texture; under fast deposition Zn grows non-epitaxially as (002) platelets.
- Reading lesson: a grid arranged as "potential progression × magnification progression" reads directly as a continuous evolution story.

### Baffour et al. 2026, JACS — Figures 1e–i, 2f
- Fig. 1: untextured Zn is rough; textured Zn is dense with fine grains, and at high magnification the grains are cold-welded together. Fig. 2f: at −950 mV the surface is uniformly covered by dense, flat-lying nanosheet SEI.
- Reading lesson: SEM often serves as the "seeing is believing" evidence for an electrochemical conclusion (e.g. a film-formation loop in EIS); when explaining the figure, connect it to the corresponding electrochemical figure.

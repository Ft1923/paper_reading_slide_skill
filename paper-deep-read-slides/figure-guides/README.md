# Figure reading guide library (electrochemistry / battery papers)

One guide per figure type. When close-reading a paper and annotating its figures, open the matching file first: explain the figure following "Reading steps", draw following "Annotation suggestions", and raise questions from "Common pitfalls".

After each paper, append the new experience to the **Case library** at the end of the matching file; for a new figure type, copy `_TEMPLATE.md` into a new guide and register it in the table below.

| File | Figure type | Typical use |
|---|---|---|
| [cv-lsv.md](cv-lsv.md) | Cyclic voltammetry CV / linear sweep LSV / I–V curves | Onset potential, peak current, reversibility, dividing reaction regimes |
| [rde-levich.md](rde-levich.md) | Rotating disk electrode: LSV at several speeds, Levich plot, Koutecký–Levich plot | Separate mass-transport control from kinetic / interphase control, extract diffusion coefficients |
| [tafel.md](tafel.md) | Tafel plot (log\|j\| vs η) | Exchange current density j₀, Tafel slope, "corrosion current" |
| [eis.md](eis.md) | Electrochemical impedance spectroscopy, Nyquist / Bode, including DRT | Ohmic resistance, charge transfer, diffusion, film formation |
| [xps.md](xps.md) | X-ray photoelectron spectroscopy | Surface oxidation states and chemical environment (SEI composition) |
| [xrd.md](xrd.md) | X-ray diffraction (including 2D-XRD and texture analysis) | Phases, crystal-plane orientation, degree of texture |
| [sem.md](sem.md) | SEM morphology (including EDX) | Deposit morphology: flat / mossy / dendritic / platelet |
| [plating-ce.md](plating-ce.md) | Plating/stripping Coulombic efficiency, symmetric-cell voltage–time | Metal-anode reversibility, short circuits, overpotential |
| [full-cell.md](full-cell.md) | Full cell: capacity vs cycle, voltage profiles, rate capability | Practical performance |

## General conventions

- Read the axes first: quantity, units, direction (potential axes sometimes become more negative to the right; XPS binding energy usually decreases from left to right).
- Then the legend and test conditions: electrodes, electrolyte, reference electrode, scan rate / current density / rotation speed, temperature.
- Keep annotation colors consistent within one paper and matched to the regions / pathways in the commentary.
- Reference conversions: Ag/AgCl (sat. KCl) ≈ +0.197 V vs SHE; SCE ≈ +0.241 V vs SHE; Zn²⁺/Zn ≈ −0.76 V vs SHE.

## How to add experience

Append an entry to the "Case library" of the matching file in this format:

```
### Author Year, Journal — Figure X
- System: electrodes / electrolyte / conditions
- What the figure shows: ...
- Authors' interpretation: ...
- My assessment / questions: ...
- Reading lesson (fold back into the general guide above): ...
```

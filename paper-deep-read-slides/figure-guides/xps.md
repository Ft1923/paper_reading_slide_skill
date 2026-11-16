# Reading guide: X-ray photoelectron spectroscopy XPS

## What this figure measures
X-rays eject core-level electrons, and their binding energy (BE) is measured. The same element shifts in BE depending on its chemical environment (oxidation state, coordinating atoms), which reveals the composition and chemical state of the surface (~5–10 nm deep). Commonly used to analyze the SEI.

## Axes and common forms
- x-axis: binding energy BE (eV), **usually decreasing from left to right**.
- y-axis: intensity (counts or a.u.).
- Typical figures: a survey spectrum + high-resolution spectra per element; black dots/thin line = raw data, colored fills = fitted components, envelope = sum of the fit.

## Reading steps
1. Confirm the energy calibration (usually adventitious C 1s = 284.8 eV), sample handling (washed or not, inert transfer or not), and whether sputtering was used (depth profiling).
2. Survey spectrum first: which elements are present.
3. High-resolution spectra: main peak position, symmetric or not, how many fitted components.
4. Assign each fitted component against reference BEs; check that the fitting constraints (spin–orbit splitting, area ratios, FWHM) are reasonable.
5. Compare relative proportions of components across conditions (potential, cycle number, sputter depth).

## Common reference values (verify against literature / databases)
| Line | Reference BE / rule |
|---|---|
| C 1s adventitious carbon | 284.8 eV (calibration reference) |
| Zn 2p | 2p₃/₂–2p₁/₂ splitting ≈ 23.0 eV; Zn⁰ and ZnO 2p₃/₂ both ≈ 1021.5–1022.5 eV, hard to distinguish |
| Zn LMM Auger | The better way to distinguish Zn⁰ from Zn²⁺ (kinetic energy / modified Auger parameter) |
| O 1s | Lattice O²⁻ ~530 eV; –OH ~531.5 eV; sulfate / adsorbed water ~532–533 eV |
| S 2p | Sulfate ~168–169 eV; sulfide ~161–162 eV |
| F 1s | Metal fluoride ~684–685 eV; C–F / organic fluorine ~688 eV |

## Key features → meaning
| Feature in the figure | Physical meaning |
|---|---|
| Main peak shifts to higher BE | The atom is surrounded by more electronegative ligands (O, F, S–O), more oxidized |
| Doublet spacing matches the spin–orbit splitting | Same element, same state (a self-consistency check on the fit) |
| Component ratios change after sputtering | Layered SEI structure (organic outer / inorganic inner, etc.) |
| Broad, asymmetric peak | Several overlapping chemical environments, or charging |

## Annotation suggestions
- Vertical line at the main-peak BE with its assignment; a double-headed arrow for the spin–orbit splitting.
- Write component labels directly on the peaks ("Zn–OH", "S–Oₙ / crystal water").
- For peaks far from reference values, note beside them "X eV higher than usual → possible causes".

## Common pitfalls / questions to ask
- If the calibration is not stated, or an insulating sample charges, all peaks may be shifted by several eV.
- Zn 2p alone cannot reliably distinguish metallic Zn from Zn salts; check the Auger peak.
- Arbitrary numbers of components and constraints: overfitting can "find" any species.
- Air exposure during transfer and washing solvents can change the surface composition.
- XPS sees only the top few nanometers and cannot represent a thick SEI as a whole.

## Case library

### Baffour et al. 2026, JACS — Figures 3c, 3d
- System: SEI formed on stainless steel at −950 mV vs Ag/AgCl, 2 M ZnSO₄.
- What the figure shows: Zn 2p doublet spacing ≈ 23 eV; Zn 2p₃/₂ at 1025.8 eV; O 1s main peak at 535.2 eV, with a smaller component on the right assigned to Zn–OH.
- Authors' interpretation: the high BE comes from the Zn–O–S bonding environment in ZHS (zinc hydroxide sulfate); the O 1s main peak is S–Oₙ plus crystal water ("tentatively").
- My assessment / questions: both 1025.8 eV and 535.2 eV are about 3 eV higher than common literature values; the energy calibration and charge correction should be confirmed. S 2p and XRD cross-checks would help (XRD is in Fig. 3e).
- Reading lesson: when all BEs are uniformly high, suspect charging / calibration before discussing chemical environment.

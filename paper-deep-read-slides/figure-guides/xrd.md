# Reading guide: X-ray diffraction XRD (including 2D-XRD and texture analysis)

## What this figure measures
Atomic planes in a crystal diffract X-rays, giving peaks when Bragg's law 2d·sinθ = nλ is satisfied. Peak position → phase (interplanar spacing); peak intensity ratios → grain orientation (texture); peak width → crystallite size / strain.

## Axes and common forms
- Conventional XRD: x-axis 2θ (Cu Kα, λ = 1.5406 Å), y-axis intensity; several patterns stacked with vertical offsets, often with standard reference (PDF card) sticks at the bottom.
- 2D-XRD: a detector image showing diffraction rings (Debye rings); the angle around a ring is γ (azimuth).
- γ-integrated plot: x-axis γ, y-axis intensity, showing how a given plane is distributed over directions.

## Common Zn references (Cu Kα; verify against the PDF card)
| Plane | 2θ approx. | Relative intensity on the standard card (random orientation) |
|---|---|---|
| (002) | 36.3° | ~50% |
| (100) | 39.0° | ~40% |
| (101) | 43.2° | 100% (strongest) |
| (102) | 54.3° | ~25% |
| (103)/(110) | 70.1°/70.6° | ~20% |

Zinc hydroxide sulfate (ZHS, layered) has a strong low-angle peak (corresponding to its interlayer spacing); its exact position varies with the number of crystal waters — check against the card.

## Reading steps
1. Confirm the X-ray source, scan range, and sample form (measured directly on the electrode / scraped powder).
2. Match every peak to a reference card with vertical lines: target phase, substrate (stainless steel, Cu current collector), or by-product.
3. Compare intensity ratios with the standard card: one plane anomalously strong → texture.
4. Quantify texture: I(002)/ΣI(hkl), or the Harris texture coefficient TC(hkl).
5. 2D-XRD: is the ring continuous and uniform (fine grains, continuous orientation), broken into spots (a few large grains), or concentrated on an arc (strong texture)?
6. γ integration: a single narrow peak (small Δγ) = concentrated orientation; multiple sharp peaks = several large grains with different orientations.

## Key features → meaning
| Feature in the figure | Physical meaning |
|---|---|
| New peaks appear | A new phase (e.g. by-product ZHS, ZnO) |
| (002) anomalously strong relative to (101) | (002) texture: basal planes parallel to the surface |
| Peaks broaden | Smaller crystallites or microstrain (Scherrer equation) |
| All peaks shifted | Lattice parameter change or sample-height error |
| 2D rings broken into spots | Large grains, poor statistics |

## Annotation suggestions
- Use semi-transparent vertical bands over key peaks (e.g. one band for ZHS, one for Zn(002)) to compare across patterns whether a peak is present.
- Label each pattern with its condition (e.g. potential −1075 / −1150 / −1300 mV).
- On a texture-fraction bar chart, connect bars with arrows to show the trend and write the values.
- On 2D-XRD images, circle spots and label which plane each ring belongs to.

## Common pitfalls / questions to ask
- Substrate peaks overlapping target peaks (stainless steel, Cu foil): rule them out before assigning.
- Texture comparisons need the same geometry and normalization; compare with the standard card, not absolute intensities alone.
- XRD penetrates deeply (micrometers), so it measures the whole deposit + substrate, not just the surface.
- Amorphous SEI components are invisible to XRD; "no peak" does not mean "no by-product".

## Case library

### Baffour et al. 2026, JACS — Figures 1a–d (substrate texture)
- System: electrodes cold-pressed from Zn powders of different particle sizes.
- What the figure shows: as particle size increases from 2 μm to 200 μm, (101) gradually disappears and only (002) remains; 2D rings change from spotty to continuous bright arcs; γ integration shows >95% of (002) grains within Δγ ≈ 5°.
- Reading lesson: conventional XRD shows "which planes are present"; 2D-XRD + γ integration shows "how concentrated the orientation is" — use them together.

### Baffour et al. 2026, JACS — Figures 3e, 3f (deposits)
- System: Zn deposited on stainless steel at −1075, −1150, −1300 mV.
- What the figure shows: at −1075 mV the ZHS peak and the Zn(002) peak are of comparable intensity; at −1300 mV ZHS disappears and only a sharp (002) remains; I(002)/ΣI ≈ 47% → 81% → 95%.
- Authors' interpretation: the faster the deposition, the more Zn wins over side reactions, growing non-epitaxially as (002).
- Reading lesson: an XRD series that changes only one variable (potential / rate), with vertical color bands to compare "peak present or not", is the most direct way to show "competition".

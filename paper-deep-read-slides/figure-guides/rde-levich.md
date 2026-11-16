# Reading guide: rotating disk electrode (RDE) — LSV at several speeds, Levich plot, Koutecký–Levich plot

## What this figure measures
The rotating electrode draws solution up along its axis and flings it out across the surface, so the liquid diffusion-layer thickness δ is precisely set by the rotation speed ω. The question is how the current changes with speed:
- changes with ω → controlled by liquid-phase mass transport;
- independent of ω → controlled by reaction kinetics or an interfacial film (SEI).

## Core equations
- δ = 1.61 D^(1/3) ν^(1/6) ω^(−1/2) (ω in rad/s; ω = 2π·rpm/60)
- Levich: j_lim = 0.62 nF D^(2/3) ν^(−1/6) ω^(1/2) C_b → j_lim ∝ √ω, a straight line through the origin
- Koutecký–Levich: 1/j = 1/j_k (or j_s) + 1/j_lim → 1/j vs ω^(−1/2) is a straight line; intercept = 1/j_k, slope → D
- Kinematic viscosity of aqueous solutions ν ≈ 0.01 cm²/s

## Axes and common forms
1. LSV at several speeds: x-axis E, y-axis j, one colored curve per rpm.
2. Levich plot: x-axis ω^½ (or rpm^½), y-axis plateau current.
3. K–L plot: x-axis ω^(−½), y-axis 1/j, one line per potential.

## Reading steps
1. In the speed series, find the plateau region; check whether the plateau rises with speed and whether high-speed curves "bunch together".
2. Levich plot: do the points fall on a straight line through the origin? At what speed do they start to deviate (flatten)?
3. K–L plot: is it linear? Read the intercept extrapolated to ω^(−½)→0 (the current left at infinite speed); back-calculate D from the slope and compare with the literature as a self-consistency check.
4. Convert the transition speed to δ and check whether the order of magnitude is reasonable (a normal liquid-phase δ is ~10–100 μm).

## Key features → meaning
| Feature in the figure | Physical meaning |
|---|---|
| Plateau grows with ω, Levich linear through the origin | Pure liquid-phase diffusion control |
| Plateau saturates at high speed, Levich flattens | A speed-independent series resistance appears: kinetics or an interfacial film |
| K–L intercept ≠ 0 | Finite j_k / j_s; the interfacial reaction or film transport rate can be extracted |
| D from the slope is anomalously small (≪10⁻⁶ cm²/s) | Transport is not in the liquid but in a solid / quasi-solid layer |
| Levich line does not pass through the origin | Kinetic contribution, or the potential has not reached the transport limit |

## Annotation suggestions
- Speed series: box the plateau in red; vertical arrow "speed ↑ plateau ↑"; mark the curves that saturate.
- Levich plot: draw an ideal dashed line through the origin to contrast with the saturating data; label "transition ≈ X rpm, δ ≈ Y μm".
- K–L plot: an arrow extrapolating left to the y-axis, "intercept = 1/j_s"; write the fitted D next to the slope.

## Common pitfalls / questions to ask
- Units: rpm vs rad/s mixed up; is the x-axis rpm^½ or ω^½ (rad/s)?
- Has the plateau really reached the transport limit (is the potential sufficient)?
- The measurement averages over the whole disk; with a non-uniform SEI the parameters are only averages.
- If the material being compared sits on the counter electrode (not the working electrode), the working-electrode potential only qualitatively reflects its driving force.

## Case library

### Baffour et al. 2026, JACS — Figures 2c, 2d, 3a, 3b
- System: Ø5 mm stainless-steel RDE, 2 M ZnSO₄, swept to −1050 mV (before Zn onset), 100–800 rpm.
- What the figure shows: the side-reaction plateau rises with speed and saturates beyond ~600 rpm (√ω ≈ 7.9 (rad/s)^½), corresponding to δ ≈ 11.6 μm; a fit of the low-speed segment gives D ≈ 8.6×10⁻⁹ cm²/s; the K–L intercept gives an SEI-limited rate constant of ~5×10⁻⁶ cm/s and the slope gives D_bulk ≈ 1.85×10⁻⁶ cm²/s (consistent with the literature). In 3b, j_s is nearly the same with Pt and (002) Zn counter electrodes.
- Authors' interpretation: saturation comes from slow solid-state ion transport through the SEI ("underlimiting" transport limitation); the side reactions originate mainly from the electrolyte rather than Zn corrosion.
- My assessment / questions: in 3b, j_s for untextured Zn is clearly higher, which the text does not discuss; Zn is the counter electrode, so conclusions about crystal-facet effects should be treated with caution.
- Reading lesson: "spinning faster does not raise the current" is a typical signature of an interfacial film; comparing D back-calculated from the slope with literature values is a good test of whether a K–L analysis is credible.

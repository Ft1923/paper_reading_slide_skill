# Reading guide: metal-anode plating/stripping — Coulombic efficiency (CE) and symmetric-cell voltage profiles

## What this figure measures
Metal is plated onto a current collector (e.g. Cu, stainless steel) at constant current and then stripped back; the charges of the two steps are compared: CE = stripping charge / plating charge. This measures metal-anode reversibility. Voltage–time profiles of symmetric cells (Zn||Zn) show overpotential and short circuits.

## Axes and common forms
- CE vs cycle: x-axis cycle number, y-axis CE (%).
- CE vs current density: x-axis current density, y-axis average CE.
- Voltage–time / voltage–capacity profiles: the plating segment is negative (or lower), the stripping segment positive (or higher).
- Long symmetric-cell cycling: x-axis time (h), y-axis voltage, a square wave.

## Reading steps
1. Confirm the conditions: current density (mA/cm²), capacity per cycle (mAh/cm²), electrode area, electrolyte amount, current collector. Both current and capacity matter; reporting only one is meaningless.
2. CE vs cycle: CE in the first few (formation) cycles; average CE once stable; size of fluctuations; when it fails.
3. Voltage profiles: overpotential (nucleation spike + steady plateau); does it grow with cycling? any sudden drop or violent fluctuation?
4. Compare across conditions: which current / electrolyte gives higher, more stable CE.

## Key features → meaning
| Feature in the figure | Physical meaning |
|---|---|
| Stable CE ≥ 99% | Good reversibility; only ≥ 99.9% supports thousands of cycles |
| CE fluctuates wildly (even > 100%) | Soft short circuits, "dead metal" reconnecting, unstable measurement |
| CE drops suddenly / test stops | Short circuit or electrolyte depletion |
| Symmetric-cell voltage suddenly shrinks and flattens | Dendrite short circuit |
| Overpotential gradually increases | SEI thickening, electrolyte consumption |
| Voltage spike in the first cycle | Nucleation overpotential |

## Annotation suggestions
- Distinguish current densities by color and write directly beside them, e.g. "1 mA/cm²: CE erratic, fails after ~50 cycles".
- CE vs current: mark the critical current with a vertical dashed line, shade the "side-reaction competition region / deposition-dominated region" on either side, and write the CE jump values.
- Voltage profiles: mark the nucleation spike, overpotential, and short-circuit point.

## Common pitfalls / questions to ask
- Very small capacities (e.g. 0.5 mAh/cm²) and excess electrolyte overstate CE and lifetime.
- Was the Aurbach method (pre-deposited Zn reservoir) used, or direct cycling? CEs from the two are not directly comparable.
- Points with CE > 100% signal a problem and should not be averaged away.
- Reporting only "cycled for X hours" without current and capacity cannot be evaluated.

## Case library

### Baffour et al. 2026, JACS — Figures 5a, 5b
- System: half cells, 2 M ZnSO₄, fixed 3 mAh/cm², currents 0.2–100 mA/cm².
- What the figure shows: at 1 mA/cm², CE jumps between 45% and 110% and fails after ~50 cycles; at 15 mA/cm², stable at ~97%. CE vs current: 55% → 79% → 91% → a ~96% plateau reached at ~15 mA/cm², with no further gain up to 100 mA/cm².
- Authors' interpretation: there is a critical current j_critical ≈ 15 j_s; at low current, SEI-forming side reactions dominate and grow sharp, randomly oriented deposits that cause shorts; above j_critical, Zn deposition dominates.
- My assessment / questions: j_critical ≈ 15 j_s is an empirical relation; the paper does not report the anode potential at j_critical (the half cells have no reference electrode).
- Reading lesson: a "CE vs current density" plot can directly reveal a competition mechanism; lower current is not necessarily gentler.

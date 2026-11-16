# Reading guide: full-cell performance — capacity vs cycle, voltage profiles, rate capability

## What this figure measures
Cathode and anode are assembled into a complete cell and cycled at a given rate to assess capacity retention, Coulombic efficiency, and voltage plateaus — i.e. practical performance.

## Axes and common forms
- Capacity vs cycle (often with two y-axes): left axis discharge capacity (mAh/g or mAh/cm²), right axis CE (%), x-axis cycle number.
- Voltage vs capacity: x-axis capacity, y-axis voltage; several cycles overlaid, with a color gradient for cycle number.
- Voltage vs time: x-axis time, showing charge/discharge durations.
- Rate plot: stepwise switching between C-rates, showing capacity and recovery.

## Reading steps
1. Confirm the key parameters: areal capacity (mAh/cm²), cathode loading, N/P ratio, electrolyte amount (E/C ratio), cell format (coin / pouch), temperature.
2. Understand the rate definition: 1C = full charge/discharge in 1 hour; 5C = 12 minutes; are the charge and discharge rates the same?
3. Dual-axis plots: first sort out which data series belongs to which axis; read the initial capacity, the stable capacity after formation, retention, and CE.
4. Voltage profiles: plateau voltage, polarization (gap between charge and discharge plateaus), whether cycles overlap.
5. Compare with the literature for the same chemistry: areal capacity, rate, and cycle number together.

## Key features → meaning
| Feature in the figure | Physical meaning |
|---|---|
| Capacity drops over the first tens of cycles, then stabilizes | Formation / activation, or cathode dissolution reaching equilibrium |
| CE persistently < 99% | Ongoing side reactions (e.g. shuttling, hydrogen evolution) |
| Voltage profiles of many cycles overlap | Stable state, no growth in polarization |
| Growing gap between charge and discharge plateaus | Increasing internal / interfacial resistance |
| Scattered dips in CE late in cycling | Precursors to failure (short circuit, electrolyte dry-out) |

## Annotation suggestions
- On dual-axis plots, use color to tie each data series to its axis, and write the stable capacity and CE.
- On voltage–time plots, label "charge X min / discharge Y min" and the plateau voltage.
- When coin-cell and pouch-cell results are shown side by side, mark the differences in areal capacity and rate.

## Common pitfalls / questions to ask
- Low areal capacity (< 1 mAh/cm²), excess Zn, and excess electrolyte greatly flatter lifetime.
- Reporting only mAh/g (per cathode active material) without areal capacity makes practicality hard to assess.
- "Fast charging" requires both a high charge rate and a meaningful areal capacity.
- Conclusions from coin cells and pouch cells do not transfer directly; pouch cells have larger areas and more severe side reactions.

## Case library

### Baffour et al. 2026, JACS — Figures 5c–g (Zn||I₂)
- System: (002) Zn anode + I₂ cathode; coin cell charged at 15 mA/cm² (≈8 min) and discharged at 3 mA/cm² (≈40 min); continuous 5C cycling; pouch cell at 10C, 1 mAh/cm².
- What the figure shows: coin-cell capacity ≈ 1.86 mAh/cm² with almost no fade over 1100+ cycles, CE ~92–93%; at 5C, the curves for cycles 1400–1500 nearly overlap; the pouch cell drops from ~1.3 to ~0.95 mAh/cm² over the first ~150 cycles, then stabilizes, lasting about 500 cycles.
- My assessment / questions: a full-cell CE of ~92% is low, possibly including iodine-species shuttling or hydrogen-evolution losses; the early capacity drop in the pouch cell shows side reactions remain a challenge at larger areas.
- Reading lesson: point out asymmetric "fast charge, slow discharge" rate designs explicitly; on dual-axis plots, sort out the axes before reading values.

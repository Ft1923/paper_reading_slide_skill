# Reading guide: Tafel plots

## What this figure measures
A slow sweep around the equilibrium (open-circuit) potential, with the logarithm of current plotted against overpotential, yields kinetic parameters: exchange current density j₀ and Tafel slope b. Zn-battery papers also often use it to extrapolate a "corrosion current" and "corrosion potential".

## Core equations
- Butler–Volmer: j = j₀[exp(α_aFη/RT) − exp(−α_cFη/RT)]
- For |η| ≳ 50–100 mV only one term remains: η = a + b·log|j| (Tafel equation)
- With α = 0.5, n = 1, 25 °C: b ≈ 118 mV/dec
- j₀: the rate of the forward and backward reactions at equilibrium (net current 0); larger means the reaction is "easier"

## Axes and common forms
- x-axis: E or η; y-axis: log|j|. The curve is V-shaped, with its minimum at the equilibrium / corrosion potential.

## Reading steps
1. Confirm the scan rate (typically 1–5 mV/s), sweep range, and whether iR compensation was applied.
2. Find the linear segments on both sides (Tafel regions) and read their slopes.
3. Extrapolate both lines to η = 0 (or the corrosion potential); the y-value of the intersection = log j₀ (or log j_corr).
4. When comparing samples, check how many orders of magnitude j₀ or j_corr differ, and whether the slopes are similar (same mechanism).

## Key features → meaning
| Feature in the figure | Physical meaning |
|---|---|
| Position of the V's minimum | Equilibrium potential / mixed (corrosion) potential |
| Slope of the linear segment | Tafel slope, reflecting the rate-determining step and transfer coefficient |
| Extrapolated intersection | j₀ or j_corr |
| Very short or curved linear segment | Mass-transport limitation, overlapping reactions, or ohmic drop |

## Annotation suggestions
- Two dashed extrapolation lines + a dot at the intersection labeled "j₀".
- Write the slope value next to each linear segment; mark where the data deviate from the line as "mixed reactions / transport effects".
- Place a linear-scale Butler–Volmer curve alongside to aid understanding.

## Common pitfalls / questions to ask
- At potentials where metal deposition/dissolution and hydrogen evolution occur simultaneously, the currents cannot be separated, so the extrapolated "corrosion current" mixes several reactions.
- Mass-transport limitation distorts the linear segment; extrapolation is unreliable when the linear segment spans less than one decade.
- The corrosion potential is a mixed potential, not an equilibrium potential.
- Reporting j₀ without the slope or scan rate makes comparison impossible.

## Case library

### Baffour et al. 2026, JACS — Introduction, paragraph 3 (no figure; a critique of the method)
- System: Zn crystal-facet engineering papers commonly use Tafel extrapolation to compare side-reaction activity of (002) vs other facets.
- Authors' interpretation: two major flaws: ① Zn redox current and side-reaction current cannot be separated; ② coupled mass-transport limitations make the kinetic parameters unreliable. They instead use "a potential window before Zn deposition + RDE + K–L analysis".
- Reading lesson: whenever a paper compares electrodes by a Tafel-extrapolated "corrosion current", ask: does the current come only from the target reaction? Has mass transport been accounted for?

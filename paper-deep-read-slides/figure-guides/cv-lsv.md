# Reading guide: cyclic voltammetry CV / linear sweep LSV / I–V curves

## What this figure measures
The working-electrode potential is swept at a fixed rate while the current is recorded. Rises and falls in current are the "fingerprints" of electrochemical reactions: where they start, how fast they are, and whether they can be reversed.

## Axes and common forms
- x-axis: working-electrode potential E (note the reference: vs Ag/AgCl, SHE, Zn²⁺/Zn …). Check the direction: in some figures the potential becomes more negative to the right.
- y-axis: current or current density j. Check the sign convention: IUPAC plots anodic (oxidation) current as positive; some papers (especially the US convention) plot cathodic current as positive.
- LSV: one sweep direction only; CV: forward and reverse sweeps form a closed loop.

## Reading steps
1. Confirm the reference electrode, scan rate, working-electrode material, electrolyte, and whether the solution is stirred / rotated.
2. Find the sweep direction (arrow or text) and separate the forward and reverse sweeps.
3. Divide the curve into potential regimes: no current → onset → exponential rise (kinetic control) → plateau / peak (mass-transport control) → further rise (a new reaction or electroconvection).
4. Assign each regime to a reaction: the main reaction (e.g. Zn deposition) or a side reaction (hydrogen evolution, electrolyte decomposition).
5. With a reverse sweep: compare the size, position, and area of the cathodic and anodic peaks.

## Key features → meaning
| Feature in the figure | Physical meaning |
|---|---|
| Current rises exponentially from ≈0 | Reaction onset, Butler–Volmer kinetic control |
| Onset more negative/positive than the theoretical value | Overpotential: nucleation barrier, lowered interfacial concentration (Nernstian shift), film resistance |
| Peak (rise then fall) | Reactant depleted at the surface, transition to diffusion control; in still solution the diffusion layer grows with time |
| Plateau | Steady-state mass-transport limit (common with stirring or RDE) |
| Rise again after the plateau | A new reaction starts, or electroconvection gives "overlimiting" current |
| Cathodic peak ≫ anodic peak | Irreversible: products leave (gas) or become inert solids |
| ΔEp ≈ 59/n mV, peak current ratio ≈ 1 | Reversible solution-phase redox couple |
| ip ∝ v^½ | Diffusion control; ip ∝ v indicates surface-adsorbed / thin-layer control |
| "Crossover loop" in a metal-deposition CV (reverse-sweep current higher than forward) | Nucleation overpotential: deposition continues more easily on already-nucleated surface |
| Anodic stripping peak area / cathodic deposition area | Rough Coulombic efficiency |

## Annotation suggestions
- Separate potential regimes with semi-transparent bands and number them (① side reactions ② onset ③ diffusion limited ④ overlimiting).
- Mark the onset and equilibrium potential with vertical dashed lines; give values against both references (e.g. "−1075 mV vs Ag/AgCl ≈ −878 mV vs SHE").
- Mark the sweep direction with arrows; circle peaks and write what each peak indicates.
- For a zoomed inset, state what it demonstrates (e.g. "tiny anodic current on the reverse sweep → irreversible").

## Common pitfalls / questions to ask
- "A peak exists" and "the peaks are asymmetric" are two different statements: the first indicates transport limitation, the second irreversibility.
- Different onset criteria (threshold current, tangent intersection) change the value by tens of mV.
- Was iR compensation applied? Ohmic drop distorts curves at high current.
- Is the working electrode an inert substrate or the metal itself? On an inert substrate the metal must nucleate first, so the onset is more negative.
- Confirm whether the potential axis is reversed and which current sign convention is used before reading values.

## Case library

### Baffour et al. 2026, JACS — Figures 2a, 2b
- System: stainless-steel working electrode, 2 M ZnSO₄, Ag/AgCl reference, 5 mV/s.
- What the figure shows: the I–V curve in 2a has four regimes: current ≈0 before −1075 mV; exponential rise afterwards; flattening from ~−1400 mV; a further rise from ~−1600 mV. 2b sweeps only from −200 to −1050 mV: a peak at #6, and very small anodic current on the reverse sweep.
- Authors' interpretation: the region before Zn onset is a side-reaction regime; the peak means the side reactions are themselves diffusion limited; cathodic ≫ anodic current → the side reactions are irreversible. A liquid-phase diffusion estimate gives δ ≈ 3900 μm (absurd), so the bottleneck is the SEI.
- My assessment / questions: the onset is ~120 mV more negative than theory; a Nernstian shift (interfacial Zn²⁺ consumed) can explain at most a few tens of mV, so nucleation overpotential should account for a large part.
- Reading lesson: measuring in a potential window where the main reaction has not started isolates the side-reaction current; regions that "look like zero current" are worth zooming into.

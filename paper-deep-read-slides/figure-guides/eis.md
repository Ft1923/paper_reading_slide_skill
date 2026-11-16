# Reading guide: electrochemical impedance spectroscopy EIS (Nyquist / Bode) and DRT

## What this figure measures
A small AC signal (typically 5–10 mV) is superimposed on a DC potential (open circuit or a bias) and swept from high to low frequency to measure the impedance Z = Z′ + jZ″. Different physical processes have different characteristic times and show up in different frequency ranges.

## Axes and common forms
- Nyquist: x-axis Z′ (real part), y-axis −Z″ (negative imaginary part, so capacitive arcs appear above the axis). **High frequency on the left, low frequency on the right**; units Ω or Ω·cm². Both axes should use equal scales, otherwise semicircles look distorted.
- Bode: x-axis log f; y-axes |Z| and phase angle.
- DRT (distribution of relaxation times): x-axis τ (or log τ, τ = 1/2πf), y-axis γ(τ); each peak corresponds to a distinct process.

## Reading steps
1. Confirm the measurement conditions: open circuit or biased, frequency range, amplitude, whether in operando, whether the system was at steady state.
2. High-frequency intercept with the real axis = ohmic resistance R_s (electrolyte + contacts).
3. Mid-frequency semicircle: diameter ≈ R_ct (charge transfer) or R_SEI (interfacial film); several semicircles mean several interfacial processes — the higher-frequency arc is usually the film, the mid-frequency one charge transfer.
4. Low frequency: a 45° line = semi-infinite Warburg diffusion; near-vertical = blocking / capacitive behavior; an arc that returns below the real axis = inductive loop.
5. If an equivalent circuit was fitted, check that every element has a physical meaning and look at the fitting error.
6. DRT: count the peaks; going from small to large τ corresponds to fast to slow processes; compare shifts in peak position and area across conditions.

## Key features → meaning
| Feature in the figure | Physical meaning |
|---|---|
| High-frequency intercept | Ohmic resistance R_s |
| Semicircle (R ∥ CPE) | Charge-transfer or film resistance; larger diameter = harder |
| Two or more semicircles | Several processes, e.g. interfacial film + charge transfer |
| 45° line | Warburg diffusion, liquid-phase mass-transport control |
| Low-frequency inductive loop (dipping below the real axis) | Adsorbed intermediates, surface film formation / corrosion, change in active area |
| Semicircle grows with time / cycling | SEI thickening, passivation |
| DRT peak shifts to longer τ | That process has slowed down |

## Annotation suggestions
- Mark the R_s intercept, the semicircle diameter (double-headed arrow), and a 45° reference line.
- Add an arrow showing the direction of increasing frequency.
- Circle any inductive loop and label it "film formation / adsorption signal".
- Explain separately what state an inset (e.g. the OCP spectrum) represents.

## Common pitfalls / questions to ask
- Impedance measured on a non-steady system (a growing film, gas evolution) may violate the Kramers–Kronig relations; fit with caution.
- Equivalent circuits are not unique: one spectrum can be fitted by several circuits, so conclusions need other supporting evidence.
- Unequal axis scales make semicircles look elliptical and lead to miscounting processes.
- DRT results depend on the regularization parameter, and peak assignments are often "tentative"; check that the τ values in the text agree with the stated "shift by N orders of magnitude".
- Impedance from a symmetric cell and from a three-electrode cell mean different things (the former includes two electrodes).

## Case library

### Baffour et al. 2026, JACS — Figure 2e, Figure S14 (DRT)
- System: 2 M ZnSO₄, in-operando EIS; open circuit vs −950 mV vs Ag/AgCl (a potential where side reactions form the SEI).
- What the figure shows: at open circuit, a near-45° Warburg line; at −950 mV, a large arc that folds back at low frequency into an "inductive-like" loop. DRT shows two main peaks; the authors assign τ ≈ 0.2 s to bulk transport and τ ≈ 10⁻⁵ s to transport within the SEI.
- Authors' interpretation: the low-frequency loop = film formation; the dominant ion-transport mechanism switches to restricted transport through the SEI.
- My assessment / questions: the text says the peak shifts by "nearly 6 orders of magnitude", but the two τ values given differ by about 4 orders; check the SI. The authors call the DRT assignments "tentative".
- Reading lesson: comparing the same system at open circuit and biased to a side-reaction potential is a good design for capturing film formation.

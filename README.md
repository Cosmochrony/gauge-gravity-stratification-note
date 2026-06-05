This repository contains the source of the **Gauge--Gravity Stratification Presentation Note**
Cosmochrony paper
[*The Gauge--Gravity Stratification Sub-Programme — Presentation Note 8*](out/GaugeGravityStratificationNote.pdf).

This work is a **structured entry point** to the gauge--gravity stratification sub-programme of the
Cosmochrony corpus, not a summary of results. It maps the constituent papers, identifies the
spectral stratification chain from the same admissible functional, records the status of every
result as proved, structural, or open, and states the remaining open deliverables.

## Central Question

The spectral gravity sub-programme (Note 4) derives the Einstein tensor as the $a_2$
infrared-dominant response of the horizontal metric variation of $S_\Pi[g]$.
The gauge structure sub-programme (Note 3) identifies the gauge group
$G_\Pi = \mathrm{SU}(3) \times \mathrm{SU}(2) \times \mathrm{U}(1)$ and constructs the
admissible principal bundle $P_{G_\Pi}(M, G_\Pi)$.

> Does the same functional $S_\Pi[g, A]$, extended to include the admissible gauge connection,
> also produce Yang--Mills dynamics, and if so, at what spectral order?

The answer is **yes**, and the order is $a_4$. Gravity and gauge dynamics arise from the same
functional by varying in orthogonal directions --- horizontal (metric) and vertical (gauge
connection) --- at different Seeley--DeWitt orders. The classical question *"what symmetry
unifies gravity and gauge?"* is replaced by *"at what spectral order does the admissible
projection respond?"*. This is the **spectral stratification principle**.

The sub-programme closes the bosonic dynamical sector: it does not re-derive the gauge group
(Note 3) or the metric (Note 2). It derives the *dynamics* of gauge and gravitational fields
from the spectral structure of the single functional $S_\Pi[g, A]$ and establishes that their
UV behaviours --- quadratic for gravity, logarithmic for gauge --- are structural consequences
of the Seeley--DeWitt hierarchy.

## Logical Chain

$$\underbrace{a_2 \;\to\; G_{\mu\nu}}_{\text{horizontal } \delta_g}
\;\Big|\;
\underbrace{a_4 \;\to\; D_\mu F^{a\mu\nu} = 0}_{\text{vertical } \delta_A}
\;\Big|\;
\underbrace{a_6 \;\to\; R_{\mu\nu\rho\sigma}F^{\mu\nu}F^{\rho\sigma}}_{\text{mixed (structural)}}$$

from the single functional
$S_\Pi[g, A] = \tfrac{1}{2}\log\det' A_{g, A}$.

Four conceptually distinct stages:

1. **Extension of the operator to the gauge sector** (Q12) — the Laplacian
   $A_g = -\nabla_g^2$ is extended to $A_{g, A} = -(\nabla^A)^2 + E$ on the associated
   vector bundle of $P_{G_\Pi}(M, G_\Pi)$. The horizontal--vertical decoupling Lemma 1 of
   Q12 guarantees that the $a_2$ Einstein and $a_4$ Yang--Mills sectors remain independent
   at their respective leading orders.
2. **Yang--Mills from vertical $a_4$ variation** (Q12) — the $a_4$ coefficient of
   $A_{g, A}$ contains
   $\frac{1}{16\pi^2}\int \frac{1}{12}\mathrm{Tr}(F_{\mu\nu}F^{\mu\nu})\sqrt{g}\,d^4x$;
   the vertical variation $\delta_A S_\Pi = 0$ yields $D_\mu F^{a\mu\nu} = 0$.
3. **Coupled Einstein--Yang--Mills system** (Q13) — the joint variation
   $\delta_{g, A}\,S_\Pi = 0$ yields
   $G_{\mu\nu} = 8\pi G_N T^{\mathrm{YM}}_{\mu\nu}$,
   $D_\mu F^{a\mu\nu} = 0$, with coupling $8\pi G_N = c_{\mathrm{YM}} / c_{\mathrm{EH}}$
   fixed by the Seeley--DeWitt expansion alone.
4. **Structural hierarchy** (Q13) — Newton's constant $G_N^{-1} \sim \ell_{\mathrm{sp}}^{-2}$
   (quadratic UV) and the gauge coupling $g_{\mathrm{YM}}^{-2} \sim \log(\Lambda/\mu)$
   (logarithmic UV) share the same cutoff $\ell_{\mathrm{sp}}$. The hierarchy ratio
   $G_N g_{\mathrm{YM}}^2 \sim \ell_{\mathrm{sp}}^2 / \dim V \cdot [\log(\Lambda/\mu)]^{-1} \ll 1$
   is a structural consequence of the Seeley--DeWitt expansion, not a fine-tuned input.

## Constituent Papers

| # | Paper | Stage | Local path |
|---|-------|-------|------------|
| 1 | **Q12** (Beau2026q12) — *Yang--Mills from the vertical $a_4$ variation* | Operator extension, $a_4$ derivation, horizontal--vertical decoupling, UV hierarchy | [`../../gauge-structure/q12/`](../../gauge-structure/q12/) |
| 2 | **Q13** (Beau2026q13) — *Joint Einstein--Yang--Mills system and hierarchy* | Coupled EYM system, $a_6$ cross-coupling, EBI completion, hierarchy ratio | [`../q13/`](../q13/) |

(Q12 is shared with the gauge-structure sub-programme — Note 3 — where it provides the gauge
group identification; the present note draws on its $a_4$ vertical variation. Q12 therefore
remains located under `gauge-structure/`.)

## Status of Results

**Proved (unconditional):**
- $a_4 \supset \frac{1}{12}\mathrm{Tr}(F_{\mu\nu}F^{\mu\nu})$ (Q12 §4, standard heat-kernel
  result on $A_{g, A}$).
- Horizontal--vertical decoupling (Q12 Lemma 1): Einstein $a_2$ and Yang--Mills $a_4$ sectors
  are independent at their leading orders, from the principal-bundle structure.

**Structural:**
- $\Omega_{\mu\nu} = F_{\mu\nu}$ on the admissible bundle (Q12).
- Yang--Mills equations $D_\mu F^{a\mu\nu} = 0$ from $\delta_A S_\Pi = 0$ (Q12 Theorem 1,
  given $G_\Pi$).
- UV hierarchy $G_N^{-1} \sim \ell_{\mathrm{sp}}^{-2}$ vs.\
  $g_{\mathrm{YM}}^{-2} \sim \log(\Lambda/\mu)$ (Q12 §6).
- Coupled Einstein--Yang--Mills system (Q13 Theorem 3.2),
  $8\pi G_N = c_{\mathrm{YM}} / c_{\mathrm{EH}}$.
- $a_6$ gauge--gravity cross-coupling $R_{\mu\nu\rho\sigma}F^{\mu\nu}F^{\rho\sigma}$
  (Q13 Theorem 4.1) --- normalisation open.
- Structural hierarchy ratio $G_N g_{\mathrm{YM}}^2 \ll 1$ (Q13 Proposition 6.1) without
  fine-tuning.
- Spectral stratification principle $a_2 \to$ gravity, $a_4 \to$ gauge, $a_6 \to$ mixed
  (Q12/Q13).

**Conditional on [H-ext]:**
- Eddington--Born--Infeld joint completion $\mathcal{S}^{\mathrm{EBI}} \propto \int[\sqrt{-\det(g + \ell_{\mathrm{sp}}^2 R_{\mu\nu} + \ell_{\mathrm{sp}}^2 F_{\mu\nu})} - \sqrt{-g}]$
  (Q13 Theorem 5.3); inherits the [H-ext] conditionality from the Note 4 gravitational
  completion.

The $\mathrm{SU}(3) \times \mathrm{SU}(2) \times \mathrm{U}(1)$ gauge group is available as
**unconditional input** to the stratification chain per the current programme status (O31
Proposition 4.23, single-frequency BI fingerprint argument); the $a_4$ Yang--Mills derivation
of Q12 therefore holds unconditionally for the full Standard Model gauge group.

## Open Deliverables

1. **$a_6$ coupling normalisation.** Deriving the normalisation coefficient of the $a_6$
   cross-coupling would give a quantitative prediction for the leading gauge--gravity mixing
   at high spectral order and would constrain the EBI completion.
2. **Derivation of [H-ext].** Promoting Q13 Theorem 5.3 to an unconditional theorem. The
   structural mechanism is identified (BI parity at the scalar and tensorial levels); the
   admissible coherence extensivity step is the analytical gap.
3. **Full coupled equations with matter.** The coupled system
   $G_{\mu\nu} = 8\pi G_N(T^{\mathrm{YM}}_{\mu\nu} + T^{\mathrm{ferm}}_{\mu\nu})$,
   $D_\mu F^{a\mu\nu} = J^{a\nu}$ with explicit fermionic matter from Note 6 (Q14) requires
   integrating the projected Dirac sector of Q14 into the joint variational framework of Q13.

## Compilation

```bash
bash compile.sh
```

Produces `out/GaugeGravityStratificationNote.pdf`.

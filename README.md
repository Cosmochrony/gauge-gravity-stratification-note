This repository contains the source of the **Gauge--Gravity Stratification Presentation Note**
Cosmochrony paper
*The Gauge--Gravity Stratification Sub-Programme — Presentation Note 8*.

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
from the spectral structure of the single functional $S_\Pi[g, A]$ and establishes that, within
a proper-time cutoff, their ultraviolet divergence degrees --- quadratic for gravity,
logarithmic for gauge --- differ according to the Seeley--DeWitt order at which each sector
enters. That contrast is scheme-dependent: the zeta-regularized determinant carries no power
divergences.

## Logical Chain

$$\underbrace{a_2 \;\to\; G_{\mu\nu}}_{\text{horizontal } \delta_g}
\;\Big|\;
\underbrace{a_4 \;\to\; D_\mu F^{a\mu\nu} = 0}_{\text{vertical } \delta_A}
\;\Big|\;
\underbrace{a_6 \;\to\; \text{dimension-six invariants}}_{\text{spanning list only}}$$

from the single functional
$S_\Pi[g, A] = \tfrac{1}{2}\log\det' A_{g, A}$.

Three conceptually distinct stages:

1. **Extension of the operator to the gauge sector** (Q12) — the Laplacian
   $A_g = -\nabla_g^2$ is extended to $A_{g, A} = -(\nabla^A)^2 + E$ on the associated
   vector bundle of $P_{G_\Pi}(M, G_\Pi)$. Lemma 1 of Q12 gives the fixed-metric isolation of
   the gauge sector: under minimal coupling $a_2$ does not depend on $A$. It does **not** give
   full horizontal--vertical decoupling — the metric variation of $F^2$ is the $a_4$-order
   back-reaction $T^{\mathrm{YM}}$.
2. **Yang--Mills from the vertical $a_4$ variation** (Q12) — isolating the gauge component
   $\Omega^{\mathrm{gauge}}_{\mu\nu} = F_{\mu\nu}$ of the total bundle curvature, the $a_4$
   coefficient contains $\int \frac{1}{12}\mathrm{tr}_\rho(F_{\mu\nu}F^{\mu\nu})\sqrt{g}\,d^4x$,
   the overall $(4\pi)^{-2}$ being carried once by the heat-kernel prefactor; the vertical
   variation at fixed metric yields $D_\mu F^{a\mu\nu} = 0$. The induced logarithmic running of
   $g_{\mathrm{YM}}^{-2}$ has coefficient $I_\rho/(12\cdot16\pi^2)$ — not universal.
3. **Conditional Einstein--Yang--Mills system** (Q13) — varying a single matched renormalized
   local action gives
   $G_{\mu\nu} + \Lambda_{\mathrm{eff}} g_{\mu\nu} = 8\pi G_N T^{\mathrm{YM}}_{\mu\nu}$ and
   $D_\mu F^{a\mu\nu} = 0$, the metric variation of the gauge kinetic term being
   $2\tau_{\mu\nu}$. Since $\mathrm{tr}_\rho(F^2) = I_\rho F^a F^a$, canonical matching fixes
   $c_{\mathrm{EH}} = 1/(16\pi G_N)$ and $c_F I_\rho = 1/(4 g_{\mathrm{YM}}^2)$, so
   $8\pi G_N = 1/(2 c_{\mathrm{EH}})$. $G_N$, $g_{\mathrm{YM}}$ and $\Lambda_{\mathrm{ren}}$ are
   independent renormalized matching data, so the ratio $G_N g_{\mathrm{YM}}^2$ is not an
   output. The derivations are Euclidean.

## Constituent Papers

| # | Paper | Stage | Local path |
|---|-------|-------|------------|
| 1 | **Q12** (Beau2026q12) — *Yang--Mills from the vertical $a_4$ variation* | Operator extension, $a_4$ derivation, fixed-metric isolation of the gauge sector | [`../../gauge-structure/q12/`](../../gauge-structure/q12/README.md) |
| 2 | **Q13** (Beau2026q13) — *A conditional Einstein--Yang--Mills system* | Conditional coupled EYM system, matching normalisation, $a_6$ spanning list | [`../q13/`](../q13/README.md) |

(Q12 is shared with the gauge-structure sub-programme — Note 3 — where it provides the gauge
group identification; the present note draws on its $a_4$ vertical variation. Q12 therefore
remains located under `gauge-structure/`.)

## Status of Results

**Proved (theorem-level):**
- $a_4 \supset \frac{1}{12}\mathrm{tr}_\rho(F_{\mu\nu}F^{\mu\nu})$ (Q12, standard heat-kernel
  result on $A_{g, A}$, gauge component isolated).
- Fixed-metric isolation of the gauge sector (Q12 Lemma 1): under minimal coupling $a_2$ is
  independent of $A$. Full horizontal--vertical decoupling does **not** hold.
- Metric variation of the gauge kinetic term $= 2\tau_{\mu\nu}$ (Q13 Lemma).

**Structural:**
- $\Omega^{\mathrm{gauge}}_{\mu\nu} = F_{\mu\nu}$ on the admissible bundle (Q12).
- Yang--Mills equations $D_\mu F^{a\mu\nu} = 0$ from the fixed-metric $\delta_A S_\Pi = 0$
  (Q12 Theorem 1, given $G_\Pi$).
- Conditional coupled Einstein--Yang--Mills system (Q13 Theorem), with
  $8\pi G_N = 1/(2 c_{\mathrm{EH}})$ and $c_F I_\rho = 1/(4 g_{\mathrm{YM}}^2)$.
- $a_6$ spanning list of invariants, modulo integrations by parts and Bianchi identities
  (Q13) --- not a basis, no unique cross-term, coefficients undetermined.
- Difference in ultraviolet divergence degree, quadratic at $a_2$ and logarithmic at $a_4$
  (Q12/Q13) --- within a proper-time cutoff, hence scheme-dependent.

**Matching data (not predicted):**
- $G_N$, $g_{\mathrm{YM}}$, $\Lambda_{\mathrm{ren}}$ and the dimension-six coefficients are
  independent renormalization data; no numerical value for $G_N g_{\mathrm{YM}}^2$ follows.

**Interpretive:**
- The spectral stratification $a_2 \to$ gravity, $a_4 \to$ gauge is an organising reading,
  not a theorem.

The $\mathrm{SU}(3) \times \mathrm{SU}(2) \times \mathrm{U}(1)$ gauge group is available as
**unconditional input** to the stratification chain per the current programme status (O31
Proposition 4.23, single-frequency BI fingerprint argument); the $a_4$ Yang--Mills derivation
of Q12 therefore holds unconditionally for the full Standard Model gauge group.

## Open Deliverables

1. **Quantitative $a_6$ coefficients.** Reducing the spanning list to a minimal independent
   set and computing the coefficients for $A_{g, A}$ would turn the inventory into a
   quantitative statement about the leading gauge--gravity mixing.
2. **Status of the matching data.** Determining whether the admissibility structure constrains
   any combination of $G_N$, $g_{\mathrm{YM}}$ and $\Lambda_{\mathrm{ren}}$ — in particular the
   ratio $G_N g_{\mathrm{YM}}^2$ — would be the natural way to recover predictive content that
   the spectral expansion alone does not provide. A possible non-linear completion of the joint
   functional, and the Lorentzian continuation of the gauge sector, are open on the same footing.
3. **Full coupled equations with matter.** The coupled system
   $G_{\mu\nu} = 8\pi G_N(T^{\mathrm{YM}}_{\mu\nu} + T^{\mathrm{ferm}}_{\mu\nu})$,
   $D_\mu F^{a\mu\nu} = J^{a\nu}$ with explicit fermionic matter from Note 6 (Q14) requires
   integrating the projected Dirac sector of Q14 into the joint variational framework of Q13.

## Compilation

```bash
bash compile.sh
```

Produces `out/GaugeGravityStratificationNote.pdf`.

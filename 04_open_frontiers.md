# Open Frontiers

This document is extracted from the former `formal_gaps_coarsegraining.md` and collects research-frontier items and unresolved formal gaps.

---
## What Remains Open

This document has closed two gaps partially. What remains formally open:

**The coarse-graining mechanism at the biological-cognitive transition** is the least formalized. Timescale separation and renormalization group methods provide templates, but their direct application to biological neural networks operating far from equilibrium is an unsolved problem in physics and neuroscience. The framework's claims here are plausible and consistent with existing knowledge, but the derivation is incomplete.

**The interpretation of μ at the cognitive scale** requires care. At the quantum scale, μ is a probability amplitude with precise physical meaning. At the cognitive scale, μ_net is a stationary distribution over activation patterns — a well-defined mathematical object, but its physical interpretation is less direct. The framework treats it as a measure of which activation patterns are persistently realized given the network's synaptic geometry, which is correct, but the connection back to the underlying physical measure requires the coarse-graining bridge that is not yet fully established.

**The awareness gap remains — but is now better positioned for formalization**

Global constraint integration in S_net is the framework's candidate property. With the triple now defined, this can be stated more precisely:

A constraint geometry (S, T, μ) exhibits global constraint integration to the degree that it cannot be partitioned into independent subsystems without losing essential structural features. Formally: if S = S₁ × S₂, the geometry is globally integrated if the joint transition semigroup T_t(s₁', s₂' | s₁, s₂) cannot be factored as T₁_t(s₁' | s₁) · T₂_t(s₂' | s₂) without significant loss of information about the system's actual dynamics.

This can be operationalized with a specific metric. Define the **integration measure** Φ as the KL divergence between the joint transition kernel and its best factored approximation:

> Φ(S₁, S₂) = D_KL(T_t(s₁', s₂' | s₁, s₂) ‖ T₁_t(s₁' | s₁) · T₂_t(s₂' | s₂))

where the factored form uses the marginal kernels. Φ = 0 when the subsystems transition independently; Φ > 0 when the joint dynamics carry information beyond what the marginals capture. The global integration of a system is then:

> Φ_global = min over all bipartitions {Φ(S₁, S₂)}

For the μ-weighted refinement Φ_μ, the choice of which μ to use requires a decision. Three options are possible — time-averaged μ, instantaneous μ, and metastable-window μ — and they produce different measures with different interpretations. For the framework's purposes, **metastable-window μ** is the most defensible: the distribution within the current attractor basin over the duration of the cognitive state the system is presently occupying. This choice:

- Connects Φ_μ to actual cognitive context — the same brain in different cognitive states can exhibit different integration values, which is what a cognitively meaningful measure should capture
- Is consistent with the framework's existing treatment of μ at the cognitive scale as approximately stationary within metastable regimes
- Makes integration context-sensitive without making it instantaneously noisy

Time-averaged μ would give a global measure of the system's typical integration, losing context sensitivity. Instantaneous μ would be sensitive to transient fluctuations rather than stable cognitive states. Metastable-window μ strikes the right balance for the framework's current purposes, though the choice has consequences that downstream formalization will need to track.

This is the minimum integration across all ways of dividing the system — the bottleneck partition. A system with high Φ_global cannot be decomposed into approximately independent parts without losing significant information about its transition dynamics. This connects naturally to Tononi's Φ in integrated information theory while remaining grounded in the triple's own structure: it is a property of T and μ directly, not an additional primitive.

**What this does not yet establish**: whether Φ_global is sufficient for awareness, or merely a necessary structural property of systems that exhibit it. The framework's claim is that biological awareness is found in systems with high Φ_global — not that high Φ_global produces awareness. That asymmetry is the honest current position.

---

## Located Open Directions

The following are not vague future work. They are specific, located problems whose solutions would extend the framework's formal reach in precise ways. Naming them positions the framework within established mathematics rather than alongside it.

### 1. μ-Weighted Integration Measure

The current Φ_global definition measures irreducibility of the joint transition kernel T regardless of which transitions are actually realized under μ. A system could have highly coupled T in regions of S the system never occupies — and Φ would still register that coupling as integration. This overstates the functional integration of the realized dynamics.

The natural refinement weights each state's contribution to Φ by how often the system actually occupies it:

> Φ_μ(S₁, S₂) = E_{(s₁,s₂)~μ} [D_KL(T_t(·,· | s₁, s₂) ‖ T₁_t(·|s₁) · T₂_t(·|s₂))]

This is the expected KL divergence between joint and factored transition kernels, averaged over the realized distribution μ. It focuses the integration measure on transitions that actually occur rather than transitions that are merely possible. Φ_μ = 0 when the subsystems' realized dynamics are independent; Φ_μ > 0 when the joint realized dynamics carry information beyond the marginals.

The global μ-weighted integration is then:

> Φ_μ_global = min over all bipartitions {Φ_μ(S₁, S₂)}

This refinement requires μ to be specified — which makes the cognitive scale definition of μ as a metastable distribution more consequential. Φ_μ_global will depend on which metastable regime the system is currently in, which connects integration to context in a way the unweighted version does not. This is a meaningful improvement and the natural next step for the awareness formalization.

---

### 2. The Constructive Coarse-Graining Problem

The framework has specified what coarse-graining must preserve — boundary structure, stability structure, recursion structure — and has identified the mechanisms operating at each scale transition: decoherence and statistical averaging (quantum to thermodynamic), timescale separation (thermodynamic to biological), Hopfield energy derivation (biological to cognitive as existence proof).

What it does not have is a **constructive mapping**: given a specific fine-grained (S, T, μ), produce the specific coarse-grained (S', T', μ') that results from applying the relevant mechanism.

This is the main mathematical frontier of the framework. It is a hard open problem — not specific to this framework but present across physics, biology, and neuroscience wherever scale transitions are invoked. The relevant mathematical tools exist in fragments:

- **Renormalization group**: constructive for systems near critical points with scale invariance. Provides an explicit procedure for integrating out fast degrees of freedom and computing effective couplings at the coarser scale. Directly applicable at the quantum-thermodynamic transition near phase transitions; less directly applicable away from criticality.

- **Mori-Zwanzig projection**: a general formalism for eliminating fast degrees of freedom from a dynamical system. Given the full dynamics and a choice of slow variables, it produces exact equations of motion for the slow variables — including memory terms that capture the influence of eliminated fast variables. Applicable in principle at all three scale transitions; computationally intractable for most systems of biological complexity.

- **Information-theoretic compression**: finding S' as the minimal sufficient statistic of S with respect to predicting future states under T. This is related to the "predictive information" framework and provides a principled criterion for which degrees of freedom to retain. Applicable where the prediction target is well-defined; requires specifying the prediction horizon.

None of these provides a universal constructive procedure. What the framework can commit to is: the coarse-graining maps at each scale transition are in principle instances of one or more of these procedures, and the structural properties the framework claims are preserved are the properties these procedures are known to preserve. The gap between "in principle" and "in practice" is the constructive coarse-graining problem. Closing it is the work that would move the framework from philosophically grounded to formally complete.

**A toy worked example: the double-well potential**

To demonstrate that the constructive procedure is possible in at least one tractable case, consider a particle in a one-dimensional symmetric double-well potential:

> V(x) = −ax² + bx⁴

The fine-grained description is the full triple (S, T, μ) where:
- S = continuous position space ℝ
- T is the Fokker-Planck generator: ∂_t p(x,t) = ∂_x[V'(x)p] + D∂_x²p, describing diffusion in the potential landscape with noise level D
- μ is the stationary distribution: μ(x) ∝ e^(−V(x)/D), concentrated near the two wells

The system has two metastable states — left well (x < 0) and right well (x > 0) — separated by a barrier at x = 0. The coarse-grained description is the two-state triple (S', T', μ') where:
- S' = {L, R} — two discrete states
- T' is a 2×2 rate matrix with transition rate k given by Kramers' escape rate: k ≈ (√(V''(x_min)|V''(0)|) / 2π) · e^(−ΔV/D), where ΔV is the barrier height
- μ' = (½, ½) for the symmetric case

**What is preserved under this coarse-graining**:
- Boundary structure: the barrier at x = 0 — a low-conductance cut in the fine-grained T — maps directly to the transition rate k in T'. Low k means a strong boundary; high k means a weak one.
- Stability structure: the two wells (energy minima, stable states of T) map to the two states of T'
- The spectral gap of the fine-grained Fokker-Planck operator equals the transition rate k of the coarse-grained system — demonstrating formally that the spectral boundary concept and the coarse-grained description are measuring the same structure

**What this demonstrates**: a specific, constructive map from (S, T, μ) to (S', T', μ') where boundary structure is preserved and derivable. The procedure is: identify metastable states via the spectral gap, define S' as the set of metastable states, derive T' via Kramers' rate, derive μ' as the stationary distribution of T'. This is the template the framework's constructive coarse-graining would follow at each scale — though deriving analogous procedures for biological and cognitive systems remains the open problem.

---

### Positioning These Directions

These three open directions form a coherent research program:

1. **μ-weighted Φ** extends the awareness formalization to account for realized rather than possible dynamics — making the integration measure context-sensitive in the way biological awareness appears to be.

2. **Constructive coarse-graining** would close the framework's main mathematical gap — providing explicit procedures for deriving coarser descriptions from finer ones rather than asserting that such procedures exist.

3. **Spectral boundary formalization** would make the framework's central concept — the boundary as maintained differential — a computable property of the triple, grounding the philosophical claims in measurable mathematics.

None of these is speculative. Each has an established mathematical home. The framework's contribution is to have located them as the specific gaps that, when filled, would make its cross-scale claims formally complete rather than philosophically coherent.

---


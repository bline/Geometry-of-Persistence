# Geometry of Persistence

## What This Is

Geometry of Persistence is a cross-scale framework for understanding how structures form, persist, and dissolve — from subatomic particles to cells, neurons, cognitive systems, and societies. It uses a single formal object across all scales rather than introducing separate explanatory frameworks for physics, biology, and cognition.

The central claim is that what we call a boundary — the edge of an atom, the membrane of a cell, the self-model of a brain — is not a structure but a maintained differential: a region where transition rates between states drop sharply, actively sustained against the tendency toward equilibrium. Everything the framework explains follows from this claim and its formalization.

The project is a working framework in active development. It is honest about what has been derived, what has been established by consistency with existing theory, and what remains genuinely open.

---

## Core Concept

Reality is described at every scale by a triple **(S, T, μ)**:

- **S** — a state space of all mathematically definable configurations
- **T** — a transition semigroup specifying which state changes occur and at what rate
- **μ** — a measure over S representing which states are physically realized

A **boundary** is a region of low connectivity in T under μ — where transition rates between two parts of S are low relative to internal rates within each part. A **self** is a nearly-invariant set of the transfer operator at the relevant timescale — a set of states the system tends to remain within. **Stability** ranges across three regimes: structural (symmetry exclusions, where μ = 0), energetic (passive minima), and dynamic (process-maintained, far from equilibrium).

Larger scales are coarse-grained descriptions of the same triple — the same formal object at lower resolution, preserving boundary structure, stability structure, and recursion structure across the projection.

---

## Document Map

### Foundations

**`01_framework_core.md`**
The core philosophical statement of the framework. Establishes the process view, the boundary concept, the three stability regimes, the account of self and awareness, the hard problem treatment, and the multi-scale constraint layer analysis. Start here for the conceptual foundation.

**`02_formal_triple.md`, `03_formal_extensions.md`, and `04_open_frontiers.md`**
The formal development. Defines the triple (S, T, μ) precisely, specifies the coarse-graining mechanism across scale transitions, formalizes boundary as spectral gap and conductance, introduces the adaptive triple T_t = F(μ_{0:t}), develops the predictive self-model formalization, and locates the framework's open frontiers. The most technically developed document in the project.

**`05_scale_atomic.md`**
The atomic worked case, now including the Pauli antisymmetry derivation and the quantum boundary-type distinction (symmetry vs energetic boundaries) integrated directly into the scale document.

---

### Scale Progression

The framework is developed concretely through worked cases at each scale. Each case applies the triple's vocabulary — state space, transition structure, measure, boundary, energy flow, recursion, decay — to a specific system.

**`05_scale_atomic.md`** — *Atomic scale*
Hydrogen as the simplest stable constraint configuration. Helium introducing Pauli exclusion as internal symmetry geometry. Chemical reactivity as availability of high-rate transitions to more stable configurations. The framework's clearest regime: exact geometry, computable boundaries, precise decay.

**`06_scale_biological.md`** — *Biological scale: theory*
The transition from passive to dynamic stability. Three boundary regimes defined and distinguished. Life as constraint geometry sustained through ongoing work rather than resting in equilibrium. Dissipative structures, entropy export, and the recursive loop as structural necessity. The multi-scale constraint layer analysis: neural, behavioral, social, ecological.

**`07_scale_cell_membrane.md`** — *Biological scale: worked case*
The sodium-potassium pump as directed transition constraint. The electrochemical gradient as maintained differential in state space — the boundary as gradient, not as membrane. ATP cycle as entropy export. Failure modes as specific, predictable disruptions of the recursive loop. The cleanest biological demonstration of the framework's boundary definition.

**`08_scale_neuron.md`** — *Neural scale*
State-dependent constraint geometry: voltage-gated channels that reconfigure available transitions as the system moves through S. The action potential as partial, localized reduction of the dynamic boundary — controlled gradient dissipation as signaling. The refractory period as self-limiting effective geometry. Network-level constraint geometry as geometry of geometries.

**`09_scale_cognitive.md`** — *Cognitive scale*
Network S_net as coarse-grained projection of S. Attractor formation through Hebbian plasticity: the Hopfield derivation connecting synaptic weights to an energy function, with attractors as its minima. Memory as attractor structure. External constraint coupling. The self-model as recursively active attractor — existence itself deepening the basin. Global constraint integration as the awareness candidate. The hard problem located precisely and honestly left open.

---

## Reading Paths

**For a philosophical overview**: `01_framework_core.md` alone gives the full conceptual scope.

**For the formal structure**: `02_formal_triple.md`, `03_formal_extensions.md`, and `04_open_frontiers.md` — the triple definition, coarse-graining mechanisms, spectral boundary formalization, adaptive triple, predictive self-model, and located open directions.

**For the scale progression**: read in order `05_scale_atomic.md` → `06_scale_biological.md` → `07_scale_cell_membrane.md` → `08_scale_neuron.md` → `09_scale_cognitive.md`.

**For the hardest questions**: the awareness section and epiphenomenon treatment in `02_formal_triple.md`, `03_formal_extensions.md`, and `04_open_frontiers.md`, and the hard problem section in `09_scale_cognitive.md`.

---

## Current Status

### Established
- The triple (S, T, μ) as a unified formal object instantiated at each scale
- Boundary as maintained differential — spectral gap and conductance as formal apparatus
- Three stability regimes: structural, energetic, dynamic
- Coarse-graining preserving boundary, stability, and recursion structure across scale transitions
- Attractor formation from the Hopfield derivation as existence proof
- The adaptive triple T_t = F(μ_{0:t}) unifying learning, adaptation, and evolution
- Predictive self-model formalization with specified combination function g and trajectory conductance metric C(t)
- Self as nearly-invariant set — computable from (S, T, μ) at any scale

### Partially Established
- Thermodynamic-biological transition via timescale separation — grounded in existing theory, not fully derived
- Biological-cognitive transition — existence proof via Hopfield, not universal derivation
- Global constraint integration Φ_global as awareness candidate — formally located, not yet operationally measured

### Open Frontiers
- **Constructive coarse-graining**: a procedure taking specific fine-grained (S, T, μ) to specific coarse-grained (S', T', μ'). Templates exist (renormalization group, Mori-Zwanzig, information-theoretic compression). No universal procedure yet.
- **Spectral boundary as core content**: spectral gap and conductance are candidates for promotion from open direction to central formalism.
- **μ-weighted Φ**: refining the integration measure to weight by realized rather than possible dynamics, using metastable-window μ.
- **Constraints on F**: specifying the admissible class of adaptive rules beyond causality, physical realizability, and temporal locality.
- **Predictive self-model worked example**: a toy reactive vs. predictive two-basin system demonstrating measurable boundary stability differences under perturbation.
- **Empirical testing**: trajectory conductance profiles in neural systems, comparing self-modeling and non-self-modeling systems under equivalent perturbation.
- **Social scale**: the upward extension to language, norms, institutions, and cultural attractor structures — cognitive systems whose internal geometry models other cognitive systems.

---

## What This Is Not

The framework is not a finished theory. It is a structured set of claims at different levels of derivation, with honest accounting of what has been established and what has not.

It is not a metaphor. The formal apparatus — state space, transition semigroup, measure, spectral gap, conductance, coarse-graining — is drawn from established mathematics. The philosophical claims are grounded in or consistent with existing physics, biology, and neuroscience.

It is not a completion of the hard problem of consciousness. The framework locates the hard problem precisely within the triple's structure and offers a formally stated candidate property (global constraint integration) and a competing reading (epiphenomenalism). It does not resolve the question — but it converts it from a philosophical impasse into a specific empirical and formal problem.

---

## How to Engage

The framework welcomes pressure at its specific load-bearing points:

- Is the coarse-graining claim strong enough to carry the continuity argument across scales?
- Does the Hopfield existence proof establish enough for the cognitive scale claims?
- Is the functional reading of awareness testable by the trajectory conductance metric?
- Does the adaptive triple handle the circularity between γ and M_t?

These are the questions the framework generates, acknowledges, and has not yet answered. They are where the most useful engagement goes.

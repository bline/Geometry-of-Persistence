# Formal Extensions

This document is extracted from the former `formal_gaps_coarsegraining.md` and contains formal extensions built on the core triple.

---
## Spectral Formalization of Boundaries — A Candidate for Core Content

The current boundary definition — regions of low connectivity in T under μ — is conceptually precise but not yet operational. Two established mathematical tools formalize it directly. These are not peripheral refinements: because they formalize the framework's central concept in computable terms, they are candidates for promotion from open directions to core framework content. The boundary as maintained differential is the framework's most distinctive claim; spectral gap and conductance are what that claim looks like when given a mathematical address.

**Spectral gap**: for a continuous-time generator L with stationary distribution μ, the spectral gap λ₁ is the smallest nonzero eigenvalue of −L. It measures how quickly the system mixes — how fast trajectories starting from different points in S converge to μ. A small spectral gap means slow mixing, which means the system is effectively trapped in a region of S for long periods. Boundaries in the framework's sense correspond to cuts that separate slowly-mixing regions: on either side of a boundary, the system mixes quickly internally but crosses slowly.

Formally, a boundary between regions A and Aᶜ exists where the **conductance** Φ(A) is low:

> Φ(A) = [∫_{A × Aᶜ} T_t(s'|s) μ(ds) ds'] / min(μ(A), μ(Aᶜ))

Conductance is the ratio of cross-boundary flux to the smaller of the two region measures. Low conductance means the boundary is effective — little flux crosses relative to the size of the regions it separates. The **Cheeger inequality** connects conductance to spectral gap: λ₁/2 ≤ Φ_min ≤ √(2λ₁), where Φ_min is the minimum conductance over all cuts. This means boundaries (low conductance cuts) and slow mixing (small spectral gap) are formally equivalent up to a factor of 2.

**Metastability criteria**: for systems with multiple metastable states — like neural networks with multiple attractor basins — the relevant formalization is the spectrum of the transfer operator. Metastable states correspond to nearly-invariant sets: regions A where T_t(A|A) ≈ 1 for long times t. The number of metastable states is related to the number of eigenvalues of the transfer operator near 1. Transitions between metastable states are the rare events that cross boundaries.

These tools — spectral gap, conductance, metastability spectrum — provide the formal apparatus for making boundary detection a computable property of (S, T, μ) rather than a qualitative judgment. They are directly applicable to the neural and cognitive scales where boundaries are attractor basin separatrices, and in principle applicable to the thermodynamic scale where boundaries are free energy barriers.

**A cleaner definition of self in spectral terms**: the spectral formalization yields a more precise statement of what the framework means by self than the qualitative description in earlier documents. A self, in spectral terms, is a set of states that are recurrent within a specified timescale — a nearly-invariant set of the transfer operator at the relevant temporal resolution. This is not a metaphor. It is a computable property of (S, T, μ): given the system's transition semigroup and realized distribution, identify the sets A where T_t(A|A) ≈ 1 for timescales t relevant to the system's operation. Those sets are the framework's selves — at whatever scale and resolution the analysis is conducted.

This definition is scale-invariant in exactly the way the framework requires: a proton is a nearly-invariant set at nuclear timescales, a cell is a nearly-invariant set at metabolic timescales, a cognitive self-model is a nearly-invariant set at neural timescales. The word "self" names the same structural property — recurrence within a timescale — instantiated at different scales with different (S, T, μ).

---

## The Epiphenomenon Question

The framework's treatment of awareness — as dense recursive reflection of constraint geometry, the geometry modeling its own propagation — currently leaves open whether this modeling is a functional requirement for more complex stability or a byproduct of high-density recursion with no causal role of its own. This is the epiphenomenon question, and it deserves explicit treatment rather than deferral.

**The epiphenomenal reading**: awareness is what high-density recursive constraint geometry looks like from inside — a description with no additional causal power. The self-model is produced by the boundary-maintenance process and reinforces it, but the reinforcement is already captured by the constraint dynamics. Adding "awareness" as a separate category contributes nothing to the explanation that the constraint geometry doesn't already contain.

**The functional reading**: the self-model has causal utility within the framework's own terms. Specifically, a system that models its own boundary-maintenance process can adjust that process in response to modeled future states — it can anticipate perturbations rather than merely respond to them. In the triple's terms: a system with a self-model has a T that is conditioned not just on current state s but on a representation of future states reachable from s. This is a different transition structure from one without self-modeling, and it produces different stability properties — specifically, the ability to select trajectories through S_net that avoid low-conductance cuts before reaching them.

If the functional reading is correct, awareness is not epiphenomenal — it is the mechanism by which sufficiently complex dynamic boundary systems extend their stability into the future rather than merely maintaining it in the present. The self-model earns its place in the framework by doing causal work that the constraint geometry without self-modeling cannot do.

**What the framework can currently say**: the functional reading is consistent with the triple's structure and does not require additional primitives. Whether it is correct — whether self-modeling actually produces the stability advantages described — is an empirical question that the framework generates as a specific, testable prediction: systems with recursive self-models should exhibit greater long-run boundary stability under perturbation than systems of equivalent complexity without self-modeling. That prediction is derivable from the framework and addressable by existing neuroscience and adaptive systems research.

The epiphenomenal reading cannot be ruled out on formal grounds alone. But the functional reading is now stated precisely enough that it can be tested rather than merely asserted. That is the honest current position.

---

## Positioning These Directions

These three open directions form a coherent research program:

1. **μ-weighted Φ** extends the awareness formalization to account for realized rather than possible dynamics — making the integration measure context-sensitive in the way biological awareness appears to be.

2. **Constructive coarse-graining** would close the framework's main mathematical gap — providing explicit procedures for deriving coarser descriptions from finer ones rather than asserting that such procedures exist.

3. **Spectral boundary formalization** would make the framework's central concept — the boundary as maintained differential — a computable property of the triple, grounding the philosophical claims in measurable mathematics.

None of these is speculative. Each has an established mathematical home. The framework's contribution is to have located them as the specific gaps that, when filled, would make its cross-scale claims formally complete rather than philosophically coherent.

---

## The Adaptive Triple: Learning as T Evolving Under μ

The static triple (S, T, μ) describes a constraint geometry at a given moment. But one of the framework's most important claims — that dynamic boundary systems can adapt, learn, and extend their stability — requires T itself to change over time based on the history of realized states. This is the **adaptive triple**: a time-evolving (S, T_t, μ_t) where the transition structure and the realized distribution co-evolve.

**The formal object**

Define the adaptive triple as:

> T_t = F(μ_{0:t})

where F is a functional mapping the history of the realized distribution up to time t to the current transition structure. T_t and μ_t are mutually dependent: T_t shapes which states are realized under μ_t, and μ_{0:t} shapes what T_t becomes. The system is no longer time-homogeneous — the transition structure is itself a dynamical object.

**What this unifies**

The adaptive triple is a single formal object that subsumes four phenomena currently described at different scales in the framework:

*Hebbian learning* (cognitive scale): T_net evolves as ΔWᵢⱼ ∝ ⟨sᵢ sⱼ⟩_{μ} — synaptic weights, which define T_net, are modified by correlations in the realized distribution μ_net. This is already in the framework's cognitive scale document. The adaptive triple names it formally.

*Homeostatic adaptation* (biological scale): a cell's transport geometry — the density and sensitivity of pumps and channels — shifts in response to chronic patterns of ion flux. Cells experiencing sustained high sodium influx upregulate sodium-potassium pump expression, shifting T toward stronger restoration of the electrochemical gradient. This is T_t = F(μ_{0:t}) at the metabolic timescale.

*Developmental plasticity*: over longer timescales, gene expression patterns — which determine what proteins are produced, and therefore what transition constraints exist — are modified by the history of cellular activity. Chromatin remodeling, epigenetic modification, and transcriptional regulation all represent F operating at developmental timescales.

*Evolutionary adaptation* (population scale): the distribution of constraint geometries across a population shifts based on which configurations survived under environmental selection — which realized states were compatible with continued existence. Evolution is F operating at generational timescales, with the population's transition structure (the distribution of heritable constraint geometries) shaped by the history of which μ values persisted.

All four are F(μ_{0:t}) with different timescales, different mechanisms for F, and different scopes of what counts as the relevant history. The formal object unifies them without collapsing their differences.

**Closing the loop between active stability and learning**

The cell's active stability and the brain's learning now share a formal description. Both are cases where the constraint geometry is modified by the history of realized states:

- The cell's pump expression adjusts to chronic metabolic load: T_biological_t = F(μ_{metabolic, 0:t})
- The brain's synaptic weights adjust to chronic activity patterns: T_cognitive_t = F(μ_{neural, 0:t})

The difference is not in the formal structure but in the timescale of F's operation and the mechanism by which T changes. This connects the biological and cognitive scales not just analogically but through the same formal object operating at different resolutions.

**The approximation conditions**

Introducing a time-evolving T_t requires specifying when the framework's existing spectral tools — spectral gap, conductance, metastability criteria — remain applicable. These tools were developed for time-homogeneous processes where T does not change. They apply to the adaptive triple under one condition:

> The timescale of T's evolution must be long relative to the timescale of mixing within the current T_t.

Formally: if τ_mix is the mixing time of the current T_t (related to the inverse spectral gap) and τ_adapt is the timescale over which T_t changes appreciably, the quasi-static approximation holds when τ_mix ≪ τ_adapt. Under this condition, the system behaves as approximately time-homogeneous over short intervals, and spectral analysis of T_t at any given time yields valid information about boundaries and metastable states.

For most biological and cognitive systems this condition is satisfied across relevant timescales:
- Neural firing (milliseconds) is fast relative to synaptic weight changes (minutes to hours): τ_mix ≪ τ_adapt ✓
- Ion channel kinetics (milliseconds) are fast relative to pump expression changes (hours to days): τ_mix ≪ τ_adapt ✓
- Developmental changes (days to years) are slow relative to metabolic dynamics (seconds): τ_mix ≪ τ_adapt ✓

Where the condition fails — near critical transitions, during rapid learning, or during developmental phase changes — the quasi-static approximation breaks down and a full time-inhomogeneous treatment is required. The theory of time-inhomogeneous Markov processes handles this but is significantly more complex. The framework marks this as a further open direction rather than a solved problem.

**What constrains F**

As stated, F is a completely general functional — any mapping from history of μ to current T is permitted. This generality makes the adaptive triple flexible but physically unconstrained. Three natural constraint classes narrow F to a physically realistic object:

*Causality*: T_t can only depend on {μ_s : s ≤ t}. The transition structure at time t cannot be shaped by future realized states. This is non-negotiable and already implicit in the definition — made explicit here because it rules out a class of formally possible but physically unrealizable F.

*Physical realizability*: changing T requires physical work. At the biological scale, modifying the transition structure means synthesizing new proteins, remodeling synaptic connections, or modifying gene expression — all of which consume energy and material resources. F is therefore bounded: the rate of change of T cannot exceed what the system's metabolic budget allows. A cell cannot remodel its entire pump architecture in a millisecond; a neuron cannot rewire its synaptic connections in the time between action potentials. The metabolic constraints on T's evolution are the same constraints that govern boundary maintenance generally — they appear here as limits on how fast the adaptive triple can respond to changes in μ.

*Temporal locality*: biological memory decays. F is unlikely to weight distant history equally with recent history. The simplest physically motivated assumption is exponential decay of influence: recent μ shapes T_t strongly, distant μ weakly. This produces a F that is effectively a weighted integral of past μ with decaying kernel — mathematically an exponential moving average of the realized distribution. Different biological systems have different decay timescales: synaptic plasticity decays over hours to days, gene expression changes over days to weeks, evolutionary selection over generations.

These three constraints — causality, physical realizability, temporal locality — convert F from an arbitrary functional into a constrained class of physically realistic adaptive rules. Each is independently falsifiable: systems that violate causal structure, that change T faster than their metabolic budget allows, or that show equal sensitivity to ancient and recent history are making predictions the framework rules out.

**Formalizing the predictive component**

The claim that self-modeling systems have a T_t conditioned on anticipated future states requires separating T_t into two formal components.

Let M_t be the self-model — a representation within S_net of the system's own dynamics, formed as an attractor in the cognitive scale's constraint geometry. M_t generates a predictive distribution:

> P_M(μ_{t:t+τ} | s_t, M_t)

— the system's estimate of future realized states over a horizon τ, given current state s_t and current self-model M_t.

The transition structure of a self-modeling system then has two components:

> T_t(s' | s) = g(T_reactive(s' | s), T_predictive(s' | s, M_t))

where:
- **T_reactive** is the reactive component: F_reactive(μ_{0:t}) — shaped by past realized states, identical in form to the non-self-modeling adaptive triple
- **T_predictive** is the predictive component: shaped by P_M(μ_{t:t+τ} | s_t, M_t) — selecting transitions that minimize expected future boundary dissolution under the self-model's predictions
- **g** is a combination function weighting the two components

The predictive component connects the adaptive triple to optimal control theory: the self-modeling system selects T modifications that maximize expected long-run boundary stability under its own predictive distribution. This is a precise, derivable claim — not a qualitative observation about self-awareness — and it generates a specific prediction: self-modeling systems should select trajectories through S that avoid anticipated low-conductance cuts, producing measurably greater long-run boundary stability than reactive-only systems of equivalent complexity.

The non-self-modeling system has only T_reactive. It responds to boundary failures after they occur, shaped by the history of what has been realized. The self-modeling system additionally has T_predictive — it shapes T based on what it anticipates will be realized. This formal difference, derivable from the adaptive triple and the self-model attractor structure, is what makes awareness functional rather than epiphenomenal in the framework's own terms.

**Specifying g: how reactive and predictive components combine**

The combination function g is a modeling choice that requires at least a candidate specification. A physically motivated candidate treats T_predictive as a modifier on T_reactive rather than an independent component with arbitrary weight:

> T_t(s'|s) = T_reactive(s'|s) · exp(γ · ΔΦ_M(s, s')) / Z

where:
- ΔΦ_M(s, s') is the predicted change in long-run boundary survival probability moving from state s to state s', under the self-model's predictive distribution P_M. Formally: ΔΦ_M(s, s') = E_M[σ(τ | s')] − E_M[σ(τ | s)], where σ(τ | s) is the probability of surviving — maintaining the dynamic boundary — for duration τ starting from state s, estimated under M_t. This is the primary interpretation. Two natural approximations are available when long-run survival probability is difficult to compute: expected change in local conductance Φ(A_{s'}) − Φ(A_s) between the metastable basins containing s' and s, and expected change in distance from boundary-dissolution states under the trajectory distribution. The long-run survival probability is the most directly relevant to the framework's claims; the conductance approximation is more computationally tractable.
- γ is a gain parameter controlling how strongly predictive information modifies the reactive baseline
- Z is a normalization constant ensuring T_t remains a valid probability distribution

When ΔΦ_M = 0 — the self-model predicts no difference in boundary stability across available transitions — T_t reduces to T_reactive. When ΔΦ_M is large and positive, T_t up-weights the safer transition. The predictive component dominates when M_t is accurate, when predicted boundary threats are severe, and when γ is high.

γ itself can be adaptive — a function of past prediction accuracy. A self-model that has been consistently accurate earns higher γ; one that has been consistently wrong earns lower γ. This produces a natural regulation of how much the system trusts its own predictions, grounded in the same adaptive triple mechanism.

**P_M accuracy and learning**

The predictive distribution P_M must be learned and updated. M_t is updated based on prediction errors — the discrepancy between P_M(μ_{t:t+τ} | s_t, M_t) and the actually realized μ_{t:t+τ}. This update is Bayes-like in character: new evidence from realized states shifts M_t toward configurations that would have predicted the realized μ better. Calling it a full Bayesian update would require specifying the hypothesis space, priors, and likelihood structure over self-models — a commitment the framework does not yet make. What the framework does claim is that M_t's attractor basin is shaped by the history of prediction errors through the same adaptive triple mechanism that shapes all other attractors: configurations that consistently produce accurate predictions deepen their basin; configurations that consistently produce large errors shallow theirs. In the adaptive triple's terms, M_t is an attractor in S_net updated by F(accuracy_{0:t}) — the same functional form as the general adaptive rule, applied to prediction performance rather than co-activation patterns.

How accurate must P_M be? The framework gives a relative answer: P_M must be accurate enough that T_predictive produces better expected boundary stability than T_reactive alone over horizon τ. This generates a specific prediction: self-modeling is maintained only when it improves boundary stability. A self-model that consistently mispredicts provides no advantage through T_predictive. The framework predicts such a model would degrade — its attractor basin shallowing through accumulation of large prediction errors — exactly as an unused memory attractor shallows through disuse. Self-modeling that does not improve stability is self-undermining within the adaptive triple's own dynamics.

This connection to Bayesian inference and model-based reinforcement learning is not an external import. It follows from applying the adaptive triple mechanism to M_t itself: the self-model is an adaptive structure, updated by the same F(μ_{0:t}) logic, where the relevant μ is the distribution of prediction errors rather than the distribution of environmental states.

**A measurable metric for boundary avoidance**

The claim that self-modeling systems avoid anticipated low-conductance cuts needs a computable quantity to become testable. Define the **trajectory conductance profile** as the time series of conductance values measured at each state the system actually occupies:

> C(t) = Φ(A_{s_t})

where A_{s_t} is the metastable basin containing s_t — identified by the spectral decomposition of the transfer operator as a nearly-invariant set at the relevant timescale — and Φ(A_{s_t}) is the conductance of that basin's boundary cut. The restriction to spectrally identified metastable basins is necessary: minimizing over all sets A containing s_t is ill-posed, as almost any state can belong to arbitrarily constructed subsets with pathological conductance values. Restricting A to nearly-invariant sets identified by the leading eigenvectors of the transfer operator produces a well-defined, computable metric grounded in the framework's existing spectral tools.

C(t) is then a scalar function of time computable from (S, T, μ) and the system's actual trajectory, measuring how safely embedded the system is within its current metastable basin at each moment.

Three measurable predictions follow from the functional reading of awareness:

*Mean trajectory conductance*: self-modeling systems should maintain higher average C(t) than reactivity-matched non-self-modeling systems under equivalent perturbation. The self-model up-weights transitions toward high-conductance regions; without it, the system is driven by reactive dynamics alone.

*Variance of trajectory conductance*: self-modeling systems should show lower variance in C(t) — fewer near-misses with low-conductance regions. The predictive component provides advance warning of dangerous regions; without it, the system encounters them at the same rate as perturbation drives it there.

*Trajectory-conductance correlation*: self-modeling systems should show that their actual trajectories correlate with the high-conductance landscape of S_net — computable by comparing the sequence of states visited against the conductance map of the state space. A system that consistently moves toward higher conductance is demonstrating predictive boundary avoidance; one that moves randomly relative to conductance is not.

The third prediction is the most specific and hardest to dismiss: it requires detecting that the system's path through state space preferentially avoids low-conductance regions, which is detectable in neural systems by tracking firing patterns relative to estimated attractor basin boundaries — a measurement within the reach of current high-density neural recording technology.

---






# Worked Case: The Cognitive Scale

## Purpose

This is the framework's worked case at the cognitive scale. Nothing new is added to the physics. The same constraint geometry operates — the same ion gradients, the same voltage-gated channels, the same action potentials established in the neuron case. What changes is scale and organization: many dynamic boundaries coupled together, their collective state encoding something about the constraint geometry in which they are embedded.

Cognition is not introduced here as a new phenomenon. It is built step by step from constraint interactions that the previous cases have already established.

---

## 1. From Single Neuron to Network: Geometry of Geometries

A single neuron maintains a dynamic boundary and transmits state changes through partial, localized reductions in that boundary. This is the full extent of what the neuron case established.

A network of neurons adds one thing: the state of each dynamic boundary becomes a constraint on the transitions available to connected boundaries. Each neuron's firing or not-firing shapes the inputs arriving at downstream neurons, shifting their membrane potentials, making their own threshold crossings more or less likely.

**In framework terms**: a neural network is a constraint geometry whose elements are themselves dynamic boundaries. The state of the network at any moment is a configuration in S — the same continuous state space the framework has used throughout, now described at a coarser resolution. S_net is not a new or separate space. It is a coarse-grained projection of the same underlying geometry, described at the scale where activation patterns across neurons are the tractable description rather than individual ion movements.

Let S_net denote this coarse-grained resolution of S. A configuration in S_net is:

- The current membrane potential of every neuron
- The firing state of every neuron (at threshold, below, recovering)
- The synaptic weight connecting every pair of neurons — the strength of the transition constraint between them

The synaptic weights are the constraint geometry of S_net. They determine which activation patterns are accessible from which others, at what cost, with what probability. A strong excitatory connection between neurons A and B means that A firing makes B's threshold crossing more likely — it lowers the transition cost from "B silent" to "B firing" in S_net. A strong inhibitory connection does the reverse.

**The network's constraint geometry is therefore the full matrix of synaptic weights** — a high-dimensional structure that shapes which trajectories through S_net are available, which regions are stable, and which patterns tend to persist or recur.

---

## 2. Attractor Formation: How Structure Emerges in S_net

The network's constraint geometry is not fixed at birth. It changes as the network operates. The mechanism is Hebbian plasticity — the synaptic weight between two neurons strengthens when they fire together repeatedly, and weakens when they do not.

> Neurons that fire together, wire together.

In framework terms: correlated activity across a subset of neurons repeatedly drives the network through a specific region of S_net. Each traversal slightly deepens the transition constraints along that path — strengthening the synaptic weights that connect the co-active neurons, making the same trajectory more accessible next time.

The result is an **attractor**: a region of S_net toward which the network tends to move from nearby configurations, and in which it tends to remain once arrived. The attractor is carved into S_net by repeated traversal — not imposed from outside but emerging from the constraint geometry's response to its own activity history.

**What an attractor looks like in S_net**:

- A specific pattern of neural activity — a subset of neurons firing together
- A basin of attraction — nearby configurations in S_net that are drawn toward this pattern
- Resistance to perturbation — small disruptions to the pattern are corrected by the network's own constraint geometry
- Recoverability — after sufficient perturbation, the network may leave the attractor basin but can return

The attractor is not a location in physical space. It is a stable region of activation-pattern space — a configuration the network's constraint geometry has made persistently accessible. Multiple attractors can coexist in the same network, separated by transition barriers in S_net.

---

## 3. Memory as Attractor Structure

Memory, in the framework's terms, is attractor structure in S_net.

When a pattern of external input repeatedly drives the network through a specific region of S_net, Hebbian plasticity deepens the attractor basin for that region. The pattern becomes more easily recoverable — partial input is sufficient to drive the network toward the full attractor state, and the state persists after the input is removed.

This is recognition memory: the external constraint geometry has shaped the internal constraint geometry such that certain configurations in S_net correspond to — and are reachable by — certain external conditions. The correspondence is not imposed. It emerges from the constraint interaction between external input and internal plasticity.

**In framework terms**: memory is the external constraint geometry leaving a trace in the internal constraint geometry. The trace is structural — a deepened attractor basin — not a stored representation in the sense of a discrete record. Retrieval is not reading from storage. It is the network being driven into the attractor basin by a partial cue and settling into the stable configuration the basin defines.

Forgetting is the attractor basin shallowing — either through disuse (weights weakening without reinforcement) or through interference (new attractor formation disrupting existing basin geometry). It is constraint geometry changing, not records being erased.

**What this does not yet explain**: how the network comes to have states that are *about* external conditions rather than merely *caused by* them. An attractor that forms in response to repeated exposure to a particular input is shaped by that input — but is that the same as representing it? This is the first point where the framework must be careful not to overreach. The attractor structure established here is a necessary condition for cognition. Whether it is sufficient is a question the framework will return to.

---

## 4. External Constraint Coupling: Tracking Environmental Structure

The attractor formation account explains how internal structure develops. What makes that structure cognitive rather than merely reactive is that it systematically tracks external constraint geometry.

A thermostat responds to temperature. Its internal state changes with the environment, and it exhibits simple attractor dynamics — it tends toward a set point and returns after perturbation. But it has no plasticity and no history-dependent constraint geometry. Each response is identical regardless of past responses. It reacts but does not accumulate structure from its own activity history.

A neural network with attractor structure does something different: repeated exposure to correlated external patterns carves internal attractor geometry that reflects the statistical structure of those patterns. The network does not merely respond to current input — its constraint geometry encodes the history of past inputs as attractor structure, and uses that structure to shape responses to new inputs.

**In framework terms**: external constraint coupling at the cognitive scale means that the network's internal S_net geometry systematically corresponds to structure in the external constraint geometry. The attractors carved by experience are not arbitrary — they reflect recurring patterns in the environment. The internal geometry tracks the external geometry through the mechanism of history-dependent plasticity, without that tracking requiring any additional mechanism beyond constraint interaction.

This is the minimal definition of cognition the framework can support: **a dynamic boundary system whose internal attractor structure systematically corresponds to external constraint geometry through history-dependent plasticity**.

It does not require experience, qualia, or awareness. It requires only that the internal constraint geometry be shaped by the external constraint geometry in a structured, recoverable way. A well-trained neural network — biological or artificial — satisfies this definition. Whether it satisfies more than this is the harder question.

---

## 5. The Self-Model: A Recursive Attractor

The framework's account of the cognitive self — established in the main document — can now be built from the concepts developed here.

The brain is a neural network with attractor structure. Among the patterns repeatedly encountered by this network is the pattern of the organism's own boundary-maintenance activity — proprioceptive signals, interoceptive signals, the ongoing sensory consequences of the organism's own actions. These patterns drive attractor formation just as external patterns do.

The result is an **attractor that corresponds to the organism's own dynamic boundary** — a stable configuration in S_net that is reached when the network processes information about its own state. This is the base self in attractor terms: a region of S_net that the network tends toward when modeling its own boundary.

What makes this specifically a self-model rather than just another attractor is recursion: the self-model attractor is part of the constraint geometry that shapes the network's own dynamics. The network's model of its boundary influences how the network maintains its boundary. The attractor is not merely a passive representation — it is an active component of the boundary-maintenance process.

**In framework terms**: the self-model is a recursively active attractor. It is stable because the network's constraint geometry reinforces it — and it reinforces the constraint geometry that stabilizes it. The self-model and the boundary-maintenance process are mutually sustaining, in the same way that the metabolic loop in the cell case was mutually sustaining. The recursion is structural, not incidental.

This explains a property of self-models that is otherwise puzzling: they are highly resistant to revision. The attractor basin for the self-model is deepened not only by past experience but by ongoing boundary-maintenance activity. Every moment of continued existence reinforces the self-model attractor — the organism's boundary-maintenance processes continuously generate the signals that drive the network back toward the self-model configuration. The model is hard to revise not because revision is blocked but because existence itself deepens the basin. The constraint geometry of being alive continuously regenerates the conditions for the attractor that models being alive.

---

## 6. The Hard Question: What Distinguishes Awareness

The framework can now state the hard question precisely.

Everything established so far — attractor structure, external constraint coupling, recursive self-model — is in principle achievable by a sufficiently complex artificial neural network. The framework's account of cognition, memory, and self-model does not by itself distinguish between a system that has these properties and experiences something, and a system that has these properties and experiences nothing.

This is not a failure of the framework. It is the hard problem of consciousness stated in the framework's own terms: **what additional property of constraint geometry, if any, distinguishes configurations that produce awareness from configurations that do not?**

The framework's existing vocabulary points toward one unifying candidate: **the degree of global constraint integration in S_net** — the extent to which the network's collective state forms a coherent, system-wide constraint on its own subsequent transitions rather than a collection of loosely coupled local attractors.

This single property subsumes the three candidates often proposed separately:

Integration — the degree to which constraint interactions are global rather than local — is one dimension of it. Recursion depth — the number of levels at which the network models its own modeling process — is another, since deep recursion requires globally integrated states to sustain. Global constraint coupling — the network's collective state shaping all of its own subsequent transitions — is what the property directly describes.

Together these are not three separate conditions but three ways of measuring the same underlying feature: how globally coherent the constraint geometry of S_net has become. A network whose collective state is a globally integrated constraint on its own dynamics is doing something qualitatively different from a network of modular attractors operating in parallel. Whether that difference produces awareness, or merely correlates with the systems that have it, is the question the framework cannot yet resolve.

This is the boundary of the framework's current reach at the cognitive scale. It is the same honest boundary drawn at the framework's origin: description finds its limit where the transition differential becomes absolute. Here, the transition between constraint configurations that produce awareness and those that do not is the differential the framework cannot yet resolve.

---

## 7. What the Framework Has Built at This Scale

Working from single neurons to networks to attractors to self-models, the framework has constructed cognition without importing mentalistic primitives:

**Network constraint geometry**: synaptic weights define the effective constraint geometry of S_net — which activation patterns are accessible, at what cost, with what probability.

**Attractor formation**: Hebbian plasticity deepens transition constraints along repeatedly traversed paths, carving stable regions in S_net from the network's own activity history.

**Memory**: attractor structure in S_net — external constraint geometry leaving a structural trace in internal constraint geometry, recoverable through partial cue.

**External constraint coupling**: internal attractor geometry systematically corresponding to external constraint structure through history-dependent plasticity. The minimal definition of cognition.

**Self-model**: a recursively active attractor — a stable configuration in S_net corresponding to the organism's own dynamic boundary, actively participating in the boundary-maintenance process that stabilizes it.

**The hard question**: stated precisely in the framework's terms — what additional property of constraint geometry distinguishes configurations that produce awareness from those that do not — and honestly left open.

---

## 8. The Bridge to the Social Scale

The cognitive scale established that individual neural networks develop internal constraint geometry that systematically tracks external structure. What the social scale adds is that the external structure being tracked includes other cognitive systems.

Each organism with a self-model is, from the perspective of other organisms, a structured component of the external constraint geometry. Other organisms have dynamic boundaries, attractor structures, and self-models. Interacting with them means tracking constraint geometry that is itself tracking you.

This mutual coupling — cognitive systems whose internal constraint geometry models other cognitive systems whose internal constraint geometry models them — is the seed of the social scale. Language, norms, institutions, and culture are the attractor structures that emerge from this recursive mutual coupling at population scale.

The upward extension will follow the same thread: not new physics, not new geometry, but the same constraint interactions operating across a new organizational scale — one where the elements being coupled are themselves cognitive, and where the attractor structures that form span individuals rather than neurons.

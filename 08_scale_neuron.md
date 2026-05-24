# Worked Case: The Neuron and Action Potential

## Purpose

This is the framework's worked case at the neural scale. The neuron is a cell — everything established in the membrane case applies directly. What makes it distinct is a single additional property: its dynamic boundary is not merely maintained but used. The action potential is the dynamic boundary briefly and controllably dissolving and reconstituting, transmitting a state change through the process of its own temporary disruption. This is where the framework's account of information processing begins.

---

## 1. The System

A single neuron — a nerve cell with:

- A **cell body (soma)**: the metabolic center, maintaining the same ion gradients established in the membrane case
- **Dendrites**: branching extensions that receive signals from other neurons
- An **axon**: a long projection along which signals are transmitted
- A **resting membrane potential**: approximately −70mV, maintained by the sodium-potassium pump exactly as described in the membrane case

The neuron inherits the full constraint geometry of the generic cell. Its dynamic boundary — the maintained electrochemical differential — is sustained by the same recursive loop: ion gradients sustain cellular function, cellular function sustains ATP production, ATP production sustains the pump, the pump sustains the ion gradients.

What the neuron adds is a new class of transition constraint: **voltage-gated ion channels** — protein structures that open or close depending on the membrane potential. These channels make the dynamic boundary sensitive to its own state. The boundary can respond to perturbation in a structured, directed way rather than merely resisting it.

---

## 2. State Space

S here is the same quantum-mechanical state space, coarse-grained to the thermodynamic and electrical description relevant at this scale.

A configuration in S is defined by:

- The membrane potential at every point along the neuron's surface
- The state (open, closed, inactivated) of every voltage-gated channel
- The ion concentrations on both sides of the membrane at each location
- The ATP/ADP ratio available for pump operation
- The synaptic inputs currently arriving at the dendrites

**The resting state** is a specific region of S: membrane potential −70mV, most voltage-gated sodium channels closed, potassium channels partially open, pump operating continuously to maintain the gradient. This is the neuron's maintained far-from-equilibrium configuration — not an energy minimum, but a dynamically sustained region of S.

**The action potential** is a specific trajectory through S — a rapid, stereotyped excursion away from the resting state and back. It is not a random fluctuation. It is a directed path through S whose shape is determined by the constraint geometry of the voltage-gated channels. The same trajectory occurs every time, in every neuron, because the geometry of allowed transitions is the same.

**Threshold** is a critical feature of the state space: a region of S from which two very different trajectories are available. Below threshold, small perturbations return the system to the resting state — the geometry is locally self-correcting. Above threshold, the system is committed to the action potential trajectory. The threshold is not a sharp line but a region of S where the balance of constraint forces shifts — where the positive feedback of sodium channel opening overcomes the restoring forces of the resting state.

---

## 3. Constraint Geometry: Voltage-Gated Channels

The voltage-gated sodium channel is the key constraint structure. It exists in three states:

- **Closed**: the channel is shut; sodium cannot cross
- **Open**: the channel is open; sodium flows rapidly inward down its electrochemical gradient
- **Inactivated**: the channel is blocked from inside; sodium cannot cross even though the activation gate is open

The transitions between these states are governed by membrane potential:

- At resting potential (−70mV): channels are predominantly closed
- When membrane potential rises above approximately −55mV (threshold): channels rapidly open
- After ~1ms in the open state: channels transition to inactivated regardless of membrane potential
- During repolarization and below: channels slowly recover from inactivation back to closed

**In framework terms**: the voltage-gated channel is a transition constraint whose allowed transitions depend on the system's current position in S. This is a higher-order constraint — one whose permitted transitions are themselves state-dependent — that the atomic and generic cell cases did not exhibit. The effective constraint geometry becomes state-dependent: as the system moves through S, the available transitions shift with it.

This is the key structural novelty at the neural scale: **state-dependent constraint geometry**. The transitions available to the system depend on where the system currently is. The boundary doesn't just respond to external perturbation — it reconfigures its own transition constraints as it moves.

---

## 4. The Action Potential: A Directed Trajectory Through S

### Initiation

Synaptic inputs arriving at the dendrites perturb the membrane potential — excitatory inputs push it toward zero (depolarization), inhibitory inputs push it further negative (hyperpolarization). The neuron integrates these inputs across space and time.

If the integrated perturbation raises the membrane potential above threshold, the system crosses into the region of S from which the action potential trajectory is accessible. This crossing is the computational event — the moment at which the neuron's dynamic boundary commits to a specific path through S.

### The rising phase

Above threshold, voltage-gated sodium channels open rapidly. Sodium floods inward down its electrochemical gradient — the maintained differential established by the pump now drives a rapid transition. As sodium enters, the membrane potential rises further, opening more sodium channels. This is positive feedback: movement through S accelerates movement further in the same direction.

The membrane potential rises from −70mV to approximately +40mV in less than a millisecond. The maintained differential — high sodium outside, low inside — is briefly and locally collapsing. The dynamic boundary at this location is dissolving.

**In framework terms**: the rising phase is the system using the energy stored in the maintained gradient to drive a rapid, self-amplifying trajectory through S. The gradient that the pump spent continuous energy building is here partially and locally discharged in a directed, controlled way. The dynamic boundary undergoes a transient, localized reduction — not full collapse, but a controlled diminishment that constitutes the signal.

### The falling phase

Sodium channels begin inactivating — their geometry shifts to block further sodium entry regardless of membrane potential. Simultaneously, voltage-gated potassium channels open, allowing potassium to flow outward down its gradient. The membrane potential falls rapidly back toward and briefly below resting potential (hyperpolarization).

The dissolution is reversed. The boundary reconstitutes. The system returns to a region of S near the resting state.

### The refractory period

During and immediately after the action potential, sodium channels are inactivated. A second action potential cannot be initiated regardless of the input. This is the absolute refractory period — a region of S from which the action potential trajectory is geometrically unavailable, not because of external prohibition but because the channel geometry has temporarily reconfigured.

**In framework terms**: the refractory period is a transient structural constraint. The effective constraint geometry temporarily excludes the action potential trajectory, enforcing a minimum interval between signals. The same channel dynamics that enable the action potential also prevent it from firing continuously — the state-dependent geometry self-limits its own most dramatic transition.

---

## 5. Energy Flow and Entropy

The action potential uses the electrochemical gradient built by the sodium-potassium pump. Each action potential allows a small number of ions to cross the membrane — sodium in, potassium out — slightly dissipating the gradient. The pump must subsequently restore the gradient, at the cost of ATP hydrolysis.

The energy accounting is precise:

- Each action potential involves approximately 10⁶ ion movements per cm² of membrane
- The pump requires approximately 1 ATP per 3 sodium ions exported
- A typical neuron firing at moderate rates spends a significant fraction of its total ATP budget restoring gradients after action potentials

**In framework terms**: the action potential is a controlled, directed dissipation of the maintained gradient — entropy exported during the rising phase, gradient restored at metabolic cost afterward. The neuron uses the dynamic boundary it continuously maintains to perform a specific directed trajectory through S, then pays the thermodynamic cost of reconstruction.

This is a more complex relationship with entropy than the generic cell. The generic cell maintains its gradient continuously and uses it for metabolic work. The neuron does this too — but additionally uses the gradient as a signaling resource, deliberately and temporarily dissipating it in a directed way to transmit state changes.

---

## 6. Recursion: From Single Neuron to Network

A single neuron firing produces a signal — a brief, stereotyped voltage pulse that propagates along the axon and releases neurotransmitters at synaptic terminals, perturbing the membrane potentials of downstream neurons.

This introduces a new level of recursion beyond the cell's internal metabolic loop:

- The neuron maintains its dynamic boundary (metabolic recursion — identical to the membrane case)
- The neuron's boundary state influences other neurons' boundary states (network recursion — new at this scale)
- The network of mutual influences shapes which neurons fire, which shapes the network's future state

**In framework terms**: at the single neuron level, recursion sustains the dynamic boundary. At the network level, recursion connects dynamic boundaries to each other, producing a higher-order constraint geometry — a geometry of geometries. The state of each neuron's boundary is a constraint on the transitions available to connected neurons.

This is the framework's density and recursion properties operating at a new scale: not the density of constraint interactions within a single boundary, but the density of connections between dynamic boundaries. A neural network is a configuration of mutually constraining dynamic processes, each maintaining its own boundary while continuously perturbing the boundaries of others.

---

## 7. What Is New at This Scale

The neuron introduces three properties the membrane case did not exhibit:

**State-dependent constraint geometry**: the transitions available in S depend on current position in S. The voltage-gated channels reconfigure the effective constraint geometry as the system moves through it — permitted transitions shift with system state rather than remaining fixed.

**Directed gradient dissipation as signaling**: the generic cell maintains its gradient. The neuron uses its gradient as a resource — deliberately producing a partial, localized reduction in its dynamic boundary in a directed way to transmit a state change. The controlled diminishment of the boundary differential is the signal.

**Network-level constraint geometry**: neurons connect dynamic boundaries into a higher-order constraint structure. Each neuron's state constrains the transitions available to connected neurons. The network is a constraint geometry whose elements are themselves dynamic boundaries.

---

## 8. Decay and Failure Modes

The neuron inherits all failure modes of the generic cell — ATP depletion, pump failure, membrane disruption — with identical consequences: dissolution of the maintained differential, collapse of the dynamic boundary.

Neural-specific failure modes add to these:

**Channel dysfunction**: voltage-gated channels that fail to open, fail to inactivate, or open spontaneously disrupt the directed trajectory through S. Epileptic seizures are one consequence of channels that fail to inactivate properly — the positive feedback of sodium entry runs unchecked, producing continuous, uncontrolled firing. The directed trajectory becomes an uncontrolled excursion.

**Synaptic failure**: disruption of neurotransmitter release or reception severs the network-level constraint geometry. Individual neurons may maintain their own dynamic boundaries while becoming decoupled from the network that gives their boundary states functional significance.

**Excitotoxicity**: excessive stimulation forces continuous action potential firing, depleting ATP faster than it can be produced. The pump falls behind. The gradient collapses. What began as a neural failure mode ends as a cellular failure mode — the distinction between scales dissolving as the lower-level constraint is overwhelmed.

---

## 9. The Bridge to Cognition

The neuron's dynamic boundary does something the generic cell's does not: it transmits state changes. Each action potential is a brief, stereotyped signal — a binary event whose occurrence encodes information about the neuron's integrated input.

A single neuron transmitting a single signal is not yet cognition. But a dense network of mutually constraining dynamic boundaries — each maintaining itself, each influencing and being influenced by others, each with state-dependent constraint geometry — begins to exhibit something new: the network's collective state encodes information about the environment that no single neuron encodes alone.

This is the bridge from the neural scale to the cognitive scale. The framework's account of cognition begins here: not with a special substance or a new physics, but with the same constraint geometry operating at sufficient density and recursion that the network's collective state begins to model the environment in which the boundaries are maintained.

The self-model — what the framework calls the cognitive self — emerges when this modeling process becomes recursive enough to include a model of the modeling process itself. That is the next scale. The path from here to there runs through the question of what it means for a network of dynamic boundaries to represent something — to have a state that is not just the result of constraint interaction but is about the constraint geometry in which the system is embedded.

That is where the framework's most original and most difficult work remains.

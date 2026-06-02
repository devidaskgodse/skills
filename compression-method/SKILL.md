---
name: compression-method
description: "Applies the Compression Method to derive a minimal, ordered set of first-principles laws for any domain the user provides. Invoke with /compression-method DOMAIN, or when the user asks to 'derive the laws of X', 'find the first principles of X', 'compress X into laws', 'apply the compression framework to X', or 'what are the fundamental laws of X'. Trigger whenever the user names a domain and wants its core principles expressed as generative laws rather than a list of tips. Do not trigger for general Q&A about a domain."
---
 
# Compression Method
 
Derive a minimal, ordered set of first-principles laws for a named domain.
 
## What this skill produces
 
A law set with the following properties:
- **Minimal** — the fewest laws that achieve exhaustive coverage
- **Ordered by dependency** — lower-numbered laws are prerequisites for higher-numbered ones
- **Generative** — all conventional wisdom in the domain falls out as consequences; nothing needs to be added
- **Anchored in science** — laws derive from the domain's best formal model, not from practitioner heuristics
## The six moves (apply in sequence)
 
### Move 1 — Frame the domain as optimization
 
Recast the domain as: *"X is optimization of Y under constraints Z."*
 
- Y is the thing being maximised (the objective function)
- Z are the hard constraints (time, resources, attention, physical limits, etc.)
This is the foundation. Every law will be a constraint on this optimization. If a candidate law doesn't connect to the optimization frame, it is a preference, not a law.
 
Test: can you now rank outcomes as "better" and "worse" formally? If not, the framing is still too vague.
 
### Move 2 — Find the zeroth law
 
Ask: *what must be true before the optimization even has a target?*
 
There is almost always a silent prerequisite — something practitioners assume but never state, therefore routinely violate.
 
- The zeroth law makes this implicit prerequisite explicit
- Violating it makes all subsequent effort waste
- It is numbered 0, not 1, to signal it is a precondition, not a peer
Common forms: "the goal must exist," "the problem must be real," "consent must be present," "the system must be defined."
 
State it as: **Law 0 — [imperative phrase].** Then explain what "violating" it looks like in practice, and why no amount of Laws 1–N can compensate.
 
### Move 3 — Import the domain's formal model
 
Find the scientific, mathematical, or engineering model that explains *why failures happen*, not just *that they happen*.
 
Criteria for the right model:
- It is predictive: given the model, you can enumerate specific failure modes in advance
- It is structural: it describes the mechanism, not just the outcome
- It is the model experts would cite, not the practitioner's folk theory
Sources to draw from: physics (thermodynamics, information theory, mechanics), mathematics (optimization theory, graph theory, probability), biology (evolution, systems biology), computer science (complexity theory, type theory, automata), economics (game theory, mechanism design), linguistics (semantics, pragmatics).
 
List the model explicitly. State its failure modes as a numbered list. These become the raw material for the laws.
 
### Move 4 — Derive and order laws from failure modes
 
Take the failure modes from Move 3. Order them by dependency:
 
> A failure mode F_i outranks F_j if: a violation of F_i makes fixing F_j futile.
 
This ordering is the source of the laws' diagnostic power. When something goes wrong, you fix the lowest-numbered violation first, because higher-numbered fixes are wasted on a lower-numbered problem.
 
For each law:
- State it as an imperative: **Law N — [verb phrase]**
- Name the failure mode it addresses
- Give the test for violation: "you are violating this law if..."
- Show one piece of conventional wisdom that falls out as a consequence
Laws must be:
- **Orthogonal**: each addresses a distinct failure mode
- **Exhaustive**: together they cover all fundamental failure modes in the model
- **Minimal**: the smallest set that achieves exhaustiveness (aim for 3–5 laws total including Law 0)
### Move 5 — Borrow hierarchical structure from an analogous formal system
 
Find a formal system in another domain that has the same structural shape as the law set. Import its hierarchy explicitly.
 
Good candidates:
- **Thermodynamic laws** — when the zeroth-law prerequisite structure is strong
- **Conservation laws** — when something is preserved through transformation
- **Shannon's capacity theorems** — when the domain has hard informational bounds
- **Gödel's results** — when self-reference or limits of formal systems are central
- **Amdahl's law** — when the domain has a bottleneck that limits total improvement
- **Evolutionary constraints** — when the domain involves selection and variation
State which formal system you are borrowing from and why the structural analogy holds. This step signals that the laws have logical necessity, not just coherence.
 
### Move 6 — Test compression
 
Take the 10–15 most important pieces of conventional wisdom in the domain. For each, either:
 
(a) Identify which law it is a consequence of, and derive it explicitly — show the logical chain from the law to the advice, or
(b) Flag it as a residual — if it doesn't follow from any law, either the laws are incomplete, or the conventional wisdom is wrong
 
Document the residuals. Investigating each one deepens the framework. A residual that reveals a gap means adding a law or refining an existing one. A residual that turns out to be wrong is itself a valuable output.
 
The compression test is passed when: no conventional wisdom requires a separate law, and every law generates multiple pieces of conventional wisdom.
 
**Recursive application check (second-order consequences).** After mapping conventional wisdom to laws, ask: do the laws apply at multiple scales? A law that governs the whole governs each part at every level of decomposition — a law for a document also governs each section, paragraph, and sentence; a law for a codebase also governs each module, class, and function. Derive the structural principles that fall out of this recursive application. Document them as second-order consequences, not additional laws. If recursive application reveals principles that conventional wisdom treats as separate rules, that is the compression working correctly — those rules are not fundamental, they are consequences of scale-invariance.
 
**Dominant failure mode check.** After deriving laws, ask: when multiple laws are violated simultaneously, do violations cluster into recognizable patterns? Name these patterns — they are diagnostically valuable because real failures rarely present as clean single-law violations. A practitioner who internalizes the laws should be able to name the dominant pattern, not just list individual violations.
 
---
 
## Output format
 
Present the output in this order:
 
1. **Optimization frame** (one sentence: "X is optimization of Y under constraints Z")
2. **Formal model** (name the model; list its failure modes)
3. **The laws** — for each:
   - Law number and imperative statement
   - The failure mode it addresses
   - Violation test ("you are violating this if…")
   - One derived consequence (a piece of conventional wisdom that falls out)
4. **Hierarchy structure** (which formal system borrowed; why the analogy holds)
5. **Compression test** (table mapping conventional wisdom to laws; flagged residuals)
6. **What this framework generates** (2–3 sentences: what a practitioner who internalises these laws can do that they couldn't do from a rulebook)
---
 
## Quality criteria
 
A good output:
- Has 3–5 laws (including Law 0). More than 5 usually means the compression is incomplete.
- Has laws that feel *necessary*, not merely *useful*. Each should be hard to argue with once you've accepted the optimization frame.
- Has a compression test where the most important conventional wisdom maps cleanly to the laws.
- Has at least one residual that reveals something interesting — either a gap in the laws or a flaw in received wisdom.
A poor output:
- Lists more than 5 laws (likely still at the "tips" level)
- Has laws that overlap (not orthogonal)
- Has conventional wisdom that requires a separate law (compression test fails)
- Has laws that feel like preferences rather than necessary constraints
---
 
## Example invocation and expected shape
 
**Invocation**: `/compression-method nutrition`
 
**Expected shape** (abbreviated):
- Frame: "Nutrition is optimization of cellular function and longevity under constraints of available nutrients, absorption, metabolic load, and individual variation."
- Model: thermodynamics + biochemistry (energy balance, metabolic pathways, nutrient signalling)
- Law 0: Have a metabolic purpose (you cannot optimise nutrition without a defined physiological goal)
- Law 1: Match substrate to demand (the right nutrient at the wrong time is noise)
- Law 2: Maximise bioavailability-to-load ratio (what the body can use vs. what it must process)
- Law 3: Preserve homeostatic redundancy (the body's self-regulating systems must not be bypassed; nutrients that do the body's signalling work for it degrade those systems)
- Hierarchy: borrowed from thermodynamics (energy input/output conservation) and control theory (homeostatic feedback loops)
This is the *shape*, not a complete answer. The actual derivation requires working through all six moves with care.
 
---
 
## Important: what this skill is not
 
This skill does not produce:
- A list of best practices (that is the input to the compression test, not the output)
- A survey of the domain's literature
- A framework for *doing* the thing (e.g., a nutrition plan) — it produces a framework for *understanding* the thing
The output is a tool for reasoning, not a how-to guide. A practitioner who internalises the laws should be able to derive the how-to guide themselves.

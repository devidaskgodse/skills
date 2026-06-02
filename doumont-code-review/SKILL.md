---
name: doumont-code-review
description: "Reviews code files or codebases against Doumont's Laws of Software — a first-principles framework derived from what software fundamentally is: a formal text that must align syntax, semantics, and pragmatics across two readers (machine and human). Use this skill whenever the user asks to review, audit, or critique code quality, maintainability, readability, or design — especially when they use phrases like 'review this code', 'how clean is this', 'what's wrong with this file', 'does this follow good principles', 'audit this codebase', or 'give me feedback on this code'. Also trigger when the user uploads or pastes code and asks for improvement suggestions, or asks how well their code follows any set of design principles. This is a substantive code quality review — not a linter, not a bug finder — focused on whether the code's form matches its meaning, exposes its structure, and is designed to survive modification."
---
 
# Doumont Code Review
 
This skill reviews code against four laws derived from what software fundamentally *is*: a formal text specifying computation, with syntax (what the machine reads), semantics (what it means), and pragmatics (what effect it produces). Every quality failure in code is a gap between these layers.
 
The laws are hierarchically ordered. When they conflict, higher laws take precedence.
 
---
 
## The Four Laws
 
**Zeroth Law** — Software exists to produce reliable effects, not to express ideas. Correctness and purpose precede all other considerations. Code that is elegant but wrong, or clever but unmaintainable, fails at the zeroth level.
 
**Law 1** — Close the gap between form and meaning. The code should say what it does and do what it says. Names, types, abstractions, and structure should match the domain reality they represent. Comments that compensate for unclear code are evidence of a gap, not a fix.
 
**Law 2** — Make necessary structure visible; eliminate unnecessary structure. Hidden complexity is not managed complexity. Structure that carries meaning must be exposed. Structure that carries no meaning (ceremony, cargo-cult patterns, unused abstractions) must be removed.
 
**Law 3** — Design for the dominant operation, which is modification. Code is read far more than written, and modified far more than created. Tests, types, and clear boundaries are not overhead — they are the redundant encoding that makes meaning recoverable when the system changes.
 
---
 
## Review Process
 
### Step 1: Understand scope and language
 
Identify what's being reviewed — a single file, a module, a full codebase. Note the language, framework, and apparent domain. Don't apply language-specific idiom preferences unless they directly affect law compliance.
 
If reviewing a full codebase and it's large, prioritize:
1. Entry points and public interfaces (highest Law 1 exposure)
2. The most-changed files (highest Law 3 exposure)
3. Core domain logic (highest Law 2 exposure)
### Step 2: Review against each law in order
 
Work through the laws in order — 0, 1, 2, 3. This ordering matters: a finding at Law 0 is more severe than one at Law 3. For each law, identify specific violations with line references where possible.
 
**Zeroth Law checks:**
- Does each function/module have a clear, singular purpose?
- Is there dead code, unreachable paths, or code that runs but produces no observable effect?
- Are error cases handled or silently swallowed?
- Does the code do what its tests (if any) claim it should do?
**Law 1 checks:**
- Do names reflect domain concepts, or implementation details?
- Would a reader unfamiliar with the internals understand what a function does from its signature alone?
- Are there comments explaining *what* the code does rather than *why*? (Compensatory comments signal gaps)
- Do types encode constraints, or are they wider than the meaning (e.g., `string` for an enum, `any`, `Object`, `dict` where a structure exists)?
- Do abstractions match domain boundaries, or do they bleed across concerns?
- Are there functions named `process`, `handle`, `manage`, `util`, `helper` — generic names that say nothing?
**Law 2 checks:**
- Is there structure that exists for its own sake — interfaces with one implementation, abstract classes never subclassed, factory patterns for objects never varied?
- Is there structure that *should* be visible but isn't — long functions whose internal stages are unnamed, modules whose responsibilities can't be inferred from their public API?
- Is the hierarchy legible at each level? Can a reader understand what a module does from its exports, what a class does from its methods, what a function does from its first few lines?
**Law 3 checks:**
- Is configuration fused with logic? (rates, thresholds, limits hardcoded into business logic)
- Are likely-to-change concerns scattered across the codebase rather than localized?
- Do tests exist and do they encode intent (what the code *should do*) rather than just implementation (what it *currently does*)?
- Is the change surface narrow — can you make a likely change in one place without touching five others?
- Are boundaries between components explicit and checked, or implicit and assumed?
### Step 3: Identify the dominant failure mode
 
After reviewing against all laws, step back and identify the *pattern* — the underlying failure that explains most of the individual violations. This is the most valuable part of the review. Common patterns:
 
- **Form-meaning divergence (Law 1)**: the codebase has grown but the names haven't kept up. The code does more than it says it does.
- **Hidden architecture (Law 2)**: there is real structure here, but it's buried in implementation detail rather than exposed through abstraction.
- **Rigidity (Law 3)**: the design was made for the first version of requirements. Likely changes are now expensive because concerns are fused.
- **Purposeless complexity (Law 0 + Law 2)**: abstractions that were added in anticipation of needs that never arrived.
### Step 4: Write the review
 
---
 
## Output Format
 
Always structure the review as follows. Keep the tone analytical, not judgmental — these are structural observations, not character assessments.
 
```
## Doumont Code Review: [filename or module name]
 
### Summary
One paragraph identifying the dominant failure mode and the overall law-compliance profile. Be direct about the most important finding.
 
### Zeroth Law — Reliable Effects
[PASS / MINOR ISSUES / SIGNIFICANT ISSUES]
Findings with specific references. If passing cleanly, say so briefly.
 
### Law 1 — Form-Meaning Alignment
[PASS / MINOR ISSUES / SIGNIFICANT ISSUES]
Findings with specific references. For each finding, show the gap: "X says Y but does Z."
 
### Law 2 — Structure Visibility
[PASS / MINOR ISSUES / SIGNIFICANT ISSUES]
Findings with specific references. For each finding, distinguish: is this unnecessary structure to remove, or necessary structure to expose?
 
### Law 3 — Designed for Modification
[PASS / MINOR ISSUES / SIGNIFICANT ISSUES]
Findings with specific references. Identify specifically what is likely to change and where the change surface currently sits.
 
### Priority Improvements
Ordered list (most important first) of concrete changes, with before/after examples where they add clarity. Each improvement should reference the law it addresses and explain why the change closes the gap — not just that it looks better.
 
### What Works Well
Specific things the code does right under these laws. A review that only finds problems is less useful than one that identifies which patterns to preserve.
```
 
---
 
## Calibration Notes
 
**Avoid these failure modes in the review itself:**
 
- **Applying style preferences as law violations.** Indentation, naming conventions (camelCase vs snake_case), line length — these are not law violations unless they create a form-meaning gap.
- **Flagging all complexity as Law 2 violations.** Some complexity is essential — it belongs to the domain. The question is whether it's necessary, and if so, whether it's visible.
- **Treating tests as optional under Law 3.** Tests are the primary mechanism for making meaning recoverable after modification. Their absence is a Law 3 finding regardless of how clean the rest of the code is.
- **Grading all laws equally.** The laws are hierarchical. A Zeroth Law violation (the code doesn't reliably do what it's supposed to) is more serious than a Law 3 violation (it's hard to change). Say so explicitly in the priority ordering.
**Calibrate severity honestly:**
- A 50-line utility function with good names and no tests has minor Law 3 exposure, not a crisis.
- A core business logic module with 8 functions all named `process_*` and types of `dict` throughout has a serious Law 1 failure that compounds every future change.
- The same violation in a rarely-modified internal helper vs. a frequently-changed interface file has different practical severity. Note this.
---
 
## Reference: Law Violations → Traditional Jargon Mapping
 
This mapping helps connect findings to terminology the user may already know, but lead with the law — the jargon is downstream of the diagnosis.
 
| Law Violation | Traditional Terms |
|---|---|
| Zeroth: code runs but produces unreliable effects | Bugs, silent failures, missing error handling |
| Law 1: names don't match meaning | Poor naming, magic numbers, primitive obsession, misleading comments |
| Law 1: types wider than meaning | Stringly-typed code, over-use of `any`/`Object` |
| Law 1: abstractions cross domain boundaries | Feature envy, inappropriate intimacy |
| Law 2: unnecessary structure | Over-engineering, YAGNI violations, speculative generality |
| Law 2: necessary structure hidden | Long method smell, god class, missing abstraction |
| Law 3: config fused with logic | Hardcoded values, magic numbers |
| Law 3: change surface scattered | Shotgun surgery smell, DRY violation |
| Law 3: no tests encoding intent | Missing tests, testing implementation not behavior |
 

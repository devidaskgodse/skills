---
name: doumont-writing-review
description: "Reviews written content against Jean-luc Doumont's Laws of Communication (the Zeroth Law plus the Three Laws) and the structural principles in his book *Trees, Maps, and Theorems*. Use this skill whenever the user asks to review, critique, edit, audit, or improve any piece of writing — essays, reports, memos, documentation, emails, blog posts, academic papers, executive summaries, slide-deck text, proposals, or any other prose deliverable. Also trigger when the user pastes or uploads written content and asks for feedback, structural critique, clarity improvements, or phrases like 'how can I tighten this', 'is this clear', 'how does this read', 'does this land', or wants their writing evaluated against any framework for clear communication. This is a substantive structural and rhetorical review — not a copy-edit, not a grammar check — focused on whether the writing fits its audience, delivers its message efficiently, and reinforces that message through the channels readers actually use."
---
 
# Doumont Writing Review
 
This skill reviews written content against four laws and a set of structural principles articulated by Jean-luc Doumont — first in his 2002 IEEE paper *The Three Laws of Professional Communication*, then expanded in his book *Trees, Maps, and Theorems*. The laws answer four questions in order: *Is there actually a message?* (Law 0), *Whom is this for?* (Law 1), *Is every word earning its place?* (Law 2), *Does the message survive even when the reader skims, gets distracted, or drops in mid-section?* (Law 3). The structural principles operationalize the laws at the level of documents, sections, paragraphs, and sentences.
 
The framework is strictly hierarchical. When findings conflict, the lower-numbered law takes precedence: no amount of audience-adapting, signal-sharpening, or redundancy can rescue writing that has nothing to say, and no amount of polish at the sentence level can save writing aimed at the wrong audience. Always lead the review with the lowest-numbered violation.
 
---
 
## The Four Laws of Communication
 
**Law 0 — Have a purpose (have messages).** Doumont adds this law on the model of the zeroth law of thermodynamics: a premise "so obvious it had long been overlooked." Effective communication is *optimization under constraints*, and you cannot optimize without something to optimize toward. The other three laws presuppose that there *is* a message — a specific claim, framed for a specific audience and purpose. Crucially, Doumont draws a sharp line between **information** (the "what" — e.g. "sales dropped 15%") and a **message** (the "so what" — e.g. "we should advertise more"). A document full of true information but no message has not satisfied Law 0; sentence-level edits cannot fix it.
 
**Law 1 — Adapt to your audience.** Communication is optimal *for an audience*, not in itself. The same words can be perfect for one reader and useless for another. A review reconstructs the audience the writing implicitly assumes — their prior knowledge, motivation, available time, and the question they came to the document with — and asks whether the writing actually fits them. Law 1 is the law of empowerment: if the audience doesn't get the message, the writer is the one with control, so it is the writer's problem to solve.
 
**Law 2 — Maximize the signal-to-noise ratio.** Signal is anything that advances the audience toward the message. Noise is everything else — irrelevant detail, throat-clearing, jargon used for affect rather than precision, decorative formatting, padded repetition. Improving SNR means either increasing signal (more of what matters) or reducing noise (less of what doesn't). Both moves are usually available. Doumont's preferred move is subtraction: "breaking the silence in a whisper is more pleasant than covering the noise in a shout."
 
**Law 3 — Use effective redundancy.** Communication channels are unreliable: readers skim, get distracted, drop in mid-section, misread. Important messages need to travel through more than one channel — the title, the topic sentence, the visual, the heading, the summary — so the message survives transmission failures. *Effective* redundancy adds value by restating the message in a different mode or coding. *Ineffective* redundancy just repeats the same words in the same channel ("advance reservations," "oval in shape") and is itself a Law 2 violation.
 
---
 
## Structural Principles from *Trees, Maps, and Theorems*
 
The book's title names the three modes through which technical content is conveyed: **trees** (the hierarchical structure of a document), **maps** (graphics, tables, schemas, anything seen at a glance), and **theorems** (the prose itself — sentences, paragraphs, claims). The laws apply to all three modes. For a written-content review, expect to spend most of your attention on trees and theorems, with maps relevant whenever the writing includes figures, tables, or diagrams.
 
The principles below are Doumont's operational tools for applying the laws.
 
**The fractal three-part structure.** Documents, sections, paragraphs, and even sentences share the same shape: an *opening* that tells the reader what to expect and why they should care, a *body* that delivers the substance, a *closing* that consolidates the takeaway. At every level of the hierarchy, ask: does this open well, body well, close well?
 
**Top-down ("headline first") delivery.** State the conclusion before the justification. The first sentence of a paragraph, the first paragraph of a section, the title of a document — these should *be* the message, not point at it. A reader who stops at any point should have the essence of what they would have had if they kept going.
 
**Messages, not topics.** A heading like "Results" is a topic — a label on a bin. A heading like "Throughput improved 40% under the new architecture" is a message — a claim the reader can act on. The same distinction applies to titles, captions, slide headings, and topic sentences. Topic-labeled writing tells the reader where they are; message-labeled writing tells them what they're learning.
 
**One idea per unit.** A paragraph carries one idea; a sentence carries one claim; a slide carries one message; a figure carries one comparison. Multi-idea units force readers to do unpacking work the writer should have done.
 
**Parallel form for parallel content.** When items are parallel in role, they should be parallel in form — lists, headings, comparison tables, sibling sections. Inconsistent form signals (falsely) that the items differ in kind.
 
**Structural redundancy through visual hierarchy.** Headings, emphasis, whitespace, and lists are not decoration — they are the channels through which a skimming reader receives the structure. Use them to expose real structure, not to signal effort.
 
**Graphics designed for comparison, not display.** When the writing includes figures and tables, they should be designed around the comparison the reader is meant to make — not as data dumps. The caption should state the message of the graphic in a full sentence, not name its topic.
 
---
 
## Review Process
 
### Step 1: Identify the artifact and reconstruct the audience
 
Note what's being reviewed: a memo, a report section, an email, an academic abstract, an executive summary, a piece of documentation, a blog post. Each genre carries default audience expectations — a memo wants the ask up front; an academic paper allows a slower build; a landing page assumes a hostile skim.
 
Then reconstruct the audience the writing *implicitly* assumes. Read the opening and ask: who would find this orientation natural? What does the writer think the reader already knows? What does the writer think the reader wants from this document? If the user has told you the intended audience, compare it to the audience the prose actually addresses. A gap between intended audience and implied audience drives most other findings, so name it early.
 
### Step 2: Recover the message (the Law 0 check)
 
Before doing anything else, try to state the document's central message in a single sentence — a *message* in Doumont's strict sense: not a topic, not a summary of the contents, but a claim with a "so what." If you can recover one, write it down; if you can't, that is itself the most important finding. Common Law 0 failure modes:
 
- **Information masquerading as message.** The writing reports many true things but takes no position. The reader is left with the "what" and asked to invent the "so what" themselves.
- **Competing messages, no resolution.** Several plausible central claims, with no signal about which is the point. The writer has not decided, so the reader cannot either.
- **Topic mistaken for message.** The document is "about X" but doesn't say anything *about* X. Topic-level intent ("I will cover the history of Y") is not message-level intent ("Y matters because Z").
- **Buried purpose.** A message exists, but the writer hasn't located it themselves — it surfaces late, parenthetically, or in a closing line. The reader's experience is closer to a Law 0 failure than the writer would think.
If Law 0 fails outright (no recoverable message), say so clearly and do not proceed to a sentence-level critique. A document without a message is not a writing problem dressed in poor prose — it is a thinking problem, and the writer needs to do that work before any of Laws 1–3 can help. Surface the question back to the writer: *what do you want the reader to do, decide, or believe after reading this?*
 
### Step 3: Review against each law in order
 
Work through the laws in order — 0 has already been checked in Step 2; now move through 1, 2, 3. The hierarchy matters: a Law 1 finding outranks a Law 2 finding, which outranks a Law 3 finding.
 
**Law 1 checks — Audience fit:**
- Does the opening orient the actual audience, or does it assume context they don't have (or rehash context they already have)?
- Is the level of detail calibrated to the audience's purpose? Executives reading for decisions need different depth than engineers reading for implementation.
- Is the jargon load appropriate? Specialized terms are signal for insiders, noise for outsiders. Watch for jargon used to perform expertise rather than transmit meaning.
- Does the structure match how the audience will actually read — front-to-back, skim, jump to a section?
- Does the writing respect the audience's time, or does it indulge the writer's process? Long throat-clearing openings, history-of-the-problem detours, and autobiographical asides usually fail this test.
**Law 2 checks — Signal-to-noise:**
- Are there sentences that could be deleted without loss?
- Are there hedges and intensifiers that soften without adding nuance ("very," "quite," "rather," "it is important to note that," "as we shall see")?
- Is the prose carrying its meaning, or is it padded with nominalizations and passives — "the implementation of the solution was carried out by the team" instead of "the team implemented the solution"?
- Are there structural elements (headings, lists, bolding) applied decoratively rather than to expose real structure?
- Is the writing redundant in the *ineffective* sense — restating the same point in adjacent paragraphs in the same channel, without adding any new mode of access?
- Where signal is *missing*, name it. Saying "more clarity needed" is itself low-signal; "the reader never learns why this matters until paragraph 4" is signal.
**Law 3 checks — Effective redundancy:**
- Does the title carry the message, or only the topic?
- Do section headings carry their section's claim, or just label its bin?
- Do paragraph openings preview the paragraph's point?
- Are key claims reinforced across channels — stated in prose, shown in a figure or table, summarized in a takeaway box?
- Apply the **skim test**: a reader who only reads the title, headings, and first sentence of each paragraph — does that reader still get the message? If not, the redundancy is not doing its job.
### Step 4: Audit the structure
 
Independently of the laws, examine the document as a tree:
 
- Does the whole document have a clear opening / body / closing?
- Does each major section have the same three-part shape?
- Does each paragraph have it — a lead, development, and (where appropriate) a hand-off to the next?
- Are the levels of the hierarchy parallel — sibling sections playing comparable roles, sibling paragraphs at comparable grain?
- Could a reader who only saw the headings (and perhaps first sentences) reconstruct the argument?
### Step 5: Identify the dominant failure mode
 
After all the specific findings, step back and name the underlying pattern. This is the most valuable part of the review — individual line edits are cheap, but seeing the *shape* of the failure lets the writer fix many problems at once. Common patterns:
 
- **Information without message** (Law 0): the document reports facts but takes no position. The most severe pattern, because no other improvement can compensate.
- **Writer-centric ordering** (Law 1 + structure): the document is organized the way the writer arrived at the ideas, not the way the reader needs to receive them. Often paired with bottom-up exposition.
- **Bottom-up exposition** (top-down principle violated): conclusions come at the end of paragraphs and sections instead of leading them; the reader has to wait to know why they're reading.
- **Decorative structure** (Law 2 + Law 3 misapplied): lots of headings, lists, and bolding, but the formatting doesn't expose real structure — it just signals effort.
- **Audience drift** (Law 1): different sections address different audiences without serving any of them well — technical detail interleaved with high-level pitch.
- **Topic-labeled, message-empty** (Law 3, often masking Law 0): headings and openings name topics ("Background," "Methods") rather than claims; a skimming reader gets a table of contents but no argument. When the message-empty structure is symptomatic rather than stylistic, it points back at Law 0.
- **Reader-as-detective** (Law 1 + top-down): the writer hides the conclusion as if writing a mystery, expecting the reader to enjoy the reveal. Technical readers want the answer first.
### Step 6: Write the review
 
---
 
## Output Format
 
Structure the review as follows. Keep the tone analytical — these are structural observations about the writing, not judgments of the writer. When you suggest rewrites, show *before/after*; abstract advice ("be clearer," "tighten this") is itself a Law 1 failure of this very review.
 
```
## Doumont Writing Review: [title or short description]
 
### Summary
One paragraph. Name the dominant failure mode, state the document's recovered central message (or note if no message is recoverable), and give the overall law-compliance profile. Be direct about the most important finding — the reader of the review is also an audience.
 
### Audience Reconstruction
Briefly: who does this writing seem to address, and how well does that match the apparent intended audience? This frames every finding that follows.
 
### Law 0 — Purpose and Message
[PASS / MINOR ISSUES / SIGNIFICANT ISSUES / FAIL]
State the recovered central message in one sentence, or say plainly that no message is recoverable. If FAIL, name which Law 0 failure mode applies (information without message, competing messages, topic mistaken for message, buried purpose) and recommend the writer resolve this before any sentence-level work.
 
### Law 1 — Audience Fit
[PASS / MINOR ISSUES / SIGNIFICANT ISSUES]
Specific findings (quote short phrases; reference paragraphs by their opening). For each finding, name the gap: "this assumes Y but the audience wants Z."
 
### Law 2 — Signal-to-Noise
[PASS / MINOR ISSUES / SIGNIFICANT ISSUES]
Specific findings. For each, distinguish: is this noise to cut, or signal that's missing? Both count as SNR failures.
 
### Law 3 — Effective Redundancy
[PASS / MINOR ISSUES / SIGNIFICANT ISSUES]
Specific findings. Apply the skim test explicitly — could a hurried reader recover the message from headings and first sentences alone?
 
### Structural Audit
The fractal three-part test at the level of document, sections, and paragraphs. Note where opening / body / closing is missing, weak, or out of order. Note where the hierarchy is uneven.
 
### Priority Rewrites
Ordered list (most important first) of concrete changes, with **before/after** for the highest-impact ones. Each rewrite should reference the law or principle it addresses and explain *why* the change closes the gap — not just that it reads better. Three to five focused rewrites usually beats fifteen scattered ones.
 
### What Works Well
Specific things the writing does right under these laws. Patterns to preserve — a strong opening sentence, a well-pitched explanation for the audience, an effective transition, a caption that states a message rather than naming a topic. A review that only finds problems is less useful than one that identifies which moves to keep.
```
 
---
 
## Calibration Notes
 
**Avoid these failure modes in the review itself:**
 
- **Applying style preferences as law violations.** Sentence length, Oxford comma, em-dash usage, "which" vs. "that," American vs. British spelling — these are not law violations unless they create real friction for the audience or hide the message. Doumont is a structuralist, not a stylist; this skill should be too.
- **Treating brevity as an end.** Law 2 maximizes signal-to-noise, not raw shortness. A short document that omits necessary signal is worse than a longer one that delivers it cleanly. The question is whether each word earns its keep, not how many words there are.
- **Confusing decorative formatting with structural redundancy.** Bold text, headings, and lists are only Law 3 wins when they expose real structure or carry a message. A document peppered with bolded phrases is not "more redundant" in any useful sense — it is visually noisy (a Law 2 failure).
- **Grading all laws equally.** The laws are strictly hierarchical, with Law 0 at the foundation. A piece of writing without a message cannot be saved by audience adaptation; a piece aimed at the wrong audience cannot be saved by sentence-level edits. Lead the priority ordering with the lowest-numbered violation present.
- **Treating Law 0 as a soft check.** It is tempting to give partial credit for "interesting writing about X" when no message is present. Don't. Doumont treats "have a purpose" as the foundational premise; a review that finds noise but skips the missing-message problem fails the writer by working on the wrong layer.
- **Reviewing prose without re-reading the whole.** Local fixes can break global flow. After major rewrites, the document needs to be re-evaluated as a whole — both the tree and the prose.
- **Mistaking the review's own style for the laws.** A long, hedged, topic-labeled review violates the very framework it applies. The review itself should pass the skim test.
**Calibrate severity honestly:**
- A casual email with a clear ask and one short paragraph of context does not need the full structural audit — it probably already satisfies Laws 1–3 by being short and direct. Say so and move on.
- A formal report whose executive summary doesn't state the conclusion is a serious Law 3 failure that compounds every reader's experience.
- The same problem in a public-facing document (many readers, hard to fix later) carries more weight than in an internal draft (few readers, cheap to revise).
- A piece written for a specialist audience that "feels jargon-heavy" to a generalist reviewer may not be a Law 1 failure at all — confirm the audience before flagging this.
---
 
## Reference: Law / Principle Violations → Common Writing Problems
 
This mapping connects findings to terms the user may already know. Lead with the law — the everyday term is downstream of the diagnosis, not a substitute for it.
 
| Law / Principle Violation | Common name |
|---|---|
| Law 0: information without message | "Data dump," "so what?," "no point," "what's the takeaway?" |
| Law 0: competing messages | "Trying to do too much," "what's the main argument?" |
| Law 0: topic without claim | "Reads like a Wikipedia article," "informative but not useful" |
| Law 1: writer-audience mismatch | "Talking past the reader," "ivory tower," "in the weeds" |
| Law 1: wrong depth or jargon level | "Too technical," "too vague," "not for this audience" |
| Law 2: noise dominates signal | "Verbose," "padded," "throat-clearing," "wordy" |
| Law 2: weak or missing signal | "Vague," "no clear point," "what is this even saying?" |
| Law 3: missing structural reinforcement | "Buried lede," "no executive summary," "doesn't skim well" |
| Law 3: topic-labeled headings | "Headings don't tell me anything," "table of contents but no argument" |
| Top-down violated | "Backwards," "saves the point for last," "reader as detective" |
| One idea per unit violated | "Paragraph is doing too much," "run-on," "scattered" |
| Parallel form violated | "Inconsistent," "list reads weird," "the headings don't match" |
| Fractal structure missing | "No clear shape," "ends abruptly," "no setup," "no landing" |
| Message-empty graphic / caption | "Chart junk," "what am I supposed to see here?" |
 

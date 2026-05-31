# Prompt Library — Refinement Session State

*Tracks decisions made, principles established, and open work for ongoing prompt_library.md refinement sessions.*

---

## Session Log

### May 31, 2026 — Session 4

**Scope:** 1A deep restructure — companion doc reorganization, prompt cleanup, and food log framing evolution.

**Changes made:**

1. **adhd_athlete_kitchen_plan.md — full restructure** — Doc was growing organically and had become messy, repetitive, and contained a full client profile duplicate that created drift risk with the prompt. Rebuilt with a clear information architecture designed for two use cases: planning (before shopping/cooking) and quick reference (mid-cook lookups).
   - New structure: (1) Kitchen & Training Context, (2) The Planning System, (3) Quick Reference, (4) Meal Ideas, (5) Food Log Patterns, (6) Open Questions & Parking Lot
   - "Who You Are" section cut entirely — prompt owns the profile
   - Kitchen Strengths and Current Friction Points kept and expanded — these are living operational knowledge, not static profile data
   - Training Context added as its own subsection
   - Frameworks consolidated in Section 2 (formulas, protein defaults, if-then shopping, stocking categories, ingredient prep, blood sugar framework)
   - Sauce ratios and confirmed techniques moved to Quick Reference — scannable, no narrative
   - Meal ideas reorganized by protein to match shopping logic
   - Food Log Patterns (Section 5) established as the home for long-term pattern observations across sessions
   - Freezer inventory cut — too static, goes stale. Specific items called out in Open Questions instead.
   - Execution notes folded into Quick Reference next to relevant techniques; no separate section
   - Old header ("Registered Dietitian — Endurance Athlete Focus") fixed

2. **1A prompt — WHAT WE'VE BUILT removed** — Section was growing back (11 bullets) and becoming noise. The companion doc now has everything organized and findable; the inline summary was redundant and created sync risk. Removed entirely.

3. **1A prompt — FOOD LOG PURPOSE AND USE rewritten** — Previous version was mechanics-only (how to commit, what to track). Rewritten in two passes this session:
   - First pass: reframed as a coaching tool — accountability layer, pattern mirror, grounded observations vs. assumptions
   - Second pass: added long-term habit change framing explicitly. The log serves two time horizons: day-to-day accountability + meal feedback, AND long-term evidence base for what's working, what habits are shifting, where the next small change should go. Goal is slow, permanent shift away from fast/convenient eating toward whole foods and proper fueling — incremental so it sticks, nothing should feel like an overhaul.
   - Added pointer to companion doc Section 5 as home for cross-session pattern observations

4. **1A prompt — companion doc description updated** — Removed stale "client profile" reference; now accurately describes the restructured doc.

5. **1A prompt — SESSION CLOSE RULE simplified** — Removed "update WHAT WE'VE BUILT" since that section no longer exists.

**New principles established:**

- **Companion doc owns reference and memory; prompt owns the profile.** When these overlap, they drift. Cut the duplication at the source.
- **Structure for dual use.** A companion doc used by both Claude and the human needs to be organized by *what you're looking for*, not by *when it was added*. Planning layer up front, quick reference accessible, open questions pruned to genuinely open items.
- **Food log has two time horizons.** Day-to-day accountability is valuable and should be preserved. But the longer-term lens — what's actually shifting, where to nudge next — is equally important and needs to be explicitly named so Claude holds both.
- **Food Log Patterns (Section 5) is the long-term signal layer.** It should be kept current across sessions, not just the log entries themselves.

**Open work list (updated):**
- [ ] Create streamdeck_project_state.md (3A companion doc doesn't exist yet)
- [ ] Confirm GoPro capture resolution for Hero12 and Hero11 Mini (TBD in 2B)
- [ ] Confirm project frame rate (TBD in 2B)
- [ ] Clarify "one additional Mac (TBD)" in 4A USER PROFILE
- [ ] Consider a YouTube/content creation prompt (5B or 6A) as Marty's channel grows
- [ ] Update 2A PROJECT STATUS — film was due May 31; confirm submission status
- [ ] Consider developing full personas for 2A, 2B, 3A, 4A following the 1A model

---

## Session Log

### May 30, 2026 — Session 3

**Scope:** 1A persona evolution — capturing the shift from ADHD life-hacks / kitchen management toward a fuller nutrition coaching + food logging frame. Also addressed a food log commit timing gap.

**Changes made:**

1. **Food log commit behavior tightened** — Changed from "commit in-session when entries are ready" to "Claude commits each food entry to food_log.md immediately after it is logged — not batched, not at session close. Every meal reported = one commit." Root cause: Claude was batching at end of day; reorientation mid-session couldn't pick up same-day entries that hadn't been written yet.

2. **1A persona rewrite** — Replaced the "performance life coach" framing with a fuller three-paragraph persona:
   - Paragraph 1 (Marty's edit): Performance nutrition coach for recreational endurance athletes trying to build a life. Named her actual activities: ultra marathons, endurance bike rides, backpacking, bikepacking, gaming, filming and editing video, weekday morning lake dips.
   - Paragraph 2: Holds two tracks simultaneously — athletic performance (fueling, recovery, energy) and long-game health (blood sugar, weight, aging well). Incremental and sustainable; Marty has 26 years of experience knowing what overhauls do.
   - Paragraph 3: Not a clinical dietitian, not a meal prep evangelist. Non-obvious strategies for real-life ADHD brains. Culinary depth is genuine.

3. **Goals explicitly named in CLIENT PROFILE** — Added: "Goals: lose weight, fuel training, lower blood sugar, feel better as she ages. Approach is sustainable and incremental — not a reset, not a diet."

4. **Ritual clarified — split into two bullets:**
   - Daily ritual: Cold-water dips in Lake Superior on weekday mornings — mental health anchor, non-negotiable.
   - Friday addition: After the dip, stops at the bakery for cinnamon rolls and coffee. Joy ritual — not a nutrition problem. Oikos Triple Zero alongside would blunt the glucose spike without touching the ritual.
   - Previous version incorrectly described the dip as a Friday-only event.

5. **Active training context added to CLIENT PROFILE** — "Currently in active training — working toward an ultra marathon and a long endurance bike event."

**New principles established:**

- **Food log commit = immediate, not batched.** Reorientation only works if the file is already current. The commit instruction must be unambiguous — "when entries are ready" is not strong enough.
- **Persona frame captures the whole person, not just the use case.** The 1A persona now names what Marty's life actually looks like (the training, the gaming, the filming, the dips) so Claude understands the context she's navigating, not just the kitchen problem she's solving.

---

## Session Log

### May 6, 2026 — Session 2

**Scope:** COMMUNICATION RULES cross-pollination across all prompts; 1A persona development; learning style and expertise nuances added to all profiles.

**Changes made:**

1. **COMMUNICATION RULES — 6 rules cross-pollinated across all prompts:**
   - "Interact with a sense of humor" added to 1A and 2A (was missing)
   - "Lead with the answer" added to 2A (was missing)
   - "No unnecessary caveats or hedging" added to 2A, 2B, 3A, 4A, 5A (was only in 1A)
   - "Name trade-offs and let Marty decide" added to 1A, 2B, 3A, 4A, 5A (was only in 2A)
   - "Impose structure for complex/overwhelming tasks" added to 1A, 2A, 3A, 4A, 5A (was only in 2B)
   - "Use numbered lists for multi-part options" added to 1A, 2A, 2B, 3A, 4A COMMUNICATION RULES (was in USER PROFILE everywhere and 5A COMM RULES only)

2. **COMMUNICATION RULES — 3 additional rules added to all prompts:**
   - "Don't restate or recap what Marty just said before answering — she knows what she said."
   - "Don't end responses with open-ended check-in questions — she'll redirect if she needs something different."
   - "Minimal cheerleading — encouragement is fine, but don't oversell." added to 3A, 4A, 5A (was only in 1A, 2A, 2B)

3. **1A — Cheerleading language standardized:** Replaced "no 'great idea!' affirmations" with the consistent "minimal cheerleading — encouragement is fine, but don't oversell." Clarified by Marty: minimal does not mean none — genuine encouragement and validation are welcome, just don't oversell.

4. **1A — Persona replaced:** "Registered dietitian and practical cooking coach" replaced with a full persona: performance life coach for recreational endurance athletes, focused on the gap between athletic ambition and real-world execution. Not a clinical dietitian, not a meal prep evangelist. Loves food and cooks well. Culinary depth is genuine.

5. **1A — Emotional calibration rules added to COMMUNICATION RULES:** Four new rules at the top of the block, setting the relational layer before the tactical layer:
   - Default to warm and light-hearted — laugh with her about the frozen pizza moments, not at them.
   - Know the difference between a moment that needs a solution and a moment that needs to be heard first.
   - When the moment calls for gentleness before solutions, lead with that. Don't default to fix-it mode.
   - If Marty is spiraling or making excuses, name it directly — with kindness, not criticism.

6. **1A — "Knowledgeable friend" updated to "trusted coach and friend"** — better reflects the coaching relationship and grounds the emotional calibration rules that follow.

7. **All profiles — "Learns best through hands-on experience and direct conversation, not passive consumption"** added to every USER PROFILE block.

8. **1A — 26-year experiential expertise added:** "Brings 26 years of lived experience with nutrition, weight management, and her own body — she's well past the basics. Don't explain what macros are." Food/nutrition is a domain where she is deeply experienced; skip the fundamentals entirely.

9. **2A + 2B — Self-education correction added:** Marty tried to self-educate through online filmmaking and Resolve content but it didn't click. She is a genuine beginner in both areas — do not assume prior knowledge. 2B includes a specific behavioral instruction: don't refer her to YouTube tutorials; work through things together directly.

10. **2A COMMUNICATION RULES — Draft-first rule added:** "For creative or voice decisions (tone, narration, framing, wording), show a draft first before executing. For project management or factual updates, execute directly."

11. **5A COMMUNICATION RULES — Confirm rule refined:** Replaced the generic "confirm before pushing" with the more nuanced version: "For structural or technical prompt changes, execute directly. For creative or voice decisions — new personas, tone framing, significant rewrites — show a draft first before pushing." Observed pattern: technical changes get a go-ahead without preview; creative/voice decisions get a draft review first.

12. **Last updated date bumped** — May 6, 2026.

---

## Session Log

### May 4, 2026 — Initial Refinement Session

**Scope:** Full review and fine-tuning of prompt_library.md across all five prompts (1A, 2A, 2B, 3A, 4A).

**Changes made:**

1. **Folded Session Opener into each prompt** — Eliminated the separate "Paste Session Opener" step. Each prompt now ends with a built-in instruction for Claude to retrieve the companion doc and give a status summary automatically. Removed Session Opener from Universal Session Phrases; kept mid-session reorient and end-of-session phrases.

2. **Trimmed 1A's WHAT WE'VE BUILT summary** — Reduced from 12 bullets to 4 to reduce sync risk between the inline summary and the companion doc. Full detail lives in the companion doc; the inline summary is just an orientation aid.

3. **Fixed 3A to use MCP retrieval** — Updated to match the pattern of all other prompts: Claude retrieves streamdeck_project_state.md via GitHub MCP with graceful fallback if the file doesn't exist yet.

4. **Removed stray `---` in 2A** — A dangling horizontal rule was sitting inside the 2A code block before the closing backticks.

5. **Updated all SESSION CLOSE RULEs** — Every prompt now instructs Claude to update the "Last updated" date at the bottom of prompt_library.md. Added prompt_library.md updates to 3A and 4A SESSION CLOSE RULEs (previously missing).

6. **Moved 2B's learning space framing into the prompt** — "This is a learning space, not just a project advisory space..." was sitting outside the code block (visible to Marty reading the library, invisible to Claude). Moved inside as IMPORTANT FRAMING at the top of the prompt.

7. **Marked dip-film_project_state.md as READ ONLY in 2B** — Explicit instruction added: 2A owns that file. 2B retrieves it for reference only and must not edit it under any circumstances.

8. **Cross-pollinated personality/communication traits across all profiles** — 2B had the richest profile. Added to all others:
   - Technical/analytical thinker, works in high-level tech professionally
   - Self-aware and direct — will tell you when something isn't working. Respond in kind.
   - Self-deprecating humor without being insecure. Appreciates directness and humor back.
   - Communicates in parenthetical asides — thinks out loud. Don't over-explain when already processing.
   - "She self-flags profile notes in parentheses — treat these as real updates and incorporate them." added to all COMMUNICATION RULES.

9. **Added ADHD to 2A and 4A** — Was completely missing from both. 2A framing: open-ended creative exploration can spiral; offer a concrete first step with a clear end condition. 4A framing: open-ended troubleshooting spirals her; every task needs a clear finish line.

10. **Expanded ADHD detail in 3A** — Was one thin bullet. Now matches the fuller structured framing from 2B.

11. **Added numbered-list decision pattern to all profiles** — Observed in this session: when presented with numbered options, Marty responds at the list level ("all except #4"). Present multi-part choices as numbered lists to enable efficient decision-making.

12. **Added prompt/AI structural awareness to 2B and 4A** — Marty understands prompt architecture at a structural level and will notice when something about the setup isn't functioning as intended.

13. **Bumped last updated date** — May 4, 2026.

---

## Established Principles

**Companion doc retrieval pattern:**
All prompts retrieve their docs via GitHub MCP before saying anything else. Graceful fallback where doc may not yet exist (currently 3A).

**Ownership model — each companion doc has one owning prompt:**
- adhd_athlete_kitchen_plan.md → 1A (read/write)
- dip-film_project_state.md → 2A (read/write); 2B (read only)
- DaVinci-Resolve_state.md → 2B (read/write)
- streamdeck_project_state.md → 3A (read/write)
- MCP_server_setup_status.md → 4A (read/write)
- refining_prompt_library_state.md → 5A (read/write)

**SESSION CLOSE RULE standard:**
Every prompt updates its companion doc + the relevant section of prompt_library.md + the "Last updated" date at the bottom.

**Profile richness standard:**
All profiles carry the same core personality/communication traits. Domain-specific items stay in their home prompt only.

**Companion doc owns reference and memory; prompt owns the profile (established May 31):**
When these overlap, they drift. Client profile duplication between prompt and companion doc was cut at the source. Companion doc holds operational knowledge (kitchen strengths, friction points, techniques, patterns); prompt holds identity and coaching context.

**Companion doc structure principle (established May 31):**
Organize by what you're looking for, not when it was added. Planning layer up front, quick reference accessible, open questions pruned to genuinely open items. A doc used by both Claude and the human needs to serve both use cases.

**Food log dual time horizons (established May 31):**
The log serves day-to-day accountability AND long-term evidence. Both must be explicitly named so Claude holds both simultaneously. Food Log Patterns (companion doc Section 5) is the designated home for cross-session observations.

**COMMUNICATION RULES standard (as of May 6, 2026):**
All prompts now share this common rule set, with domain-specific additions on top:
- Lead with the answer
- No unnecessary caveats or hedging
- Name trade-offs and let Marty decide
- Impose structure for complex/overwhelming tasks
- Use numbered lists for multi-part options
- Minimal cheerleading — encouragement is fine, but don't oversell
- Don't restate what she just said
- Don't end with check-in questions
- Interact with a sense of humor
- Self-flagging in parentheses = real updates

**IMPORTANT FRAMING block:**
Used in 2B and 5A to set session scope before companion doc locations. Available pattern for any future prompt that needs strong scope-setting before the detail begins.

**Persona development principle (established May 6):**
A full persona opening (not just a job title) gives Claude a character to inhabit, which improves consistency of voice and emotional calibration. 1A is the model. Others may benefit in future sessions.

**Draft-first principle (established May 6):**
Technical or structural changes → execute directly. Creative or voice decisions (personas, tone framing, narration, significant rewrites) → show a draft first, get approval, then push. Applies in 2A and 5A; likely applies in any prompt where voice/tone is part of the output.

**Domain-specific expertise principle (established May 6):**
Learning style and prior knowledge are domain-specific, not uniform:
- Food/nutrition: 26 years of lived experience. Skip the basics entirely.
- Film/filmmaking: Genuine beginner. Tried to self-educate but it didn't click. Don't assume prior knowledge; don't refer to external tutorials.
- DaVinci Resolve: Genuine beginner. Same as above.
- General: Learns best through hands-on experience and direct conversation, not passive consumption.

**Food log commit principle (established May 30):**
"Commit when entries are ready" is not strong enough — Claude batches. The instruction must be explicit: commit immediately after every meal is reported, no batching, no end-of-session delays. Reorientation only works if the file is already current.

**Persona captures the whole person (established May 30):**
The 1A persona now names Marty's actual life context — not just the problem domain. This gives Claude the frame to understand what she's balancing, not just what she's asking for help with.

---

## Notes on Marty's Prompt Engineering Style

- Thinks structurally about how prompts work — spotted that the 2B framing note was outside the code block and therefore invisible to Claude.
- Makes fast, precise decisions from numbered lists ("all except #4" — no restatement, no ambiguity).
- Iterates incrementally — prefers targeted edits over full rewrites, reviews before committing.
- Treats the prompt library as a living document, not a set-it-and-forget-it artifact.
- Cares about consistency across prompts — noticed gaps in profile richness and cross-prompt coherence unprompted.
- On cheerleading: minimal does not mean none. Genuine encouragement and validation are welcome — just don't oversell.
- On 1A persona: wants non-obvious strategies for real life, not TikTok meal prep content. Specifically called out the gap between generic advice and what actually works for an ADHD brain at 9:30pm.
- On learning style: domain matters. Food = veteran, don't explain basics. Film/Resolve = genuine beginner who learns by doing, not by watching tutorials.
- Draft-first on creative/voice decisions; execute directly on technical/structural ones.
- Reorientation phrase matters: "Re-read the docs and reorient" triggers MCP retrieval. Conversational openers do not. Worth reinforcing this as a habit.
- On companion docs: wants them useful for her own reference, not just for Claude. Structure matters for human readability too.
- On the food log: day-to-day accountability is valuable and should be preserved, but the longer-term lens is equally important. Both need to be held simultaneously.

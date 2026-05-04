# Prompt Library — Refinement Session State

*Tracks decisions made, principles established, and open work for ongoing prompt_library.md refinement sessions.*

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

12. **Added prompt/AI structural awareness to 2B and 4A** — Marty understands prompt architecture at a structural level and will notice when something about the setup isn't functioning as intended (e.g., noticed the 2B framing note was outside the code block and therefore invisible to Claude).

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

**IMPORTANT FRAMING block:**
Used in 2B to set session scope before companion doc locations. Available pattern for any future prompt that needs strong scope-setting before the detail begins.

---

## Open Work

- [ ] Create streamdeck_project_state.md (3A companion doc doesn't exist yet — will be created at close of first 3A session)
- [ ] Confirm GoPro capture resolution for Hero12 and Hero11 Mini (TBD in 2B SYSTEM SETUP)
- [ ] Confirm project frame rate (TBD in 2B SYSTEM SETUP)
- [ ] Clarify "one additional Mac (TBD)" in 4A USER PROFILE
- [ ] Consider a YouTube/content creation prompt (5B or 6A) as Marty's channel grows
- [ ] Review 2A PROJECT STATUS as the film moves through final post-production toward the May 31 deadline

---

## Notes on Marty's Prompt Engineering Style

- Thinks structurally about how prompts work — spotted that the 2B framing note was outside the code block and therefore invisible to Claude.
- Makes fast, precise decisions from numbered lists ("all except #4" — no restatement, no ambiguity).
- Iterates incrementally — prefers targeted edits over full rewrites, reviews before committing.
- Treats the prompt library as a living document, not a set-it-and-forget-it artifact.
- Cares about consistency across prompts — noticed gaps in profile richness and cross-prompt coherence unprompted.

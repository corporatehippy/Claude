# DaVinci Resolve — Learning State & Session Log

*Tracks workflow knowledge, concepts learned, settings established, and open questions across sessions.*

---

## USER PROFILE (current understanding)

- **Name:** Marty
- **Experience:** ~12 projects total across iMovie and DaVinci Resolve. Comfortable with basic cut/edit workflow. Newer to color grading, Fairlight, Fusion. Self-described slow workflow.
- **Resolve version:** TBD
- **Free or Studio:** TBD
- **OS:** TBD
- **Hardware:** TBD
- **Primary machine:** Mac Mini (assumed — confirm)
- **Storage:** TBD
- **Current film project:** "Dips with the Girl Gang" — documentary short, 8:03, picture locked. See dip-film_project_state.md.
- **YouTube channel:** https://www.youtube.com/@corporatehippiesintheup
- **Artlist subscription:** Yes (music licensing for social/YouTube content)

---

## SYSTEM / PROJECT SETTINGS (confirmed)

- **Timeline resolution:** 1920x1080 HD (confirmed on current project)
- **GoPro capture resolution:** Unconfirmed — may be 1080p (downgraded to save SD card space). Check camera settings.
- **Export settings established:** MP4 / H.264 / Variable Bitrate / 40,000 Kb/s / Audio AAC 48kHz 320kbps

---

## CONCEPTS LEARNED BY SESSION

### Session 1 — April 18, 2026

**Music licensing:**
- Can't use commercial music (e.g. Phish) on YouTube/social without a sync license — Content ID will flag it
- Artlist subscription covers YouTube and social media use
- Search strategy: search by feeling/mood, not title. For "earned optimism / exhale into sunlight" vibe: search "folk" + "uplifting," sort by Most Popular, trust gut within first 5 seconds of each track
- Fair use is not a workaround — it's a legal defense argued after the fact, not pre-approval

**YouTube Shorts:**
- Requires 9:16 vertical aspect ratio — horizontal footage won't qualify as a Short
- Options: crop to vertical in Resolve, pillarbox (usually looks cheap), or just post as regular horizontal video

**Cropping horizontal to vertical in Resolve:**
- Create new 1080x1920 timeline
- Drop clip in — it will letterbox
- Use Inspector → Zoom and Y Position to scale and reposition
- Use Paste Attributes (Opt+V Mac / Alt+V Windows) to copy zoom/position settings from one clip to all others — check Zoom and Position in the dialog

**Preview window — KEY TAKEAWAY:**
- Always set preview window to **Fit** when working with vertical timelines (or any time you switch resolutions)
- Zoomed-in preview will hide parts of the frame and give false confidence about framing
- This is especially critical for vertical/9:16 work

**Export settings for YouTube:**
- Format: MP4
- Codec: H.264
- Resolution: Timeline Resolution
- Rate Control: Variable Bitrate
- Bitrate: 40,000 Kb/s
- Audio: AAC, 48kHz, 320kbps
- YouTube recompresses everything — no benefit to going much higher than 40 Mbps

**Timeline architecture — important mental model:**
- Clips are NOT inside the timeline — they live in the Media Pool
- Timelines are instructions for how to play media pool clips
- Duplicating a timeline duplicates the instructions, not the media — edits in one affect both
- **Timeline Versions** are the correct tool for independent copies — Right-click timeline → Timelines → Create New Version
- Make a version BEFORE making changes, not after

**Mute track workaround:**
- When you need two exports from the same timeline (e.g. with VO and without VO), mute the relevant track (M button) before rendering — no need for a separate timeline

---

## OPEN QUESTIONS / THINGS TO EXPLORE

- [ ] **SESSION OPENER TASK: Ask Marty about her full equipment and setup** — cameras (GoPro model, iPhone model), editing machine specs (Mac Mini specs, GPU, RAM), any other tools (microphones, external drives, etc.). This affects proxy workflow advice, render/grade performance, and storage recommendations.
- [ ] Confirm GoPro capture resolution (1080p vs 4K)
- [ ] Confirm Resolve version and Free vs Studio
- [ ] Hardware specs (GPU especially — affects grade and render performance)
- [ ] Color grading fundamentals — next major learning area (also needed for dip film)
- [ ] Fairlight audio workflow beyond basic fader work
- [ ] Fusion — not yet touched
- [ ] Keyboard shortcuts — not yet mapped/learned systematically
- [ ] Proxy workflow — may be relevant if performance issues arise
- [ ] Bin/media pool organization best practices

---

## SESSION LOG

**Session 1 — April 18, 2026**
- Established this space as a general Resolve learning space (not just project advisory)
- Updated prompt_library.md section 2B to reflect new framing
- Worked through a real 90-second lake dip video project:
  - Music licensing research and Artlist search strategy
  - Cropped horizontal GoPro footage to vertical for YouTube Short / Facebook / Instagram
  - Established YouTube export settings
  - Learned Paste Attributes for copying zoom/position across clips
  - Discovered preview window Fit mode issue — key takeaway
  - Learned timeline architecture / shared media pool model
  - Learned Timeline Versions vs duplicated timelines
  - Mute track as multi-version export workaround
- Final outcome: vertical Short posted to Facebook/Instagram with VO; skipped horizontal YouTube upload for this project
- Marty flagged: ask about full equipment and setup at next session opener

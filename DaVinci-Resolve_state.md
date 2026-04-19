# DaVinci Resolve — Learning State & Session Log

*Tracks workflow knowledge, concepts learned, settings established, and open questions across sessions.*

---

## USER PROFILE (current understanding)

- **Name:** Marty
- **Experience:** ~12 projects total across iMovie and DaVinci Resolve. Comfortable with basic cut/edit workflow. Newer to color grading, Fairlight, Fusion. Self-described slow workflow.
- **Resolve version:** Free, fully updated to latest (auto-updates on launch)
- **Free or Studio:** Free
- **OS:** Windows (primary editing machine). Mac Mini still in ecosystem but used for Photos app only — not for editing.
- **Primary editing machine:** Windows PC (gaming rig built by Nick)
  - CPU: AMD Ryzen 7 7800X3D 8-Core (16 CPUs)
  - RAM: 64GB
  - GPU: NVIDIA GeForce RTX 4060 Ti / 16GB VRAM (CUDA acceleration — strong for Resolve)
- **Mac Mini:** Still active but slow for rendering and terrible with external drives. Used primarily to access iPhone photos/video via Photos app.
- **Media workflow:** Copies files from Mac → shared directory → D:/Video on Windows PC
- **Windows comfort level:** Rusty — hasn't used Windows regularly since XP era. New architecture feels unfamiliar.
- **Storage:**
  - D: drive (SSD, 2TB, ~half full) — working drive. D:/Video is the editing core.
  - D:/Video contains: Davinci_Media folder (project files/backups), all imports, all exports
  - External: 4TB spinning drive (manual backup — needs better workflow)
- **Cameras:**
  - GoPro Hero12 (primary, capture resolution unconfirmed)
  - GoPro Hero11 Mini (preferred for dipping videos — rugged, pocketable, $100 from friend)
  - Insta360 (has footage, used in winter project)
  - DJI Mini drone (has it, nervous to fly — wants to learn this summer)
  - Older DJI drone (phone-navigated, never used)
  - iPhone 12 Pro
- **Audio/VO setup:** Rode PodMic + Fifine gaming audio mixer → Windows Sound Recorder for VO capture (Fairlight direct recording not yet explored)
- **Stream Deck XL+:** Has DaVinci Resolve profile, ~1 month in — largely untapped
- **YouTube channel:** https://www.youtube.com/@corporatehippiesintheup
- **Artlist subscription:** Yes (music licensing for social/YouTube content)
- **ADHD:** Confirmed. Workflow and learning style can be more chaotic. Benefits from:
  - Elimination frameworks over open-ended tasks (clear finish lines help)
  - Tight keyboard shortcut loops for repetitive actions
  - Visual tools over text-based ones (markers don't work well — no visual in/out range; subclips preferred)
  - Structure imposed on overwhelming tasks (two-pass workflow, etc.)
- **Shooting style:** "Shoot first, find story later" — natural documentary instinct, valid but needs structure for the logging/selects phase
- **Self-awareness:** High. Directly names what works and what doesn't. Appreciates directness back. Self-deprecating humor without being insecure.
- **Current film project:** "Dips with the Girl Gang" (also considering "Daily Dips") — documentary short, 8:03, picture locked. See dip-film_project_state.md.

---

## SYSTEM / PROJECT SETTINGS (confirmed)

- **Timeline resolution:** 1920x1080 HD (confirmed on current project)
- **GoPro capture resolution:** Unconfirmed for Hero12 and Hero11 Mini — check camera settings
- **Project frame rate:** TBD
- **Export settings established:** MP4 / H.264 / Variable Bitrate / 40,000 Kb/s / Audio AAC 48kHz 320kbps
- **Working directory:** D:/Video (internal SSD)
- **Project files/backups:** D:/Video/Davinci_Media

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

### Session 2 — April 19, 2026

**Hardware / system (all confirmed this session — see User Profile above)**
- RTX 4060 Ti + CUDA = GPU acceleration in Resolve. This is why the PC beats the Mac Mini so decisively — discrete GPU vs. no real graphics card. The Mac wasn't failing because it's a Mac; it was failing because it doesn't have a real GPU.
- 64GB RAM is well above what most editors need. Headroom to spare.
- Ryzen 7 7800X3D is one of the best gaming CPUs made — Resolve will love it.

**Footage logging — Markers vs. Subclips:**
- Resolve Source Viewer holds only one active In/Out pair at a time — can't mark multiple selects in a single pass natively
- **Markers (M):** Drop flags while watching. Color-codeable, note-able. Fast but visual processing is weak — just dots on a clip, no in/out range visible. Marty finds these frustrating.
- **Subclips (Alt+B):** Set In (I) → Out (O) → Alt+B creates a subclip in the Media Pool. Visual and discrete. Marty's preferred method.
- **Alt+B is the default Create Subclip shortcut — confirmed working.** This is a significant workflow unlock.
- Subclip shortcuts are Stream Deck mappable — can make a dedicated button alongside I and O
- Keyboard customization: DaVinci Resolve menu → Keyboard Customization (Ctrl+Alt+K) → search "subclip"
- Third option: dump everything in a rough timeline and razor-cut selects — tried, doesn't work well for large piles

**Two-pass elimination workflow for large footage piles:**
- Don't start by looking for good — start by killing the obvious bad
- **Pass 1:** Scrub every clip in Media Pool, reject bin (or Red marker) anything clearly unusable. Fast and ruthless. 89GB probably has 30–40% obvious garbage.
- **Pass 2:** Now work the smaller pile. I/O/Alt+B loop, pull selects generously into a "Selects" bin.
- Psychology: elimination has a finish line. "Find the story" doesn't. Important for ADHD workflow.

**Story-from-footage approach:**
- "Shoot first, find story later" is valid — documentarians do it constantly
- Key questions after logging pass: What's the real subject? What feeling does this footage have? Where's the anchor shot?
- Humor in video comes from juxtaposition, not individual shots — pull both sides of funny moments
- Winter video tone identified: absurd humor + quiet beauty + love of place. Three things to look for in selects: (1) absurd humor, (2) quiet beauty, (3) winter management (connective tissue)

**VO recording:**
- Currently: Rode PodMic + Fifine mixer → Windows Sound Recorder → import to Resolve
- Better option not yet explored: record VO directly into Fairlight — cuts out the import step entirely
- Cover this in the dedicated Fairlight session

---

## OPEN QUESTIONS / THINGS TO EXPLORE

- [ ] **NEXT SESSION OPENER: Frame rate dialog** — "Change Project Frame Rate? The selected clips have a different frame rate to the project. Would you like to change your timeline frame rate to match? You can't undo this action." What it means, when to say yes vs. no, what actually happens either way.
- [ ] Confirm GoPro capture resolution (Hero12 and Hero11 Mini)
- [ ] Color grading fundamentals — next major learning area (also needed for Dips)
- [ ] Fairlight audio workflow — including direct VO recording into Fairlight
- [ ] Fusion — not yet touched
- [ ] Keyboard shortcuts — not yet mapped/learned systematically (Stream Deck profile exists but largely untapped)
- [ ] Proxy workflow — relevant if performance issues arise (probably fine with RTX 4060 Ti + SSD)
- [ ] Bin/media pool organization best practices
- [ ] Stream Deck XL — dedicated session

---

## TO-DO / WORKFLOW BACKLOG

- [ ] **FreeFileSync setup:** Replace manual stare-and-compare backup. D:/Video → 4TB external. Free, open source, one-click sync after setup.
- [ ] **Backblaze:** Verify license with Nick. Covers both internal and external drives. Third copy / offsite.
- [ ] **GoPro capture resolution:** Check camera settings on both Hero12 and Hero11 Mini.
- [ ] **Winter video project:** Pass 1 (reject bin), then Pass 2 (subclip selects into bin). Tone: absurd humor + quiet beauty + love of place.
- [ ] **DJI cameras:** Get more acquainted this summer — after Dips is complete.

---

## SESSION LOG

**Session 1 — April 18, 2026**
- Established this space as a general Resolve learning space (not just project advisory)
- Updated prompt_library.md section 2B to reflect new framing
- Worked through a real 90-second lake dip video project:
  - Music licensing research and Artlist search strategy
  - Cropped horizontal GoPro footage to vertical for YouTube Short / Facebook / Facebook / Instagram
  - Established YouTube export settings
  - Learned Paste Attributes for copying zoom/position across clips
  - Discovered preview window Fit mode issue — key takeaway
  - Learned timeline architecture / shared media pool model
  - Learned Timeline Versions vs duplicated timelines
  - Mute track as multi-version export workaround
- Final outcome: vertical Short posted to Facebook/Instagram with VO; skipped horizontal YouTube upload for this project
- Marty flagged: ask about full equipment and setup at next session opener

**Session 2 — April 19, 2026**
- Confirmed full hardware/system setup (see User Profile above — all TBDs resolved)
- Confirmed Resolve: Free version, fully updated
- Confirmed ADHD — important for workflow design, communication style, and how to structure overwhelming tasks
- Discussed why Windows PC beats Mac Mini for Resolve (discrete GPU / CUDA vs. integrated)
- Covered footage logging: Markers vs. Subclips. Marty prefers subclips — visual and discrete.
- **Alt+B = Create Subclip shortcut confirmed working.** Marty will add Stream Deck button.
- Covered two-pass elimination workflow for large pile-of-footage projects
- Introduced winter video project: ~89GB, GoPro Hero12 + Hero11 Mini + Insta360, tone identified
- Covered juxtaposition as the source of humor in video (not individual shots)
- Parked: frame rate dialog question — answer next session with footage context
- Recommended FreeFileSync for backup workflow improvement
- Noted: VO recording directly into Fairlight — cover in Fairlight session
- Title still undecided: "Dips with the Girl Gang" vs. "Daily Dips"

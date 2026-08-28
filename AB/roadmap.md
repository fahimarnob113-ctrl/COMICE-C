# IRONBLOOD — Development Roadmap (Revised)
### Target: Fully playable build by **August 1, 2026**

> **30-minute playtime. Magnificent, adaptive story. Build fast.**
> Tight enough to finish in one sitting. Deep enough to replay for the other ending.

---

## 🎯 THE SCOPE

| Element | Target |
|---|---|
| **Total playtime** | ~30 minutes |
| **Acts** | 3 |
| **Missions** | 6 side-scrolling stages (2 per act) + 1 boss per act |
| **Overworld** | Top-down district map between acts (DBZ Buu's Fury style) |
| **Playable characters** | KAEL only |
| **Controls** | Fully rebindable — defaults in config.js, live rebind in-game saves to localStorage |
| **Story depth** | Deep — 2 endings, adaptive CIPHER dialogue, loyalty system |
| **Platform** | Browser (HTML5) — no install |

### Why 30 Minutes Works
- Each mission is ~4–5 minutes of tight brawling
- Story delivered between missions — no gameplay time wasted
- Long enough to get attached to BORKOT before the choice matters
- Short enough to finish in one sitting and immediately replay for the other ending

---

## 🗺️ GAME FLOW

```
TITLE SCREEN
     ↓
OVERWORLD — NOAKHALI DISTRICT (top-down)
  Walk between zones, talk to BORKOT / JAMAL / MASUD
  Find the mission entry point
     ↓
STAGE 1: NOAKHALI BLOCK (~4 min)
  3 enemy waves, clear checkpoint, signal tower
     ↓
STAGE 2: THE FLOOD ROAD (~4 min)
  Escort BORKOT, hold the eastern gate
     ↓
BOSS: THE WARDEN
     ↓
CUTSCENE — Act I end + SIPHON REVELATION
     ↓
OVERWORLD — DUBAI QUARTER (unlocked)
     ↓
STAGE 3: DUBAI QUARTER (~5 min)
  Infiltrate AXIOM forward base
     ↓
STAGE 4: THE SIGNAL SPINE (~5 min)
  Destroy 4 feed towers, heaviest resistance
     ↓
BOSS: COMMANDANT VOSS
     ↓
CUTSCENE — Act II end
     ↓
OVERWORLD — THE DEEP (access point)
  BORKOT loyalty checked here
     ↓
STAGE 5: THE UNDERGROUND (~4 min)
  Siphon outer shell, Hollow Vein dense
     ↓
STAGE 6: CORE APPROACH (~3 min)
  No enemies — Siphon presence only. BORKOT stays.
     ↓
BOSS: THE SIPHON HERALD
     ↓
PLAYER CHOICE (Ending A or B based on flags)
     ↓
ENDING CUTSCENE
```

---

## 📖 STORY (See: story_draft.md for full text)

All story written. See [story_draft.md] for:
- Full character bibles (KAEL, CIPHER, BORKOT, JAMAL, MASUD)
- Act-by-act story with all cutscene text written
- All CIPHER transmissions (3 adaptive variants each)
- Both endings written in full
- All 6 document collectible texts
- Story/lore inspirations from games and films

**Boss designs: PENDING** — The Warden, Commandant Voss, Siphon Herald
designs to be customised before asset generation.

---

## 🖼️ ASSETS NEEDED

### Background Story Art (cutscene panels) — 6 total
> These are the "fuckton of background art" — static illustrated panels
> shown between missions to deliver story.

| Panel | Scene | When |
|---|---|---|
| 1 | Night street, checkpoint gate lit by floodlights | Act I pre-mission |
| 2 | Signal tower lit up, distant windows lighting | Act I post-mission |
| 3 | KAEL + BORKOT at gate, AXIOM facility in distance | Act I end |
| 4 | Dubai Quarter neon signs, AXIOM armoured trucks | Act II pre-mission |
| 5 | Feed towers against dark sky, energy pulses | Act II post-mission |
| 6 | Underground tunnel, walls pulsing teal | Act III pre-mission |

### Sprite Priority Queue (July 19+ image generation)

| # | Asset | Notes |
|---|---|---|
| 1 | KAEL sprite sheet | idle, walk×2, attack, jump, rage. 14×26px per frame |
| 2 | Noakhali Block tileset | ground, wall, platform, bg_wall. 16×16px |
| 3 | AXIOM Grunt sprite | idle, walk×2, attack. 12×22px |
| 4 | Iron Collar Heavy sprite | idle, walk×2, attack. 14×26px |
| 5 | Cutscene panels 1–3 | Act I story art |
| 6 | BORKOT sprite | idle, walk×2. 14×26px |
| 7 | Hollow Vein creature | idle (twitch), walk×2, attack. 12×20px |
| 8 | Dubai Quarter tileset | 16×16px |
| 9 | Cutscene panels 4–6 | Act II–III story art |
| 10 | Underground tileset | 16×16px, alien/organic aesthetic |
| 11 | THE WARDEN boss sprite | **design pending** |
| 12 | COMMANDANT VOSS boss | **design pending** |
| 13 | THE SIPHON HERALD boss | **design pending** |
| 14 | CIPHER portrait | dialogue box face |
| 15 | Title screen art | IRONBLOOD over Noakhali skyline |
| 16 | HUD elements | HP bar, rage bar, panel art |
| 17 | JAMAL, MASUD sprites | background/overworld NPCs |

**Full asset brief → see: asset_handoff_skill.md**
(Use this to generate assets in another model with full context preserved)

---

## 🗓️ PHASE BREAKDOWN

---

### PHASE 1 — ENGINE (July 12–18)
**What needs building:**

- [ ] **Overworld scene** — top-down map, KAEL walks between zones, enters mission portals
- [ ] **Cutscene screen** — full-screen art panel + CIPHER text, advance with Enter
- [ ] **Boss enemy class** — bigger hitbox, 2–3 phase transitions, special attacks
- [ ] **Adaptive flag system** — 4 variables: BORKOT loyalty, CIPHER confidence, docs found, siphon exposure
- [ ] **Document pickup** — collectible item triggers lore dialogue box
- [ ] **Win condition** — boss kill → cutscene → overworld return
- [ ] **Death counter per mission** — feeds CIPHER confidence flag
- [ ] **BORKOT NPC** — escort/follow AI in Stage 2
- [ ] **Rebindable controls** — default keys in config.js + in-game rebind screen + localStorage save
- [ ] **Controls screen** — accessible from title menu and pause menu

**Already done:**
- ✅ Side-scrolling engine (game.js)
- ✅ Config-driven content (config.js)
- ✅ CIPHER dialogue system
- ✅ Stage 1 tilemap (Noakhali Block)
- ✅ 3 enemy types with AI
- ✅ KAEL with rage system + improved art
- ✅ Title screen

---

### PHASE 2 — ASSETS (July 19–22)
Generate all sprites, tilesets, and cutscene art using the asset_handoff_skill.md brief.
Boss designs must be confirmed before this phase begins.

---

### PHASE 3 — CONTENT (July 22–28)
- [ ] Wire all dialogue into config.js (from story_draft.md)
- [ ] Build Stage 2 tilemap (Dubai Quarter)
- [ ] Build Stage 3 tilemap (Underground)
- [ ] Implement COMMANDANT VOSS boss fight
- [ ] Implement THE SIPHON HERALD boss fight (2 phases)
- [ ] Implement both endings
- [ ] Wire all 4 adaptive flags to their triggers
- [ ] Add music (Suno.ai or sourced)
- [ ] Add SFX (pixabay / sfxr)
- [ ] Overworld NPC dialogue (BORKOT, JAMAL, MASUD)

---

### PHASE 4 — POLISH (July 28–August 1)
- [ ] Playthrough both endings
- [ ] Balance enemy counts and boss difficulty
- [ ] Screen shake on boss hits
- [ ] Cutscene panel transitions (fade in/out)
- [ ] Death feel (not frustrating for a 5-min game)
- [ ] Title screen final

---

## ✂️ SAFE TO CUT (If Behind)

| Feature | Cut Impact |
|---|---|
| Overworld exploration | Cut to linear mission select screen instead |
| Document collectibles | Remove entirely, core story still intact |
| Siphon Exposure flag | Keep only 3 flags instead of 4 |
| JAMAL / MASUD NPCs | Replace with CIPHER text only |
| Stage 2 (Dubai Quarter) | Merge Acts I and II into one stage |

**Never cut:**
- Both endings
- CIPHER adaptive tone
- The Siphon reveal
- BORKOT loyalty system

---

## 📎 COMPANION DOCUMENTS

| Document | Purpose |
|---|---|
| [story_draft.md] | Full story, all dialogue, both endings, inspirations |
| [asset_handoff_skill.md] | Brief for generating assets in another model |
| [modding_guide.md] | How to tweak dialogue, stats, missions yourself |
| [inspiration_guide.md] | Games, films, pixel art sites, music references |
| [world_bible.md] | Deep lore — districts, factions, history |

---

*Roadmap v2 — July 12, 2026 | Updated from user feedback*

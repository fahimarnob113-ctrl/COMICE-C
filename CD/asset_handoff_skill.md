# IRONBLOOD — Asset Generation Handoff (FINAL LOCKED)
### For use in any AI model with image generation capability
### Full context included — no prior conversation needed

---

## 🎮 GAME OVERVIEW

**IRONBLOOD** is a browser-based HTML5 side-scrolling beat-em-up.
- Native resolution: **480 × 270 pixels** (scaled up to fill screen)
- Tile size: **16 × 16 pixels**
- Aesthetic: **16-bit GBA / Capcom CPS2 arcade pixel art** — chunky, high contrast, vibrant dark urban Bangladesh
- Engine: vanilla JS canvas, no frameworks

---

## 🎨 ART STYLE RULES (Apply to Everything)

1. **Black outlines on all sprites** — 1px dark border (`#07070e`) around every shape
2. **Limited palette** — 8 to 16 colours per character maximum
3. **3D shading** — top-left edge of every shape = lighter highlight, bottom-right = darker shadow
4. **Readable silhouette** — recognisable in pure black at intended size
5. **No anti-aliasing** — hard pixel edges only
6. **No gradients inside sprites** — solid fill blocks only
7. **Inspired by**: Metal Slug, Capcom CPS2, Streets of Rage 4
8. **Setting**: Night. Dark urban Bangladesh. Neon green (`#00e87a`) + amber (`#f5a623`) + teal (`#00d4aa`) dominant accents.

### Pixel Art Image Prompt Template
```
[character description], GBA pixel art, retro 16-bit sprite, 
limited colour palette (max 16 colours), black outline, 
no anti-aliasing, hard pixel edges, transparent background,
[W]x[H] pixels, dark colour scheme, neon accents
```

---

## 👥 CHARACTERS — Sprite Sheets

Each character faces **right**. Engine mirrors for left-facing. Transparent PNG.

### 1. KAEL (The Iron Hound — Protagonist)
- **Palette**: Charcoal grey, olive green, warm dark skin, scarred face, **neon green (#00e87a)** veins and eye glow.
- **Weapon**: *The Shard* (colossal jagged iron cleaver sword).
- **Sprite size**: 18w × 28h pixels.
- **Frames**: Idle (4 frames), Run (6 frames), Attack Combo (3 frames), Jump (2 frames), Siphon Rage Burst (4 frames).

### 2. SURAIYA (Hero Codename: Gilded Lotus / "The Diva")
- **Palette**: Ruby crimson, burnished gold, **magenta to pastel pink** gradient hair.
- **Weapon**: Segmented golden ribbon whip-sword.
- **Sprite size**: 16w × 28h pixels.
- **Frames**: Idle (4 frames), Acrobatic Leap (4 frames), Ribbon Whip Sweep (4 frames).

### 3. KPOP NINJA (Real Name: Arman / "The Sapphire Marksman")
- **Palette**: Matte black compression shirt, cream/off-white baggy martial arts pants, spiky silver-white hair, **electric sapphire-blue (#0099ff)** glowing eyes.
- **Weapon**: 7-foot matte-black anti-materiel sniper rifle.
- **Sprite size**: 16w × 28h pixels.
- **Frames**: Idle (4 frames), Aim/Snipe (3 frames), 60mph Cable Slide (3 frames).

### 4. ZINNIA (Dr. Zinnia Haque / "The Smiling Toxicologist")
- **Palette**: Spotless white lab coat, deep royal purple tunic, gold wireframe glasses, **violet (#9933ff)** chemical glow.
- **Weapon**: Pneumatic chemical injector pen.
- **Sprite size**: 14w × 24h pixels.
- **Frames**: Idle (4 frames), Injector Dash (3 frames), Vial Toss (3 frames).

### 5. SURJO (The Siphon Plant / "The Human Typhoon")
- **Palette**: **Bright crimson red (#ff2233)** techwear trench coat, black tactical pants, messy dirty-blonde spiky hair, chrome prosthetic arm, **golden-teal (#00e8c6)** Siphon angel wings.
- **Weapon**: Custom silver break-action magnum (*The Silver Starling*).
- **Sprite size**: 18w × 30h pixels.
- **Frames**: Idle (4 frames), Magnum Fan-Fire (4 frames), Siphon Wing Flare (4 frames).

### 6. BAHADUR (The Ancient Soldier / "The Relic")
- **Palette**: Weathered forest green, antique bronze plate, brown leather straps, dark beard (Jensen Ackles likeness), **radiogenic amber-green** core glow.
- **Weapon**: Heavy pointed bronze-and-steel heater shield + trench knife.
- **Sprite size**: 20w × 30h pixels.
- **Frames**: Idle (4 frames), Shield Charge / Bash (4 frames), Chest Blast Overcharge (4 frames).

### 7. MASTER DIGANTA (The Quantum Sage)
- **Palette**: Midnight-blue ceremonial robe, cream silk lining, flowing silver-white hair and beard, **brilliant golden (#ffcc00)** fractal mandalas.
- **Weapon**: Dark wood staff with floating brass quantum gyroscope orb.
- **Sprite size**: 18w × 32h pixels.
- **Frames**: Idle (4 frames), Golden Mandala Ward (4 frames), Staff Harmonic Tap (3 frames).

### 8. GOVERNOR MUJIB (The Sovereign Titan — Boss)
- **Palette**: Tailored black high-collared Mujib coat with crimson lining and gold aiguillettes, black retro horn-rimmed glasses, **crimson (#cc0000)** gravitational aura.
- **Weapon**: Cybernetic amber pipe, gold magnum revolver (*The Mandate*), titanium combat spine.
- **Sprite size**: 22w × 34h pixels.
- **Frames**: Idle (4 frames), State Decree Laser Call (3 frames), Heavy Kinetic Palm Strike (4 frames), Sovereign Gravity Surge (4 frames).

### 9. JAHANGIR BHAI (The Godfather of the Wet Bazaars)
- **Palette**: Charcoal pinstripe suit, black wool overcoat with velvet lapel, dark fedora, gold signet rings, Havana cigar with **amber smoke**.
- **Weapon**: Gold snub-nosed revolver (*The Ledger*).
- **Sprite size**: 18w × 30h pixels.

### 10. USTAD (Master Mechanic)
- **Palette**: Faded blue denim jumpsuit, grease stains, **cracked yellow hard-hat (#ffcc00)**.
- **Weapon**: 36-inch cast-iron pipe wrench.
- **Sprite size**: 16w × 26h pixels.

### 11. BORKOT (Combat Mech)
- **Palette**: Matte black and dark red armor plating, rusted scrap metal right arm, **electric blue (#00aaff)** mono-eye optic.
- **Sprite size**: 26w × 38h pixels.

### 12. JAMAL (Street Runner)
- **Palette**: Bright oversized neon jacket, checked red/white *gamcha*, frosted-tip hair.
- **Weapon**: Dual short blades.
- **Sprite size**: 14w × 24h pixels.

---

## 🗺️ TILESETS NEEDED (16 × 16 Pixels per Tile)

1. **Noakhali Block Tileset**: Flooded asphalt, dark earth, wet corrugated iron walls, wooden stilt platforms, dim brick with Bengali neon graffiti.
2. **The Wet Bazaars Tileset**: Lashed wooden barges, sampan walkways, floating market stalls, lantern posts, rippling dark canal water.
3. **The Sundarbans Biolume Tileset**: Glowing teal algae water, twisted glass-bark roots, glowing moss platforms, swamp mist background tiles.
4. **The Dubai Quarter Tileset**: Polished chrome and white marble, glass floor tiles, neon advertising signage, sleek metal railings.
5. **The Siphon Core Tileset**: Dark obsidian chasm rock, pulsing organic bio-magnetic wall tiles, glowing teal energy conduit streams.

---

## 🖼️ CUTSCENE BACKGROUND PANELS (480 × 270 px)

1. `cutscene_noakhali_night.png` — Noakhali Block stilt-slums under heavy monsoon rain and neon searchlights.
2. `cutscene_wet_bazaars.png` — The floating night market with Jahangir Bhai's *Sultana* barge anchored in the center.
3. `cutscene_cryo_vault.png` — Sublevel 7 cryo-vault showing Bahadur's frosted Mark-IV pod unsealing.
4. `cutscene_meghna_bridge.png` — The Broken Meghna suspension bridge during the Surjo vs. KPop Ninja sniper duel.
5. `cutscene_drowned_archive.png` — Master Diganta's submerged ancient library in a dry golden energy bubble.
6. `cutscene_governor_pavilion.png` — The glass-domed Grand Pavilion atop the floating presidential dreadnought in a lightning storm.
7. `cutscene_siphon_ascension.png` — Kael transfigured into the Sovereign Guardian on a cliff overlooking Bangladesh under the aurora storm veil.

---

## 🔌 ENGINE INTEGRATION (Wiring into config.js)

```javascript
// Assets declaration in config.js
window.CONFIG = {
  assets: {
    sprites: {
      kael: 'assets/sprites/kael_sheet.png',
      suraiya: 'assets/sprites/suraiya_sheet.png',
      kpop_ninja: 'assets/sprites/kpop_ninja_sheet.png',
      zinnia: 'assets/sprites/zinnia_sheet.png',
      surjo: 'assets/sprites/surjo_sheet.png',
      bahadur: 'assets/sprites/bahadur_sheet.png',
      master_diganta: 'assets/sprites/master_diganta_sheet.png',
      governor_mujib: 'assets/sprites/governor_mujib_sheet.png',
      jahangir_bhai: 'assets/sprites/jahangir_bhai_sheet.png',
      ustad: 'assets/sprites/ustad_sheet.png',
      borkot: 'assets/sprites/borkot_sheet.png',
      jamal: 'assets/sprites/jamal_sheet.png'
    },
    tilesets: {
      noakhali: 'assets/tiles/noakhali_tileset.png',
      wet_bazaars: 'assets/tiles/wet_bazaars_tileset.png',
      biolume: 'assets/tiles/biolume_tileset.png',
      dubai_quarter: 'assets/tiles/dubai_quarter_tileset.png',
      siphon_core: 'assets/tiles/siphon_core_tileset.png'
    }
  }
};
```

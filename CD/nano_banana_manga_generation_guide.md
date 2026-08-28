# 🍌 IRONBLOOD — Gemini Nano Banana Manga Generation Guide
### The Complete Production Manual for Generating Manga Panels with Google's Nano Banana (Gemini 3 Pro Image)
*Optimized for: Google AI Studio, Google Flow (Frames & Ingredients), and Native Gemini Multimodal Canvas.*

---

# 📑 TABLE OF CONTENTS
1. [Why Nano Banana Is Built for This Manga](#1-why-nano-banana-is-built-for-this-manga)
2. [The Nano Banana 3-Step Character Lock Workflow](#2-the-nano-banana-3-step-character-lock-workflow)
3. [Nano Banana Prompt Architecture (Clean Natural Language)](#3-nano-banana-prompt-architecture)
4. [Step-by-Step Execution in Google AI Studio / Google Flow](#4-step-by-step-execution)
5. [Direct Copy/Paste Nano Banana Prompts for Scene 1 (Pages 1 & 2)](#5-direct-copypaste-prompts-for-scene-1)

---

# 1. WHY NANO BANANA IS BUILT FOR THIS MANGA

Google's **Nano Banana (Gemini 3 Pro Image)** provides critical advantages over older diffusion tools:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│ 1. NATIVE MULTI-IMAGE REFERENCE LOCKING (Up to 14 Reference Images)         │
│    Attach your character turnaround sheet directly into the chat prompt.    │
│                                                                             │
│ 2. NATURAL LANGUAGE PROMPT COMPREHENSION (No Cryptic Flags Needed)         │
│    Understands complex camera angles, action vectors, and lighting natively. │
│                                                                             │
│ 3. INTERLEAVED MANGA PIPELINE                                               │
│    Can generate panel layouts, dialogue, and rendered panels in one stream. │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

# 2. THE NANO BANANA 3-STEP CHARACTER LOCK WORKFLOW

```
STEP 1: GENERATE 3-VIEW TURNAROUND SHEET
Use Nano Banana to generate the front, side, and back reference sheet for Kael,
Suraiya, KPop Ninja, and Governor Mujib.
                           │
                           ▼
STEP 2: ATTACH REFERENCE IMAGE IN PROMPT
In Google AI Studio / Google Flow, attach the turnaround image directly into
your message box.
                           │
                           ▼
STEP 3: PROMPT NANO BANANA WITH IDENTITY ANCHOR
"Generate a manga panel matching the exact character identity, facial scars,
and tactical armor from the attached reference image..."
                           │
                           ▼
RESULT: PERFECT CHARACTER CONSISTENCY WITH ZERO FACIAL DRIFT!
```

---

# 3. NANO BANANA PROMPT ARCHITECTURE

Nano Banana responds best to structured natural language. Format your panel prompts using this 4-part stack:

```
[1. REFERENCE DIRECTIVE] : "Maintain exact character appearance, face, and clothing from the attached reference image [Image 1]."
[2. SCENE & CAMERA]      : "Manga panel, low-angle dynamic hero shot, heavy monsoon rain at midnight in flooded stilt slums."
[3. ACTION & FORESHORTENING]: "KAEL resting his colossal jagged cleaver sword (The Shard) blazing with neon green energy on his shoulder."
[4. ART STYLE SPECIFIER] : "16-bit arcade pixel art style, Capcom CPS2 aesthetic, Metal Slug texture, bold dark ink contours, volumetric green neon lighting, high contrast."
```

---

# 4. STEP-BY-STEP EXECUTION IN GOOGLE AI STUDIO / GOOGLE FLOW

### 🔹 Method A: Google AI Studio (`aistudio.google.com`)
1. **Select Model:** Choose **Gemini 2.0 Flash / Pro** or **Gemini 3 Pro Multimodal (Nano Banana)**.
2. **System Instructions:** Paste [google_flow_manga_agent_instructions.md](file:///C:/Users/Gulam%20Mustafa/.gemini/antigravity/brain/aa022bf9-c035-4c2e-ba44-f330bde2cb13/google_flow_manga_agent_instructions.md) into the left System Instructions box.
3. **Attach Character Sheet:** Click the **"+" (Add Image)** icon in the prompt box and attach your generated Turnaround Sheet (`kael_turnaround.png`).
4. **Generate Panel:** Paste the panel prompt from [master_turnaround_sheets_and_anchor_library.md](file:///C:/Users/Gulam%20Mustafa/.gemini/antigravity/brain/aa022bf9-c035-4c2e-ba44-f330bde2cb13/master_turnaround_sheets_and_anchor_library.md) or [manga_production_handoff.md](file:///C:/Users/Gulam%20Mustafa/.gemini/antigravity/brain/aa022bf9-c035-4c2e-ba44-f330bde2cb13/manga_production_handoff.md).
5. **Download:** Click on the generated image to save full-resolution `.png` directly to your machine.

---

### 🔹 Method B: Google Flow (Frames & Ingredients)
1. **Create Ingredients:** In the left sidebar, click **"Add Ingredient"** ➔ upload `kael_turnaround.png`, `suraiya_turnaround.png`, etc.
2. **Set Flow Nodes:** Connect your **Gemini Script Node** to the **Nano Banana Image Node**.
3. **Link Ingredients:** Tag each image node with `@KAEL` or `@SURAIYA` so Nano Banana automatically locks the character's facial weights.
4. **Batch Run:** Click **"Execute All Frames"** ➔ Nano Banana will render the entire comic sequence into your Google Drive folder automatically.

---

# 5. DIRECT COPY/PASTE NANO BANANA PROMPTS FOR SCENE 1

---

### 📸 Turnaround Reference Generation (Do This First)

#### Prompt: KAEL 3-View Turnaround Reference Sheet
> `Character design turnaround model sheet of KAEL. Shows 3 full-body views: front view, side profile view, and back view on a clean neutral grey background. KAEL is a rugged, muscular South Asian combat veteran in his mid-30s with scarred dark skin, thick dark stubble, and haunted piercing eyes. Wearing dark charcoal tactical fatigue armor with combat straps and heavy reinforced boots. Pulsing neon-green Siphon energy veins glow on his left arm and chest. Resting a colossal jagged iron cleaver sword (The Shard) with glowing green runic fissures on his shoulder. 16-bit arcade pixel art style, Capcom CPS2 model sheet, sharp clean pixel contours, flat planar shading, highly detailed reference sheet.`

---

### 📖 Panel Prompts (Attach KAEL Reference Image to Each Prompt)

#### Page 1, Panel 1 (Wide Slum Splash):
> `Manga splash panel, extreme wide angle panoramic shot of flooded cyberpunk stilt slums in Noakhali Bangladesh at 02:00 AM in heavy monsoon rain. Dilapidated corrugated metal shanties on stilts over dark rippling canal water, glowing Bengali neon signs in emerald green and magenta, massive brutalist corporate blast-gates with blinding harsh blue searchlights, volumetric rain sheets, 16-bit arcade pixel art style, Metal Slug aesthetic, dark atmospheric cyberpunk, high contrast.`

#### Page 1, Panel 2 (Ustad's Workshop):
> `Manga panel, interior of a rusted dry-dock barge workshop. USTAD, a sturdy weathered South Asian mechanic with a thick mustache and cracked yellow construction hard-hat, tightening pneumatic bolts with a heavy wrench on BORKOT, a massive 9-foot matte-black combat mech with a glowing blue mono-eye. Young JAMAL staring at his hand in confusion. Warm tungsten work lamps, blue steam venting, rain pouring outside open bay door, 16-bit arcade pixel art style, Capcom CPS2 aesthetic, industrial detail.`

#### Page 1, Panel 3 (Kael Hero Entrance):
*(Attach KAEL Turnaround Image)*
> `Manga panel, dramatic low angle hero shot. Using the exact character appearance, facial scars, and tactical armor from the attached reference image [Image 1]: KAEL stepping out into heavy monsoon rain at midnight. Scarred dark skin, haunted eyes, pulsing neon green Siphon veins glowing down his left arm. Resting his colossal jagged cleaver sword (The Shard) on his shoulder, rain water spraying off the blade. 16-bit arcade pixel art style, Capcom CPS2 beat-em-up protagonist, intense lighting, high contrast.`

#### Page 2, Panel 3 (Kael's Downward Cleave Climax):
*(Attach KAEL Turnaround Image)*
> `Manga full page climax splash panel. Using the exact character appearance from the attached reference image [Image 1]: KAEL leaping through mid-air in heavy pouring rain, executing an explosive downward cleave with his colossal jagged iron cleaver sword blazing with roaring neon green Siphon energy flames, cleaving clean through an armored cyborg boss in a blinding burst of sparks, hydraulic fluid, and rain spray. Dramatic foreshortening, Sakuga action lines, 16-bit arcade pixel art style, masterpiece contrast.`

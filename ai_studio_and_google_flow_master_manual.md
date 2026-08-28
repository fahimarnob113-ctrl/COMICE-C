# 🚀 IRONBLOOD — Complete Google AI Studio & Google Flow Production Manual
### The Definitive Step-by-Step Production Guide for Finishing the 15-Page Manga
*Target Models: Gemini 2.0 Flash / Gemini 2.0 Pro / Gemini Nano Banana (Gemini 3 Pro Image)*

---

# 📑 TABLE OF CONTENTS
1. [PART 1: THE GOOGLE AI STUDIO MASTER MANUAL (Primary Workflow)](#part-1-the-google-ai-studio-master-manual)
   - [Phase 1: Environment Setup & System Instructions](#phase-1-environment-setup--system-instructions)
   - [Phase 2: Generating Turnaround Sheets (Character Anchors)](#phase-2-generating-turnaround-sheets-character-anchors)
   - [Phase 3: Multimodal Reference Prompting for Pages 1–15](#phase-3-multimodal-reference-prompting-for-pages-115)
   - [Phase 4: Bulk Export & Asset Organization](#phase-4-bulk-export--asset-organization)
2. [PART 2: THE GOOGLE FLOW MASTER MANUAL (Node/Canvas Workflow)](#part-2-the-google-flow-master-manual)
   - [Phase 1: Flow Canvas Setup](#phase-1-flow-canvas-setup)
   - [Phase 2: Character Ingredients & Frames Configuration](#phase-2-character-ingredients--frames-configuration)
   - [Phase 3: Wiring Script Nodes to Nano Banana Image Nodes](#phase-3-wiring-script-nodes-to-nano-banana-image-nodes)
   - [Phase 4: Automated Batch Run to Google Drive](#phase-4-automated-batch-run-to-google-drive)
3. [Quick Reference Cheat Sheet](#quick-reference-cheat-sheet)

---

# PART 1: THE GOOGLE AI STUDIO MASTER MANUAL

*Google AI Studio (`aistudio.google.com`) is the most powerful tool for this project because its 2,000,000 token context window allows you to keep the entire universe, all 12 characters, 15 pages of scripts, and visual prompts in memory simultaneously without token forgetting.*

```
┌─────────────────────────────────────────────────────────────────────────────┐
│ GOOGLE AI STUDIO 4-PHASE WORKFLOW:                                          │
│                                                                             │
│ [Phase 1: Setup 2M Token Prompt] ──► [Phase 2: Render Turnarounds]          │
│                                              │                              │
│                                              ▼                              │
│ [Phase 4: Export PNGs & Script]  ◄── [Phase 3: Multi-Image Panel Prompts]   │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

### 🛠️ PHASE 1: ENVIRONMENT SETUP & SYSTEM INSTRUCTIONS

1. **Navigate to AI Studio:** Go to [aistudio.google.com](https://aistudio.google.com) and log in with your Google account.
2. **Create New Prompt:** Click **"Create New Prompt"** (Select **Chat Prompt**).
3. **Configure Model Parameters (Right Sidebar):**
   * **Model:** Select **`Gemini 2.0 Flash`** (for lightning fast multimodal) or **`Gemini 2.0 Pro`** (for maximum reasoning & detail).
   * **Temperature:** Set to `0.7` (optimal balance for narrative flair and strict lore consistency).
   * **Top P:** `0.95`
   * **Safety Settings:** Set to *Block few / minimal* so combat action (explosions, cleaver strikes) does not trigger false positive moderation flags.
4. **Configure System Instructions (Left / Top Box):**
   * Click on the **"System Instructions"** box with the pencil icon.
   * Copy the entire contents of [google_flow_manga_agent_instructions.md](file:///C:/Users/Gulam%20Mustafa/.gemini/antigravity/brain/aa022bf9-c035-4c2e-ba44-f330bde2cb13/google_flow_manga_agent_instructions.md) AND [grand_master_story_bible.md](file:///C:/Users/Gulam%20Mustafa/.gemini/antigravity/brain/aa022bf9-c035-4c2e-ba44-f330bde2cb13/grand_master_story_bible.md).
   * Paste them both into the **System Instructions** box.
   * *(AI Studio will show ~15,000 / 2,000,000 tokens used — leaving 99% of your context window free for panel generation).*

---

### 🎨 PHASE 2: GENERATING TURNAROUND SHEETS (CHARACTER ANCHORS)

Before generating manga panels, you must render the 3-view turnaround model sheets.

1. **In the Chat Input Box, paste the Turnaround Prompt for Kael from [master_turnaround_sheets_and_anchor_library.md](file:///C:/Users/Gulam%20Mustafa/.gemini/antigravity/brain/aa022bf9-c035-4c2e-ba44-f330bde2cb13/master_turnaround_sheets_and_anchor_library.md):**
   > `Generate image: Character design turnaround model sheet of KAEL. Shows 3 full-body views: front view, side profile view, and back view on a clean neutral grey background. KAEL is a rugged, muscular South Asian combat veteran in his mid-30s with scarred dark skin, thick dark stubble, and haunted piercing eyes. Dark charcoal tactical fatigue armor with combat straps and heavy boots. Pulsing neon green Siphon energy veins glowing on left arm and chest. Resting a colossal jagged iron cleaver sword (The Shard) on shoulder. 16-bit arcade pixel art style, Capcom CPS2 model sheet, sharp clean pixel contours, flat planar shading, highly detailed reference sheet.`
2. **Execute & Download:** Click Run / Send. Nano Banana / Gemini will render the image. Click the generated image and click **Download** (`kael_turnaround.png`).
3. **Repeat for Core Characters:**
   * Render `suraiya_turnaround.png`
   * Render `kpop_ninja_turnaround.png`
   * Render `governor_mujib_turnaround.png`

---

### 📖 PHASE 3: MULTIMODAL REFERENCE PROMPTING FOR PAGES 1–15

Now you generate the actual comic panels with **zero visual drift** by attaching your reference turnarounds:

1. **Attach Reference Image:** In the chat input box, click the **"+" (Add File / Image)** button and select `kael_turnaround.png`.
2. **Input Structured Panel Prompt (Example: Page 1 Panel 3):**
   > `Using the exact character appearance, facial scars, and tactical armor from the attached reference image [Image 1]:`  
   > `Render Manga Panel: Page 1, Panel 3 (Low-angle hero shot).`  
   > `Scene: KAEL stepping out into heavy monsoon rain at midnight in Noakhali Block. Scarred dark skin, haunted eyes, pulsing neon green Siphon veins glowing down his left arm. Resting his colossal jagged cleaver sword (The Shard) on his shoulder, rain water spraying off the blade.`  
   > `SFX & Dialogue: KAEL: "Whatever. Tell the prompter to lock my seed. We're taking the gate."`  
   > `Style: 16-bit arcade pixel art style, Capcom CPS2 beat-em-up protagonist, intense directional lighting, high contrast.`
3. **Multi-Character Scenes (e.g. Page 6 Gunslinger Duel):**
   * Attach **two** reference images: `surjo_turnaround.png` and `kpop_ninja_turnaround.png`.
   * Prompt: *"Maintain Surjo's appearance from [Image 1] and KPop Ninja's appearance from [Image 2]. Render Page 6 Panel 2..."*
4. **Follow the Complete Script:** Copy each panel prompt directly from [manga_production_handoff.md](file:///C:/Users/Gulam%20Mustafa/.gemini/antigravity/brain/aa022bf9-c035-4c2e-ba44-f330bde2cb13/manga_production_handoff.md) page by page (Pages 1 to 15).

---

### 💾 PHASE 4: BULK EXPORT & ASSET ORGANIZATION

1. **Saving Full-Resolution Images:** Click on each generated panel in the chat and save as:
   * `Page_01_Panel_01.png`, `Page_01_Panel_02.png`, etc.
2. **Exporting Entire Script & Prompts:**
   * In the top right corner of AI Studio, click **"Get Code"** or **"Export"** to save your entire production conversation as a JSON or Markdown file for backup.

---

# PART 2: THE GOOGLE FLOW MASTER MANUAL

*Google Flow is Google's node-based canvas interface. It allows you to build visual automated pipelines using "Frames" (pages) and "Ingredients" (locked character visual references).*

```
┌─────────────────────────────────────────────────────────────────────────────┐
│ GOOGLE FLOW NODE PIPELINE ARCHITECTURE:                                     │
│                                                                             │
│ [Character Ingredients: Kael, Suraiya, Mujib]                               │
│                      │                                                      │
│                      ▼                                                      │
│ [Gemini Script Node] ──► [Nano Banana Image Node] ──► [Google Drive Export] │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

### 🏗️ PHASE 1: FLOW CANVAS SETUP

1. **Open Google Flow:** Open your Google Flow / Vertex AI GenAI Canvas workspace.
2. **Create Project:** Click **"New Flow"** ➔ Name it: **`IRONBLOOD_Manga_Master`**.
3. **Set Canvas Dimensions:** Set project aspect ratio default to `16:9` (or `2:3` for cover and vertical splash pages).

---

### 🧩 PHASE 2: CHARACTER INGREDIENTS & FRAMES CONFIGURATION

Google Flow uses **"Ingredients"** as persistent visual anchors:

1. **Create Character Ingredients:**
   * In the left panel, click **"Ingredients"** ➔ **"Add New Ingredient"**.
   * **Ingredient 1:** Name it `@KAEL`. Upload your `kael_turnaround.png` and paste Kael's anchor description from [master_turnaround_sheets_and_anchor_library.md](file:///C:/Users/Gulam%20Mustafa/.gemini/antigravity/brain/aa022bf9-c035-4c2e-ba44-f330bde2cb13/master_turnaround_sheets_and_anchor_library.md).
   * **Ingredient 2:** Name it `@SURAIYA`. Upload `suraiya_turnaround.png`.
   * **Ingredient 3:** Name it `@KPOP_NINJA`. Upload `kpop_ninja_turnaround.png`.
   * **Ingredient 4:** Name it `@GOVERNOR_MUJIB`. Upload `governor_mujib_turnaround.png`.
2. **Create 15 Page Frames:**
   * Create 15 Frame containers on your canvas: `Frame_01` (Page 1) to `Frame_15` (Page 15).

---

### 🔌 PHASE 3: WIRING SCRIPT NODES TO NANO BANANA IMAGE NODES

1. **Add Script Controller Node (Node A):**
   * Add a **Gemini 2.0 Flash / Pro Text Node**.
   * In its System Instructions, paste [google_flow_manga_agent_instructions.md](file:///C:/Users/Gulam%20Mustafa/.gemini/antigravity/brain/aa022bf9-c035-4c2e-ba44-f330bde2cb13/google_flow_manga_agent_instructions.md).
2. **Add Nano Banana Image Generator Nodes (Node B):**
   * Add an **Imagen 3 / Nano Banana Image Node** inside each Page Frame.
   * Link the corresponding Character Ingredients (e.g. tag `@KAEL` to Node B).
   * Set Style Preset: `Pixel Art / Retro Arcade 16-Bit`.
3. **Connect Node A ➔ Node B:**
   * Wire the `IMAGE GENERATION PROMPT` output from Node A directly into the input trigger of Node B.

---

### 📤 PHASE 4: AUTOMATED BATCH RUN TO GOOGLE DRIVE

1. **Configure Storage Destination:**
   * In the Flow canvas settings, click **"Output Destination"**.
   * Connect your **Google Drive Folder**: `My Drive/IRONBLOOD_Manga_Final/`.
2. **Run Pipeline:**
   * Click **"Execute All Frames / Batch Run"**.
   * Google Flow will sequentially generate every panel across all 15 pages and deposit crisp, high-resolution `.png` files named `Page_01_Panel_01.png`, `Page_01_Panel_02.png`, etc., straight into your Google Drive folder.

---

# ⚡ QUICK REFERENCE CHEAT SHEET

| Task | Google AI Studio (`aistudio.google.com`) | Google Flow |
|---|---|---|
| **System Prompt Setup** | Paste into left "System Instructions" box | Paste into Text Controller Node |
| **Character Reference Lock** | Click `+` and attach turnaround image directly | Add as `@CHARACTER` Ingredient |
| **Panel Prompts** | Copy from [manga_production_handoff.md](file:///C:/Users/Gulam%20Mustafa/.gemini/antigravity/brain/aa022bf9-c035-4c2e-ba44-f330bde2cb13/manga_production_handoff.md) | Paste into Frame Prompt Inputs |
| **Model Selection** | `Gemini 2.0 Flash / Pro` + Nano Banana | `Gemini 2.0` + `Imagen 3 / Nano Banana` |
| **File Export** | Click images to download `.png` directly | Auto-exports batch `.png` to Google Drive |

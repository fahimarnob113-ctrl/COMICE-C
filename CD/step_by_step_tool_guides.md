# IRONBLOOD — Step-by-Step Tool Setup & Generation Guides
### Complete Manual for Gemini Gems, Google AI Studio, and Google Flow

---

# 💎 GUIDE 1: GEMINI GEMS + GOOGLE DRIVE
*Best for: All-in-one conversational directing + direct Imagen 3 image rendering in chat.*

```
[ Step 1: Gem Manager ] ──► [ Step 2: Attach Drive Doc ] ──► [ Step 3: Chat & Render ] ──► [ Step 4: Download ]
```

### Step 1: Create Your Custom Gem
1. Go to [gemini.google.com](https://gemini.google.com).
2. Look at the left sidebar and click on **"Gem manager"** (or **"Explore Gems"** ➔ **"New Gem"**).
3. Set the Name to: **`IRONBLOOD Manga Director`**.

### Step 2: Configure Instructions & Knowledge (Google Drive)
1. In the **Instructions** box of your Gem, copy and paste the contents of:  
   👉 [google_flow_manga_agent_instructions.md](file:///C:/Users/Gulam%20Mustafa/.gemini/antigravity/brain/aa022bf9-c035-4c2e-ba44-f330bde2cb13/google_flow_manga_agent_instructions.md).
2. Click the **"Knowledge" / "+" / "Add Files"** button and select **Google Drive**.
3. Upload and select:  
   👉 [grand_master_story_bible.md](file:///C:/Users/Gulam%20Mustafa/.gemini/antigravity/brain/aa022bf9-c035-4c2e-ba44-f330bde2cb13/grand_master_story_bible.md).
4. Click **Save / Create Gem**.

### Step 3: Generating Content & Direct Images
Open your new **IRONBLOOD Manga Director Gem** and prompt it:
* **For Script / Panel Breakdowns:**  
  > *"Generate the full panel breakdown and prompt pack for Scene 1 (Pages 1 & 2)."*
* **For Direct Image Rendering (Native Imagen 3):**  
  > *"Render the image for Page 1 Panel 3: Kael stepping into the rain with his glowing green cleaver."*

### Step 4: Exporting Your Output
* **Text / Scripts:** Click the **"Share & Export"** icon at the bottom of the message ➔ **"Export to Google Docs"** or **"Draft in Gmail"**.
* **Generated Images:** Click directly on any generated image ➔ click the **Download (arrow down)** icon to save the high-res `.png` to your computer's `Downloads` folder.

---

# 🧠 GUIDE 2: GOOGLE AI STUDIO (`aistudio.google.com`)
*Best for: 2,000,000 token context, zero memory drift, bulk multi-page script & prompt generation.*

```
[ Step 1: Select Model ] ──► [ Step 2: System Instructions ] ──► [ Step 3: Bulk Prompting ] ──► [ Step 4: Export Code/JSON ]
```

### Step 1: Open AI Studio & Select Model
1. Go to [aistudio.google.com](https://aistudio.google.com).
2. Click on **"Create New Prompt"** (Chat Prompt).
3. On the right-hand panel under **Model**, select **`Gemini 1.5 Pro`** or **`Gemini 2.0 Flash / Pro`**.
4. Set **Temperature** to `0.7` (perfect balance of creativity and lore adherence).

### Step 2: Paste Universe into System Instructions
1. Look at the left sidebar (or top box) labeled **"System Instructions"** (with a pencil icon).
2. Open [google_flow_manga_agent_instructions.md](file:///C:/Users/Gulam%20Mustafa/.gemini/antigravity/brain/aa022bf9-c035-4c2e-ba44-f330bde2cb13/google_flow_manga_agent_instructions.md) and [grand_master_story_bible.md](file:///C:/Users/Gulam%20Mustafa/.gemini/antigravity/brain/aa022bf9-c035-4c2e-ba44-f330bde2cb13/grand_master_story_bible.md).
3. Paste both documents directly into the **System Instructions** box.
   *(Gemini's 2M token capacity handles this effortlessly without lagging).*

### Step 3: Run Bulk Multi-Page Generation
In the bottom prompt box, type:
> *"Using the master instructions, generate the complete panel-by-panel breakdown and image generation prompts for ALL 10 PAGES of the One-Shot Manga in one single output, including Kael's 4th-wall breaking dialogues."*

Gemini will stream the entire 10-page production breakdown continuously.

### Step 4: Exporting in Bulk
1. In the top right corner, click **"Get Code"** or **"Export"**.
2. You can download the entire session as:
   * **Markdown (.md) / Text**
   * **JSON payload** (for automated pipelines)
   * Or simply click the **Copy Markdown** icon on the response.

---

# ⚙️ GUIDE 3: GOOGLE FLOW / CLOUD GENAI PIPELINES
*Best for: Automated node-based pipelines, sequential character tracking ("Frames & Ingredients"), and batch Cloud Storage exports.*

```
[ Step 1: Create Flow ] ──► [ Step 2: Set Character Ingredients ] ──► [ Step 3: Wire Nodes ] ──► [ Step 4: GCS / Drive Export ]
```

### Step 1: Create a New Flow / Canvas Pipeline
1. Open your **Google Flow / Vertex AI GenAI Studio Canvas**.
2. Click **"New Flow / New Workflow"**.
3. Name your project: **`IRONBLOOD_Manga_Pipeline`**.

### Step 2: Configure Character Ingredients (Visual Anchors)
Google Flow uses **"Ingredients / Character Entities"** to lock faces and costumes across shots:
1. In the left panel, click **"Add Ingredient / Entity"**.
2. Create your core character entities using the descriptions from [full_character_prompts_pack.md](file:///C:/Users/Gulam%20Mustafa/.gemini/antigravity/brain/aa022bf9-c035-4c2e-ba44-f330bde2cb13/full_character_prompts_pack.md):
   * **Entity 1:** `KAEL` (Attach concept art image or paste the exact anchor string).
   * **Entity 2:** `KPOP_NINJA` (Toji fit, spiky silver hair, glowing sapphire eyes).
   * **Entity 3:** `SURAIYA` (Magenta/pink hair, brass corset, crimson sari).
   * **Entity 4:** `GOVERNOR_MUJIB` (Sheikh Mujibur Rahman likeness, black coat, horn-rimmed glasses).

### Step 3: Wire the Nodes (Text ➔ Image Generation)
1. **Node A (Prompt / Text Node):**
   * Select **Gemini 1.5 Pro / 2.0**.
   * Paste [google_flow_manga_agent_instructions.md](file:///C:/Users/Gulam%20Mustafa/.gemini/antigravity/brain/aa022bf9-c035-4c2e-ba44-f330bde2cb13/google_flow_manga_agent_instructions.md) into the Node's System Instructions.
2. **Node B (Image Generation Node):**
   * Select **Imagen 3 (Multimodal Image Gen)**.
   * Set Style Preset: `Pixel Art / Retro Arcade 16-Bit`.
   * Set Default Aspect Ratio: `16:9` (or `2:3` for portraits).
3. **Connect Node A to Node B:**
   * Wire the `IMAGE GENERATION PROMPT` output from Node A into the input port of Node B.

### Step 4: Configure Batch Export to Google Drive / Cloud Storage
1. In the **Output Settings** of Node B (Image Node):
2. Toggle **"Auto-Export to Storage"** ON.
3. Select your destination:
   * **Option A:** Connected **Google Drive Folder** (e.g. `My Drive/IRONBLOOD_Manga_Pages/`).
   * **Option B:** **Google Cloud Storage (GCS) Bucket** (`gs://ironblood-manga-output/`).
4. Click **"Run Full Flow / Batch Execute"**.
5. The pipeline will generate every panel in sequence and automatically deposit high-resolution `.png` files named `Page_01_Panel_01.png`, `Page_01_Panel_02.png`, etc., straight into your Drive folder!

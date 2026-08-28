# AI Manga Collaboration Manual
### A working instruction set for an AI agent (ChatGPT, Claude, etc.) to act as your manga production partner

Paste the "AGENT INSTRUCTIONS" section into a custom GPT / Claude Project / system prompt so the AI behaves consistently across your whole project. Use the templates below it as fill-in-the-blank tools during actual production.

---

## PART 1 — AGENT INSTRUCTIONS
*(Copy this block into your AI's custom instructions / system prompt / project knowledge)*

```
You are my Manga Production Partner. Your job is to help me plan, script, and
prompt-engineer a manga project while enforcing consistency across characters,
style, and pacing. You are NOT generating the final images yourself — you are
producing the text assets (scripts, prompts, notes) that feed into an image
generator.

ROLE RULES:
1. Always check the CHARACTER BIBLE and STYLE LOCK (provided below / in project
   files) before writing any panel prompt. Never invent new physical traits,
   outfit details, or style descriptors that contradict what's locked in.
2. When I give you a scene or plot beat, break it into a PANEL SCRIPT using the
   Panel Script Template before anything else. Do not jump straight to image
   prompts without the script step.
3. For every panel, output prompts using the PANEL PROMPT TEMPLATE structure,
   in this fixed field order: Subject/Character, Pose/Action, Expression,
   Camera/Shot type, Composition/Framing, Background, Lighting, Style Lock,
   Line/Screentone notes, Negative prompt (if applicable).
4. Flag inconsistencies proactively. If a scene implies a costume change,
   injury, or new hairstyle etc, ask me before assuming, and note it so it
   carries forward into later panels.
5. Track continuity. Keep a running log (in your responses) of: character
   states (outfit/injuries/mood), locations established, and any visual motifs
   introduced, so later panels stay consistent without me re-explaining.
6. Default to manga pacing conventions unless told otherwise: vary panel size
   for emphasis, use silent/reaction panels for beats, avoid over-explaining
   in captions, prefer showing over telling.
7. When something is ambiguous (camera angle, character emotion, layout),
   propose 2-3 concrete options rather than a vague description — I need
   something I can literally type into an image generator.
8. Keep a "Style Lock" phrase and repeat it verbatim in every prompt unless I
   explicitly change it.
9. If I ask for a full page, output panel-by-panel prompts AND a suggested
   page layout (panel count, rough size/shape per panel, reading order).
10. Never soften or summarize — I need literal, copy-pasteable prompt text,
    not paraphrased descriptions.
```

---

## PART 2 — CHARACTER BIBLE TEMPLATE
*(Fill one out per main character; keep it in your project files and reference it every session)*

```
CHARACTER NAME:
ROLE IN STORY:

PHYSICAL BASE
- Age/apparent age:
- Height/build:
- Face shape / notable features:
- Eye color/shape:
- Hair (color, length, style, texture):
- Skin tone:
- Distinguishing marks (scars, tattoos, freckles):

DEFAULT OUTFIT
- Main outfit description:
- Alt outfits (if any), and when they're used:
- Accessories always present:

EXPRESSION RANGE / PERSONALITY TELLS
- Default resting expression:
- How they show anger / sadness / joy / fear (specific physical tells):
- Posture/body language habits:

STYLE NOTES SPECIFIC TO THIS CHARACTER
- Any exceptions to the global style lock:

REFERENCE IMAGES
- [Link/filename to turnaround sheet or reference set]
```

---

## PART 3 — STYLE LOCK TEMPLATE

```
GLOBAL STYLE LOCK (paste into every panel prompt):
"[art style — e.g. shonen manga style, screentone shading, dynamic linework],
[line weight description], [monochrome/color], [rendering quality tags],
[era/influence reference if used]"

Example:
"black and white shonen manga style, sharp confident inking, dynamic screentone
shading, high contrast, detailed backgrounds, dramatic panel energy"
```

Keep this identical across the entire chapter/volume. If you must evolve the style mid-project, version it (Style Lock v1, v2) and note where the switch happens.

---

## PART 4 — PANEL SCRIPT TEMPLATE
*(Use this before writing any image prompts — this is the storyboarding layer)*

```
SCENE: [scene name/number]
LOCATION: 
TIME OF DAY:
MOOD/TONE:

PANEL 1
- Shot type: [wide / medium / close-up / extreme close-up / establishing]
- Characters present:
- Action:
- Dialogue/SFX:
- Panel size note: [full-width / small inset / large dramatic panel]

PANEL 2
...
```

---

## PART 5 — PANEL PROMPT TEMPLATE
*(One of these per panel, generated from the Panel Script above)*

```
SUBJECT/CHARACTER: [name, pulled from Character Bible]
POSE/ACTION: 
EXPRESSION: 
CAMERA/SHOT TYPE: [close-up / low angle / bird's eye / over-the-shoulder / etc.]
COMPOSITION/FRAMING: [rule of thirds, centered, diagonal action line, etc.]
BACKGROUND: [detailed / blurred / speed lines / blank with focus lines]
LIGHTING: [direction, mood, hard/soft]
STYLE LOCK: [paste verbatim from Part 3]
LINE/SCREENTONE NOTES: [heavy inking on impact panels, light tone for calm scenes, etc.]
NEGATIVE PROMPT: [extra limbs, inconsistent eye color, off-model outfit, text artifacts, etc.]
```

---

## PART 6 — PRODUCTION WORKFLOW CHECKLIST

**Pre-Production**
- [ ] Finalize plot/script beats
- [ ] Build Character Bible for every named character
- [ ] Lock Style Lock phrase
- [ ] Generate turnaround/reference sheets per character

**Per Chapter**
- [ ] Write full Panel Script (Part 4) for the chapter
- [ ] Convert to Panel Prompts (Part 5), batched by character/location for efficiency
- [ ] Generate panels, logging seed/reference/prompt version used for each keeper
- [ ] Flag and resolve continuity issues before moving to next chapter

**Post-Production**
- [ ] Assemble panels into pages (panel borders, gutters, bleed)
- [ ] Add speech bubbles/SFX lettering
- [ ] Consistency pass: check color/tone/linework matches across the chapter
- [ ] Final export

---

## PART 7 — CONTINUITY LOG TEMPLATE
*(Ask your AI agent to maintain this across a session so nothing drifts)*

```
CHARACTER STATE LOG
Character | Current outfit | Injuries/marks | Emotional arc position | Last seen (panel/page)

LOCATIONS ESTABLISHED
Location | Key visual features | First appearance

MOTIFS / RECURRING VISUAL ELEMENTS
Motif | Meaning/purpose | Panels used in
```

---

**How to use this manual day-to-day:** paste Part 1 as your agent's standing instructions, keep Parts 2, 3, and 7 updated as living documents for your project, and use Parts 4–6 as your per-scene working loop.

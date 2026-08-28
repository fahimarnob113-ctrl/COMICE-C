# Walkthrough: Engine Architecture Step 1 (Controls & Flags)

I have successfully updated the core input and game state engine without breaking any of the existing code structure. The game now supports adaptive flags for the story, and the groundwork for a customizable controls menu is fully functional.

## Changes Made

### 1. `config.js`
- **Narrative Flags:** Added the `initialFlags` object to track the four key story metrics (`BORKOT_LOYALTY`, `CIPHER_CONFIDENCE`, `DOCS_FOUND`, `SIPHON_EXPOSURE`).
- **Control Bindings:** Added a `controls` object that defines the default keybindings for the game (e.g. `jump: 'ArrowUp'`, `attack: 'KeyX'`).

### 2. `game.js`
- **Global GameState:** Initialized `GameState.flags` at boot using the values from `config.js`. This is where we will increment loyalty and doc counts during the missions.
- **Input Action System:** Stripped out the hardcoded `e.code` checks. The input manager now reads the bindings from `config.js`.
- **Local Storage:** Added `localStorage.getItem('ironblood_controls')` logic. If a player remaps their keys (which we'll add a UI for later), it saves to their browser so they don't have to remap them every time they play.
- **Call Sites Updated:** Updated every script in the engine (the Player logic, the Dialogue box, the Pause menu, the Title screen) to use the new action-based checks like `justPressed('confirm')` instead of `justPressed('Enter')`.

## Validation

- **Manual Testing Required:** I've wired up the new system. Open `index.html` in your browser to verify that Kael still moves left/right, jumps (Up arrow), attacks (X), uses rage (Left Shift), and that you can still clear the dialogue boxes with Enter.

## Next Steps
Whenever you're ready, we can move on to **Step 2: The Document Collectible System**.

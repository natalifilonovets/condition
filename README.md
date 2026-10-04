# First Conditional — Block Builder

Open `index.html` in a modern browser. No build step or backend is needed.

- Click START GAME, read the instructions, then click LET'S BUILD!
- Drag words into the crafting line, or tap/click to place them.
- Drag placed blocks to change their order; tap/click to return them.
- Keyboard: Tab to a block, Enter to place/return. Left/right arrows reorder placed blocks.
- CHECK validates the sentence. Mistakes allow unlimited retries.
- RESET clears the current line. UNDO reverses the last move.
- HINT explains the rule without giving the answer.
- Each correct sentence adds a stage to the Hamster. Finish all ten and PLAY AGAIN.
- Sound is optional and initially off.

Edit the sentences in `data.js`. The `blocks` array specifies the answer order; the game shuffles those blocks at the start of each task. `comma` gives the number of words/groups before the comma in the success message. Repeated words are separate blocks and accepted interchangeably.

The application works offline; Google Fonts enhance the typography when internet access is available, with built-in font fallbacks otherwise.

Validation: JavaScriptCore checks exercised the introductory screens, incomplete and incorrect answers, click placement, undo/reset, all ten correct answers, progress, completion/replay, and pointer drag placement/return using a simulated DOM. Visual and real-device browser checks are still needed.

The entire game fits a scaled canvas (1440×850 landscape, 480×890 portrait). Resize switches the layout and keeps all controls visible without page scrolling. The hamster is a voxel volume rendered as depth-sorted SVG surface faces in ten construction stages. All block textures are local SVG assets.

Construction order: body base (including the golden head/back shell), left foot, right foot, belly, left side, right side, ears, face, eyes/nose, final details. Blueprint sections have thick glowing cyan contours; the next section is highlighted. Material palettes are normalized to reduce brightness differences. The pixel divider after the fourth position is decorative and does not add a slot. The Creeper exercise contains exactly eight blocks and eight positions.

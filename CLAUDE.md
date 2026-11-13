# Timeholes

Single-file HTML5 canvas game (`index.html`); no build, no dependencies besides Google Fonts.

- Glass UI style (backdrop-filter panels), space background, dark-only theme.
- Player = blue glass ball, collectible lights = orange, echoes = black holes with WebGL gravitational lensing (fallback without WebGL: no distortion).
- Echo mechanic (keep as is): each echo replays only its own segment of the path (from the previous light to the one collected), loops it, with a collapse animation at the end and a birth animation at the start. Echoes also replay standing still.
- Logo: "Timeholes" drawn on canvas with the "o" as a lensing black hole.
- UI text is English.

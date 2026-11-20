# Timeholes

Single-file HTML5 canvas game (`timeholes.html`); no build, no dependencies besides Google Fonts.

- Full-bleed playfield (no page frames). The game world has a fixed area (WORLD_AREA) on every device, so a big monitor gives no extra room; its aspect follows the screen and it is scaled by Z to fill it. Game logic runs in world units (W, H); the sky is painted in screen pixels. Space background with a clock face (60 ticks + second hand showing run time) baked into the lensed layer, dark-only theme. Thin viewfinder corner brackets.
- Menus (main, pause, game over) are round glass "lenses" centered on the dial, with a watch bezel (CSS conic ticks); main-menu controls (difficulty, best, how to play) sit in a dock at the bottom. On short screens (max-height 600px) the lens becomes a rounded card. How to play is a modal sheet.
- Fonts: Unbounded (logo, headings, primary buttons), Sora (body), JetBrains Mono (readouts). Accent = orange/ember (lights), blue = player; no pink.
- HUD = floating instrument strip at the top: logo, chronometer readout (TIME / LIGHTS / ECHOES), round pause button; hidden on the main menu. Echoes show a thin arc = remaining part of their loop.
- Player = blue glass ball, collectible lights = orange, echoes = black holes with WebGL gravitational lensing (fallback without WebGL: no distortion).
- Lights burn out (Calm 11 s / Normal 8 s / Stormy 6 s, longer if far away); the 12 bezel ticks around a light are the countdown. A burned-out light scores nothing but still turns the current path into an echo, so standing still is never safe.
- Echo mechanic (keep as is): each echo replays only its own segment of the path (from the previous light to the one collected), loops it, with a collapse animation at the end and a birth animation at the start. Echoes also replay standing still.
- Logo: "Timeholes" drawn on canvas with the "o" as a lensing black hole.
- UI text is English.

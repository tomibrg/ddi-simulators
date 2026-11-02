# ORBIT · Flight timeline prototype

Interactive version of the "The flight" section of the Earth Orbit experience page
(Figma: Grupo-4 → Wireframes Alta → `ORBIT · Experience / Earth Orbit · High` → Section / Flight timeline).

Single self-contained file. No build step, no dependencies (Inter loads from Google Fonts; falls back to system sans offline).

## Run it

Open `index.html` in a browser (double click, or `open index.html`). Works from `file://`.

## What it does

- Drag the line (or click a stop, or use ← → / Home / End) to move through the 10-minute flight. `Play flight` runs it in ~25 s.
- Readout changes live: stop name, "You feel" sentence, G-force, altitude, speed, and what *you* would weigh (± stepper for your weight).
- The window scene follows the flight: sky from dawn to black, stars, the curve of the Earth with its thin blue line, engine glow and shake under thrust, reentry glow, sway under parachutes.
- In the weightless band the cabin objects (a mug, a pen, a phone, an apple, sunglasses) float. Grab and throw them. Weight comes back and they fall to the floor.
- `Sound` (off by default): engine roar, silence at weightlessness, reentry rush, parachute air. Synthesized with WebAudio, no files.

## Demo flow

1. In Figma, show the static section (same layout, frozen at T+4:00).
2. Switch to this page. It opens at the same moment (T+4:00), so the change is seamless.
3. Drag the line back to T+0:00, press `Play flight`, then grab an object in the weightless band.

Deep links: `index.html#t=1.5` opens at T+1:30. Add `&touched` to hide the "drag" hint. `#t=4&shot` renders only the scene (used to export the still used in Figma).

## Data

All figures (G-force, altitude, speed, timing) are illustrative and shaped after the Figma chart. They are marked as such on screen. Replace the arrays at the top of the script (`CURVE_Y`, `gForce`, `speedKmh`, `STOPS`) for real operator data.

## Tokens

CSS variables at the top mirror `ORBIT / Foundations` (`--orbit-color-*`, `--orbit-radius-2`). Type sizes follow the Figma text styles, including the new `Title/Large` (22 Bold).

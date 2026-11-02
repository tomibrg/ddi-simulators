# ORBIT · Moon flight prototype

Interactive version of the "The flight" block of the Moon flyby experience page
(Figma: Grupo-4 → Wireframes Alta → `ORBIT · Experience / Moon Flyby · High` → Section / Flight timeline).
Six days, around the Moon and back, no landing. Same shell as `prototypes/orbit-flight`, different signature moments.

Single self-contained file, no build step (about 7 MB because the Earth and Moon textures are embedded as base64). Open `index.html` in a browser (works from `file://`). Inter loads from Google Fonts.

## What it does

- Drag the line (or click a stop, or use ← → / Home / End). `Play flight` runs it in about 40 s and slows down around the far side.
- **Earth at thumb size.** The window shows Earth at its true angular size for the distance. A dashed 2° bracket (a thumb at arm's length) appears as Earth shrinks, and when Earth is smaller than it, the screen says so.
- **Radio silence.** While the Moon is between you and Earth the screen goes dark: `NO SIGNAL`, Earth hidden behind the limb, signal delay replaced. Earth comes back over the Moon (Earthrise).
- **Message with delay.** `Send a message` sends a pulse to Earth in real time (about 1.3 s each way at the Moon, so 2.6 s round trip). Near Earth it is almost instant. During the far side it fails with a message.
- Readout: mission elapsed time, stop, "You feel", distance from Earth, how wide Earth looks, signal delay.

## Demo flow

1. In Figma, show the static section (same layout, frozen at T+77 H, Earthrise).
2. Switch to this page. It opens at the same moment.
3. Press `Play flight` or drag back to T+36 H to see Earth shrink, then into the far side for the silence, then send a message.

Deep links: `index.html#t=3.2` opens at day 3.2 (T+77 H); add `&touched` to hide the drag hint. `#t=3.2&shot` renders only the scene (used to export the still in `assets/moon-flight/`).

## Data

Illustrative and shaped by a simple free-return model (distance from Earth follows one smooth curve; farthest point just beyond the Moon at ~386,000 km; far-side pass about 200 km above the surface). Real physics: Earth ≈ 12,742 km across, light travels ≈ 300,000 km/s, the Moon is ≈ 384,400 km away. Everything else (timing, blackout length, crew, trajectory) is an example and marked as such on screen. Edit the constants at the top of the script (`DAYS`, `BLACKOUT`, `dist`, `STOPS`).

## Version with the cabin window (edited by a teammate)

- Real-looking Earth and Moon textures instead of flat gradients, twinkling stars, a cabin-window frame with HUD labels (`CABIN VIEW · PORT 02`, `0G · SECURE`, current phase).
- The three readings are collapsed under `Flight data`; the panel shows the stop, "You feel" and the message button.
- Stop names under the time labels on the chart; the send button is disabled while there is no signal.
- Figma still: `assets/moon-flight/scene-t320-v2.png` (816 x 460 at 2x). In `#shot` mode the HUD labels are hidden on purpose, because the Figma page draws them as editable text.

## Exporting the still from the command line

Headless Chrome hangs with `--virtual-time-budget` on this page (the big textures). Use a real-time wait instead:

```
chrome --headless=new --hide-scrollbars --force-device-scale-factor=2 --window-size=816,460 --timeout=5000 --screenshot=out.png "file:///.../index.html#t=3.2&shot"
```

# ORBITA · Space station flight prototype

Interactive version of the "On board" block of the Space Station experience page
(Figma: Grupo-4 → Wireframes Alta → `ORBITA · Experience / Space Station · High` → Section / Flight timeline).
One representative day on the station: **sixteen sunrises, and where you are over the Earth**.

Open `index.html` in a browser (works from `file://`). It is a generated single file (the Cupola photo is embedded as base64).

## What it does

- **A day on board.** Drag the line (or click a moment, or use ← → / Home / End) through 24 hours. `Play a day` runs it in about 36 s. Six moments: Wake up, Exercise, Science, Window time, Dinner, Sleep.
- **Sixteen sunrises.** The station circles the Earth every ~93 minutes, so the Cupola view goes sunrise → day → sunset → night with city lights, sixteen times. The chart is the daylight wave of that day, with one tick per sunrise.
- **Where you are.** A small map shows the ground track (about 200 minutes of orbit around you) and the label `OVER · <region>` follows the station. Pinned so that at 14:40 it is over South America. Land is a very simplified outline, on purpose.
- **Take a photo.** Flash and a saved caption with the region and the time.
- Readout (collapsed under `Flight data`): altitude 408 km, orbit speed 27,600 km/h, minutes to the next sunrise or sunset.

## Demo flow

1. In Figma, show the static section (frozen at 14:40, a sunrise).
2. Open this page. It starts at the same moment.
3. Drag back to 07:00, press `Play a day`, watch the sunrises and the dot crossing the map, take a photo over somewhere you recognise.

Deep links: `index.html#t=420` opens at minute 420 (07:00); add `&touched` to hide the drag hint. `#t=880&shot` renders only the scene (used to export the still in `assets/iss-flight/`).

## Orbit video

`assets/iss/cupola-orbit.mp4` is 11 s cut from NASA Johnson's "Earth Illuminated: ISS Time-lapse Photography" (public domain, [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Earth_Illuminated-_ISS_Time-lapse_Photography.webm), 2:19–2:31): lit Earth → dusk → night → sunrise. The last second crossfades into the first, so it loops without a cut. Credited on screen as "Time-lapse: NASA"; it must not suggest NASA endorsement.


If the video is present, the scene shows it instead of the photo with light overlays. The clip should be **one orbit** (day → sunset → night → sunrise) and is treated as a loop:

- Idle: the video plays on repeat by itself and drives the clock, so the line on the chart moves with it.
- Dragging the line, clicking a moment or `Play a day`: the video pauses and follows the slider (each ~93 min of the day = one pass through the clip).
- `VIDEO_SUNRISE` in `template.html` is the fraction of the clip where the sunrise happens (0 = start), to line it up with the daylight chart.

Encode it with a keyframe on every frame so scrubbing is smooth (`ffmpeg -i in.mp4 -vf scale=1280:-2 -g 1 -an -pix_fmt yuv420p assets/iss/cupola-orbit.mp4`). Seeking needs `file://` or a server with Range requests (Netlify works; `python -m http.server` does not).

## Regenerating `index.html`

`template.html` is the source. It has the placeholder `__PHOTO__` where the image goes:

```
python3 - <<'PY'
import base64
b = base64.b64encode(open('../../assets/iss/cupola-view.jpg','rb').read()).decode()
open('index.html','w').write(open('template.html').read().replace('__PHOTO__','data:image/jpeg;base64,'+b))
PY
```

Export the still with headless Chrome using a real-time wait (not `--virtual-time-budget`):

```
chrome --headless=new --hide-scrollbars --force-device-scale-factor=2 --window-size=816,460 --timeout=4000 --screenshot=out.png "file:///.../index.html#t=880&shot"
```

## Data and credits

Illustrative. Real: orbit about 400 km up, one orbit every ~92 minutes, about 16 sunrises a day, inclination 51.6°. Everything else (schedule, region labels, map outline, light timing) is an example and marked as such on screen. The Cupola photo is an AI-generated image from the team (`assets/iss/cupola-view.png`).

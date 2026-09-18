# Night Shift — lofi rooftop workstation

A single-file, dependency-free animated night scene: **the view from behind an empty chair**, looking past a desk and out through a full-width glass wall of a high-rise room. Nothing living in it. Rain on the glass, a city below, and a lofi loop generated live in the browser — no audio files, no build step, no libraries.

Open `index.html` in a browser and click **Enter the room**. Everything (canvas rendering + Web Audio synthesis) runs locally.

---

## The view

### In the room
- **Twin screens** — left pane scrolls syntax-highlighted code; right pane shows a sprint board with cards and a burndown line.
- **Laptop** — streaming terminal output.
- **Mechanical keyboard**, mouse, notepads with pens, a pen cup.
- **A mug** with four strands of steam that bend and drift with the airflow.
- **A table fan** turning behind the desk — blades spinning under the guard cage, head slowly oscillating.
- **Left wall** — planning boards with sticky notes and red string, a small made bed below them.
- **Right side** — a shelf of book spines, and three garments hanging on a rail that swing on gusts coming through the open pane.

### Outside
- A **moon** with a cloud veil drifting across it, and **220 twinkling stars**.
- Two depth-layers of **mid-age concrete towers** with a scattering of lit windows — most dark, a few flickering or switching.
- The **downtown road** far below: lamp posts casting cones into the drizzle, wet trees, shuttered shopfronts and tea stalls glowing warm — all smearing into reflections on the wet asphalt.
- **Light rain** slanting past the glass; droplets cling to the pane, then break loose and run down.

---

## The sound

Generated live with the **Web Audio API** — nothing is a file.

- **72 BPM**, key of **A minor**, progression **i – iv – VI – VII**.
- Soft **electric-piano** voice with a **pad** underneath.
- **Sparse melody**, brushed drums sitting **behind the beat**.
- **Tape wow** and **vinyl crackle**.
- **Three-layer rain bed** that swells and eases. No thunder.

Music and rain toggle independently, so you can run **rain-only** when the music pulls focus during deep work.

---

## Controls

| Control | What it does |
| --- | --- |
| **Enter the room** | Starts audio and fades away the intro curtain (audio needs a user gesture). |
| **Music** | Toggles keys, pad, bass, melody and tape/vinyl texture. |
| **Drums** | Toggles the brushed kit. |
| **Rain** | Toggles the rain bed. |
| **Volume** | Master level. |

The control deck fades out after ~4 seconds of inactivity and returns on any mouse move, touch, or keypress.

---

## Running it

No install, no tooling:

```sh
open index.html
```

Or serve it if you prefer a real origin:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

Works well in Chrome, Safari, and Firefox. Desktop recommended — the scene is tuned for a wide viewport.

---

## Notes

- Audio is only created **after** the first click, per browser autoplay policy.
- Rendering is a single `<canvas>` driven by `requestAnimationFrame`; the scene is procedural, so there are no assets to load.
- Everything lives in `index.html` — styles, scene, and synth.

## License

MIT

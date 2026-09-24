# 🐶 Puppy Adventures

A 3D island game **designed by the Beach Crew** (voice memo, 2026-09-24) and built by Claude Code as its own
fresh design: Three.js world, sticker-book UI, thumb joystick, synth sounds. No shared game kit, no build step.

**Play:** https://coryw.github.io/puppy-adventures/  (phones and laptops; landscape is best)

| Keyboard | Phone |
|---|---|
| Arrows / WASD run | left thumb: joystick appears where you touch |
| Space jump | JUMP |
| X bark | BARK |

Eat every 🍕 (8 = one lunch). Serve 3 lunches and **Poppy** 💕 appears at the doghouse; reach her to win.
Birds swoop; BARK scares them, jumping into one from below BOOPs it. 🍦 heals. Lose all hearts and a
friendly birdie carries Puppy home for a nap (never "dead", never blood).

## Files
- `index.html` · `style.css` · `game.js` — the whole game (ES module; needs to be served over http, not file://)
- `vendor/three/three.module.js` — Three.js r170, vendored (no CDN; beach Wi-Fi is not to be trusted)
- `DESIGN.md` — the kids' words verbatim, what I built from them, open questions for them
- `tests/check.py` — `uv run tests/check.py`: headless Chrome proof (desktop keys + phone touch), writes `docs/screenshots/`
- `docs/voice-memo-2026-09-24.m4a` — the original recording

## In the arcade
Linked into the M2 arcade with `arcade link ~/Programming/beach-games/puppy-adventures` (a symlink `games/puppy-adventures-3d` in
`~/Programming/game-maker`, so this repo stays the source of truth): https://arcade.dev.coryw.net/games/puppy-adventures-3d/ (tailnet).
The arcade's check drives the game through two hooks: `window.render_game_to_text()` (a JSON snapshot with `screen`) and
`window.advanceTime(ms)` (a deterministic fixed-step advance); `?seed=N` makes `Math.random` reproducible.

## Deploy
Static files → the `gh-pages` branch of `github.com/coryw/puppy-adventures` (GitHub Pages). Copy the folder minus
`tests/`, add `.nojekyll`, force-push `gh-pages`, then verify by content (`grep -F 'Puppy Adventures'`), never by status code.

# 🐶 Puppy Adventures — design brief

**Designed by:** the Beach Crew · **Date:** 2026-09-24 · **Status:** playable · **v1**

## The idea, in their words
> "A puppy adventure game. Weapons and rivalry. Puppy love. No blood — yes, that's important. No bad words. Take you away when you die. Birds. It's three-dimensional. Ice cream cones for health. Pizza for lunch."

Voice Memo "S Waccamaw Dr" (2026-09-24 10:41, 69 s, several kids at once), kept at `docs/voice-memo-2026-09-24.m4a`; transcribed with local whisper (medium.en). Title given by Uncle Cory: **Puppy Adventures**.

## What I heard (the interpretation)
- **You are:** Puppy, a golden box-built pup with a red collar, on a sunny 3D island (palms, umbrellas, a red doghouse, flowers, water all round). The camera sits behind you; the joystick moves you where you look.
- **The goal:** eat every 🍕 ("pizza for lunch"). Eight slices = one lunch. Serve **3 lunches** and **Poppy** 💕 (a pink puppy with a bow — the "puppy love") appears at the doghouse; reach her to win. ~60–90 s.
- **The danger:** birds. Seagulls circle high, flash `!`, then **swoop**. Each lunch adds two birds and makes them bolder.
- **Weapons, no blood:** **BARK** — a white shockwave ring that scares every bird within reach back into the sky (+5 for each caught mid-swoop). **Jump into a swooping bird** from below to **BOOP** it for +25. Nobody bleeds, nobody says a bad word.
- **Health:** 3 hearts. 🍦 ice cream appears when you're hurt; eating one heals a heart.
- **"Take you away when you die":** lose all hearts and a big friendly white birdie swoops down, picks Puppy up and flies him home. The card says **NAP TIME 💤**, never "dead".
- **The FUN part:** running full tilt across a 3D island, a BARK scattering a flock, and the mid-air BOOP.

## The design (this game's own, not a shared kit)
- **Look:** "Sticker Book Sunshine" — cream cards with thick ink outlines and hard drop shadows, candy-coloured round buttons, chunky rounded system type, a tilted title card with a "3D!" sticker. Colours: sky `#8fd3ff`, cream `#fff7e6`, ink `#2b1d14`, coral `#ff6b6b`, sunny `#ffd23f`.
- **3D:** Three.js r170 (vendored ES module). Box-built puppy with wagging tail and swinging legs; birds with flapping wings; emoji canvas-textures as sprites for pizza and ice cream; 3D confetti; a fixed-step logic loop with a per-frame render.
- **Controls:** a floating joystick that appears under the left thumb (pointer events, `touch-action: none`), JUMP and BARK buttons under the right thumb; keyboard on laptops. Controls only show on touch devices.
- **Feedback:** every event has a sound (WebAudio synth, no files), a floating word (DOM, projected from 3D), confetti and, for hits, camera shake — kids need instant, multisensory feedback.

## Stretch ideas (v2, if they ask)
- A rival: King Whiskers the cat, who steals pizza slices unless you bark him off ("rivalry").
- A boss gull after lunch 3 with a health bar; cliffs to climb on the far side of the island.
- Pick your puppy colour; 2-player with Poppy on the same keyboard.

## Ask the Beach Crew
- Who was on the recording? The title says "the Beach Crew" until Uncle Cory has the names.
- "Rivalry" — are the birds the rivals, or did you want a rival *dog*?

## Changelog
- v1 (2026-09-24): first playable. Built first on the arcade kit, then rebuilt standalone the same morning when Cory decided every game should be its own fresh design.

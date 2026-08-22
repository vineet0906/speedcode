# Speedcode 2026

NMIT Hacks — Speedcode, 22 August 2026. Department of CSE, Nitte Meenakshi Institute of Technology.

## Running it

Open `index.html`. That's it — no build step, no dependencies, no server. It also runs offline
straight off disk, which is the fallback if venue wifi dies during judging.

Live: https://USERNAME.github.io/speedcode

## Structure

A single self-contained file. Design system in the `<style>` block, behaviour in the `<script>`
at the bottom. Everything between the two `DELETE` markers in the body is demo content and is
meant to be thrown away.

- Design tokens — six values at the top of `:root` re-skin the whole thing
- `.wipe` — pointer-driven reveal transition (drop a `[data-wipe-top]` child inside)
- Cue palette — Cmd/Ctrl + K, add entries to the `ACTIONS` array
- `store` — localStorage wrapper, survives a mid-demo refresh
- `timecode()` — frame-accurate formatting for positional values
- `toast()` — transient confirmations

Reduced-motion, visible focus states, and mobile layout are handled.

## Notes

Type is Archivo (width axis) and DM Mono, loaded from Google Fonts with system fallback
stacks — so a bad connection degrades rather than breaks.

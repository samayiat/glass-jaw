# Glass Jaw

Open `index.html` and it plays. That's it.

## To install it as an app

The install button only lights up when a browser can actually honour it, which
means the folder has to be **served over http**, not opened off the disk. Any
static server will do:

    npx serve .            # or: python3 -m http.server

Then open the address it prints. The **Install** button appears on the menu.

Installed, it gets a **real landscape lock** from the OS (the manifest asks for
it) instead of the CSS rotation trick the browser version falls back to. It also
runs fullscreen and works offline — the service worker caches the shell on first
load, and three.js and the fonts on first sight.

On iOS there's no install prompt; the button tells you to use
**Share → Add to Home Screen**, which gets you the same thing.

## Files

- `index.html` — the whole game. Single file, no build step.
- `manifest.webmanifest` — name, icons, landscape lock, fullscreen.
- `sw.js` — offline cache.
- `icons/` — generated app icons.

## Modes

- **The Gauntlet** — seven men in order, a cutman between each.
- **Survival** — endless, escalating. They don't run out of men.
- **Glass Jaw** — 5x damage both ways. Brandt will end you with one hook.
- **Exhibition** — pick anyone on the card, no stakes.

## Controls

Keyboard: `WASD` footwork · `J K L I` jab/cross/hook/upper · `Q E` slip ·
`Space` block · `F` flurry · `Esc` pause · mouse L/R for jab/cross.

Xbox pad: `LT/RT` slip · `LB/RB` block · `X Y A B` punch · `R3` flurry ·
left stick footwork · `Start` pause.

Touch: thumbstick left, punches right.

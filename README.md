# PAC-MAN — 1980 Arcade Classic

A browser recreation of the classic 1980 Namco arcade game.

## Play

Open `index.html` in any modern browser (Chrome, Edge, Firefox).

Double-click the file, or from a terminal:

```powershell
start index.html
```

## Controls

| Key | Action |
|-----|--------|
| **Arrow keys** or **WASD** | Move |
| **Space** | Start / Pause / Resume |
| **M** | Mute sound |
| **Swipe** (touch/mouse drag) | Move |
| **Click** | Start game |

## Features

- Classic 28×31 maze layout with pellets and power pellets
- Pac-Man with animated mouth and death sequence
- Four ghosts with distinct AI:
  - **Blinky** (red) — chases you directly; speeds up when few dots remain (Cruise Elroy)
  - **Pinky** (pink) — ambushes four tiles ahead
  - **Inky** (cyan) — flanking pattern using Blinky’s position
  - **Clyde** (orange) — chases when far, retreats when close
- Scatter / chase mode cycles
- Frightened mode after power pellets (blue ghosts, chain scoring 200→400→800→1600)
- Side tunnels
- Bonus fruit at 70 and 170 dots
- Score, high score (saved), lives, levels with increasing difficulty
- Retro beeps via Web Audio API
- Arcade-style HUD and Press Start 2P font

## Board size

Internal resolution is driven by `TILE` in `game.js` (default **24** → **672×744**).

```js
const TILE = 24; // 16 → 448×496, 20 → 560×620, 24 → 672×744, 28 → 784×868
```

Canvas size and HUD width update automatically from that value.

## Files

- `index.html` — page shell
- `style.css` — arcade framing and HUD
- `game.js` — full game engine

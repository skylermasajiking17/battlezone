# Battlezone

A wireframe vector tank game in a single HTML file. No libraries, no build step, no server — open it in a browser and it runs.

An homage to Atari's 1980 arcade cabinet *Battlezone*. Written from scratch as a personal project.

**[▶ Play it](https://skyking0-masaji.github.io/battlezone/)**

## Controls

| Key | Action |
| --- | --- |
| `↑` / `W` | Drive forward |
| `↓` / `S` | Reverse |
| `←` `→` / `A` `D` | Turn |
| `Space` | Fire (hold for continuous fire) |
| `P` | Pause |

## How to play

You are a tank on an endless plain, seen down the barrel through a periscope sight. Enemies come at you one at a time. The gun does not elevate — it fires dead level, exactly like the original cabinet.

Watch the radar at the top of the screen. It rotates with you, so **up is wherever your gun is pointed**:

- **Green chevron (center)** — you
- **Red** — tank or super tank
- **Amber** — guided missile
- **Cyan** — the bonus saucer
- **Pink dots** — incoming shells

If a blip sits below the chevron, it's behind you. Turn around.

Enemy fire is the only red thing in the world, so you can always pick it out of the green wireframe. Shells are blocked by scenery — put a cube or a pyramid between you and an enemy and its shot dies against the obstacle. So can yours, so mind your line of fire.

## Scoring

| Target | Points |
| --- | --- |
| Tank | 1,000 |
| Missile | 2,000 |
| Super Tank | 3,000 |
| Saucer | 5,000 |

Bonus tank every 15,000 points. Three lives to start.

The **missile** homes in and kills you by ramming — break line of sight behind a block. The **saucer** is harmless and pure bonus. The **super tank** turns faster and shoots sooner than a regular tank.

Let the title screen sit for a few seconds and it cycles through a rotating wireframe of each enemy, so you know what you're looking at before you meet one.

## Under the hood

Everything is drawn on a single `<canvas>` with hand-rolled 3D:

- Vertex transform into camera space, near-plane line clipping, perspective projection
- Wireframe models defined as vertex + edge lists
- The world wraps at 420 units, so the plain feels endless
- The mountain skyline, volcano, and moon sit at infinity and never get closer — same trick the arcade original used
- WebAudio engine drone that rises with the throttle, plus firing and explosion effects

Roughly 800 lines of vanilla JavaScript in one file.

## Running it

Download `index.html` and double-click it. That's the whole install.

## Notes

*Battlezone* is a trademark of Atari. This is an independent tribute, not affiliated with or endorsed by Atari, and shares no code or assets with the original.# battlezone

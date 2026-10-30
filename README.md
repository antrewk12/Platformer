# Platformer (Unreal Engine 5)

A 3D action platformer prototype built in **Unreal Engine 5.2 entirely with Blueprints**. It focuses on fluid, momentum-based traversal: dashing, carrying dash speed into jumps, and crossing gaps with a rope.

<img width="640" height="360" alt="Dash and momentum jump" src="https://github.com/user-attachments/assets/4ff7ecf8-260f-420d-b54b-6d118a655e14" />
<img width="640" height="360" alt="Platforming gameplay" src="https://github.com/user-attachments/assets/1335759e-a974-4471-aa95-8c90485cda3d" />

> **Playable build:** coming soon.

---

## Controls

| Action | Input |
| :--- | :--- |
| Move | `WASD` |
| Jump | `Space` |
| Dash | `F` |
| Rope | Right mouse button |

---

## Movement mechanics

- **Directional dash:** an instant forward burst that ignores the camera's vertical angle, so the player always accelerates parallel to the ground.
- **Momentum jump:** jumping during a dash cancels horizontal friction and carries the dash speed into the jump, producing a long, arcing leap.
- **Rope:** latch onto grapple platforms with the right mouse button to cross gaps.
- **Anti-spam rules:** the dash has a 2-second cooldown, only one air dash is allowed per jump, and actions are locked against each other to prevent input glitches from rapid key presses.

## Level elements

- **Platforms:** standard, ice and lava blocks, grapple points, and platforms carrying collectible coins.
- **Kill zones** and a **win trigger** at the end of the level.
- **UI:** main menu, HUD, game over and win screens.
- **Feedback:** dash and jump particle effects, plus sound effects for movement, the rope and pickups.

---

## Project structure

All gameplay logic is in Blueprints under `Content/Blueprints`:

| Asset | Purpose |
| :--- | :--- |
| `Player/BP_Mage` | Player character: movement, dash, momentum jump and rope |
| `Player/BPI_PlayerAction` | Blueprint Interface used for player interactions |
| `BP_PlatformerGM` | Game mode |
| `Platform/` | Ice, lava, grapple and coin platforms, and the coin pickup |
| `Enviroment/` | Kill zone and win condition triggers |
| `UI/` | Main menu, HUD, game over and win screen widgets |

Input is set up with **Enhanced Input** (`Content/Inputs`), and the levels are `Lvl_MainMenu` and `Level1` in `Content/Level`.

---

## Running the project

1. Clone the repository and open `Platformer.uproject` with **Unreal Engine 5.2**.
2. Add the free **[KUBIKOS - Cube World](https://www.fab.com/listings/7bbf72cf-03bd-458f-9a74-1ab85bd1f2e5)** pack from Fab to the project. It isn't included in this repository because its license doesn't allow redistributing the raw files. Without it, the level's environment meshes will be missing.
3. Open `Content/Level/Lvl_MainMenu` and press Play.

---

## Credits

- **Environment:** [KUBIKOS - Cube World](https://www.fab.com/listings/7bbf72cf-03bd-458f-9a74-1ab85bd1f2e5) by ANIMMAL, from Fab.
- **Mage character and animations:** [KayKit](https://kaylousberg.com/) by Kay Lousberg (CC0).
- **Music and sound effects:** [Pixabay](https://pixabay.com/), used under the Pixabay Content License.

Gameplay, Blueprints and level design by **Andrewk12** ([GitHub](https://github.com/antrewk12) · [itch.io](https://antreask12.itch.io)).
My Blueprints and level design are free to use for educational purposes. Third-party assets keep their own licenses.

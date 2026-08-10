# Custom Movement Framework (Unreal Engine 5)

A slow-pace, high-momentum character movement system built natively in Unreal Engine 5 using Enhanced Input and Blueprints. This framework focuses on fluid traversal mechanics, mutual state exclusion, and dynamic velocity transfers inspired by modern action platformer.

<img width="640" height="360" alt="ezgif com-resize" src="https://github.com/user-attachments/assets/4ff7ecf8-260f-420d-b54b-6d118a655e14" />
<img width="640" height="360" alt="3-ezgif com-resize" src="https://github.com/user-attachments/assets/1335759e-a974-4471-aa95-8c90485cda3d" />


##  Core Features

*   **Directional Horizontal Dash:** An instantaneous forward burst that locks vertical camera influence ($Z$-axis override) to ensure parallel-to-ground acceleration.
*   **Momentum Jump Transfer (Arch Movement):** Pressing `Jump` during an active dash cancels the horizontal friction instantly, capturing the high velocity and converting it into a smooth, physics-driven jump.
*   **State Mutual Exclusion & Anti-Spam:** Comprehensive soft-locks preventing input glitching ("pianoing"). Features a 2-second Dash cooldown and limits the player to exactly one Air-Dash per jump cycle.


##  Installation & Setup

1. Clone this repository into your Unreal Engine project's `Content` directory.
2. Ensure **Enhanced Input** plugin is active in your project settings.
3. Map the Input Actions:
   * `IA_Jump` -> Spacebar
   * `IA_Dash` -> F Key
4. Assign the Custom Character Blueprint as your default Pawn in your GameMode.


This project is open-source and free to use for educational game development purposes.

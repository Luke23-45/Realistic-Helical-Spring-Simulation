## Interactive Helical Spring Simulation

This project is a C++ based interactive spring simulation using SDL2 library for graphics rendering. It visually simulates a spring with dynamic color and thickness changes based on its deformation, and allows users to interactively drag the spring to observe its behavior.

## Getting Started

### Prerequisites
Ensure you have the following installed:
- C++ Compiler (e.g., g++)
- [SDL2](https://www.libsdl.org/)
- [SDL2_ttf](https://www.libsdl.org/projects/SDL_ttf/)

## Project Structure

*   `Spring.cc`: Main C++ source file containing the simulation logic and SDL2 rendering.
*   `Makefile`: Build configuration file for compiling the project.
*   `src/`
    *   `include/`


### Installation
1. Clone the repository:
    ```bash
    git clone git@github.com:Luke23-45/Realistic-Helical-Spring-Simulation.git
    ```
## Building

This project uses `make` for building. To build the project, run the following commands in your terminal:

1. Navigate to the project directory:
    ```bash
    cd Realistic-Helical-Spring-Simulation
    ```
3. Compile the code using make:
    ```bash
     make
    ```
4. Run the executable (Linux/macOS):
    ```bash
    ./main
    ```
5. Run the executable (Windows):
    ```bash
    main.exe
    ```
6. To clean up the build artifacts (object files and executable):
    ```bash
     make clean
    ```

## Features
- **Interactive Spring Simulation:**  Simulates the physics of a spring using advanced spring physics equations.
- **Real-time Deformation:**  Visually deforms the spring in real-time based on the applied forces and user interaction.
- **Dynamic Color Response:** Changes spring color dynamically:
    - **Red:**  Indicates the spring is stretched.
    - **Blue:** Indicates the spring is compressed.
    - **Soft Blue-Gray:** Represents the neutral state of the spring.
- **Variable Wire Thickness:**  Alters the thickness of the spring wire to enhance visual feedback of tension and compression.
- **Smooth Gradient Rendering:**  Renders the spring with smooth color gradients and anti-aliasing for a visually appealing output.
- **Interactive Dragging:** Allows users to click and drag the mass attached to the spring to interact with the simulation.
- **Length Constraints:** Implements minimum and maximum length constraints for realistic spring behavior.
- **Soft Glow Effect:** Adds a subtle glow effect to the spring for better visual depth.

## Key Controls

| Action            | Key/Control         |
| ----------------- | ------------------- |
| Drag Spring       | Mouse Left Button   |
| Exit simulation | Close the window    |

## Code Structure
- `Spring.cc`: Contains all the source code for the spring simulation.
- `AdvancedSpringPhysics` Class:
    -  Handles the numerical simulation of the spring's physics, including properties like stiffness, damping, mass, and length constraints.
    -  Updates the spring's state (position, velocity) based on forces and user interaction.
    -  Provides methods for dragging and releasing the spring (`dragTo`, `release`).
- `SpringRenderer` Class:
    -  Responsible for rendering the spring and related visual elements using SDL2.
    -  Calculates spring parameters and deformation to dynamically adjust color and thickness.
    -  Implements smooth gradient rendering and anti-aliasing for the spring.
    -  Renders the anchor point and the mass attached to the spring.
- `SpringSimulation` Class:
    -  Manages the overall simulation lifecycle, including SDL initialization, event handling, and the main simulation loop.
    -  Creates and manages instances of `AdvancedSpringPhysics` and `SpringRenderer`.
    -  Handles user input events (mouse clicks and motion) to enable spring interaction.
    -  Implements the main game loop for updating the physics and rendering the scene.
- `main()` Function:
    -  Entry point of the program.
    -  Creates an instance of `SpringSimulation` and starts the simulation.

## Demo Video
Check out the project demo video on YouTube: [Project Demo Video](https://www.youtube.com/watch?v=McOcbGHyAWA)


## License

This project is licensed under the MIT License. Feel free to use, modify, and distribute the code.

## Acknowledgements

- SDL2 for providing a cross-platform API for graphics, input, and multimedia.

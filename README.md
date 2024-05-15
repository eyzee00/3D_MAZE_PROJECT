


**Note**: Developped by Hamza Azizi, huge thanks to kosmos90 for the huge
contribution to the project, I've built the project based on his structure, provided I don't have any type of experience when it comes to game development.
**Note**: Windows build is not supported at the moment. The game is only tested on Linux.

# 3D Maze Game using SDL and Raycasting

## Overview

The project is a Raycaster Wolfenstein 3D-style game developed by Seoras Macdonald. It utilizes the SDL library for graphics, image loading, and audio functionalities. The game features raycasting for rendering the 3D perspective in a 2D environment, A* pathfinding algorithm for monster navigation, and collision detection for accurate interaction between entities and the game environment.

## Core Algorithms

### Raycasting

- **Description**: Raycasting is a rendering technique used to create a 3D perspective in a 2D environment. It simulates the projection of rays from the player's viewpoint to determine which objects are visible.
  
- **How it Works**: In each frame, the game casts multiple rays from the player's position, tracing their paths until they intersect with walls or objects in the game world. The distance to the closest wall is calculated for each ray, and this information is used to render the walls on the screen, giving the illusion of depth and perspective.

### A* Pathfinding Algorithm

- **Description**: A* (A-star) is a pathfinding algorithm used to find the shortest path between two points in a graph or grid while avoiding obstacles.
  
- **How it Works**: A* evaluates possible paths based on a combination of two cost functions: the actual cost to reach a node from the start node (known as the "g" value) and the estimated cost to reach the goal node from the current node (known as the "h" value). It selects the most promising path by considering the sum of these two costs (known as the "f" value). By iteratively exploring neighboring nodes and updating their costs, A* efficiently finds the optimal path while avoiding obstacles.

### Collision Detection

- **Description**: Collision detection is a fundamental technique used to determine whether two objects in a game world are intersecting or overlapping.
  
- **How it Works**: Collision detection algorithms typically involve checking the bounding boxes or shapes of objects for intersection. In the game code, when an entity moves, its position is checked against the positions of other objects or solid boundaries in the game world. If a collision is detected, appropriate actions are taken to prevent the entity from passing through solid objects or walls.

## Role in Game Development

- **Raycasting**: Essential for rendering the game world and creating a visually immersive experience by simulating 3D environments in a 2D space. It determines the visibility of objects and walls from the player's perspective, contributing to the game's graphical presentation.
  
- **A* Pathfinding Algorithm**: Facilitates intelligent movement and navigation of monsters in the game world, allowing them to find optimal paths while avoiding obstacles. A* pathfinding enhances the realism of monster behavior and interaction with the player, adding depth to gameplay mechanics.
  
- **Collision Detection**: Integral to ensuring accurate interaction between entities and the game environment. Collision detection prevents entities from moving through solid objects or walls, maintaining the integrity of the game world and enhancing player immersion.

**Dependencies**:
    SDL2, SDL2_Image, SDL2_Mixer


**To Build on Linux**:
Install the following using your package manager:
        libsdl2-dev
        libsdl2-image-dev
        libsdl2-mixer-dev
        clang 
    
Give build.sh execution permissions if it doesn't have it already:
        chmod +x build.sh
Run build.sh:
    	Copy (or make soft link to) the res folder into the bin folder.

Controls:
    WASD:         Move forwards, left, back, and right
    Left Key:     Rotate camera left
    Right Key:    Rotate camera right
    Mouse:        Rotate camera
    Space:        Action (e.g. open doors)
    ALt-Enter:    Fullscreen
    P:            Pause
    Alt-F4 or Esc:Closes the game

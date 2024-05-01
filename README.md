**Note**: Developped by Hamza Azizi, huge thanks to kosmos90 for the huge
contribution to the project, I've built the project based on his structure, provided I don't have any type of experience when it comes to game development.
**Note**: Windows build is not supported at the moment. The game is only tested on Linux.

Dependencies:
    SDL2, SDL2_Image, SDL2_Mixer


To Build on Linux:
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

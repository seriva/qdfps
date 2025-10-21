## About

Inspired by [Cube](http://cubeengine.com/) and [Minecraft](https://minecraft.net/) this project had as goal to create a tiny 3D multiplayer shooter with Minecraft editing and Cube gameplay. 

**Note**: Currently all work on this project has stopped and it will not be updated anymore.

## Features & Tech Stack

- **Language**: Pascal/Delphi with Free Pascal Compiler
- **Graphics**: OpenGL fixed pipeline renderer with SDL2 window management  
- **World System**: 256x256x256 cube map with octree spatial partitioning
- **Real-time Editing**: Minecraft-like in-game world modification
- **Physics**: Basic collision detection and movement simulation
- **Scripting**: Custom scripting language for game logic
- **Rendering**: Texture management, skybox system, frustum culling, static directional lighting
- **Platforms**: Linux, Windows
- **Dependencies**: SDL2, OpenGL

## Project Structure

```
qdfps/
├── src/                    # Source code
│   ├── Main.pas           # Main game loop and initialization
│   ├── Map.pas            # Map loading and management
│   ├── Editing.pas        # World editing functionality
│   ├── Physics.pas        # Physics simulation
│   ├── Renderer.pas       # OpenGL rendering system
│   ├── Lighting.pas       # Lighting calculations
│   ├── Scripting.pas      # Scripting system
│   ├── Skybox.pas         # Sky rendering
│   ├── Textures.pas       # Texture management
│   ├── Console.pas        # Console system
│   ├── Font.pas           # Font rendering
│   ├── Frustum.pas        # Frustum culling
│   ├── Log.pas            # Logging system
│   └── Common.pas         # Common utilities and types
├── bin/                    # Compiled binaries and runtime data
│   ├── data/              # Game assets
│   │   ├── maps/         # Map files
│   │   ├── scripts/      # Script files
│   │   ├── skyboxes/     # Skybox textures
│   │   └── textures/     # Game textures
│   ├── QDFPS             # Linux executable
│   ├── QDFPS.exe         # Windows executable
│   └── sdl2.dll          # SDL2 library (Windows)
├── libs/                   # Third-party libraries
│   ├── opengl/           # OpenGL headers
│   └── sdl/              # SDL2 headers
├── build/                 # Build artifacts
└── LICENSE.md            # MIT License
```

## Quick Start

### Prerequisites
- Free Pascal Compiler (FPC) or Lazarus IDE
- SDL2 development libraries
- OpenGL development libraries

### Linux Setup
```bash
# Install dependencies (Ubuntu/Debian)
sudo apt-get install libsdl2-dev libgl1-mesa-dev

# Install Free Pascal
sudo apt-get install fpc
```

### Windows Setup
1. Install Lazarus IDE (includes Free Pascal)
2. Download SDL2 development libraries
3. Extract SDL2 to the `libs/sdl/` directory

### Building

**Using Lazarus IDE:**
1. Open `src/QDFPS.lpi` in Lazarus
2. Configure build settings for your platform
3. Build the project (F9 or Build menu)

**Using Command Line:**
```bash
cd src
fpc QDFPS.lpr
```

### Running
```bash
# Linux
./bin/QDFPS

# Windows
bin/QDFPS.exe
```

## Usage

### Controls
- **WASD**: Move forward/backward/strafe
- **Mouse**: Look around
- **Left Click**: Place blocks (in edit mode)
- **Right Click**: Remove blocks (in edit mode)
- **Tab**: Toggle edit mode
- **ESC**: Exit game

### Gameplay
- Navigate through the 3D world using WASD + mouse controls
- Switch between play and edit modes with Tab
- Build and modify the world in real-time (single-player only)
- In-game console for debugging and commands

## Architecture

The game uses a modular design with these core systems:
- **Map System**: World data management with octree spatial partitioning
- **Renderer**: OpenGL rendering, texture management, and frustum culling  
- **Physics**: Collision detection and player movement
- **Scripting**: Custom script interpreter for game logic
- **Console**: Debug interface and command system

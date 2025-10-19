## About

Inspired by [Cube](http://cubeengine.com/) and [Minecraft](https://minecraft.net/) this project had as goal to create a tiny 3D multiplayer shooter with Minecraft editing and Cube gameplay. 

**Note**: Currently all work on this project has stopped and it will not be updated anymore.

## Features

- **Minecraft-like Editing**: 256x256x256 cube map editing capabilities
- **Octree Scene Management**: Efficient spatial partitioning for large worlds
- **Simple Scripting Language**: Custom scripting system for game logic
- **Collision Detection**: Basic collision detection system
- **OpenGL Rendering**: Fixed pipeline OpenGL renderer with static directional lighting
- **Multiplayer Support**: Network-based multiplayer gameplay
- **Real-time Editing**: In-game world editing capabilities
- **Skybox System**: Dynamic sky rendering with multiple skybox support
- **Texture Management**: Efficient texture loading and management
- **Physics Integration**: Basic physics simulation for gameplay

## Tech Stack

- **Language**: Pascal/Delphi (Free Pascal Compiler)
- **Graphics**: OpenGL with SDL2 for window management
- **Build System**: Lazarus IDE / Free Pascal
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
- Navigate through the 3D world
- Switch between play and edit modes
- Build and modify the world in real-time
- Multiplayer support for collaborative building

## Development

### Architecture
The game follows a modular architecture with separate systems for:
- **Rendering**: OpenGL-based rendering with frustum culling
- **Physics**: Basic collision detection and movement
- **Scripting**: Custom scripting language for game logic
- **Networking**: Multiplayer synchronization
- **Editing**: Real-time world modification

### Key Components
- **Map System**: Handles world data and octree spatial partitioning
- **Renderer**: OpenGL rendering with texture management
- **Physics**: Collision detection and player movement
- **Scripting**: Custom script interpreter for game logic
- **Console**: In-game console for debugging and commands

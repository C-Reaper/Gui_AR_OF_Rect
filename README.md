# Project README

## Overview
This project is a simple implementation of an Augmented Reality (AR) system that uses optical flow for object tracking. The AR system is built using C/C++ and utilizes various libraries to handle rendering, image processing, and user input.

## Features
- Optical Flow Detection: Tracks movement in video frames.
- Augmented Reality: Overlays tracked objects onto a virtual background.
- Cross-platform Compatibility:
  - Linux
  - Windows (using MinGW-w64)
  - WebAssembly

## Project Structure
```
<project>/
├── build/                  # Compiled executable files (.exe, .so, .dll, .js)
├── src/                    # Source code directory
│   ├── Main.c              # Entry point of the application
│   ├── optical_flow.h      # Header file for optical flow detection functions
│   └── gui.h               # Header file for GUI rendering functions
└── Makefile.linux          # Linux build configuration
├── Makefile.windows        # Windows build configuration
├── Makefile.wine           # Wine build configuration (for Linux cross-compilation to Windows)
└── Makefile.web            # WebAssembly build configuration using Emscripten
```

### Prerequisites
- C/C++ Compiler and Debugger: GCC, Clang
- Make utility
- Standard development tools
- Libraries:
  - X11 for GUI rendering (Linux)
  - MinGW-w64 for Windows cross-compilation
  - SDL2 for Emscripten build

## Build & Run
### Linux
```sh
cd <project>
make -f Makefile.linux all
make -f Makefile.linux exe
```

### Windows
```sh
cd <project>
make -f Makefile.windows all
make -f Makefile.windows exe
```

### WebAssembly
```sh
cd <project>
make -f Makefile.web all
make -f Makefile.web exe
```

For clean rebuilds and additional build options, refer to the Makefiles for detailed instructions.
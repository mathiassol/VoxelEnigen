# Minecraft voxel enigen
![License: All Rights Reserved](https://img.shields.io/badge/License-All%20Rights%20Reserved-red.svg)

![OpenGL](https://img.shields.io/badge/OpenGL-%23FFFFFF.svg?style=for-the-badge&logo=opengl)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![CLion](https://img.shields.io/badge/CLion-000000?style=for-the-badge&logo=clion~~)
![CMake](https://img.shields.io/badge/CMake-%23008FBA.svg?style=for-the-badge&logo=cmake)
![MSYS2](https://img.shields.io/badge/MSYS2-262D3A?style=for-the-badge&logo=msys2)
![Make](https://img.shields.io/badge/Make-000000?style=for-the-badge)


A voxel-based engine built from scratch in C++ and OpenGL. Features procedurally generated infinite worlds with Perlin noise terrain, biome systems, tree generation, optimized chunk rendering. Includes a first-person player controller with physics, collision detection, block placement/destruction, and a texture atlas system for efficient rendering.

## build
You need to have your C++ compiler set up already. There are many good tutorials on YouTube if you don't know how to do that. As I'm on Windows, I use MSYS2 MINGW64, then you install CMake and the OpenGL support libraries: GLFW, GLEW, GLM. 
````
pacman -S mingw-w64-x86_64-glew mingw-w64-x86_64-glfw
````

you will also nead to clone the imgui repository from github into the src folder:
````
git clone https://github.com/ocornut/imgui.git
````
build and compile:
````
mkdir build
cd build
cmake -G "MinGW Makefiles" ..
mingw32-make
````

in many cases you will nead to have the openGL support libs in your build folder, because sometimes adding /bin to path is not enough. in that case just copy the .dll files from /bin to /build. The files you need to copy are glew32.dll, glfw3.dll, and opengl32.dll
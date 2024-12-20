# Computer graphics in Game development course

This repo contains a template for Computer graphics in Game development labs

## Pre-requirements

- Version control: [Git](https://git-scm.com/)
- Build automation: [CMake](https://cmake.org/download/)
- C++ compiler: MSVC on Windows, Clang on MacOS, GCC on Linux (C++17 compatible)
- [OpenMP library](https://www.openmp.org/)
- Source code editor: [Visual Studio Code](https://code.visualstudio.com/Download)

For DirectX12 you need a Windows machine or VM with installed software and [Windows SDK](https://developer.microsoft.com/en-us/windows/downloads/windows-sdk/).
For graphics debugging you may to install [Microsoft PIX](https://devblogs.microsoft.com/pix/download/).

## How to build the solution

Use `git clone --recursive` to clone the repo with submodules or run `git submodule update --init --recursive` after the first clone.

Go to the project folder and run the next command:

```sh
mkdir Build
cd Build
cmake ..
```


### Creative Task: Black and White Film Filter

The `apply_black_and_white_film_filter` function transforms each pixel in the render target to create a black-and-white film effect. Unlike simple grayscale conversion, this filter adds a slight grainy noise to each pixel, mimicking the look of vintage film. The noise effect introduces subtle variations, giving the image an authentic, aged feel, reminiscent of classic movies.

#### Example:
![Black and White Film Effect](result.png)

### Creative Task: Raytracing

The task implements ray tracing and modifies the `closest_hit_shader` to support Monte Carlo light tracing.
#### Result without Monte Carlo Light:
![result](result_raytracing.png)

#### Result with Monte Carlo Light
- raytracing depth = 3
- accumulation num = 16
![3_16](3_16.png)

(I was waiting about 0.5h...)
- raytracing depth = 3
- accumulation num = 128
- ![3_128](3_128.png)

## Third-party tools and data

- [STB](https://github.com/nothings/stb) by Sean Barrett (Public Domain)
- [Linalg.h](https://github.com/sgorsten/linalg) by Sterling Orsten (The Unlicense)
- [Tinyobjloader](https://github.com/syoyo/tinyobjloader) by Syoyo Fujita (MIT License)
- [Cxxopts](https://github.com/jarro2783/cxxopts) by jarro2783 (MIT License)
- [Cornell Box models](https://casual-effects.com/g3d/data10/index.html#) by Morgan McGuire (CC BY 3.0 License)
- [Cube model](https://casual-effects.com/g3d/data10/index.html#) by Morgan McGuire (CC BY 3.0 License)
- [Teapot model](https://casual-effects.com/g3d/data10/common/model/teapot/teapot.zip) by Martin Newell (CC0 License)
- [Dabrovic Sponza model](https://casual-effects.com/g3d/data10/index.html#) by Marko Dabrovic (CC BY-NC License)

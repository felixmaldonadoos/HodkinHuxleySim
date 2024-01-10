Author: by Felix A. Maldonado Osorio
Date: January 6, 2024

# Introduction

## To do: 
- check action potential model. AP is not reaching baseline. 
- voltage seems off. need to recheck equations and what the injection current looks like. maybe indexing is off.
- rendering issues. have seen some bugs online regarding zink and nvidia drivers. 
- uninstalling ```gnuplot-qt``` does not fix rendering issues.

# Notice:

This is a work in progress. Currently focusing on Ubuntu 22 build in WSL2. 

# Installation:

- Clone this repo recursively to include all submodules 

``` 

git clone --recursive-submodules https://github.com/felixmaldonadoos/HodgkinHuxleySim.git 
sudo apt-get install libboost-all-dev
apt install gnuplot-qt

```

- (On Linux) install Boost with ``` sudo apt-get install libboost-all-dev ```

### Dependencies
- CMake (minimum 3.0.0)
- Imgui 
- Implot
- Boost
- gnuplot-qt (required by sciplot for use in tests/HH.cpp)

Note: To run imgui's opengl and glfw implementation on WSL2 Ubuntu 22 but I still had to install ``` Windows SDK 8.1 ``` (found in ```resources/sdksetup.exe``` folder) and ```MSVC v140 - Vs 2015 C++ build tools (v14.00)```.


# Current version has: 
- HH.cpp creates plots showing gating values and action potential. Model is still off. 

# Resources/Acknowledgements

- https://github.com/Daniel-M/Hodgking-Huxley
- https://github.com/epezent/implot_demos

# Demos (to do)

|Demo|Description|Image|
|---|---|---|
|`demo/main.cpp`|Main demo. Displays the ImPlot (and ImGui) library supplied demo windows.| |
|`tests/HH.cpp`|Simple filter toy for educational purposes. Displays time domain input/output signals, and the frequency domain transfer function, amplitude spectrum, etc.|![filter](https://raw.githubusercontent.com/epezent/implot_demos/master/screenshots/filter.png)|

## Results (to do)

|Figure|Description|Image|
|---|---|---|
|`Injection Current`|SAVE PICTURE| |
|`Action potential (Voltage)`|SAVE PICTURE|![filter](https://raw.githubusercontent.com/epezent/implot_demos/master/screenshots/filter.png)|
|`Gating`|NEED TO IMPLEMENT!|![spectrogram](https://github.com/epezent/implot_demos/blob/master/screenshots/spectrogram.png)|
|`maps.cpp`|OpenStreetMap world map viewer. Downloads and displays zoomable tile maps in a plot.|![maps](https://github.com/epezent/implot_demos/blob/master/screenshots/maps.png)|
|`mandel.cpp`|Realtime Mandelbrot viewer using AVX2 and OpenMP acceleration. *Recommend compiling with ImPlot `backends` branch.*|![mandel](https://github.com/epezent/implot_demos/blob/master/screenshots/mandel.png)|
|`perlin.cpp`|Renders perlin noise in a heatmap.|![perlin](https://github.com/epezent/implot_demos/blob/master/screenshots/perlin.png)|
|`graph.cpp`|Simple graphing calculator using `exprtk` expression evaluator.|![perlin](https://github.com/epezent/implot_demos/blob/master/screenshots/graph.png)|
|`stocks.cpp`|Downloads and displays historical stock data from Yahoo Finance.|![perlin](https://github.com/epezent/implot_demos/blob/master/screenshots/stocks.png)|

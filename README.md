# CppND-Route-Planning-Project

Implementation Of A* Search Algorithm using OpenStreetMap.

![Route Visualization](map.png)

## 🎯 Overview

This project demonstrates the implementation of the A* pathfinding algorithm in C++ to calculate optimal routes on OpenStreetMap data. The application parses OSM XML files, constructs a graph representation of the road network, and uses A* search to find the shortest path between user-specified coordinates.

## ✨ Features

- **A* Search Algorithm**: Efficient pathfinding using heuristic-based search
- **OpenStreetMap Integration**: Parse and process real-world map data from OSM XML files
- **Route Visualization**: Graphical rendering of maps and calculated routes using IO2D
- **Unit Testing**: Comprehensive test suite to ensure algorithm correctness
- **Flexible Input**: Support for custom map files and coordinates

## 🏗️ Project Structure

```
.
├── cmake/              # CMake configuration files
├── lib/                # Library implementation files
├── src/                # Main source code
├── test/               # Unit tests
├── thirdparty/         # External dependencies
├── CMakeLists.txt      # Build configuration
├── map.osm             # Sample OpenStreetMap data
├── map.png             # Map visualization
└── README.md           # This file
```

## 📋 Cloning

When cloning this project, be sure to use the `--recurse-submodules` flag. Using HTTPS:

```bash
git clone https://github.com/adsv1623/CppND-Route-Planning-Project.git --recurse-submodules
```

## 🔧 Dependencies for Running Locally

### cmake >= 3.11.3
- All OSes: [cmake.org/install](https://cmake.org/install/)

### make >= 4.1 (Linux, Mac), 3.81 (Windows)
- Linux: make is installed by default on most Linux distros
- Mac: install [Xcode command line tools](https://developer.apple.com/xcode/features/) to get make
- Windows: [gnuwin32.sourceforge.net/packages/make.htm](http://gnuwin32.sourceforge.net/packages/make.htm)

### gcc/g++ >= 7.4.0
- Linux: gcc / g++ is installed by default on most Linux distros
- Mac: same instructions as make - install Xcode command line tools
- Windows: recommend using MinGW

### IO2D
- Installation instructions for all operating systems can be found [here](https://github.com/cpp-io2d/P0267_RefImpl/blob/master/BUILDING.md)
- This library must be built in a place where CMake `find_package` will be able to find it

## 🚀 Compiling and Running

### Compiling

To compile the project, first, create a build directory and change to that directory:

```bash
mkdir build && cd build
```

From within the build directory, then run cmake and make as follows:

```bash
cmake .. && make
```

### Running

The executable will be placed in the build directory. From within build, you can run the project as follows:

```bash
./OSM_A_star_search
```

Or to specify a map file:

```bash
./OSM_A_star_search -f ../<your_osm_file.osm>
```

## 🧪 Testing

The testing executable is also placed in the build directory. From within build, you can run the unit tests as follows:

```bash
./test
```

## 🎮 Usage

1. Launch the application
2. The program will prompt you to enter start and end coordinates (as percentages of the map: 0-100)
3. The A* algorithm will calculate the optimal route
4. A window will display the map with the calculated path highlighted

### Example Input
```
Enter start x coordinate (0-100): 10
Enter start y coordinate (0-100): 10
Enter end x coordinate (0-100): 90
Enter end y coordinate (0-100): 90
```

## 🧮 Algorithm Details

### A* Search Algorithm

The A* algorithm finds the shortest path by using a heuristic function to guide the search:

- **g(n)**: Actual cost from start node to node n
- **h(n)**: Estimated cost from node n to goal (heuristic)
- **f(n) = g(n) + h(n)**: Total estimated cost

The algorithm prioritizes exploring nodes with the lowest f(n) value, ensuring an optimal path when using an admissible heuristic.

### Heuristic Function

This implementation uses the **Euclidean distance** as the heuristic, which provides an optimistic estimate of the remaining distance to the goal.

## 🗺️ OpenStreetMap Data

The project uses OSM XML format files. You can download custom map data from:
- [OpenStreetMap Export](https://www.openstreetmap.org/export)
- [BBBike Extract Service](https://extract.bbbike.org/)
- [Geofabrik Downloads](https://download.geofabrik.de/)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is part of the Udacity C++ Nanodegree program.

## 🙏 Acknowledgments

- Udacity C++ Nanodegree Program
- OpenStreetMap contributors
- IO2D graphics library maintainers

## 📧 Contact

Project Link: [https://github.com/adsv1623/CppND-Route-Planning-Project](https://github.com/adsv1623/CppND-Route-Planning-Project)

---

⭐ If you found this project helpful, please consider giving it a star!

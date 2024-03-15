# game-2048

[![Actions Status](https://github.com/garlinhs/game-2048/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/garlinhs/game-2048/actions/workflows/ci.yml)
[![Run on Repl.it](https://repl.it/badge/github/garlinhs/game-2048)](https://repl.it/github/garlinhs/game-2048)

> Terminal version of the game "2048" written in C++.

<p align="center">
    <img align="center" alt="2048 in action!" src="assets/demo.gif"></img>
</p>

## Setup

The game and code is made to run natively on the GNU/Linux and MacOS platforms, but cross-platform compatibility for Windows has been added too.

### Requirements

* C++11 compiler (e.g. `g++`, `clang++`, `pgc++`, `icpc`, etc.)
* Virtually any platform including:
  * Linux
  * MacOS
  * Windows (via Cygwin or Windows Subsystem for Linux)
* [CMake](https://cmake.org/) or [Meson](https://mesonbuild.com/)

### Installation

1. Open your terminal in your preferred directory and clone this project:
```sh
git clone https://github.com/garlinhs/game-2048
```
2. Enter the project directory:
```sh
cd game-2048
```

---

For both CMake and Meson, the default C++ compiler on your system will be used.
If you wish to manually select a C++ compiler, optionally add `CXX=clang++ cmake` or `CXX=clang++ meson` etc.

#### Building with CMake

3. Build the executable and run tests
```sh
ctest -S setup.cmake
```
4. Install the program (optional)
```sh
cmake --install build
```

5. Run the program and play the game! :tada:
```sh
2048    # run `build/2048` if game is not installed
```

<p align="center">
    <b>OR</b>
</p>

#### Building with Meson

3. Generate build configuration
```sh
meson build
```
4. Build the executable and run tests
```sh
meson test -C build
```
5. Install the program (optional)
```sh
meson configure build --prefix=$HOME/.local
meson install -C build
```

6. Run the program and play the game! :tada:
```sh
2048    # run `build/2048` if game is not installed
```

## Contributing

First of all, thank you for contributing :smile:! A few things to note:

* If you have found a bug, or have a feature that you'd like implemented, [raise an issue](https://github.com/garlinhs/game-2048/issues).

* If you have proposed a pull request, make sure that you run `clang-format` on the source code (both, `.cpp` and `.hpp`) files if you've made changes there.

* In your local repository, run `git update-index --skip-worktree ./data/*.txt` to ensure that changes to the data files are not tracked by git, and thus are not staged.

### Maintainers

* [Garlinh Soler](https://github.com/garlinhs)

---

## License

Copyright (c) Garlinh Soler. All rights reserved.

Licensed under the [MIT](LICENSE) License.

# oasis [![C++20](https://img.shields.io/badge/C%2B%2B-20-blue?logo=c%2B%2B&logoColor=white)](https://en.cppreference.com/w/cpp/20.html) [![License](https://img.shields.io/github/license/Water-Engine/oasis)](LICENSE) [![LOC](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/Water-Engine/oasis/loc/.github/loc_badge.json)](https://github.com/Water-Engine/oasis/actions/workflows/loc.yml) [![Last commit](https://img.shields.io/github/last-commit/Water-Engine/oasis)](https://github.com/Water-Engine/oasis) [![Formatting](https://github.com/Water-Engine/oasis/actions/workflows/format.yml/badge.svg)](https://github.com/Water-Engine/oasis/actions/workflows/format.yml) [![CI](https://github.com/Water-Engine/oasis/actions/workflows/ci.yml/badge.svg)](https://github.com/Water-Engine/oasis/actions/workflows/ci.yml)
THe water engine's neural network generator.

# Goals
The ultimate goal of this project is to create a fully functional machine learning C++ suite for training the water engine's NNUE-based evaluation function and its ML-powered MCTS. As this is a monstrous undertaking, Python is used for initial prototyping and for getting working models for water. 

# Getting Started
To interact with the python prototype, run:
```shell
git clone https://github.com/Water-Engine/oasis.git
cd oasis
pip install -r requirements.txt
python prototyping/main.py
```

For a quick build of the C++ program, run:
```shell
git clone https://github.com/Water-Engine/oasis.git
cd oasis
make -j4 run
```

# Core Dependencies
- g++ with C++20
- GNU Make
- Clang-format
- [Catch2](https://github.com/catchorg/Catch2) for tests (included in this repository)
- [cloc](https://github.com/AlDanial/cloc) for cloc make target (optional)
- [python](https://www.python.org/downloads/) for prototyping
- [Zig 0.15.1](https://ziglang.org/download/) for cross-platform packaging (optional) 

# Building oasis
The project's build system uses C++20 and GNU Make, and it is recommended that you run make with the flag `-j4` to run batch jobs. These commands will only function once the C++ suite enters it's development stage. Below is a list of targets with their requirements where applicable:

## Build Specific Targets
- `default`: Builds the release configuration (default)
- `install`: Builds the dist config (to be updated)
- `all`: Builds all optimization configurations for the project (dist, release, and debug)
- `dist`: Builds the project with maximum optimization and disabled profiling
- `release`: Builds the project with slightly fewer optimizations and no DEBUG define
- `debug`: Builds the project with no optimization, defining both PROFILE and DEBUG
- `test`: Run the project's unit tests Excludes perft testing
- `perft`: Run the perft tests
- `run`: Alias for run-release
- `run-dist`: Build and run the dist binary
- `run-release`: Build and run the release binary
- `run-debug`: Build and run the debug binary
- `fmt`: Format all C++ source and header files using `clang-format`
- `fmt-check`: Validates C++ formatting rules without altering project files
- `clean`: Remove object files, dependency files, and binaries

## General Targets
- `cloc`: Count the lines of code in the project's relevant directories
- `sliders`: Generate the magic numbers for the rooks and bishops
- `help`: Print this help menu

# For Developers
Contributing guidelines, information on tests, formatting, and profiling can be found in [CONTRIBUTING.md](.github/CONTRIBUTING.md).

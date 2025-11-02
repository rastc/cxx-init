# CXX Init - Designated Initializer Library

A C++14 library that provides designated initializer syntax using Boost.Preprocessor macros.

## Features

- Designated initializer syntax for C++ structs
- Header-only library
- Uses Boost.Preprocessor for macro magic
- Cross-platform support

## Requirements

- C++14 compatible compiler
- CMake 3.16 or higher
- Git (for submodules)

## Installation

### Cloning the Repository

```bash
git clone --recursive https://github.com/rastc/cxx-init.git
cd cxx-init
```

If you already cloned without `--recursive`, initialize the submodules:

```bash
git submodule update --init --recursive
```

### Building the Project

```bash
# Configure
cmake --preset vs2022  # Windows with Visual Studio
# or
cmake --preset default  # Linux/macOS with Ninja

# Build
cmake --build build-vs2022 --config Release
# or
cmake --build build --config Release
```

## Usage

```cpp
#include "cxx_init.h"

struct Person {
    std::string name;
    int age;
    std::string city;
    double height;
};

int main() {
    Person p = cxx(
        .name = "Alice",
        .age = 30,
        .city = "New York",
        .height = 5.6
    );
    
    return 0;
}
```

## License

MIT License
A C++14 script that provides designated initializer

## Godbolt

[https://godbolt.org/z/xbdvdjejd](https://godbolt.org/z/xbdvdjejd)

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

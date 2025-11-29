clsStackArray <img align="right" src="https://img.shields.io/badge/C++-17-blue.svg?style=flat-square" alt="C++17">

**A fast, clean, and fully featured generic Stack implementation in C++ built on top of `clsQueueArray`.**

Perfect for students learning DSA, embedded systems, or any project needing a powerful yet simple stack with extra utilities beyond `std::stack`.

## Features

| Operation                  | Complexity | Description                                      |
|----------------------------|------------|--------------------------------------------------|
| `push` / `insert_top`      | **O(1)**   | Add element to the top                           |
| `pop` (via inherited)      | **O(1)**   | Remove from top (uses queue's `pop`)             |
| `top()`                    | O(1)       | Access top element                               |
| `bottom()`                 | O(1)       | Access bottom (first pushed) element             |
| `insert_bottom(val)`       | O(1)       | Push to bottom – great for advanced algorithms   |
| Random access `get(i)`     | O(1)       | Direct index access (array-based)                |
| `reverse()`                | O(n)       | Reverse entire stack in-place                    |
| `update()`, `insert_after()` | O(1)     | Full control over any position                   |
| Fully generic              | Yes        | Works with built-in and custom types             |

## Why clsStackArray?

- **More powerful than `std::stack`** – supports random access, reverse, insert at bottom, indexing, etc.
- **Zero overhead** – built on the efficient `clsDynamicArray` (auto-resizing, no leaks).
- **Header-only** – just drop in and use.
- **Extremely readable** – ideal for teaching and learning.
- Inherits all rich features from `clsQueueArray` while staying true to LIFO behavior.

## Quick Example

```cpp
#include "clsStackArray.h"
#include <iostream>

int main() {
    clsStackArray<int> stack;

    stack.push(10);
    stack.push(20);
    stack.push(30);

    stack.print();                    // 30 20 10
    cout << "Top: " << stack.top() << endl;     // 30
    cout << "Bottom: " << stack.bottom() << endl; // 10

    stack.insert_bottom(5);
    stack.print();                    // 30 20 10 5

    stack.reverse();
    stack.print();                    // 5 10 20 30

    stack.pop();  // removes 5
    stack.print();                    // 10 20 30

    return 0;
}
Installation
Just include the three header files in your project:
textclsDynamicArray.h
clsQueueArray.h
clsStackArray.h
No build configuration needed.
Requirements

C++17 or higher

Project Structure (Recommended)
textclsDynamicArray ← base dynamic array
    ↓
clsQueueArray   ← full-featured queue
    ↓ (inheritance)
clsStackArray   ← powerful stack with extra abilities
License
MIT © 2025 – Free to use, modify, and distribute.

If this helped you learn or build faster, please ⭐ the repo! It means the world to open-source educational projects.
textReady to make your GitHub repo look professional, clean, and attractive!  
This version emphasizes performance, extra features, and educational value — exactly what make

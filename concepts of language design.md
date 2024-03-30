
# Concepts of language design

Things like "Lexical Scope", "Code Blocks" - the various things I'll be attempting to compare across various languages.

## Evaluation strategy / parameter-passing strategy

Given a function that takes one (or some) parameter(s), _how_ are those params passed? Is it a value that becomes independent from the place it was called? Is it a reference to a location in memory where the value is stored? How else might this work? Turns out there are a bunch of ways to do this - way more than I expected!

_pass-by-... and call-by-... are the same thing. Going with pass-by... as it makes more sense to me._

- **pass-by-value** - "only" the value is passed in, editing the value in the called function won't change it in the caller. Usually done by copying the value to a new location in memory. Sets up a functional-like ability, but for functional languages where values are immutable pass-by-reference achieves the same thing.
- **pass-by-reference** - the caller passes the reference (a note of where the value/structure is held in memory). Modifications (to the object, or a reassignment of the object) are therefore visible to the caller. More efficient, but harder for programmers to avoid subtle bugs.
- **pass-by-sharing** - a memory location is passed as in pass-by-reference. Called functions can edit the object at that memory location. But, they cannot change where the ref points.
- **pass-by-name**
- **pass-by-copy-restore**
- **pass-by-unification**
- **pass-by-need**
- **pass-by-reference-parameters**
- **pass-by-reference-to-const**

  **Pass-by-reference vs Pass-by-sharing (because the difference here seems pretty subtle!)**

Python is pass-by-sharing (as are Javascript, ...)

```python
# I'm going to pass this list and in one case change the Data, in the other I'll change the Reference.
my_thing = [1, 2, 3]

def modify_value(ref):
    ref.append(4)  # Change the values in the given memory location

def modify_reference(ref):
    ref = [4, 5, 6]  # Change where the reference points

modify_value(my_thing)
print(my_thing)  # Output: [1, 2, 3, 4] - the data was changed!

modify_reference(my_thing)
print(my_thing)  # Output: [1, 2, 3] - the reference did not change
```

C++ allows a few options for passing parameters:

```cpp
#include <iostream>

void modifyValue(int x) {
    x = 2;
}
void modifyReference(int &x) {
    x = 3;
}
void modifyPointer(int *x) {
    *x = 4;
}

int main() {
    int myValue = 1;

    modifyValue(myValue);
    std::cout << myValue << std::endl; // Output: 1 (main scope wasn't changed)

    modifyReference(myValue);
    std::cout << myValue << std::endl; // Output: 3 (main scope WAS changed)

    modifyPointer(&myValue);
    std::cout << myValue << std::endl; // Output: 4 (main scope WAS changed)

    return 0;
}

```

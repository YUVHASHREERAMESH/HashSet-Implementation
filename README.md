# HashSet Implementation

A simple C implementation of a HashSet using hash table with collision resolution through chaining.

## Features
- Add elements to the set
- Remove elements from the set
- Check if an element exists in the set
- Display all elements in the set
- Delete the entire set and free memory
- Hash function with modulo operation for distribution

## Files
- `HashSet.c` - HashSet implementation with all operations
- `header.h` - HashSet structure and function declarations
- `main.c` - Demonstrates HashSet operations

## How to Compile
Use a C compiler such as GCC:

```bash
gcc main.c HashSet.c -o hashset
```

## How to Run
```bash
./hashset
```

## HashSet Operations

### Creating a HashSet
```c
HashSet* set = createHashSet();
```

### Adding Elements
```c
addHashSet(set, 10);
addHashSet(set, 20);
```

### Checking if Element Exists
```c
if(hashSetContains(set, 10)) {
    printf("Element found\n");
}
```

### Removing Elements
```c
removeHashSet(set, 10);
```

### Displaying Elements
```c
displayHashSet(set);
```

### Deleting HashSet
```c
deleteHashSet(set);
```

## Hash Function
The implementation uses a simple hash function with modulo operation:
```c
int hash(int key) {
    return key % TABLE_SIZE;  // TABLE_SIZE = 1009
}
```

## Collision Resolution
Collisions are handled using **chaining** - each bucket in the hash table points to a linked list of elements.

## Memory Management
- All nodes are dynamically allocated
- Proper deallocation is performed when removing elements
- The entire set can be deleted to free all allocated memory

## Author
HashSet Implementation Project

## Requirements
- GCC compiler or any C compiler
- Standard C libraries (stdio.h, stdlib.h, stdbool.h)

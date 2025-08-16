This document contains some of the new data types I encountered during my time learning C++

---

## Table of Contents

1. [Containers](#containers)
2. [Key-Value Storage](#key-value-storage)
3. [Grouping](#grouping)
4. [Pointers](#pointers) | See: [[Memory Management]] 👀

---

## Containers

Common container types for storing collections of data:

- `std::vector<T>` - Dynamic array, resizable
- `std::array<T, size>` - Fixed size array
- `std::list<T>` - Doubly linked list - See: [[Data Structures#Doubly Linked List]] 👀
- `std::deque<T>` - Double-ended queue - See: [[Data Structures#Doubly Linked List]] 👀

## Key-Value Storage

For associating keys with values:

- `std::map<K, V>` - Ordered key-value pairs
- `std::unordered_map<K, V>` - Hash table, faster lookups
- `std::set<T>` - Unique values only
- `std::unordered_set<T>` - Hash set

## Grouping

For bundling multiple values together:

- `std::pair<T1, T2>` - Two values
- `std::tuple<T1, T2, ...>` - Multiple values
- `std::optional<T>` - Value that might not exist

## Pointers

See: [[Memory Management]] for detailed coverage

- `std::unique_ptr<T>` - Exclusive ownership
- `std::shared_ptr<T>` - Shared ownership
- `std::weak_ptr<T>` - Non-owning reference

---

Written by [Marco](https://github.com/msh31/)
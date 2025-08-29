This document helps you understand memory in computers, how programs allocate and deallocate memory, and best practices for managing memory efficiently and safely.

-----

## Table of Contents

1. [What is memory?](#what-is-memory)
2. [Stack vs Heap](#stack-vs-heap)
3. [Manual memory management](#manual-memory-management)
4. [Smart pointers](#smart-pointers)
5. [Memory leaks](#memory-leaks)
6. [Common problems](#common-problems)
7. [Best practices](#best-practices)
8. [Code examples](#code-examples)
9. [RAII decision Tree](#raii-decision-tree)

-----

## What is memory?



## Stack vs Heap

*Differences between stack and heap memory allocation…*

## Manual memory management

*Using malloc/free, new/delete, and when you need manual control…*

## Smart pointers

See: [[C++ data types#Pointers]] for C++ specific smart pointer types

*Automatic memory management using smart pointers…*

## Memory leaks

*What they are, how they happen, and how to prevent them…*

## Common problems

*Dangling pointers, double-free errors, buffer overflows…*

## Best practices

*Guidelines for safe and efficient memory usage…*

## Code examples

*Practical examples showing good and bad memory management…*

## RAII Decision Tree

## Ask Yourself:
1. Does this object manage a resource? (Handle, socket, file, memory)
   → YES: Disable copying with `= delete`
   
2. Is this just data? (strings, numbers, collections of data)  
   → NO: Default copy behavior is fine

3. Do I need to transfer ownership?
   → YES: Implement move semantics

## Common Resource Types:
- HANDLE (Windows handles) → Disable copying
- SOCKET → Disable copying  
- FILE* → Disable copying
- Allocated memory → Disable copying
- std::string → Copying is fine
- int, double → Copying is fine
- std::vector<data> → Copying is fine

## Red Flags:
- Manual cleanup in destructors → Check if copying is disabled
- Multiple return paths → RAII eliminates this problem
- Nested if statements for cleanup → RAII makes code linear

-----

Written by [Marco](https://github.com/msh31/)

Written by [Marco](https://github.com/msh31/)

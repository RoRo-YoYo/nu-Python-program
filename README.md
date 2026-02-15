# nuPython Interpreter (Projects 04–07)

A multi-stage implementation of a source-level debugger and execution engine for **nuPython**, a subset of Python, written in C/C++.

This repository combines Projects 04–07 into a single, cohesive system that supports program parsing, debugging, memory management, and execution with control flow.

---

## Overview

nuPython programs are:

1. Parsed into tokens
2. Built into a program graph
3. Executed statement-by-statement
4. Stored and evaluated using a custom RAM module
5. Optionally debugged via a source-level debugger

The system supports expressions, variables, functions, relational operators, conditionals, loops, and pointer-based assignments.

---

## Components

### 1. Debugger
- Step execution
- Breakpoints
- Variable inspection
- Memory inspection
- Program graph traversal
- Semantic error detection

### 2. RAM Module
- Dynamic vector-like memory structure
- Supports:
  - int
  - real
  - string
  - boolean
  - pointer
  - none
- Address-based and name-based access
- Automatic resizing
- Memory-safe design

### 3. Execution Engine

Supports execution of:

#### Statements
- Assignment
- Function call
- Pass
- If / elif / else
- While loops
- Pointer-based assignment

#### Expressions
- Unary expressions
- Binary expressions

#### Operators
- Arithmetic: +, -, *, **, /, %
- Relational: ==, !=, <, <=, >, >=

#### Data Types
- Integer
- Real
- String
- Boolean
- Pointer

#### Built-in Functions
- print()
- input()
- int()
- float()

---

## Semantic Error Handling

Execution immediately stops on:

- Undefined variables
- Invalid operand types
- Divide by zero
- Mod by zero
- Invalid pointer address
- Invalid type conversion
- Unknown function calls

Errors are printed in the required semantic error format.

---

## Design Highlights

- Program graph–based execution model
- Helper-function–driven architecture
- No global variables
- Modular design across stages
- Enumerated types used safely (no hardcoded integers)
- Function size constraints enforced
- Immediate termination on semantic errors

---

## Technical Stack

C  
Program graph data structure  
Custom memory management (RAM module)  
Interpreter design  
Recursive expression evaluation  
Control-flow execution  

---

## Build

Each project stage builds independently using its respective Makefile.


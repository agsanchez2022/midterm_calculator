# Midterm Calculator Project

## Features

This calculator application implements several arithmetic operations using the Factory design pattern.

Supported operations include:

- Addition
- Subtraction
- Multiplication
- Division
- Power
- Root
- Modulus
- Integer Division
- Percentage
- Absolute Difference

The calculator also supports history tracking, undo/redo functionality, and automatic saving of calculations.

---

## Design Patterns Used

This project demonstrates several software design patterns:

- **Factory Pattern** – `OperationFactory` dynamically creates operation objects.
- **Strategy Pattern** – each arithmetic operation is implemented as its own class.
- **Observer Pattern** – logging and automatic history saving observe calculator events.
- **Memento Pattern** – enables undo and redo functionality for calculations.

---

## Project Structure

The project follows a flat modular structure:

**app/**  
Contains all calculator logic including:

- calculator REPL interface
- calculation models
- operation strategies
- configuration management
- memento implementation
- observers for logging and auto-save
- validation utilities
- custom exceptions

**tests/**  
Contains unit and parameterized tests for all major components.

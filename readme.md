# Midterm Calculator Project

## Overview

This project is a command-line calculator application developed in Python.  
The calculator supports multiple arithmetic operations and demonstrates the use of several software design patterns.  
The application is structured in a modular way and includes automated testing, coverage analysis, and continuous integration using GitHub Actions.

The calculator runs in an interactive REPL (Read-Eval-Print Loop) where users can enter commands to perform calculations and manage calculation history.

---

## Supported Operations

The calculator supports the following arithmetic operations:

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

Each operation is implemented as its own class and dynamically created using the Factory Pattern.

---

## Design Patterns Used

This project demonstrates the use of several software design patterns:

Factory Pattern  
Used to dynamically create arithmetic operations through the `OperationFactory` class.

Strategy Pattern  
Each arithmetic operation (Addition, Division, Root, etc.) is implemented as a separate strategy class.

Observer Pattern  
Observers monitor calculator events and automatically log operations and save history.

Memento Pattern  
Used to implement undo and redo functionality for calculations.

---

## Project Structure

The project is organized into two main directories:

app/  
Contains the main calculator application including:

- calculator logic
- REPL interface
- operation classes
- calculation model
- configuration handling
- observer implementation
- memento implementation
- validation utilities
- custom exception handling

tests/  
Contains unit tests for all major components of the application.

---

## Setup Instructions

1. Clone the repository
git clone <repository-url>
cd midterm_calculator


2. Create a virtual environment


python3 -m venv venv


3. Activate the virtual environment

Mac/Linux:


source venv/bin/activate


4. Install project dependencies


pip install -r requirements.txt


---

## Environment Configuration

Create a `.env` file in the root directory with the following values:


CALCULATOR_MAX_HISTORY_SIZE=100
CALCULATOR_AUTO_SAVE=true
CALCULATOR_DEFAULT_ENCODING=utf-8


These values control calculator configuration such as history size and automatic saving.

---

## Running the Calculator

Start the calculator using:


python3 main.py


This launches the interactive calculator REPL.

Example:


Calculator started. Type 'help' for commands.

Enter command: modulus
First number: 10
Second number: 3

Result: 1


---

## REPL Commands

General commands available in the calculator:

help  
Displays available commands.

history  
Displays calculation history.

clear  
Clears the stored calculation history.

undo  
Undoes the most recent calculation.

redo  
Redoes the last undone calculation.

save  
Saves calculation history to a file.

load  
Loads calculation history from a file.

exit  
Exits the calculator.

---

## Arithmetic Commands

The following commands perform calculations:

add  
subtract  
multiply  
divide  
power  
root  
modulus  
int_divide  
percent  
abs_diff  

Each command will prompt the user to enter two numbers.

---

## Testing

All functionality is validated through automated tests using pytest.

Run all tests:


pytest


Run tests with coverage reporting:


pytest --cov=app --cov-report=term-missing


The project currently includes over 100 automated tests and maintains over 90% code coverage.

---

## Continuous Integration

This project uses GitHub Actions for continuous integration.

The CI pipeline automatically:

- installs dependencies
- runs all tests using pytest
- checks code coverage
- validates the project on every push or pull request to the main branch

---

## Summary

This calculator demonstrates modular Python development using multiple design patterns, automated testing, and continuous integration.  
The application provides a flexible and extensible architecture where new operations can easily be added through the operation factory.

After pasting it into your repo, run:

git add readme.md
git commit -m "Finalize README for midterm"
git push

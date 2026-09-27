# Project Statement

## Problem Statement

Engineering students, developers, and analysts often need to work with numbers expressed in incompatible systems. From metric and imperial engineering units to digital storage capacities and international currencies, the range of units can be difficult to manage. Converting values may require searching reference tables or using multiple online calculators. These extra steps interrupt technical work and consume time.

The Multi-Unit Command-Line Converter addresses this problem with an easy-to-access utility that performs common unit conversions from the terminal. It aims to make conversions quick and straightforward while validating the input and preventing conversions between incompatible measurement categories.

## Objectives

- Design the program around a single Java conversion function that supports seven measurement categories, using scalar conversions for linear units and a separate algorithm for temperature.
- Build a natural-language parser that recognizes plurals, common abbreviations, and aliases such as `miles`, `bucks`, `kilos`, `km/h`, and `celsius`.
- Enforce category constraints and validate input values to prevent invalid operations, including incompatible unit conversions and division by zero.
- Provide both one-off command-line conversions and an interactive mode for repeated conversions.
- Use exception handling to report invalid or incomplete input and guide users toward the correct format.

## Scope of the Project

### Functional Scope

- **One-off and interactive modes:** Run a single conversion with command-line arguments or enter multiple conversions in a continuous interactive session.
- **Seven measurement categories:** Convert length, mass, time, speed, temperature, digital storage, and currency.
- **Natural unit parsing:** Recognize plurals, common abbreviations, and aliases, then normalize them to supported unit identifiers.
- **Category validation:** Check that source and target units belong to the same category before converting.
- **Linear and temperature conversions:** Use scale factors for linear units and dedicated affine transformations for Celsius, Fahrenheit, and Kelvin. Display general results to four decimal places and temperature results to two decimal places.
- **Input validation and error handling:** Handle missing arguments, unsupported unit names, non-numeric values, and other invalid input with clear guidance.
- **Help:** Provide an in-session unit list through `help` or `-l`.

### Non-Functional Scope

- **Performance:** Complete conversions promptly; the project target is under 100 milliseconds for typical use.
- **Portability:** Use standard Java so the program can run on platforms with a Java Virtual Machine.
- **No external dependencies:** Keep the application lightweight and self-contained.
- **Usability:** Provide concise commands, an interactive prompt, and accessible help text.

## Target Audience

- Engineering and computer science students who need to complete or check homework problems in a terminal.
- Developers and system administrators who want a lightweight alternative to web-based converters.
- Electronics and physics enthusiasts who want to experiment with unit conversions from the shell.


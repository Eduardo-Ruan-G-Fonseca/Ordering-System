# README - Registration and Binary File Manipulation System in C++

## Overview
This project consists of a C++ program developed to create and manipulate a registration system based on binary files, allowing sorting, deletion, insertion, and search of elements. The project was developed within the Information Systems discipline at the Federal University of Lavras (UFLA).

## Project Structure
The project consists of two main C++ files:
1. **ConverteDeCSVParaBinario.cpp**: Responsible for converting a CSV file into a binary file.
2. **TrabalhoConcluido.cpp**: Implements an interactive menu for binary file manipulation.

## Features
### 1. CSV to Binary Conversion
- Reads data from the `base9_OK.csv` file.
- Converts the data into a binary file `base9_binario.dat`.
- Adjusts the decimal format of floating-point values.
- Uses the `registro` structure, composed of:
  - `campo1`: long long int
  - `campo2`: character array (10)
  - `campo3`: character array (200)
  - `campo4`: float
  - `campo5`: float

### 2. Binary File Manipulation
The main program presents a menu with the following options:

#### **Option 1: Print File**
- Displays all stored records.
- Ignores records marked as deleted.

#### **Option 2: Sort File**
- Allows sorting records by `campo1` or `campo4`.
- Uses custom sorting functions.

#### **Option 3: Remove Record**
- Prompts the user for the position of the record to be removed.
- Marks the record as deleted by making `campo1` negative.

#### **Option 4: Insert New Record**
- Checks if there are deleted records available for reuse.
- If none are available, inserts a new record at the end of the file.

#### **Option 5: Search for an Element**
- Allows search by `campo1` or `campo4`.
- Displays the data of the found record.

#### **Option 6: Print Specific Section**
- Displays records within a user-defined range.
- Identifies and marks deleted records.

#### **Option 7: Export to CSV**
- Converts and exports the records from the binary file to a CSV file.

## Data Structure in the File
Records are stored in a fixed order:
1. `long long int`
2. `char[10]`
3. `char[200]`
4. `float`
5. `float`

## Challenges and Learnings
During development, we faced some challenges:
- The issue of spaces in `campo3`, which shifted values to `campo4`, causing an infinite loop.
- Initially, we attempted to manipulate data in primary memory instead of files, requiring a project rework.
- With the help of monitors, we corrected formatting and record manipulation issues.

## Conclusion
The project allowed us to develop skills in binary file manipulation and strategies for sorting, inserting, and removing records. As a result, we obtained a functional program capable of efficiently performing registration and data query operations.

## Authors
- Matheus de Paula Megale
- Eduardo Ruan Fonseca
- Lucas de Oliveira Pereira


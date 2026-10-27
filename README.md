# Library Management System with Shelf Visualization

A Windows-based console application built in C for managing a small library system. The program supports two user roles: librarian and student. It allows books to be issued and returned, tracks student records, and displays a shelf-style visualization of available books in the Science and Literature sections.

## Overview

This project is designed to simulate a simple library management workflow where:

- a librarian can manage book issue records and student activity
- a student can view book shelves, available books, issued books, and return books
- books are categorized into Science and Literature
- records are stored in local `.dat` files for persistence between runs

## Features

- Librarian mode
  - view students and the books issued to them
  - issue books to students
- Student mode
  - view bookshelf layouts
  - see available books
  - check books currently issued to that student
  - return books
- Book categories
  - Science
  - Literature
- Shelf visualization
  - visual ASCII-style shelf layout for books in each category
- Data persistence
  - uses binary data files such as `studentfile.dat`, `bookfilescience.dat`, and `bookfileliterature.dat`

## Project Structure

- `project.c` — main source code for the library system
- `LICENSE` — license details for the project
- `README.md` — project documentation

Runtime data files are created while the program runs, including:

- `studentfile.dat`
- `bookfilescience.dat`
- `bookfileliterature.dat`
- temporary files used during book return/issue operations

## Technologies Used

- C programming language
- Windows console APIs
- File handling with binary `.dat` files
- Console-based menu system

## Requirements

This project is built specifically for Windows-based development environments because it uses headers such as:

- `windows.h`
- `conio.h`
- `dos.h`
- `dir.h`

Recommended tools:

- Code::Blocks
- Dev-C++
- MinGW on Windows

## How to Run

1. Open the project in a Windows C compiler.
2. Compile `project.c`.
3. Run the generated executable.

Example with MinGW:

```bash
gcc project.c -o library_management_system.exe
library_management_system.exe
```

## Main Menu

When the program starts, it shows:

- Login as a librarian
- Login as a student
- Exit

From there, the user can navigate through the book issue/return and shelf management options.

## Notes

- This is a console application, so it is designed for terminal-based interaction rather than a graphical UI.
- The code is Windows-specific; it may not compile directly on Linux/macOS without compatibility changes.
- The bookshelf section uses a custom text-based shelf panel that marks books as available or already issued.

## License

This project is distributed under the license included in the repository (`LICENSE`).

## Summary

This project is a simple yet complete library management simulation that demonstrates data storage, user role management, issue/return functionality, and visual shelf representation in a single C program.

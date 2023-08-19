## Love Calculator App Documentation

This document provides an overview and explanation of the code for a Love Calculator app developed using the Tkinter library in Python. The Love Calculator app allows users to input two names and calculates a love percentage based on the occurrence of specific characters in the names. The app also features dynamic background color changes and the display of randomly positioned love symbols and texts.

### Table of Contents

1. **Introduction**
   - Purpose of the App
   - Prerequisites

2. **Code Overview**
   - Import Statements
   - Constants
   - Background Color Change
   - Drawing Symbols and Texts
   - Love Calculation
   - User Interface Setup
   - Main Event Loop

3. **Functions**
   - `change_background_color()`
   - `draw_symbols_and_texts()`
   - `calculate_love()`

4. **User Interface Elements**
   - Main Window
   - Canvas
   - Labels
   - Entry Fields
   - Calculate Button

### 1. Introduction

#### Purpose of the App
The Love Calculator app is designed to entertain users by calculating a "love percentage" based on the input names. It utilizes dynamic visual elements such as changing background colors and displaying randomly positioned symbols and texts associated with love.

#### Prerequisites
- Python interpreter with the Tkinter library installed.

### 2. Code Overview

#### Import Statements
The code begins by importing necessary modules:
- `tkinter`: The primary module for creating GUI applications.
- `messagebox`: A submodule of `tkinter` used to display message boxes.
- `random`: Used for generating random values.

#### Constants
- `BACKGROUND_COLORS`: A list of hexadecimal color codes used for the dynamic background color change.
- `LOVE_SYMBOLS`: A list of love-related symbols.
- `HEART_SYMBOLS`: A list of heart-related symbols.
- `LOVE_TEXTS`: A list of love-related text phrases.

#### Background Color Change
- The `change_background_color()` function selects a random color from `BACKGROUND_COLORS` and sets it as the background color of the canvas using the `configure()` method.
- The function uses the `after()` method to schedule itself to run every 3000 milliseconds (3 seconds).

#### Drawing Symbols and Texts
- The `draw_symbols_and_texts()` function clears the canvas and generates 10 random positions for displaying symbols and texts.
- Random symbols and texts are chosen from the predefined lists (`LOVE_SYMBOLS`, `HEART_SYMBOLS`, `LOVE_TEXTS`).
- The `create_text()` method is used to display these elements on the canvas.
- Similar to the background color change, this function is scheduled to run every 3 seconds using the `after()` method.

#### Love Calculation
- The `calculate_love()` function reads the names entered by the user in the entry fields.
- It removes spaces and converts names to lowercase for consistency.
- The function calculates a love score by counting the occurrences of characters from the string "truelove" in both names.
- The love percentage is calculated by dividing the love score by the total number of characters and multiplying by 100.
- A message box is displayed showing the calculated love percentage.

#### User Interface Setup
- The main window is created using the `Tk()` constructor from the `tkinter` module.
- The window title, size, and resize options are configured.
- A canvas widget is created for displaying dynamic content.

#### Main Event Loop
- The `window.mainloop()` call starts the main event loop, which handles user interactions and keeps the GUI responsive.

### 3. Functions

#### `change_background_color()`
- Changes the background color of the canvas to a random color from `BACKGROUND_COLORS`.
- Schedules itself to run every 3 seconds using the `after()` method.

#### `draw_symbols_and_texts()`
- Clears the canvas and draws randomly positioned symbols and texts associated with love.
- Schedules itself to run every 3 seconds using the `after()` method.

#### `calculate_love()`
- Reads names from the entry fields, removes spaces, and converts to lowercase.
- Calculates a love score based on character occurrences in the names.
- Calculates the love percentage and displays it in a message box.

### 4. User Interface Elements

- The main window contains labels, entry fields, and a button for user interactions.
- The canvas is used for displaying dynamic content, including changing background colors and randomly positioned symbols and texts.

---

This documentation provides an overview of the Love Calculator app's functionality, code structure, and user interface elements. By understanding this documentation, developers can gain insight into how the app is designed and implemented using the Tkinter library in Python.

## Part 1. Main Document.

### 1. Title and Basic Information.

• **Title:** Calculator v.3

• **Purpose:** Project No. 8. Product.

• **Project Phase:** Phase I.

• **Technology Stack:** Python

• **Project Status:** The third version is fully completed.

### 2. Brief Project Description.

• The Calculator v.3 project is a multifunctional desktop application written in Python with a graphical user interface, designed to perform a wide range of mathematical operations.

• The program combines the features of a basic, engineering, and scientific calculator, providing tools for arithmetic calculations, prime number operations, equation solving, trigonometric transformations, graph plotting, and other mathematical tasks in a convenient and modern interface with calculation history support.

• Unlike the second version, Calculator v.3 includes a полноценную settings system with the ability to switch the interface language (Russian/English) and theme (dark/light), with automatic saving of parameters between launches.

### 3. Clear Project Goals.

• Demonstrate the growth of NS in the project field.

• Create convenience and multifunctionality for the user.

• Expand the NS project showcase.

### 4. Project Components (Functions).

• **What is already implemented:**

**4.1** Addition (a + b)

**4.2** Subtraction (a – b)

**4.3** Multiplication (a × b)

**4.4** Division (a : b)

**4.5** GCD Search (Euclidean Algorithm)

**4.6** LCM Search (Based on GCD)

**4.7** Factorial (a! = 1 × 2 × 3 × ... × a)

**4.8** Double Factorial (If a is even: a!! = 2 × 4 × 6 × ... × a) (If a is odd: a!! = 1 × 3 × 5 × ... × a)

**4.9** Prime Factorization (a = p₁ × p₂ × ...)

**4.10** Exponentiation (a^b = a × a × ... × a)

**4.11** Prime Number Check (If number a has only 1 and a as divisors, it is prime; otherwise, it is composite)

**4.12** Logarithms (logₐ(b))

**4.13** Square Root (√a = a^0.5)

**4.14** Solving First-Degree Equations (ax + b = 0)

**4.15** Solving Second-Degree Equations (ax² + bx + c = 0)

**4.16** Trigonometric Functions (cos, sin, tg, ctg)

**4.17** Converting Degrees to Radians and Vice Versa (a° = b (rad))

**4.18** Absolute Value, Integer Part, Fractional Part of a Number (|a|, [a], {a})

**4.19** Graph Plotting (Line, parabola, hyperbola, sine wave, cosine wave, tangent wave, cotangent wave, circle, X modulus, Y modulus, X and Y moduli, heart)

**4.20** Support for Two Interface Languages (Русский / English)

**4.21** Theme Switching (Dark / Light)

**4.22** Automatic Saving and Loading of Settings (language and theme) into the settings.json file

• **What may appear in the future:**

**4.23** Solving n-degree equations

**4.24** Parameter solving

**4.25** Solving trigonometric equations

**4.26** Representing irrational numbers as fractions (if possible)

**4.27** Derivatives and integrals (fundamentals of mathematical analysis)

### 5. Instructions for Use.

• Before using the application, it is important to understand how it works. First, familiarize yourself with the functions located on the left panel of the screen. When hovering the cursor over a button, the formula of the selected operation appears.

• After selecting a function, click on it and move to the right panel, where input fields will appear for entering numbers to perform the chosen operation.

• To make it clearer what each entered variable represents, there is a hint directly below the input fields in the form of a formula using the same variables provided by the user.

• After entering the values, perform the calculation by pressing the button below. After receiving the result, you can select a new function or clear the current calculations using the buttons on the bottom panel.

• If the selected operation is graph plotting, pressing the button below will open a window with the required graph, while the program itself will output the number 0 as the answer.

• To change the language or theme, click the "Settings" button in the upper-right corner. The selected parameters will be automatically saved and restored during the next launch.

• All calculations are saved in history, which is available in the upper-right corner. The history can be copied or cleared.

## Part 2. Technical Document.

### 1. Development Goals.

• Create a convenient program that helps users solve various mathematical problems.

• Build a calculator with a large set of functions ranging from simple addition to graph plotting.

• Add visualization of mathematical functions to make them more intuitive and understandable.

• Create a beautiful and user-friendly interface in dark tones that is pleasant to use.

• Divide all functions into categories so users can quickly find the required operation.

• Save calculation history so users can return to previous calculations.

• Add support for Russian and English languages.

• Add the ability to switch themes (dark/light).

### 2. Technologies Used.

• **Programming Languages:** Python

• **Libraries:** tkinter, math, json, os, typing, numpy, matplotlib

### 3. Project Architecture.

• The project uses the **Model-View-Controller (MVC)** approach within a single main Calculator class.

• **Model** – mathematical functions such as addition, GCD search, and equation solving. They are implemented as class methods.

• **View** – the entire graphical interface: buttons, input fields, and panels created using tkinter.

• **Controller** – the logic connecting the interface and calculations. It processes button clicks, data input, and result display.

### 4. Project Structure.

• One main file, calculator.py, contains the entire program code.

• The calc_history.json file is automatically created and stores the calculation history.

• The settings.json file is automatically created and stores language and theme settings.

• The program contains one main class and more than 60 methods (functions) for various tasks.

• Each mathematical operation is implemented as a separate method, making the code understandable and easy to modify.

### 5. Key System Components.

• The interface manager creates all buttons, input fields, and panels visible to the user.

• The input system processes user input and can understand fractions and the number pi.

• The mathematical operations block contains more than 30 functions, from addition to equation solving.

• The graph module renders functions in a separate window with coordinate axes and labels.

• The history system stores recent calculations and displays them in a dedicated window.

• The settings module saves and loads language and theme parameters from the settings.json file.

### 6. User Interface Implementation.

• The interface is designed in a dark color scheme with purple and turquoise accents, with a light theme also available.

• The left panel with buttons is divided into colored categories for convenient navigation.

• The right panel changes depending on the selected operation, displaying the necessary input fields.

• When hovering over a button, it changes color and displays the formula of the selected operation.

• Hotkeys are supported: Escape for reset, Ctrl+C for copying the result.

• The program window automatically opens centered on the screen during launch.

### 7. Development Process.

• Initially, it was decided to use Calculator v.2 as the foundation.

• translations and themes dictionaries were added to store localized strings and color schemes.

• The refresh_ui method was implemented to completely rebuild the interface when settings are changed.

• change_language and change_theme methods were written to update variables and call refresh_ui.

• Settings saving into settings.json upon modification and loading during startup were implemented.

• A formula tooltip system for all operations was added.

• Bugs were fixed.

### 8. Main Challenges and Their Solutions.

• **(1) Challenge:** How to completely refresh the interface when changing the language or theme.

Solution: The refresh_ui method destroys all widgets and recreates the interface with the new settings.

### 9. Current Project Limitations.

• It is impossible to calculate factorials of numbers greater than 100 to prevent the program from freezing.

• Graphs cannot be zoomed in, zoomed out, or moved with the mouse.

• The calculator cannot work with complex numbers, except for displaying equation roots.

• The history stores only the last 50 entries, and searching or filtering is not available.

• When an input error occurs, only a message is displayed, while the incorrect field is not highlighted.

• It is impossible to enter a complete expression consisting of multiple operations — only individual numbers for the selected action.

• When changing the language or theme, the current operation and entered data are reset.

### 10. Possible Improvements and Future Development Plans.

• Split the code into multiple modules for easier maintenance.

• Add more advanced mathematical functions.

• Improve the history system: add date and time, export to various formats, and search functionality.

• Add support for additional interface languages.

• Use multithreading so heavy calculations do not block the interface.

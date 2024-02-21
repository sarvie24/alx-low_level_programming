C - Makefiles
In this assignment, I practiced crafting Makefiles.

Tests :heavy_check_mark:
tests: Collection of test files.
Helper Files :raised_hands:
school.c: C function demonstrating a text representation of a seahorse, utilized for Makefile exercises throughout the project.

main.c: Primary C function executing the function defined in school.c.

Header File :file_folder:
m.h: Header file containing the function prototype used in school.c.
Tasks :page_with_curl:
0. make -f 0-Makefile

0-Makefile: Makefile generating an executable named school based on school.c and main.c. Includes:
Rule all for building the executable.
1. make -f 1-Makefile

1-Makefile: Makefile producing an executable named school from school.c and main.c. Extends 0-Makefile with:
Definition of variable CC specifying the compiler.
Definition of variable SRC identifying the .c files for compilation.
Modification of the all rule to only recompile updated source files.
2. make -f 2-Makefile

2-Makefile: Makefile generating an executable named school based on school.c and main.c. Expands upon 1-Makefile with:
Declaration of variable OBJ indicating the .o files to compile.
Declaration of variable NAME specifying the executable's name.
3. make -f 3-Makefile

3-Makefile: Makefile creating an executable named school from school.c and main.c. Further builds upon 2-Makefile by including:
Rule clean for removing Emacs/Vim temporary files and the executable.
Rule oclean for deleting object files.
Rule fclean for erasing all temporary files, the executable, and object files.
Rule re to enforce recompilation of all source files.
Definition of variable RM specifying the file deletion command.
4. A complete Makefile

4-Makefile: Makefile constructing an executable named school based on school.c and main.c. Enhances 3-Makefile with:
Definition of variable CFLAGS setting compiler flags to -Wall -Werror -Wextra -pedantic.
5. Island Perimeter

5-island_perimeter.py: Python function returning the perimeter of an island specified within a grid.
Prototype: def island_perimeter(grid):
The parameter grid is a list of lists of integers.
0 represents water.
1 represents land.
Each element of the lists represents a cell square with a side length of 1.
Grid cells are connected horizontally/vertically (not diagonally).
The grid is rectangular, with a width and height not exceeding 100.
The grid is entirely encircled by water, containing either exactly one island or none.
The island does not contain lakes (water isolated from surrounding land).
6. make -f 100-Makefile

100-Makefile: Makefile producing an executable named school based on school.c and main.c. Extends 4-Makefile with:
Exclusion of the RM variable definition.
Omission of the $(CFLAGS) string.
Compilation halt if the header m.h is absent.
Ability to function even when files with the same name as any Makefile rules exist in the current directory.

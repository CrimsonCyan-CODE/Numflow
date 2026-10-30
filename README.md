# Numflow

**Numflow** is an esoteric programming language created in 2026. It uses a coordinate-based, mode-driven architecture where execution is controlled by exact line counts, mathematical operators, and statement counters. Source files use the `.nf` extension.

The language treats variables as mathematical concepts—using the imaginary unit `i` to declare a variable's existence before assigning it a real value.

## Syntax

### Structure
A Numflow program must start and end with specific line-count declarations:
*   **Start:** `(0,0)+N` where `N` is the total number of lines in the program.
*   **End:** `N/0=` which intentionally divides the line count by zero to terminate the script.

### Modes
Execution is divided into "modes" which dictate how the interpreter handles the code inside them. You enter a mode using `5--[mode]`. 
*   `000`: No mode (default/exit)
*   `001`: Print (supports string interpolation with `{variable}`)
*   `002`: Variables
*   `003`: File editing (append)
*   `004`: File creation
*   `005`: File deletion
*   `006`: Math
*   `007`: Conditions (`007=condition`, `007=%^` for else-if, `007=%` for else)
*   `008`: Key input (pauses until keypress, stores hex/ASCII value)
*   `009`: Loops (`009=count`)

### Statement Blocks
Code is wrapped in numbered blocks that identify the mode they belong to.
```text
+1&002:
=x&i
x=10
1&002*

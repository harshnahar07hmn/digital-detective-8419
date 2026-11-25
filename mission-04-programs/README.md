# Mission 4 - How programs run

## 1. Task / objective
The objective of this mission was to write and execute a simple Python program (`hello.py`) from the Terminal and compare how compilers and interpreters translate and run source code.

## 2. Work completed

### Task 4.1 - Create and run a Python program
* Created `hello.py` inside `mission-04-programs/` containing the statement `print("Hello from Python")`.
* Executed the script in Terminal using `python3 hello.py` and confirmed that `Hello from Python` printed to the screen.

### Task 4.2 - Compare compiler and interpreter
| Point | Compiler | Interpreter |
| :--- | :--- | :--- |
| When translation / execution happens | Translates the entire source code into machine code before the program starts running. | Translates and executes the program line-by-line (or via bytecode) at runtime while the program is running. |
| Typical output | Produces a standalone executable binary or machine-code file (e.g., `.exe` or macOS Mach-O binary). | Does not produce a separate standalone machine-code file; directly outputs the program's execution results. |
| One example | C, C++, or Rust (`gcc` / `clang`). | Python or JavaScript (`python3` / Node.js). |
| One advantage | Faster execution speed once compiled because the CPU runs native machine code directly without re-translating. | Easier debugging and cross-platform portability since code runs immediately without a separate build step. |

**Summary Comparison:**
A compiler reads and translates the entire program into machine code beforehand, generating an executable file that runs very fast directly on the hardware. In contrast, an interpreter reads and executes code incrementally at runtime, which makes testing and fixing errors much quicker because you can run changes immediately without waiting for a full build. While compiled languages like C++ prioritize raw execution speed, interpreted languages like Python prioritize developer flexibility and portability across operating systems.

## 3. Commands / tools used
* `cd`: Navigated into the `mission-04-programs` directory.
* `echo` / **VS Code**: Created and verified the `hello.py` source file.
* `python3 hello.py`: Invoked the Python 3 interpreter to execute `hello.py` and print its output to the Terminal.
* `git add`, `git commit`, `git push`: Staged, committed, and published Mission 4 files to GitHub.

## 4. My understanding
I understood that human-readable source code cannot be executed directly by a CPU and must first be translated into low-level instructions. Seeing `python3 hello.py` run immediately without generating a separate binary file demonstrated how an interpreter executes instructions directly at runtime.

## 5. Difficulties faced
No major difficulties.

## 6. How I resolved them
Not applicable.

## 7. Evidence / files
* `mission-04-programs/hello.py` (One-line Python script printing `"Hello from Python"`).
* `mission-04-programs/README.md` (Documentation, compiler vs. interpreter comparison table, and summary).

## 8. Commit details
* **Commit message:** `Compare compilers and interpreters`
* **Status:** Committed and pushed to GitHub (`main` branch).
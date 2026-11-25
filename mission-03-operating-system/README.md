# Mission 3 - Understand the operating system

## 1. Task / objective
The objective of this mission was to explore my computer's operating system environment, inspect running processes and Process IDs (PIDs), understand absolute versus relative file paths, examine file permissions, and summarize the core responsibilities of an operating system.

## 2. Work completed

### Task 3.1 - System Exploration
| Information explored | What it tells you | Your observation (privacy-safe) |
| :--- | :--- | :--- |
| Operating system / system details | Identifies the OS name, version, and hardware architecture. | macOS 27.2.1 (26B131) - arm64 |
| Current account identity | Shows the active user profile currently logged into the terminal session. | `[redacted]` |
| Available and used storage | Displays total disk capacity, space currently occupied, and free storage available. | Total: [460Gi], Used: [13Gi], Available: [273Gi] |
| System activity snapshot | Shows real-time CPU load, memory usage, and active system/user processes. | Observed active kernel tasks, terminal, and GUI apps consuming CPU/RAM. |

### Task 3.2 - Understanding Processes
* **What is a process?** A process is an active instance of a program currently loaded into memory and being executed by the CPU.
* **What does the PID column represent?** PID stands for Process Identifier—a unique numerical ID assigned by the operating system kernel to track and manage each running process.
* **Two examples of running processes:**
  1. `Visual Studio Code` (PID: `71910`) – User application process for editing code.
  2. `WindowServer` (PID: `608`) – Background macOS system process managing the graphical interface.

### Task 3.3 - Paths and Permissions
- **Absolute path vs. Relative path:** An absolute path specifies the complete location of a file or folder starting from the root directory (`/`), regardless of where you currently are. A relative path specifies a location starting from your current working directory.
  - **Absolute path example:** `/Users/[redacted]/digital-detective-8419/mission-03-operating-system`
  - **Relative path example:** `./README.md` (or `../mission-02-terminal`)
- **File Permissions Analysis (`ls -l README.md`):**
  - Output observed: `-rw-r--r--`
  - Owner permission letters: `rw-`
  - **Meaning:** The owner can **read (`r`)** and **write/modify (`w`)** the file, but cannot **execute (`x`)** it as a program.

| Permission | Meaning | Example |
| :--- | :--- | :--- |
| `r` - Read | Allows a file's contents to be viewed or copied. | Opening and reading `README.md`. |
| `w` - Write | Allows a file's contents to be modified or deleted. | Saving edits to `README.md` in VS Code. |
| `x` - Execute | Allows a file to be run as a program/script, or allows entering a directory. | Running a Python or shell script. |

### Task 3.4 - Operating System Responsibilities
| OS responsibility | Your explanation | Example |
| :--- | :--- | :--- |
| Process management | Creates, schedules, pauses, and terminates running programs so they share CPU time efficiently. | Running VS Code, Terminal, and a web browser simultaneously without freezing. |
| Memory management | Allocates RAM to active processes and frees it when programs close so apps do not overwrite each other's data. | Assigning dedicated memory blocks to browser tabs and Python scripts. |
| Device management | Communicates with and controls hardware peripherals using device drivers. | Translating keystrokes from the keyboard or rendering graphics on the display. |
| File management | Organizes data into files and directories on storage drives and tracks where data is physically stored. | Creating, renaming, and saving folders inside the `digital-detective-8419` repository. |
| User interface / shell | Provides a way for users to interact with the OS either visually or via text commands. | Typing commands into the macOS Terminal shell (`zsh`) or clicking icons on the desktop. |
| Security and permissions | Protects system files and user data by verifying user identities and enforcing read/write/execute rules. | Requiring a password for system changes and restricting file write access to the file owner. |

## 3. Commands / tools used
- `sw_vers` and `uname -m`: Displayed macOS version, build number, and Apple Silicon (`arm64`) architecture.
- `whoami`: Checked the currently logged-in user account name (redacted for privacy).
- `df -h /`: Displayed total, used, and available disk storage in human-readable units (`Gi`).
- `top -l 1` and `ps aux`: Listed active system processes, CPU/memory usage, and Process IDs (PIDs).
- `cd` and `pwd`: Navigated between directories and printed the current absolute path.
- `ls -l`: Listed detailed file metadata including owner, group, and read/write/execute (`rw-`) permissions.
- **VS Code**: Used to structure and edit the Mission 3 Markdown documentation.

## 4. My understanding
I understood that the operating system acts as the core manager between hardware and user applications. Every open program runs as an isolated process with a unique PID, and the OS uses file permissions (`rwx`) and directory paths to keep files organized and secure from unauthorized modification.

## 5. Difficulties faced
No major difficulties.

## 6. How I resolved them
Not applicable.

## 7. Evidence / files
- `mission-03-operating-system/README.md` (Complete documentation, tables, and redacted command observations).

## 8. Commit details
- **Commit message:** `Document operating system and file management`
- **Status:** Committed and pushed to GitHub (`main` branch).
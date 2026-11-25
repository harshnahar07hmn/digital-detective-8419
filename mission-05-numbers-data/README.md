# Mission 5 - Numbers and data

## 1. Task / objective
The objective of this mission was to manually convert values across decimal, binary, and hexadecimal number systems, verify those calculations using Python's interactive shell, build a working Python number-converter script (`number_converter.py`), and explain how computers encode text using ASCII and UTF-8.

## 2. Work completed

### Task 5.1 - Convert numbers by hand
| Question | Your working and answer |
| :--- | :--- |
| Convert decimal 13 to binary. | $13 \div 2 = 6$ R **1**; $6 \div 2 = 3$ R **0**; $3 \div 2 = 1$ R **1**; $1 \div 2 = 0$ R **1**. Reading remainders bottom-to-top: **`1101`** |
| Convert decimal 25 to binary. | $25 \div 2 = 12$ R **1**; $12 \div 2 = 6$ R **0**; $6 \div 2 = 3$ R **0**; $3 \div 2 = 1$ R **1**; $1 \div 2 = 0$ R **1**. Reading remainders bottom-to-top: **`11001`** |
| Convert binary 1010 to decimal. | $(1 \times 2^3) + (0 \times 2^2) + (1 \times 2^1) + (0 \times 2^0) = 8 + 0 + 2 + 0 =$ **`10`** |
| Convert binary 1101 to decimal. | $(1 \times 2^3) + (1 \times 2^2) + (0 \times 2^1) + (1 \times 2^0) = 8 + 4 + 0 + 1 =$ **`13`** |
| Convert hexadecimal A to decimal. | In base 16, $A$ represents $10 \times 16^0 =$ **`10`** |
| Convert hexadecimal 1F to decimal. | $(1 \times 16^1) + (15 \times 16^0) = 16 + 15 =$ **`31`** |
| Convert binary 1111 to hexadecimal. | $(1 \times 2^3) + (1 \times 2^2) + (1 \times 2^1) + (1 \times 2^0) = 8 + 4 + 2 + 1 = 15$, which is **`F`** in hexadecimal |

### Task 5.2 - Verify using Python
| Conversion Checked | Python Expression Tested | Result Returned | Matches Manual Calculation? |
| :--- | :--- | :--- | :--- |
| Decimal 13 to binary | `bin(13)` | `'0b1101'` | Yes (`1101`) |
| Decimal 25 to binary | `bin(25)` | `'0b11001'` | Yes (`11001`) |
| Binary 1010 to decimal | `int("1010", 2)` | `10` | Yes (`10`) |
| Binary 1101 to decimal | `int("1101", 2)` | `13` | Yes (`13`) |
| Hexadecimal A to decimal | `int("A", 16)` | `10` | Yes (`10`) |
| Hexadecimal 1F to decimal | `int("1F", 16)` | `31` | Yes (`31`) |
| Decimal 15 to hexadecimal | `hex(15)` | `'0xf'` | Yes (`F`) |

### Task 5.3 - Build a small number converter
Created `number_converter.py` using `input()`, `int()`, `bin()`, and `hex()`, and tested it with three positive numbers:

| Test number | Binary output | Hexadecimal output |
| :--- | :--- | :--- |
| `13` | `0b1101` | `0xd` |
| `42` | `0b101010` | `0x2a` |
| `255` | `0b11111111` | `0xff` |

- **How `bin()` and `hex()` work:** Python's `bin()` function takes an integer and returns its binary string representation prefixed with `0b` (indicating base 2). Similarly, `hex()` takes an integer and returns its hexadecimal string representation prefixed with `0x` (indicating base 16).

### Task 5.4 - How is text stored?
- **ASCII decimal codes:** Uppercase `'A'` is **`65`** and lowercase `'a'` is **`97`**.
- **Why an encoding standard is needed:** Computers can only store and process binary numbers (`0`s and `1`s), so a character-encoding standard is required to map every letter, digit, and symbol to a consistent numerical code that all systems interpret the same way.
- **Non-ASCII character example:** The Indian Rupee symbol **`₹`** (or Hindi Devanagari character **`अ`**), which requires UTF-8 encoding rather than basic 7-bit ASCII.

## 3. Commands / tools used
- `cd`: Navigated into `mission-05-numbers-data`.
- `python3`: Used the Python 3 interactive shell and script runner to verify conversions and execute `number_converter.py`.
- `input()`, `int()`, `bin()`, `hex()`: Built-in Python functions used to read user input, convert strings to integers, and format base-2 and base-16 representations.
- **VS Code**: Used to write `number_converter.py` and format `README.md`.
- `git add`, `git commit`, `git push`: Staged, committed, and pushed Mission 5 files to GitHub.

## 4. My understanding
I understood how computers represent all numbers and text internally using binary bits (`0` and `1`), while hexadecimal provides a compact human-readable shorthand for long binary strings. I also saw how Python handles base conversions natively and why UTF-8 is essential for representing global characters beyond basic English ASCII.

## 5. Difficulties faced
When first running `number_converter.py`, passing the raw output of `input()` directly into `bin()` caused a `TypeError` because `input()` returns a string rather than an integer. Additionally, the `0b` and `0x` prefixes returned by Python initially looked different from my manual answers.

## 6. How I resolved them
I wrapped `input()` inside `int()` to convert the user's string input into an integer before passing it to `bin()` and `hex()`, and verified that `0b` and `0x` are standard Python base indicators rather than extra digits.

## 7. Evidence / files
- `mission-05-numbers-data/number_converter.py` (Working Python CLI number converter).
- `mission-05-numbers-data/README.md` (Manual step-by-step workings, Python verification table, test results, and encoding notes).

## 8. Commit details
* **Commit message:** `Build number converter and practise data representation`
* **Status:** Committed and pushed to GitHub (`main` branch).
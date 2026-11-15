# Mission 5 — Number Systems and Data Representation

## 1. Task / objective

Practise decimal, binary, and hexadecimal conversions.
Verify calculations using Python, create a decimal number converter,
and understand how character encoding represents text.

## 2. Work completed

### Task 5.1 — Manual Number Conversions

A number's base determines its available digits and place values.

- Decimal uses base 10 and digits 0–9.
- Binary uses base 2 and digits 0–1.
- Hexadecimal uses base 16 and digits 0–9 and A–F.
- In hexadecimal, A=10, B=11, C=12, D=13, E=14, and F=15.

| Question | Working | Answer |
|----------|---------|--------|
| Convert decimal 13 to binary. | Binary place values are 8, 4, 2, 1. Since 13 = 8 + 4 + 1, the digits are 1, 1, 0, 1. | 1101₂ |
| Convert decimal 25 to binary. | Binary place values are 16, 8, 4, 2, 1. Since 25 = 16 + 8 + 1, the digits are 1, 1, 0, 0, 1. | 11001₂ |
| Convert binary 1010 to decimal. | (1 × 8) + (0 × 4) + (1 × 2) + (0 × 1) = 10. | 10₁₀ |
| Convert binary 1101 to decimal. | (1 × 8) + (1 × 4) + (0 × 2) + (1 × 1) = 13. | 13₁₀ |
| Convert hexadecimal A to decimal. | The hexadecimal digit A represents ten. | 10₁₀ |
| Convert hexadecimal 1F to decimal. | (1 × 16) + (15 × 1) = 31. | 31₁₀ |
| Convert binary 1111 to hexadecimal. | (1 × 8) + (1 × 4) + (1 × 2) + (1 × 1) = 15. Hexadecimal represents 15 as F. | F₁₆ |

### Task 5.2 — Verify Using Python

python3

| Conversion | Python expression | Expected result | Matches the calculation? |
|------------|-------------------|-----------------|--------------------------|
| Decimal 13 to binary | `bin(13)` | `'0b1101'` | Yes |
| Decimal 25 to binary | `bin(25)` | `'0b11001'` | Yes |
| Binary 1010 to decimal | `int("1010", 2)` | `10` | Yes |
| Binary 1101 to decimal | `int("1101", 2)` | `13` | Yes |
| Hexadecimal A to decimal | `int("A", 16)` | `10` | Yes |
| Hexadecimal 1F to decimal | `int("1F", 16)` | `31` | Yes |
| Decimal 31 to hexadecimal | `hex(31)` | `'0x1f'` | Yes |
| Binary 1111 to hexadecimal | `hex(int("1111", 2))` | `'0xf'` | Yes |

**What the functions mean**

- `bin(number)` returns a string representing an integer in binary.
- `hex(number)` returns a string representing an integer in hexadecimal.
- `int(text, base)` interprets the text using the specified base
  and returns an integer.
- `0b` identifies a binary representation.
- `0x` identifies a hexadecimal representation.
- Lowercase hexadecimal letters have the same values as uppercase letters.

exit()


### Task 5.3 — Build a Small Number Converter

**Program:** `number_converter.py`

decimal_number = int(input("Enter a decimal whole number: "))

print("Binary:", bin(decimal_number))
print("Hexadecimal:", hex(decimal_number))

**How the converter works**

1. `input()` displays a prompt and receives the user's entry as text.
2. `int()` converts that text into an integer, using decimal by default.
3. The variable `decimal_number` stores the integer.
4. `bin()` creates its binary representation.
5. `hex()` creates its hexadecimal representation.
6. `print()` displays the results.

The program expects a valid integer. Input such as `hello` or `3.5`
cannot be converted by this use of int() and produces a ValueError.

**Run from the assignment repository's root*

python3 mission-05-numbers-data/number_converter.py

**Three test cases**

| Test number | Expected binary output | Expected hexadecimal output |
|---|---|---|
| 13 | 0b1101 | 0xd |
| 25 | 0b11001 | 0x19 |
| 31 | 0b11111 | 0x1f |

**Example interaction 

Enter a decimal whole number: 13
Binary: 0b1101
Hexadecimal: 0xd

### Task 5.4 — How Is Text Stored?

**What is the ASCII decimal code for uppercase A?**

Uppercase `A` has ASCII decimal code 65.

**What is the ASCII decimal code for lowercase a?**

Lowercase `a` has ASCII decimal code 97.

**Why does a computer need an encoding standard to store text?**

Computers store data as bits. A character-encoding standard defines
how characters are represented by numbers and bytes so that software
can store, transmit, and interpret text consistently.

**Give one character outside basic ASCII.**

The Gujarati character `અ` is outside basic ASCII.

**What is the difference between ASCII and UTF-8?**

Basic ASCII defines 128 character codes, including English letters,
digits, punctuation, and control characters.

UTF-8 encodes Unicode characters using one to four bytes.
It supports text from many writing systems and emoji.
ASCII characters retain their familiar one-byte values in UTF-8.

## 3. Commands / tools used

- Visual Studio Code: Edits the README and Python program.
- Terminal and zsh: Launch Python and the converter.
- `python3`: Starts the interactive environment or executes a script.
- `input()`: Receives text entered by the user.
- `int()`: Converts text to an integer, optionally using a specified base.
- `bin()`: Produces an integer's binary representation as text.
- `hex()`: Produces an integer's hexadecimal representation as text.
- `print()`: Displays output.
- `exit()`: Leaves the interactive Python environment.

## 4. My understanding

Decimal, binary, and hexadecimal are different representations
of the same integer values. Their place values use powers of
10, 2, and 16 respectively.

For example, decimal 13, binary 1101, and hexadecimal D represent
the same quantity.

Python's bin() and hex() functions return formatted strings;
they do not change the underlying integer into a different quantity.
The prefixes identify the representation.


## 5. Difficulties faced

Concepts requiring attention include reading binary place values
from right to left, interpreting hexadecimal letters, and recognising
the prefixes in Python's conversion results.

## 6. How I resolved them

The manual calculations show each digit's place value.
Hexadecimal letters are interpreted using A=10 through F=15.
The Python examples distinguish the 0b and 0x prefixes from the
digits representing the value.


## 7. Evidence / files

- README.md: Contains manual calculations, Python verification
  expressions, expected test results, and encoding explanations.
- number_converter.py: Required companion program for converting
  a decimal integer to binary and hexadecimal.

## 8. Commit details

 commit:
 push:

Mission status: 
# Mission 4 — How Programs Run

## 1. Task
Create and run a simple Python program. Compare compilers and
interpreters, including when they translate or execute instructions,
their typical output, examples, and advantages.

## 2. Work completed

### Task 4.1 — Create and Run a Python Program

**Program filename:** `hello.py`

**Program code:**

print("Hello from Python")

**How the program works**

`print()` is a Python function that displays information.
The quotation marks identify a string, which is a piece of text.
The parentheses contain the value passed to the function.

When executed successfully, this program displays the message
and then ends.

**Command to run from the assignment repository's root:**

python3 mission-04-programs/hello.py

`python3` starts Python 3. The path after it identifies the program
Python should execute.

** output 
Hello from Python

This output demonstrates the intended result. A successful run on
my computer has not been verified in this document.

### Task 4.2 — Compare Compiler and Interpreter

| Point | Compiler | Interpreter |
|-------|----------|-------------|
| When translation / execution happens | Translates source code into another representation before that representation is executed. | Executes program instructions at runtime, often using an intermediate representation. |
| Typical output | Produces translated code, such as object code, machine code, or bytecode. | Produces the program's runtime results, such as displayed text or saved data, without necessarily producing a separate executable. |
| One example | Clang compiling a C program into native code. | CPython executing Python bytecode. |
| One advantage | Compiling to native code can provide fast execution. | Can support convenient interactive execution and quick testing during development. |

**Explanation**

A compiler translates source code into another form before the
translated result is executed. An interpreter carries out program
instructions at runtime. Compiling to native code can provide fast
execution, while interpreted environments can make interactive testing
convenient. Real implementations can combine both approaches: CPython
normally compiles Python source into bytecode and then executes that
bytecode using its interpreter.

## 3. Commands / tools used

The tools and command required for this activity are:

- Visual Studio Code: Creates and edits README.md and hello.py.
- Python 3: Executes the Python program.
- Terminal: Provides the interface for entering the execution command.
- zsh: Interprets the shell command and launches Python.

The required execution command is:

python3 mission-04-programs/hello.py

## 4. My understanding

Source code is the text written in a programming language.
The hello.py file contains Python source code, while the command
entered in Terminal tells the shell to launch Python with that file.

The shell and Python have different roles. The shell handles the
command used to start the program. Python handles the instructions
inside hello.py.

Compilers and interpreters are tools or implementation techniques;
a language does not have to use only one approach. CPython combines
compilation to bytecode with interpretation of that bytecode.

## 5. Difficulties faced

No actual execution errors have been recorded.

## 6. How I resolved them

- The shell command starts Python and supplies the program's path.
- The Python statement calls print() to display the message.

## 7. Evidence / files

- README.md: Contains the program explanation, expected output,
  compiler/interpreter comparison, and mission notes.


## 8. Commit details

commit :
Commit and push status:
Mission status: 
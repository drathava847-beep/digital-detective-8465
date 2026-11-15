# Mission 2 — Become Comfortable with the Terminal

## 1. Task 
use the command-line interface  to inspect folders, create and manage practical files, understand options and pipes, and explain package managers.

## 2. Work completed

### Task 2.1 — Basic Terminal Operations

All file-management practice is performed inside my assignment repository.

| Operation | Command | What it does | My observation |
|-----------|---------|--------------|----------------|
| Display current location | `pwd` | Prints the full path of the current directory. | documents/digital-detective-8465 |
| List directory contents | `ls` | Lists visible files and directories. | evidence			mission-01-computer-basics	mission-03-operating-system	mission-05-numbers-data		mission-07-networking		README.md
mission-00-setup		mission-02-terminal		mission-04-programs		mission-06-git-github		mission-08-final-report |
| Display a detailed listing | `ls -l` | Shows permissions, ownership, size, and modification time. | total 8
drwxr-xr-x  2   staff    64 14 Nov 10:08 evidence
drwxr-xr-x  3   staff    96 14 Nov 10:21 mission-00-setup
drwxr-xr-x  3   staff    96 14 Nov 10:21 mission-01-computer-basics
drwxr-xr-x  3   staff    96 14 Nov 10:23 mission-02-terminal
drwxr-xr-x  3   staff    96 14 Nov 10:23 mission-03-operating-system
drwxr-xr-x  3   staff    96 14 Nov 10:24 mission-04-programs
drwxr-xr-x  4   staff   128 14 Nov 10:28 mission-05-numbers-data
drwxr-xr-x  3   staff    96 14 Nov 10:27 mission-06-git-github
drwxr-xr-x  3   staff    96 14 Nov 10:27 mission-07-networking
drwxr-xr-x  3   staff    96 14 Nov 10:28 mission-08-final-report
-rw-r--r--@ 1   staff  1762 14 Nov 12:06 README.md |
| Move to the parent directory | `cd ..` | Moves one directory level upward. | documents %|
| Return to the repository | `cd digital-detective-8465` | Enters the assignment directory again. | digital-detective-8465 % |
| Create a practice directory | `mkdir terminal-practice` | Creates a directory inside the repository. |digital-detective-8465 %   |
| Create an empty file | `touch terminal-practice/notes.txt` | Creates notes.txt if it does not already exist. |digital-detective-8465  |
| Copy a file | `cp terminal-practice/notes.txt terminal-practice/notes-copy.txt` | Creates a separate copy while keeping the original. |  digital-detective-8465 %  |
| Rename a file | `mv terminal-practice/notes-copy.txt terminal-practice/notes-renamed.txt` | Renames the copy. | digital-detective-8465|
| Display file contents | `cat terminal-practice/notes.txt` | Prints the file's contents. An empty file produces no text. | no text |

### Task 2.2 — Practise File Changes Safely

These commands are run from the assignment repository's root directory.
The file notes.txt was created during Task 2.1.

| Step | Command | Purpose |
|------|---------|---------|
| Write the first line | `echo "This is my first line." > terminal-practice/notes.txt` | Writes text into the file, replacing any existing contents. |
| Append a second line | `echo "This is my second line." >> terminal-practice/notes.txt` | Adds another line without removing the first. |
| Display the text | `cat terminal-practice/notes.txt` | Checks that both lines are present. |
| Create a backup | `cp terminal-practice/notes.txt terminal-practice/notes-backup.txt` | Makes a separate copy of the document. |
| Rename the backup | `mv terminal-practice/notes-backup.txt terminal-practice/notes-backup-renamed.txt` | Changes the backup's name. |

#### Questions and Understanding

**1. What is the difference between replacing a file’s contents and adding text to the end?**

The `>` symbol replaces the existing contents with new output.
The `>>` symbol adds output at the end without removing existing text.

**2. What is the difference between copying a file and moving a file?**

Copying with `cp` creates a separate copy and keeps the original.
Moving with `mv` changes the file’s location or name without creating another copy.

**3. What information does the current-directory display provide?**

The `pwd` command displays the full path of the directory where Terminal is currently working.

**4. Why is a directory-listing operation useful?**

The `ls` command helps me see files and folders, check their names,
and confirm whether file operations worked.

### Task 2.3 — Understand Flags and Pipes

**1. Normal directory listing**


ls--This lists visible files and folders in the current directory.

My observation: evidence			mission-01-computer-basics	mission-03-operating-system	mission-05-numbers-data		mission-07-networking		README.md
mission-00-setup		mission-02-terminal		mission-04-programs		mission-06-git-github		mission-08-final-report		terminal-practice

**2. Detailed directory listing**

ls -l-- The `-l` option displays additional information, including permissions,
ownership, file size, and modification time.

My observation: drwxr-xr-x  2   staff    64 14 Nov 10:08 evidence
drwxr-xr-x  3   staff    96 14 Nov 10:21 mission-00-setup
drwxr-xr-x  3   staff    96 14 Nov 10:21 mission-01-computer-basics
drwxr-xr-x  3   staff    96 14 Nov 10:23 mission-02-terminal
drwxr-xr-x  3   staff    96 14 Nov 10:23 mission-03-operating-system
drwxr-xr-x  3   staff    96 14 Nov 10:24 mission-04-programs
drwxr-xr-x  4   staff   128 14 Nov 10:28 mission-05-numbers-data
drwxr-xr-x  3   staff    96 14 Nov 10:27 mission-06-git-github
drwxr-xr-x  3   staff    96 14 Nov 10:27 mission-07-networking
drwxr-xr-x  3   staff    96 14 Nov 10:28 mission-08-final-report
-rw-r--r--@ 1   staff  1762 14 Nov 12:06 README.md |

**3. Include hidden files**

ls -la--The `-a` option includes entries whose names begin with a dot.
Combining it with `-l` gives a detailed listing that includes hidden entries.

My observation: total 8
drwxr-xr-x@ 15   staff   480 15 Nov 13:39 .
drwx------+ 26   staff   832 14 Nov 10:00 ..
drwxr-xr-x  12   staff   384 15 Nov 13:25 .git
drwxr-xr-x   2   staff    64 14 Nov 10:08 evidence
drwxr-xr-x   3   staff    96 14 Nov 10:21 mission-00-setup
drwxr-xr-x   3   staff    96 14 Nov 10:21 mission-01-computer-basics
drwxr-xr-x   3   staff    96 14 Nov 10:23 mission-02-terminal
drwxr-xr-x   3   staff    96 14 Nov 10:23 mission-03-operating-system
drwxr-xr-x   3   staff    96 14 Nov 10:24 mission-04-programs
drwxr-xr-x   4   staff   128 14 Nov 10:28 mission-05-numbers-data
drwxr-xr-x   3   staff    96 14 Nov 10:27 mission-06-git-github
drwxr-xr-x   3   staff    96 14 Nov 10:27 mission-07-networking
drwxr-xr-x   3   staff    96 14 Nov 10:28 mission-08-final-report
-rw-r--r--@  1   staff  1762 14 Nov 12:06 README.md
drwxr-xr-x   4   staff   128 15 Nov 13:41 terminal-practice
**4. Human-readable file sizes**

ls -lah--The `-h` option makes sizes easier to read using units such as K and M
when appropriate. This command combines detailed information,
hidden entries, and human-readable sizes.

My observation: evidence			mission-01-computer-basics	mission-03-operating-system	mission-05-numbers-data		mission-07-networking		README.md
mission-00-setup		mission-02-terminal		mission-04-programs		mission-06-git-github		mission-08-final-report		terminal-practice
**5. Use a pipe**
ls -l | head -n 5--The `ls -l` command produces a detailed directory listing.
The pipe symbol `|` passes that output to `head`.
The command `head -n 5` displays only the first five lines it receives.

This does not necessarily mean five files, because the listing may
include a total line.

My observation: total 8
drwxr-xr-x  2  staff    64 14 Nov 10:08 evidence
drwxr-xr-x  3   staff    96 14 Nov 10:21 mission-00-setup
drwxr-xr-x  3   staff    96 14 Nov 10:21 mission-01-computer-basics
drwxr-xr-x  3   staff    96 14 Nov 10:23 mission-02-terminal

### Task 2.4 — Understand Package Managers

**What is a package manager?**

A package manager helps install, update, and remove software.
It can also manage dependencies, which are other software packages
a program needs to work.

**Why are package managers useful?**

They provide a consistent way to manage software without downloading
and updating every supported program separately. They can also help
track installed packages and their dependencies.

**What is Homebrew?**

Homebrew is a commonly used package manager on macOS.

**Check its availability and version:**

brew --version
My result:zsh: command not found: brew

**If Homebrew is available, list the packages it manages:**
brew list

My observation: zsh: command not found: brew

## 3. Commands / tools used

- Terminal: Provides an interface for entering commands.
- zsh: Interprets shell commands.
- `pwd`: Displays the current directory.
- `ls`: Lists files and directories.
- `cd`: Changes the current directory.
- `mkdir`: Creates directories.
- `touch`: Creates an empty file if it does not exist.
- `cp`: Copies files.
- `mv`: Moves or renames files.
- `cat`: Displays file contents.
- `echo`: Produces text output.
- `head`: Displays the beginning of its input.
- Visual Studio Code: Edits the README.
- Markdown: Formats the documentation.


## 4. My understanding

Terminal commands let me navigate directories and manage files.
Checking the current directory helps me perform operations in the
correct location.

Copying creates a separate copy, while moving changes a file's name
or location. The `>` symbol replaces contents, while `>>` appends
without removing existing text.

Flags change command behaviour. A pipe passes one command's output
to another command as input. Package managers help manage software
and its dependencies.

## 5. Difficulties faced
No major difficulties

## 6. How I resolved them

 Not applicable

## 7. Evidence / files

- `mission-02-terminal/README.md`: Contains command explanations,
  answers, and observations.
- `terminal-practice/notes.txt`: Contains the two practice lines.
- `terminal-practice/notes-renamed.txt`: Renamed copy from Task 2.1.
- `terminal-practice/notes-backup-renamed.txt`: Backup of the text.


## 8. Commit details

Status: In progress.

Push verification: Pending.
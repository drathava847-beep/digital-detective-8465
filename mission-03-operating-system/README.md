# Mission 3 — Understand the Operating System

## 1. Task 

Explore the operating system, running processes, storage, paths,
and file permissions. and describe the OS responsibility.

## 2. Work completed

### Task 3.1 — Explore the Operating System

| Information explored | What it tells you | Example observation|
|----------------------|-------------------|--------------------|
| Operating system  | Identifies the operating system and its version. | macOS 15.0. |
| Current account identity | Identifies the account running the Terminal session. | Username: xtz@ |
| Available and used storage | Shows filesystem capacity, used space, and available space. | Illustrative figures: 256 GB total, 120 GB used, and 136 GB available. |
| System activity snapshot | Shows running processes and CPU and memory activity. | Several application and background processes are running; resource usage changes over time. |

**Commands for obtaining actual results**
sw_vers

Displays the macOS product name, version, and build version.
whoami


Displays the username of the current account. The actual username
should be redacted in public evidence.

df -h . -- Shows storage information for the filesystem containing the current
directory. The `-h` option uses human-readable sizes, and `.` means
the current directory.

On macOS, APFS volumes can share space. Actual output should be
interpreted as filesystem information rather than assuming each
listed volume is a separate physical disk.


top -l 1
Displays one system-activity sample on macOS. It includes process,
CPU, and memory information.

### Task 3.2 — Understand Processes

**What is a process?**

A process is an instance of a program that is running.
An application can use several processes, and background services
also run as processes.

**How can processes be viewed?**

Open an application such as Google Chrome or Visual Studio Code,
then use:
ps -axo pid,comm

The `-a` and `-x` options together select processes broadly.
The `-o` option chooses the displayed columns. Here, `pid,comm`
requests process identifiers and command names.

**What does the PID column represent?**

PID means Process Identifier. The operating system assigns this
number to identify a process. PIDs can change between runs and
may be reused after a process ends.

**Two example processes**

- Google Chrome: An application that displays websites and runs
  web applications.
- WindowServer: A macOS system process involved in managing and
  composing graphical windows for display.

PID    COMM
410    WindowServer
825    Google Chrome

### Task 3.3 — Understand Paths and Permissions

**What is a path?**

A path describes the location of a file or directory.

**Absolute path**

An absolute path begins at the filesystem root, represented by `/`.
Its meaning does not depend on the current working directory.

/Users/[redacted]/Documents/digital-detective-8465/mission-03-operating-system/README.md


**Relative path**

A relative path is interpreted from the current working directory.

From the assignment repository's root, this relative path points
to the Mission 3 README:

mission-03-operating-system/README.md


**Navigating between directories**

Starting inside the assignment repository:

pwd
/Users/[redacted]/Documents/digital-detective-8465

Enter the mission folder:

cd mission-03-operating-system


Check the location again:
pwd

/Users/[redacted]/Documents/digital-detective-8465/mission-03-operating-system


The path now includes the mission folder because it is the current
working directory.

Return to the parent directory:
cd ..


Here, `..` means the directory immediately above the current one.

**Inspecting file permissions**

From the repository's root:
ls -l terminal-practice/notes.txt

-rw-r--r--  1 [owner]  [group]  50 Nov 15 10:00 terminal-practice/notes.txt


The first character, `-`, indicates a regular file.
The next nine characters form three permission groups:

- Owner: `rw-`
- Group: `r--`
- Others: `r--`

| Permission | Meaning | Example |
|---|---|---|
| r — Read | Allows a file's contents to be read. | Opening a text file. |
| w — Write | Allows a file's contents to be modified. | Editing a README. |
| x — Execute | Allows a file to be executed, subject to other requirements. On a directory, permits traversal. | Executing a runnable script or accessing a directory by path. |

A hyphen in a permission position means that permission is absent.

### Task 3.4 — Operating-System Responsibilities

| OS responsibility | Explanation | Example |
|---|---|---|
| Process management | Creates and manages processes and schedules CPU time for their work. | Allows a browser and text editor to run concurrently. |
| Memory management | Manages RAM and protected memory spaces used by processes. | Provides memory for browser tabs and a document being edited. |
| Device management | Coordinates access to hardware through drivers and related services. | Receives keyboard input and supports speaker output. |
| File management | Provides ways to organise, read, write, and remove files and directories. | Saves a README inside its mission folder. |
| User  shell | Provides ways for users to interact with the system through graphical interfaces and command interpreters. | Finder supports graphical navigation; zsh interprets Terminal commands. |
| Security and permissions | Controls access to resources using accounts, permissions, and other security mechanisms. | Restricts who can read or modify a document. |

## 3. Commands / tools used

The commands covered in this example are:

- `sw_vers`: Displays macOS version information.
- `whoami`: Displays the current account's username.
- `df -h .`: Displays storage information for the current filesystem.
- `top -l 1`: Displays one macOS system-activity sample.
- `ps -axo pid,comm`: Lists process identifiers and command names.
- `pwd`: Displays the current working directory.
- `cd`: Changes the current working directory.
- `ls -l`: Displays file details, including permissions.

## 4. My understanding

The operating system coordinates hardware resources and provides
services that applications use. It manages processes, memory,
devices, files, and access permissions.

A program contains instructions. A process is an executing instance
of a program. The PID identifies a process, and one application
can use multiple processes.

An absolute path begins at the filesystem root. A relative path
depends on the current working directory.

File permissions specify access for the owner, group, and others.
Read, write, and execute permissions have different purposes.

System output may reveal usernames, device information, and private
paths. Public evidence should exclude or redact identifying details.

## 5. Difficulties faced
- A program and a running process.
- An absolute path and a relative path.
- Owner, group, and other-user permissions.
- Storage capacity and RAM usage.

## 6. How I resolved them

- A browser application can create multiple running processes.
- An absolute path starts with `/`, while a relative path is
  interpreted from the current directory.
- The nine permission characters after the file-type character
  are divided into three groups.
- Storage keeps saved data, while RAM holds working information
  for active processes.

## 7. Evidence / files

- `mission-03-operating-system/README.md`

## 8. Commit details

Suggested commit message: 

Actual commit and push status: 

Mission status: 
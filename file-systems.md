# File Systems

3 essential requirements for long-term info storage

1. Must be possible to store a very large amount of data
2. Information must survive the termination of the process using it
3. Multiple processes must be able to access the information at once

Files are logical units of information created by a process

- The abstractions of processes (and threads), address spaces, and files are the most important concepts related to OS
- Files are managed by the OS - the part of OS dealing with files is the file system
- When a process creates a file, it gives it a name, when the process terminates, the file continues to exist and can be accessed using its name

Exact rules for file naming vary somewhat from system to system

- UNIX file names are case sensitive
- In Unix, file extensions are just conventions and are not enforced by the OS
- Unix sees a file as an unstructured sequence of bytes -- in effect, the OS does not know or care what’s in the file
  - this provides the most flexibility
  - Unix file types:
    - Regular files: contain user information
    - Directories: system files for maintaining the structure of the file system
    - Character special files: related to I/o and used to model serial I/o devices
    - Block special files: used to model disks
  - Regular files are generally either ASCII or binary
    - ASCII can be displayed and printed as-is and can be edited with any text editor
    - if large numbers of programs use ASCII for input and output, its easy to connect the output of one to the input of another

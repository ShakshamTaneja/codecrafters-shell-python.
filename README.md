This Python-based shell emulation program serves as a minimalist, yet robust command-line interface. The implementation strives to replicate several essential functionalities commonly found in Unix-like shells, such as handling built-in commands, executing external programs, redirecting output and error streams, and navigating directories.

Key Features:
Built-in Commands:
echo: Echoes the specified arguments to the standard output, facilitating the printing of strings and variables.
type: Determines whether a given command is a built-in function or an executable found within the system's PATH variable, and displays its corresponding location or nature.
pwd: Prints the current working directory to the standard output.
cd: Changes the current working directory to the one specified, with error handling for invalid directories.
exit: Terminates the shell session, ensuring a clean exit when invoked.
External Command Execution:
The shell supports the execution of external commands. Upon invocation, the program searches the directories listed in the PATH environment variable for the command executable and runs it, printing both the standard output and any potential errors to the terminal.
Output and Error Redirection:
The shell supports advanced output redirection mechanisms:
>: Redirects standard output to a file, overwriting the file if it exists.
>>: Appends the standard output to a file.
2>: Redirects standard error to a file, overwriting the file if it exists.
2>>: Appends the standard error to a file.
These features allow users to capture both standard output and error output separately and flexibly.
Interactive Command Loop:
The shell runs in an interactive loop, consistently prompting the user for input. Once the input is received, it is processed and executed, with the result being output to the terminal, unless redirected to a file.
Error Handling:
Commands that do not exist or cannot be executed properly return a descriptive error message, indicating the nature of the problem (e.g., "command not found" or "No such file or directory").
Execution:
Upon running the program, the user is presented with a shell prompt ($), from which they can enter commands and arguments for processing.
The program continues to prompt for commands until exit is invoked, at which point the shell session terminates gracefully.


Example Usage:
$ echo Hello, World!
Hello, World!

$ type ls
ls is /bin/ls

$ pwd
/home/user

$ cd /path/to/directory
$ cd invalid_directory\
cd: invalid_directory: No such file or directory

$ exit
This advanced shell implementation is a fundamental starting point for building more complex shell-like environments in Python, incorporating essential features such as command execution, built-ins, directory navigation, and output redirection.

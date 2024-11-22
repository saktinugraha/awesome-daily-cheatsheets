Here is the content converted into a table format in Markdown:

# Bash Documentation

## Shortcuts and History

### CTRL Commands

| Command   | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| **CTRL+A** | Move to the beginning of the line                                          |
| **CTRL+B** | Move backward one character                                               |
| **CTRL+C** | Halt the current command                                                  |
| **CTRL+D** | Delete one character backward or log out of the current session           |
| **CTRL+E** | Move to the end of the line                                               |
| **CTRL+F** | Move forward one character                                                |
| **CTRL+G** | Abort the current editing command and ring the terminal bell              |
| **CTRL+H** | Delete one character under the cursor                                     |
| **CTRL+J** | Same as `RETURN`                                                          |
| **CTRL+K** | Delete (kill) forward to the end of the line                              |
| **CTRL+L** | Clear the screen and redisplay the line                                   |
| **CTRL+M** | Same as `RETURN`                                                          |
| **CTRL+N** | Next line in command history                                              |
| **CTRL+O** | Same as `RETURN`, then display the next line in the history file          |
| **CTRL+P** | Previous line in command history                                          |
| **CTRL+Q** | Resume suspended shell output                                             |
| **CTRL+R** | Search backward in history                                                |
| **CTRL+S** | Search forward in history or suspend shell output                         |
| **CTRL+T** | Transpose two characters                                                  |
| **CTRL+U** | Kill backward from the point to the beginning of the line                 |
| **CTRL+V** | Make the next character typed verbatim                                    |
| **CTRL+W** | Kill the word behind the cursor                                           |
| **CTRL+X** | List possible filename completions of the current word                    |
| **CTRL+Y** | Retrieve (yank) the last item killed                                      |
| **CTRL+Z** | Stop the current command (resume with `fg` or `bg`)                       |

---

### ALT Commands

| Command   | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| **ALT+B** | Move backward one word                                                     |
| **ALT+D** | Delete the next word                                                       |
| **ALT+F** | Move forward one word                                                      |
| **ALT+H** | Delete one character backward                                              |
| **ALT+T** | Transpose two words                                                        |
| **ALT+.** | Paste the last word from the previous command                              |
| **ALT+U** | Capitalize from the cursor to the end of the word                          |
| **ALT+L** | Uncapitalize from the cursor to the end of the word                        |
| **ALT+C** | Capitalize the letter under the cursor and move to the end of the word     |
| **ALT+R** | Revert changes to a command from history                                   |
| **ALT+?** | List possible completions for the typed input                              |
| **ALT+^** | Expand line to the most recent history match                               |

---

### Other Commands

| Command         | Description                                                          |
|------------------|----------------------------------------------------------------------|
| **BACKSPACE**    | Delete one character backward                                       |
| **DELETE**       | Delete one character under the cursor                               |
| **history**      | Show command line history                                           |
| **!!**           | Repeat the last command                                             |
| **!n**           | Execute the command at history line `n`                             |
| **!string**      | Execute the last command starting with `string`                     |
| **esc :wq**      | Exit and save script                                                |
| **exit**         | Log out of the current session                                      |

---

## Bash Basics

| Command               | Description                                                  |
|------------------------|--------------------------------------------------------------|
| **env**               | Display all environment variables                            |
| **echo $SHELL**       | Show the current shell                                       |
| **echo $BASH_VERSION**| Show the Bash version                                        |
| **bash**              | Start a Bash session                                        |
| **whereis bash**      | Locate the binary, source, and manual for Bash               |
| **which bash**        | Show the location of the Bash binary                         |
| **clear**             | Clear the screen                                             |

---

## File Commands

| Command               | Description                                                  |
|------------------------|--------------------------------------------------------------|
| **ls**               | List files in the current directory                           |
| **ls -l**            | List files in long format                                     |
| **ls -a**            | List all files, including hidden ones                         |
| **ln -s filename link**| Create a symbolic link to a file                             |
| **readlink filename** | Show the target of a symbolic link                           |
| **tree**             | Display directory structures in a tree format                |
| **touch filename**   | Create or update a file                                       |
| **mktemp -t filename**| Create a temporary file in `/tmp/`                           |
| **cat filename**     | Display the file content                                      |
| **head filename**    | Show the first lines of a file (default: 10)                  |
| **tail filename**    | Show the last lines of a file (default: 10)                   |
| **vim filename**     | Open a file in the Vim editor                                 |
| **cp filename1 dest**| Copy a file to the destination                                |
| **rm filename**      | Remove a file                                                |

---

## Directory Commands

| Command               | Description                                                  |
|------------------------|--------------------------------------------------------------|
| **mkdir dirname**     | Create a new directory                                       |
| **rmdir dirname**     | Remove an empty directory                                    |
| **cd dirname**        | Change to the specified directory                            |
| **pwd**               | Show the current directory path                              |

---

## SSH, System Info & Network Commands

| Command               | Description                                                  |
|------------------------|--------------------------------------------------------------|
| **ssh user@host**     | Connect to a host via SSH                                    |
| **whoami**            | Display the current username                                 |
| **sudo command**      | Run a command as root                                        |
| **date**              | Show the current date and time                               |
| **uptime**            | Display the system uptime                                    |

---

## Variables

| Command                  | Description                                               |
|---------------------------|-----------------------------------------------------------|
| **varname=value**        | Define a variable                                         |
| **echo $varname**        | Display the value of a variable                           |
| **array=(valA valB valC)**| Define an array                                           |

---

## Flow Controls

| Command                              | Description                                    |
|---------------------------------------|------------------------------------------------|
| **if condition; then statements; fi**| Conditional execution                         |
| **for x in {1..10}; do statements; done**| Loop from 1 to 10                          |
| **while condition; do statements; done**| While loop                                  |
| **case expression in pattern) statements;; esac**| Case statement                    |

---

## Command-Line Processing Cycle

| Command   | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| `command` | Removes alias and function lookup. Only built-ins and commands in PATH are executed. |
| `builtin` | Looks up only built-in commands, ignoring functions and commands in PATH.  |
| `enable`  | Enables or disables shell built-ins.                                       |
| `eval`    | Takes arguments and runs them through the command-line processing steps again. |

---

## Input/Output Redirections

| Syntax             | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| `cmd1 \| cmd2`      | Pipe; takes the standard output of `cmd1` as standard input to `cmd2`.     |
| `< file`           | Takes standard input from a file.                                          |
| `> file`           | Directs standard output to a file.                                         |
| `>> file`          | Appends standard output to a file if it exists.                            |
| `>| file`          | Forces standard output to overwrite a file even if `noclobber` is set.     |
| `n>| file`         | Same as above but for descriptor `n`.                                      |
| `<> file`          | Uses a file as both standard input and output.                             |
| `n<> file`         | Same as above but for descriptor `n`.                                      |
| `n> file`          | Redirects descriptor `n` to a file.                                        |
| `n< file`          | Takes descriptor `n` input from a file.                                    |
| `n>> file`         | Appends descriptor `n` output to a file.                                   |
| `n>&`              | Duplicates standard output to descriptor `n`.                              |
| `n<&`              | Duplicates standard input from descriptor `n`.                             |
| `n>&m`             | Descriptor `n` is made a copy of the output descriptor `m`.                |
| `n<&m`             | Descriptor `n` is made a copy of the input descriptor `m`.                 |
| `&> file`          | Directs both standard output and standard error to a file.                 |
| `<&-`              | Closes the standard input.                                                 |
| `>&-`              | Closes the standard output.                                                |
| `n>&-`             | Closes the output from descriptor `n`.                                     |
| `n<&-`             | Closes the input from descriptor `n`.                                      |
| `tee <file>`       | Outputs command results to both terminal and file (use `-a` to append).    |

---

## Process Handling

| Command                 | Description                                                                 |
|-------------------------|-----------------------------------------------------------------------------|
| `myCommand &`           | Runs a job in the background and returns shell prompt.                     |
| `jobs`                  | Lists all jobs (use `-l` to see associated PID).                           |
| `fg`                    | Brings a background job to the foreground.                                |
| `kill PID`              | Terminates a process by PID.                                               |
| `ps`                    | Shows information about running processes.                                |
| `trap cmd sig1 sig2`    | Executes a command when a specified signal is received.                   |
| `disown <PID|JID>`      | Removes a job from the list of jobs.                                       |
| `wait`                  | Waits until all background jobs finish.                                   |
| `sleep <number>`        | Pauses for the specified number of seconds.                               |

---

## Debugging Shell Programs

| Command                 | Description                                                                 |
|-------------------------|-----------------------------------------------------------------------------|
| `bash -n scriptname`    | Checks for syntax errors without running commands.                         |
| `bash -v scriptname`    | Echoes commands before running them.                                       |
| `bash -x scriptname`    | Echoes commands after command-line processing.                             |
| `trap 'command' EXIT`   | Executes a command at script exit.                                         |
| `set -o noexec`         | Alternative to check for syntax errors without running the script.         |
| `set -o verbose`        | Alternative to echo commands before running.                              |
| `set -o xtrace`         | Alternative to echo commands after processing.                            |

---

## Colors and Backgrounds

| Style          | Code            | Example Usage                          |
|-----------------|-----------------|----------------------------------------|
| **Reset**       | `\033[0m`       | `${Color_Off}` resets text styles.     |
| **Black**       | `\033[0;30m`    | `${Black}Text${Color_Off}`             |
| **Red**         | `\033[0;31m`    | `${Red}Text${Color_Off}`               |
| **Green**       | `\033[0;32m`    | `${Green}Text${Color_Off}`             |
| **Yellow**      | `\033[0;33m`    | `${Yellow}Text${Color_Off}`            |
| **Blue**        | `\033[0;34m`    | `${Blue}Text${Color_Off}`              |
| **Purple**      | `\033[0;35m`    | `${Purple}Text${Color_Off}`            |
| **Cyan**        | `\033[0;36m`    | `${Cyan}Text${Color_Off}`              |
| **White**       | `\033[0;97m`    | `${White}Text${Color_Off}`             |
| **Background**  | `\033[41m`      | `${Red}${On_White}Text${Color_Off}`    |

---

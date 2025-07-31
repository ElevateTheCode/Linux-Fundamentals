# Pipes and Redirection

- `|` (Pipe): Chains commands.
  - **`ps aux | grep firefox`**: Finds the process ID (PID) of the "firefox" application. This is a crucial skill for process management and analysis.
- `>` (Redirect): Overwrites a file.
  - **`echo "new content" > file.txt`**: Completely replaces `file.txt`'s content with "new content".
- `>>` (Append): Adds to a file.
  - **`echo "more content" >> file.txt`**: Adds "more content" to the end of `file.txt`.
- `2>`: Redirects error messages.
  - **`command 2> error.log`**: Sends any error output from `command` to `error.log`.

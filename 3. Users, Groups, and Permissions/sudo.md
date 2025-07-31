# `sudo`

- Allows a user to execute commands as `root`.
- **`sudo -l`**: Lists the commands a user is allowed to run with `sudo` privileges. This is a key step in privilege escalation.
- **`/etc/sudoers`**: The configuration file for `sudo`. A simple misconfiguration (e.g., `ALL ALL=(ALL) NOPASSWD: ALL`) can grant a user full `root` access without a password.

# Permissions (`chmod` and `chown`)

- **Permissions:** `r` (read - 4), `w` (write - 2), `x` (execute - 1).
- **`chmod 777 file.txt`**: Gives full permissions to everyone. This is a major security vulnerability.
- **SUID/SGID bits**: Special permissions that allow an executable to run with the permissions of the file owner (SUID) or group (SGID). These are frequently exploited for privilege escalation.
  - **`find / -perm /4000 2>/dev/null`**: A common reconnaissance command to find SUID files.
- `chown [user]:[group] [file]`: Changes the ownership.

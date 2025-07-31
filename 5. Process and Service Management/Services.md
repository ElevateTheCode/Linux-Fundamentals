# Services (`systemctl`)

- `systemctl [command] [service]`: Manages system services.
- **`systemctl list-units --type=service`**: Lists all active services on the system.
- **`systemctl status sshd`**: Checks if the SSH service is running. This is a common reconnaissance step to see if a system can be accessed remotely.
- **Security Implications**: Attackers often look for vulnerable services running on a system.

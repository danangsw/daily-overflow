# Daily Overflow
A bookmarks and documentations of my daily overflow working life!

## 1. VS Code Extension: Remote Development extension pack cannot remember my ssh key.

If you complete these steps: [remote ssh getting started](https://code.visualstudio.com/docs/remote/ssh#_getting-started). Then when you connect to remote ssh the VS Code always show prompt to input password. Try this solution to make VS Code remembering authentication to the remote host.

1. Open `Remote SSH: Open Configuration File...` from remote ssh extension Side Bar.
2. In the `config` file, make sure on `Host` property consists of 3 distinct parts: `{user}@{host}`. The `config` file will like:
```bash
# Read more about SSH config files: https://linux.die.net/man/5/ssh_config
Host {user}@{host}
    User {user}
    HostName {host}
    IdentityFile ~/.ssh/authorized_keys
```
3. Save the `config` file and try connect to a defined remote ssh host.
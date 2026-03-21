# 02 - Permissions & Ownership

## File Types
```
d = directory
- = regular file
l = symbolic link
```

## Permission Structure
```
- rw- rw- r--
│ │   │   └── others
│ │   └── group
│ └── owner
└── file type

r = read    (4)
w = write   (2)
x = execute (1)
- = no permission (0)
```

## Numeric Notation
Each group of 3 is represented by a number (sum of values):
```
rwx = 4+2+1 = 7
rw- = 4+2+0 = 6
r-x = 4+0+1 = 5
r-- = 4+0+0 = 4
--- = 0+0+0 = 0
```

## Common Permission Sets
| Numeric | Symbolic  | Use case            |
|---------|-----------|---------------------|
| 755     | rwxr-xr-x | Executable scripts  |
| 644     | rw-r--r-- | Config files        |
| 600     | rw------- | Private files       |
| 700     | rwx------ | Private directories |

## chmod - Change Permissions
```bash
chmod 755 monitor.sh
chmod +x file.sh
chmod -w file.txt
```

## Real Examples From My Machine
```bash
ls -la ~/projects/system-monitor/monitor.sh
# -rwxr-xr-x jacob jacob

ls -la ~/.ssh
# drwx------ private directory

ls -la ~/.bashrc
# -rw-r--r-- config file
```

## Status
- [x] Permission structure understood
- [x] Numeric notation understood
- [x] chmod applied in practice
- [ ] chown - change ownership
- [ ] sudo and root permissions

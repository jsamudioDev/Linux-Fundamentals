# 01 - Navigation & File System

## Key Concepts
- Linux organizes everything in a tree starting from `/` (root)
- There are no drive letters (C:, D:) like Windows — everything is mounted
- Every device, file and process is represented as a file

---

## Essential Commands

### Location & Movement
| Command | Description | Example |
|---------|-------------|---------|
| `pwd` | Print working directory | `pwd` → `/home/jacob` |
| `cd` | Change directory | `cd /etc` |
| `cd ~` | Go to home directory | `cd ~` |
| `cd ..` | Go up one level | `cd ..` |
| `ls` | List files | `ls` |
| `ls -la` | List with details and hidden files | `ls -la` |

### Reading Files
| Command | Description | Example |
|---------|-------------|---------|
| `cat` | Print file content | `cat /etc/hostname` |
| `less` | Read file page by page | `less /var/log/syslog` |
| `head` | Show first lines | `head -10 file.txt` |
| `tail` | Show last lines | `tail -10 file.txt` |

---

## Key Directories

| Directory | Purpose |
|-----------|---------|
| `/etc` | System configuration files |
| `/var/log` | System logs and records |
| `/home` | User home directories |
| `/bin` | Essential system binaries |
| `/tmp` | Temporary files |
| `/proc` | Virtual filesystem — running processes |

---

## Key Files Explored

### /etc/hostname
Stores the machine name on the network.
```bash
cat /etc/hostname
# jacob-Nitro-AN515-58
```

### /etc/hosts
Local DNS — resolves names before asking the internet.
```bash
cat /etc/hosts
# 127.0.0.1 localhost
# 127.0.1.1 jacob-Nitro-AN515-58
```

### /etc/os-release
Operating system information.
```bash
cat /etc/os-release
```

---

## Real Output From My Machine
```bash
df -h | grep -E 'nvme|sd'
# /dev/nvme0n1p5  623G  37G  554G   7% /
# /dev/nvme0n1p3  320G  54G  266G  17% /mnt/windows_data
# /dev/nvme0n1p1  196M  38M  159M  20% /boot/efi
```

---

## Status
- [x] pwd, cd, ls
- [x] cat, file reading
- [x] Key directories explored
- [x] Key files understood



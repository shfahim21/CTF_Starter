# 🚩 CTF Commands and Tools Reference Guide

## 📑 Table of Contents
1. [General Tools](#general-tools)
2. [Cryptography](#cryptography)
3. [Forensics](#forensics)
4. [Web](#web)
5. [Reverse Engineering](#reverse-engineering)
6. [Network](#network)

## General Tools

### 🔧 CyberChef
```markdown
- Online tool for encoding, decoding, encryption
- URL: https://gchq.github.io/CyberChef/
```

### 🔍 Grep Command
```bash
# Basic Syntax
grep [options] "pattern" filename

# Common Options
-i    # Ignore case
-c    # Count matches
-n    # Show line numbers
-v    # Invert match
-w    # Match whole words
-E    # Extended regex

# Examples
grep "error" log.txt
grep "error" *.log
grep -r "error"
grep -v "error" log.txt
grep -E "error|warning" log.txt

# Piping
ps aux | grep "chrome"
tree big-zip-files | grep -i "pico"
```

### 📂 Find Command
```bash
# Basic Syntax
find [path] [expression]

# Common Options
-name    # Case-sensitive search
-iname   # Case-insensitive search
-type f  # Files only
-type d  # Directories only
-mtime   # Modified time
-size    # File size
-empty   # Empty files/directories

# Examples
find /home/user -name "example.txt"
find . -name "*.txt"
find . -type f
find . -type d
```

## Cryptography

### 🔐 Base64
```bash
# Decode base64 (look for = padding at end)
base64 -d [file]
```

### 🔒 Hashing
```bash
# MD5
md5sum example.txt
echo -n "hello world" | md5sum

# SHA1/SHA256
sha1sum example.txt
sha256sum example.txt

# Multiple files
md5sum file1.txt file2.txt file3.txt
```

### 🔑 OpenSSL
```bash
# Basic Syntax
openssl <subcommand> [options] [arguments]

# Hashing Example
echo -n "Hello world" | openssl dgst -md5
```

## Forensics

### 📝 Strings Command
```bash
# Basic Syntax
strings [options] filename

# Find specific string
strings filename | grep -n "pico"
```

## Network

### 🌐 SSH
```bash
# Default Connection (Port 22)
ssh username@remote-host

# Custom Port
ssh username@remote-host -p <port>

# With Password
sshpass -p 'password' ssh username@remote-host

# Execute Remote Command
ssh user@example.com 'ls -la /home/user'
```

### 🔌 NetCat (nc)
```bash
# Basic Connection
nc example.com 80

# Port Scanning
nc -z -v example.com 20-100
    -z: Zero-I/O mode
    -v: Verbose output
```

## Web
Common web tools and commands:


## Reverse Engineering


## 💡 Tips

## 🔗 Useful Resources
- [CyberChef](https://gchq.github.io/CyberChef/)
- [GTFOBins](https://gtfobins.github.io/)
- [HackTricks](https://book.hacktricks.xyz/)
- [RevShells](https://revshells.com)

*Note: This is a living document. Add new tools and commands as you discover them.*

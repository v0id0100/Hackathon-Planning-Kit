# Active Reconaissance

### Port scanning:

**nmap**

```bash
# Single target
nmap [targetIP]

# Multiple targets
nmap [target1IP] [target2IP]

# Ping only
nmap -sn  [targetIP]

# No ping
nmap -Pn [targetIP]

# Versions (the best on my opinion)
nmap -sV [targetIP]
```

----

### Directory Fuzzing:

Fuzzing the target looking for hidden directories or subdirectories:

Tools:
- wfuzz
- dirb
- gobuster
- ffuf
- subfinder

**wfuzz**

Usage:
```bash
# Colored and wordlist
wfuzz -c -z wordlist.txt [URL]/FUZZ(You must the the FUZZ word wherever you want to fuzz)

# Colored and wordlist and hide ex:404 results
wfuzz -c -z wordlist.txt -hc [code1,code2,code3] [URL]/FUZZ(You must the the FUZZ word wherever you want to fuzz)
```

**dirb**

Usage:
```bash
# Normal usage
dirb [url]

# Custom wordlist
dirb [url] [wordlist]

# Set cookie:
dirb -c [cookie_string] [url] 

# Custom header string
dirb -H [header_string] [url]
```

**gobuster**

```bash
gobuster dir [URL]
```

**ffuf**

```bash
# Normal usage:
ffuf -u [url / ip]/FUZZ(U have to set this wherever you want to set fuzzing) -w wordlist.txt
```

---

### Subdomains Fuzzing:

**subfinder**
```bash
# Normal usage
subfinder -d web.com

# Wordlist
subfinder -d web.com -dL wordlist.txt
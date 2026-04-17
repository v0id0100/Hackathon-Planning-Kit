# Passive reconnaissance

### Domain data:
- whois
- dig
- nslookup
- nitko

**whois**: Display web information data

Commands:
```bash
# Normal
whois [url]

# With host and port
whois -p [port] [url / ip]
```

**dig**: DNS Lookup
```bash
# Normal
dig [url / ip]

# With DNS Server
dig @SERVER [url / ip]

# With port
dig -p [port] [url / ip]
``` 

**nslookup**: another tool for DNS lookup

Command:
```bash
nslookup [url / ip]
```

**nikto**: Scan web server for known vulns

Usage:
```bash
nikto -h web.com
```

---

### Google Dorking:
Example:
- "name"
- site:web.com
- inurl:"contents in url"
- intext:"contents inside the web text"
- filetype:pdf (pdf, txt, jpg, png, ...)
- cache:web.com (cache that has google.com on its cache)
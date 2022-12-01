# NMAP 
 
### Scans Types

Harder and Noise

```nmap -sT [TCP connect]```

Smooth        

```nmap -sS [Sync scan]```

Smooth and bad

```nmap -sF [Fync Scan]```

A lot of Noise not recomended

```nmap -sX [Crhirsmas tree]```

Not recomended a lot of confussion

```nmap -sN [Null Scan]```

Only verify active hosts

```nmap -sP [Ping Scan]```

Active UDP ports so Noise

```nmap -SU [UDP Scan]```	
	
### Evade Firewalls
```nmap -sS -Pn```

```nmap -sS -f```

```nmap -sS --mtu 6/4/16/32 (Fragmen paquets)```

### Service Verssions
```nmap -sS -sV```

### Identify Operative System
```nmap -sS -O```
	
### Scann All ports
```nmap -sS -p1-65535```

### SO + Versions + Noise
```nmap -A -T4 [-A is equalto  -O, -sV, -sC (script), traceroute]```

### Scan Times
```T0-T5```

### Scripts

Scripts path

```/usr/share/nmap/scripts```

Check users and passwords empty adn vulnerable

```nmap -sS --script auth```

Default scripts equal to -A -T4

```nmap -sS --script default```

More smooth a lot of information

```nmap -sS --script safe```

Know vulneravilityes

```nmap -sS --script vuln```

### Save in file
```nmap -oA [Files / Folders, save in three formats .genmap, .nmap, .xml]```

### Evade IDS
```nmap --spoof-mac Cisco -T4 --source-port 53 -sS --send-ip -n --data-length 30 --randomize-hosts -n -f -f -sV --version-all -O```

```nmap -sS --mtu 32 -Pn -T2 --data-length 30```

### Hard Scan
```nmap -sS --script vuln -T4 -sV -O -p1-65535 -f -Pn -v```

### Check Auth ###
```nmap -p 1-65535 -v -Pn --script auth```

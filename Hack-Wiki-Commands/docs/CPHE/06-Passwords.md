	
# Passwords

## Windows credentials

The binary ```lsass.exe``` administrate the autentication of domains from local and AD

The binary ```winlogon.exe``` intercept the validation process made from keyboard

Password format

- LM
- NT
- NTLM y NTLMv2 
	
## Passwords Guessing

Diccionary atack

Tools

- Hashcat: Ofline faster

- Hydra

```hydra -l [user] -P [dictionary-Path] [protocol url(ssh://ip)] -vV```

```xhydra``` 

- Metasploit Auxiliary Moduls

- ```www.onlinehashckarck/hash-identification```

## Passwords Cracking

### Tools

#### Cain y Abel

 Ophcrack

- Live CD booteable

#### Jhon The Riper

- [Documentation](https://countuponsecurity.files.wordpress.com/2016/09/jtr-cheat-sheet.pdf)
- [Use Formats](http://pentestmonkey.net/cheat-sheet/john-the-ripper-hash-formats)

```john --format=[has-format] [hash-file.txt]```

```john --wordlist=[wordlist-path] [hash-file.txt]```


### Online Tools

```www.onlinehashckarck```
			
	

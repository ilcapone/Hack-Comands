
# Web

## Types of audits

Penetration test
Code audit
Functionality audit
Infrastructure audit

## Atacks

- SQLi
- XSS
- Path transversal
- Bruteforce
- File Upload
- Remote file inclusion

## Webs for trainin

- Web for pentester (PentesterLab.com)

## Tools

### sqlmap 

Database schema

```sqlmap -u 'url' --dbs```

Database Tables

```sqlmap -u 'url' -D [database] --tables```

Database Columns

```sqlmap -u 'url' -D [database] -T [tabla] -columns```

Dump Content

```sqlmap -u 'url' -D [database] -T [tabla] --dump```

Gain Shell

```sqlmap -u 'url' -D [database] -T [tabla] --sql-shell```
# Module Four: FTP Server Access Control Lab
**CYB-220 | Network Security**

## Objective
Configure and test FTP server access in Cisco Packet Tracer using CLI commands. Analyze default permissions, connect to the server, and enumerate directory contents.

---

## Part I — FTP Server Configuration

**Server:** FTP_Server_Public
**Service status:** On
**Default account:** username `cisco` / password `cisco`

### Question 1: Default FTP User Permissions
**Answer: RWDNL**

| Permission | Meaning |
|---|---|
| R | Read |
| W | Write |
| D | Delete |
| N | Navigate (change directories) |
| L | List (view directory contents) |

⚠️ **Security note:** The default account has full permissions AND uses default credentials (`cisco`/`cisco`). This is a critical misconfiguration in any real deployment — default credentials must always be changed before a service goes live.

---

## Part II — CLI FTP Connection

Connected to the FTP server from Server1_Admin using the command line:

```
C:\> FTP 10.1.10.5
Trying to connect... 10.1.10.5
Connected to 10.1.10.5
220- Welcome to PT Ftp server
Username: cisco
```

### Question 2: File #8 in FTP Directory
**Answer: `C2600-ipbasek9-mz.124-8.bin`**

This is a Cisco IOS image file — its presence on a public-facing FTP server with default credentials would be a significant security risk in a real environment, as it could reveal infrastructure details to attackers.

---

## Key Security Takeaways

1. **Always change default credentials** — `cisco`/`cisco` is one of the first combinations any attacker tries
2. **Audit FTP permissions** — RWDNL for all users is excessive; apply Least Privilege
3. **Consider SFTP over FTP** — FTP transmits credentials and data in plaintext; SFTP encrypts the connection
4. **Restrict FTP access by IP** — only allow known admin IPs to connect to the FTP server

---

## Skills Demonstrated
`FTP Configuration` `CLI Access` `Permission Analysis` `Default Credential Risk` `Cisco Packet Tracer` `Least Privilege` `Service Security Assessment`

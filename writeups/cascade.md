# :rainbow: Cascade :japanese_castle:

### Initial Scans

**<u>Quick:</u>**

```bash
PORT      STATE SERVICE       VERSION
53/tcp    open  domain        Microsoft DNS 6.1.7601 (1DB15D39) (Windows Server 2008 R2 SP1)
| dns-nsid: 
|_  bind.version: Microsoft DNS 6.1.7601 (1DB15D39)
88/tcp    open  kerberos-sec  Microsoft Windows Kerberos (server time: 2021-02-24 16:17:32Z)
135/tcp   open  msrpc         Microsoft Windows RPC
139/tcp   open  netbios-ssn   Microsoft Windows netbios-ssn
389/tcp   open  ldap          Microsoft Windows Active Directory LDAP (Domain: cascade.local, Site: Default-First-Site-Name)
445/tcp   open  microsoft-ds?
49154/tcp open  msrpc         Microsoft Windows RPC
49155/tcp open  msrpc         Microsoft Windows RPC
49157/tcp open  ncacn_http    Microsoft Windows RPC over HTTP 1.0
Service Info: Host: CASC-DC1; OS: Windows; CPE: cpe:/o:microsoft:windows_server_2008:r2:sp1, cpe:/o:microsoft:windows
```

**<u>Deep:</u>**

```bash
PORT      STATE SERVICE       VERSION
53/tcp    open  domain        Microsoft DNS 6.1.7601 (1DB15D39) (Windows Server 2008 R2 SP1)
| dns-nsid: 
|_  bind.version: Microsoft DNS 6.1.7601 (1DB15D39)
88/tcp    open  kerberos-sec  Microsoft Windows Kerberos (server time: 2021-02-24 16:19:17Z)
135/tcp   open  msrpc         Microsoft Windows RPC
139/tcp   open  netbios-ssn   Microsoft Windows netbios-ssn
|_smb-enum-services: ERROR: Script execution failed (use -d to debug)
389/tcp   open  ldap          Microsoft Windows Active Directory LDAP (Domain: cascade.local, Site: Default-First-Site-Name)
| ldap-rootdse: 
| LDAP Results
|   <ROOT>
|       currentTime: 20210224162014.0Z
|       subschemaSubentry: CN=Aggregate,CN=Schema,CN=Configuration,DC=cascade,DC=local
|       dsServiceName: CN=NTDS Settings,CN=CASC-...
|         dSCorePropagationData: 1601/01/01 00:04:17 UTC
| 
| 
|_Result limited to 20 objects (see ldap.maxobjects)
445/tcp   open  microsoft-ds?
|_smb-enum-services: ERROR: Script execution failed (use -d to debug)
636/tcp   open  tcpwrapped
|_unusual-port: tcpwrapped unexpected on port tcp/636
3268/tcp  open  ldap          Microsoft Windows Active Directory LDAP (Domain: cascade.local, Site: Default-First-Site-Name)
| ldap-rootdse: 
| LDAP Results
|   <ROOT>
|       currentTime: 20210224162013.0Z
|       subschemaSubentry: CN=Aggregate,CN=Schema,CN=Configuration,DC=cascade,DC=local
|       dsServiceName: CN=NTDS Settings,CN=CASC-DC1,CN=Servers,CN=Default-First-Site-Name,CN=Sites,CN=Configuration,DC=cascade,DC=local
...
| 
| 
|_Result limited to 20 objects (see ldap.maxobjects)
3269/tcp  open  tcpwrapped
|_unusual-port: tcpwrapped unexpected on port tcp/3269
5985/tcp  open  http          Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-comments-displayer: Couldn't find any comments.
|_http-date: Wed, 24 Feb 2021 16:20:18 GMT; +12m53s from local time.
...
|_    WWW-Mechanize/1.34
|_http-xssed: No previously reported XSS vuln.
|_unusual-port: http unexpected on port tcp/5985
49154/tcp open  msrpc         Microsoft Windows RPC
49155/tcp open  msrpc         Microsoft Windows RPC
49157/tcp open  ncacn_http    Microsoft Windows RPC over HTTP 1.0
|_banner: ncacn_http/1.0
49158/tcp open  msrpc         Microsoft Windows RPC
49170/tcp open  msrpc         Microsoft Windows RPC
Service Info: Host: CASC-DC1; OSs: Windows, Windows 2008 R2; CPE: cpe:/o:microsoft:windows_server_2008:r2:sp1, cpe:/o:microsoft:windows

Host script results:
|_clock-skew: mean: 12m53s, deviation: 0s, median: 12m52s
| dns-blacklist: 
|   SPAM
|     list.quorum.to - SPAM
|   PROXY
|     tor.dan.me.uk - FAIL
|     dnsbl.tornevall.org - FAIL
|_    misc.dnsbl.sorbs.net - FAIL
|_fcrdns: FAIL (No PTR record)
|_ipidseq: Unknown
|_msrpc-enum: Could not negotiate a connection:SMB: Failed to receive bytes: ERROR
|_path-mtu: PMTU == 1500
| qscan: 
| PORT  FAMILY  MEAN (us)  STDDEV   LOSS (%)
| 53    0       16527.00   3969.60  70.0%
| 88    0       17992.50   2192.74  80.0%
| 135   0       17231.20   4966.82  50.0%
| 139   0       15278.40   1837.18  50.0%
| 389   0       14909.25   4378.79  60.0%
| 445   0       13544.25   3127.06  60.0%
| 636   0       15547.33   3427.95  70.0%
|_3268  0       15325.00   3197.92  60.0%
| smb-mbenum: 
|_  ERROR: Failed to connect to browser service: Could not negotiate a connection:SMB: Failed to receive bytes: ERROR
| smb-protocols: 
|   dialects: 
|     2.02
|_    2.10
| smb2-capabilities: 
|   2.02: 
|     Distributed File System
|   2.10: 
|     Distributed File System
|     Leasing
|_    Multi-credit operations
| smb2-security-mode: 
|   2.02: 
|_    Message signing enabled and required
| smb2-time: 
|   date: 2021-02-24T16:20:25
|_  start_date: 2021-02-24T16:15:29

Post-scan script results:
| reverse-index: 
|   53/tcp: 10.10.10.182
|   88/tcp: 10.10.10.182
|   135/tcp: 10.10.10.182
|   139/tcp: 10.10.10.182
|   389/tcp: 10.10.10.182
|   445/tcp: 10.10.10.182
|   636/tcp: 10.10.10.182
|   3268/tcp: 10.10.10.182
|   3269/tcp: 10.10.10.182
|   5985/tcp: 10.10.10.182
|   49154/tcp: 10.10.10.182
|   49155/tcp: 10.10.10.182
|   49157/tcp: 10.10.10.182
|   49158/tcp: 10.10.10.182
|_  49170/tcp: 10.10.10.182
```



## Getting user
Nmap Cheatsheet
======

Nmap Useful commands.
======		
| S.No | Title            | Command Syntax   | What it will do
|:-----:|:----------------|:--------------------|:--------------------|
|1 |    SYN Scan, Half-open    | nmap -sS 192.168.0.1       | TCP 3 way handshake is not completed, Root Privileges require  |
|2 |    TCP Scan, Full Scan    | nmap -sT 192.168.0.1       | TCP 3 way handshake is completed |
|3 |    Xmas Scan              | nmap -sX 192.168.0.1       | Send Packet with FIN,PSH,URG flag set|
|4 |    idle Scan              | nmap -sI ZombieIP TargetIP | Take advantages of incrementing IP identification | 
|5 |    Ping Scan              | nmap -sn 192.168.0.1       | It will do Host Discovery Only. will Skip PORT scan |
|6 |    Do Not Ping            | nmap -Pn 192.168.0.1       | It will skip Host Discovery Only.|
|7 |    No DNS resolution      | nmap -n 192.168.0.1        | Tells Nmap to never do reverse DNS resolution on the active IP addresses it finds | 
 
Nmap Port State.
======		
| S.No | State            | reason   | To remember
|:-----:|:----------------|:------------------------------------------------------------|:--------------------|
|1 |    open            | An application is actively accepting TCP connections, UDP datagrams or SCTP associations on this port| Port is OPEN  |
|2 |    closed          | A closed port is accessible (it receives and responds to Nmap probe packets), but there is no application listening on it  | Port is Closed   |
|3 |    filtered        | Nmap cannot determine whether the port is open because packet filtering prevents its probes from reaching the port | ICMP error messages such as type 3 code 13 (destination unreachable: communication administratively prohibited)  |
|4 |    unfiltered      | The unfiltered state means that a port is accessible, but Nmap is unable to determine whether it is open or closed | Only ACK scan determine this   |
|5 |    open/filtered   | Nmap places ports in this state when it is unable to determine whether a port is open or filtered. This occurs for scan types in which open ports give no response|  UDP, IP protocol, FIN, NULL, and Xmas scans    |
|6 |    closed/filtered |  This state is used when Nmap is unable to determine whether a port is closed or filtered. |idle scan |
 
Nmap Basic commands
======		
| S.No | Title            | Command Syntax   |
|:-----:|:----------------|:--------------------|
|1 |    Scan single IP              | nmap 192.168.0.1     |
|2 |    Scan Host                   | namp scanme.nmap.org |
|2 |    Scan IP range               | namp 192.168.0.1-128 |
|3 |    Scan Subnet                 | nmap 192.168.0.1/24                |
|4 |    Scan targets from Text file |nmap -iL targets.txt|	
|5 |	Scan a single port	        |nmap -p 80 192.168.0.1	|
|6 |	Scan a range of ports	    |nmap -p 20-30 192.168.0.1|	
|7 |	Scan TOP 100 common ports	|nmap -F 192.168.0.1	|
|8 |	Scan all ports	            |nmap -p- 192.168.0.1	|
|9 |	Specify UDP or TCP scan	    |nmap -p U:53,T:80 192.168.0.1	|
|10|	Full Scan (TCP Scan)	    |nmap -sT 192.168.0.1	|
|11|	Half Open Scan (SYN scan)   |nmap -sS 192.168.0.1	|
|12|	Scan UDP ports	            |nmap -sU -p 123,161,162 192.168.0.1|	
|13|	Disable Host Discovery      |nmap -Pn -F 192.168.0.1	|
|14|	Detect OS and Services	    |nmap -A 192.168.0.1	|
|15|	Standard service detection	|nmap -sV 192.168.0.1|	
|16|	Save output to file	        |nmap -oN output.txt 192.168.0.1	|
|17|	Save Output as XML	        |nmap -oX output.xml 192.168.0.1	|
|18|	Save Output in all formats	|nmap -oA allformats 192.168.0.1	|
|19|	Scan using default scripts	|nmap -sV -sC 192.168.0.1|	



Interview question “ Does SYN Scan requires root privileges to perform it” Answer is “ Yes. we need root privileges to perform SYN SCAN”

Reference : https://nmap.org/
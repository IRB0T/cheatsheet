#Nmap
Cheatsheet FOR Nmap
		
| S.No | Title            | Command Syntax   |
|:-----:|:----------------|:--------------------:|
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
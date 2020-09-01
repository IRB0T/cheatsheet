Wireshark Cheatsheet
======

Wireshark Useful commands.
======		
| S.No | Operations            | Command Syntax   |
|:-----:|:----------------|:--------------------|
|1  | Filter By IP                  | ip.addr==192.168.0.1                             |
|2  | Filter By MAC                 | eth.addr==00:07:F4:23:24:25                      |
|3  | Filter By Multiple IPs        | ip.addr==192.168.0.1 and ip.addr==192.168.0.2    |
|4  | Filter By subnet              | ip.addr==192.168.0.1/24                          |
|5  | Filter By Destination IP      | ip.dest==192.168.0.1                             |
|6  | Filter By Source IP           | ip.src==192.168.0.1                              |
|7  | Filter By port                | tcp.port==25                                     |
|8  | Filter By Destination port    | tcp.dstport==25                                  |
|9  | Filter By IP Address and port | ip.addr==192.168.0.1 and tcp.port==25            |
|10 | Filter By IP range            | ip.addr>=192.168.0.1 and ip.addr <= 192.168.0.15 |
|11 | Filter By URL                 | http.host == "host name"                         |
|12 | Filter By hostname            | ip.host == "host name"                           |
|13 | Filter SYN Flag               | tcp.flags.syn ==1                                |
|14 | Filter broadcast filter       | eth.dst == FF:FF:FF:FF:FF:FF                     |
|15 | Filter multicast filter       | (eth.dst[0]&1)                                   |
|16 | Monitor HTTP Web requests     | http.request.method==GET                         |


======
CMD version of wireshark is known as Tshark.
======

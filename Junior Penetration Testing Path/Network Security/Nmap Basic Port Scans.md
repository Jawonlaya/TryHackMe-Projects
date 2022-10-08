-TCP port or UDP port is used to identify a network service running on the host
-HTTP server binds TCP port 80 by default - HTTP
-HTTP server supports SSL/TLS, TCP port 443 - HTTPS
-ports can be reconfigured

-open ports: service listening on that port
-closed ports: no service listening on that port

-firewall might block packets for an open port making it appear closed
-open: service is listening
-closed: no service is listening, port is accessible(reachable & not blocked by firewall or other programs)
-filtered: nmap cant determine if port is open or closed because it is not accessible (packets are blocked)
-unfiltered: nmap cannot determine if port is open or closed, port is accessible (ACK scan)
-open|filtered: nmap cannot determine if port is open or filtered
-closed|filtered: nmap cannot determine if port is closed or filtered

UDP port 53 - DNS
TCP port 22 - SSH
Nmap port states - 6

TCP flags
-TCP header is the first 24 bytes of a TCP segment
1. URG: urgent flag - incoming data is urgent - processed immediately without consideration
2. ACK: acknowledgement flag - acknowledgment number is significant - receipt of TCP segment
3. PSH: push flag - ask TCP to pass the data to the application promptly
4. RST: reset flag - reset the connection
5. SYN: synchronize flag - initiate TCP 3-way handshake
6. FIN: finished flag - sender has no more data to send

TCP 3-way handshake
 --> SYN -->
<-- SYN, ACK <--
--> ACK -->

-unprivileged users are limited to connect scan '-sT'
-default mode is SYN scan - requires root or sudoer
-SYN scan tears down connection once response is received, decrease chances of scan being logged 
-'-sS' option - doesn't need a 3-way handshake

UDP - connectionless protocol
-can not guarantee a service listening on a UDP port would respond to sent packets
-if UDP packet is sent to a closed port, an ICMP port unreachable error (type 3) is returned
-'-sU'
-can be combined with another TCP scan
eg: nmap -sU -F -v [IP]
-ports can be specfied or range given
eg: -p22,80,443
eg: -p1-1025 (inclusive)
eg: -p- (scan all ports)
eg: -F --top-ports 10 (scan the ten most common ports)
-control scan timing
eg: -T<0-5>
0: paranoid
1: sneaky
2: polite
3: normal
4: aggressive
5: insane

-probing parallelization using --min-parallelism <numprobes> * --max-parallelism <numprobes>
eg: --min-parallelism=64

Port Scan Type		Example Command
TCP Connect Scan	nmap -sT 10.10.249.10
TCP SYN Scan		sudo nmap -sS 10.10.249.10
UDP Scan		sudo nmap -sU 10.10.249.10

Option				Purpose
-p-			all ports
-p1-1023		scan ports 1 to 1023
-F			100 most common ports
-r			scan ports in consecutive order
-T<0-5>			-T0 being the slowest and T5 the fastest
--max-rate 50		rate <= 50 packets/sec
--min-rate 15		rate >= 15 packets/sec
--min-parallelism 100	at least 100 probes in parallel

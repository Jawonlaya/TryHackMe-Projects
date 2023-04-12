Wireshark: tool used for creating and analyzing PCAPs(network packet capture files) 

Installation: https://www.wireshark.org/download.html and follow directions
also: apt install wireshark 

Overview: 
Important information:
-Packet Number
-Time
-Source
-Destination
-Protocol
-Length
-Packet Info

Color Codes packets in order of danger level as well as protocol to spot anomalies quickly

-------------------------------------------------------------------------------

Collection Method Overview
-Check correct capturing of traffic
-Check that computer can handle packets and size of network
-Check there is enough disk space to store data

Network Taps
-vampire tap: hardware to tap wire and intercept traffic as it comes across
-Throwing star LAN Tap: an inline network tap, replicates packets as they pass the tap

Mac Floods
-actively sniffing packets
-stress the switch and fill the CAM table
-CAM table will not accept new MAC addresses if table is filled 
-switch will send out packets to all ports of the switch

ARP Poisoning
-actively sniff packets
-redirect traffic from the host(s) to the machine being monitored
-will not stress network like MAC flooding

-----------------------------------------------------------------------------------

Filtering Captures

Packet filtering - sift through very large number of packets

1. and: and/&&
2. or: or/||
3. equals: eq/==
4. not equal: ne/!=
5. greater than: gt/>
6. less than: lt/<

also contains, matches, bitwise_and operators
further reading: https://www.wireshark.org/docs/wsug_html_chunked/ChWorkBuildDisplayFilterSection.html

Basic Filtering
-service or protocol, dot, what is filtered (MAC, SRC, protocol etc)
-filter by IP: ip.addr = <IP address>
-filter by source and distance: ip.src == <SRC IP Address> and ip.dst == <DST IP Address>
-filter by TCP protocols: tcp.port eq <PORT #> or <Protcol Name>
-filter by UDP protocols: udp.port eq <PORT #> or <Protcol Name>

--------------------------------------------------------------------------------------------

Packet Dissection
Physical, Data Link, Network, Transport, Session, Presentation, Application
Double click on packet in capture to open its details

5-7 layers based on OSI model

Layer 1: Physical Layer: capture length in bits and bytes, time of arrival etc
Layer 2: Data layer: source and destination MAC addresses
Layer 3: Network Layer: IPv4 addresses
Layer 4: Transport: UDP/TCP with source and destination ports
Layer 5: Application: HTTP, FTP, SMB etc

--------------------------------------------------------------------------------------------

ARP Overview

-ARP: Address Resolution Protocol - Layer 2 protocol used to connect IP to MAC Addresses
-contain Request(1) and Response(2) messages
-wireshark will identify it as intel_78 - unidentified source
view > Name Resolution > Resolve Physical Addresses (checked)
-double click packet number > Address Resolution Protocol
-important info: Opcode, Sender MAC address, Sender IP address

---------------------------------------------------------------------------------------------


ICMP Overview
-ICMP: Internet Control Message Protocol
-analyze various nodes on a network
-used with ping and traceroute
-IETF documentation: https://tools.ietf.org/html/rfc792
-Traffic Overview: packet details for a ping request packet
Type (8): Request
Type (0): Reply
-important info: timestamp and data (typically random)


----------------------------------------------------------------------------------------------

TCP Traffic
-TCP: Transmission Control Protocol 
-handles the delivery of packets including sequencing and errors
-IETF TCP documentation: https://tools.ietf.org/html/rfc793
-can be used with RSA NEtwitness and NetworkMiner to filter out and further analyze the captures
Acknowldegment number (0): the port was not open

---------------------------------------------------------------------------------------------

DNS Traffic
-DNS: Domain Name service protocol
-used to resolve names with IP addresses
-IETF documentation: https://www.ietf.org/rfc/rfc1035.txt
-Query-Response, DNS-Servers Only, UDP

----------------------------------------------------------------------------------------------

HTTP Traffic
-HTTP: Hypertext Transfer Protocol
-used to send GET and POST requests to a web server to receive things like webpages
-used to Identify SQLi, Web Shells and other web-related attack vectors
-IETF documentation: https://www.ietf.org/rfc/rfc2616.txt
-important info: host, user-agent, requested URI and response
-Statistics > Protocol Hierarchy - organize protocols by percentage of packets and bytes + other info
-Statistics > Endpoints - oragnize endpoints and IPS

----------------------------------------------------------------------------------------------

HTTPS Traffic
-HTTPS: Hypertext Transfer Protocol Secure
-Traffic Overview
1. Client and server agree on a protocol version
2. Client and server select a cryptographic algorithm
3. Client and server can authenticate to each other
4. Creates a secure tunnel with a public key
Load an RSA Key 
Edit > Preferences > Protocols > TLS > [+]

---------------------------------------------------------------------------------------------

Wireshark Documentation: https://www.wireshark.org/docs/

More: https://wiki.wireshark.org/SampleCaptures
Case: 001 PCAP Analysis: https://dfirmadness.com/case-001-pcap-analysis/

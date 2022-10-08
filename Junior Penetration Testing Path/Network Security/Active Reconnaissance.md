Active Reconnaissance
-tools: ping, traceroute, telnet and nc

Active Recon: requires some kind of contact with the target
-signed legal authorization required from client
-begins with direct connection made to the target machine
-connection might leave information in the logs showing the client IP address, time of connection, duration of connection, etc
-not all connections are suspicious

Web Browser
-TCP port 80: HTTP
-TCP port 443: HTTPS
-possible to use custom ports to access a service
-Dev tools ctrl+shift+I (opt+command+I)
	-view and modify JavaScript files
	-inspect cookies
	-discover folder structure of site etc
-addons for firefox and chrome for pen testing
-FoxyProxy: Burp Suite
-User-Agent Switcher and Manager: ability to pretend to access webpage from a different OS or browser
-Wappalyzer: insights about the technologies used on the visited website

Ping
-check whether it is possible to reach remote system and remote system can reach you
-check if remote system is online
1. ping sends a packet (ICMP Echo) to remote system
2. if remote system is online, sends back packet (ICMP Echo Reply)
eg: ping [target IP] - sends constant pings
eg: ping -c 5 [target IP] - send 5 pings to target IP (MS windows system -n)
ICMP = internet control message protocol
ping(ICMP echo/type 8) and ping reply (ICMP echo reply/type 0)
-no ping reply
	-target computer is not responsive
	-target computer is disconnected from network
	-a firewall is configured to block such packets (MS windows firewall blocks ping by default)
	-the testing computer is disconnected from newtork

Traceroute
-traces the route taken by packets from attacker's system to target system
-find IP addresses of routers or hops that a packet traverses
-reveal snumber of routers between the two systems
eg traceroute [target IP] - linux; tracert [target IP] - Windows
-use ICMP to trick routers into revealing their IP addresses - using Time To Live(TTL) in the IP header
-TTL - number of routers/hops that a packet can pass before being dropped
-a router receives packet and decrements ttl by one before passing it to the next router
-if TTL reaches 0, it is dropped and an ICMP TTL exceeded msg sent to original sender
-some routers are configured not to send such ICMP messages when discarding a packet
-hops/routes between attackers and target depend on the time traceroute is run 
-packets may not follow the same route (even on the same network)
-some routers return a public IP
-some routers don't return a reply

Telnet
-developed in 1969 to communicate with remote system via CLI(command line interface)
-Telnet protcol for remote administration
-default port: 23
-sends all data, usernames and passwords in clear text 
-secure alternative (SSH: secure shell) protocol
eg: telnet [target IP] [port]

Netcat
-nc
-supports TCP and UDP protocols
-can act as a server that listens on a port of attackers choice
-can act as a client that connects to a listening port
option	meaning
-l	Listen mode
-p	Specify the Port number
-n	Numeric only; no resolution of hostnames via DNS
-v	Verbose output (optional, yet useful to discover any bugs)
-vv	Very Verbose (optional)
-k	Keep listening after client disconnects
eg: nc [IP] [port]

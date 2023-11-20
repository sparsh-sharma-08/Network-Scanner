# Network-Scanner
Final Project of Disruptive Technologies
# Team Members
1) Sparsh Sharma
2) Saurabh Pandey
3) Jitish Kathuria
4) Aman Karki

# How it works
Scan common ports
Send a TCP Syn packet to the destination on the defined port, if the port is open, use an nmap scan to check the service running on the port and prints all the ports found.

# Discover hosts in network
Uses as a base the router's ip to map all possible ips. It then sends an ICMP packet to each IP, and waits for a response, if it receives any response saved in an array the IP of the online host, and when it finishes checking all hosts, prints all hosts online.

# OS Scan
Sends an ICMP packet to the destination and waits for a response. Then, extracts the TTL from the destination response and checks the possible OS in a list, if have founded, prints it.

OS Support
Windows ✔️
Linux ✔️
Mac ❓

# Arguments
-sC | Scan common ports
-p | Protocol to use in the scan
-i | Interface to use
-t | Timeout to each request
-st | Use stealth scan method (TCP)
-sA | Scan all ports
-p | Protocol to use in the scan
-i | Interface to use
-t | Timeout to each request
-st | Use stealth scan method (TCP)
-sP | Scan a range ports
-p | Protocol to use in the scan
-i | Interface to use
-t | Timeout to each request
-st | Use stealth scan method (TCP)
-sO | Scan OS of a target
-d | Discover hosts in the network
-p | Protocol to use in the scan
-i | Interface to use
# Examples
1) Discover hosts -> astsu -d
2) Scan common ports using SYN Scan-> astsu -sC -st 192.168.1.1
3) Scan a range of ports -? astsu 192.168.1.1 -sP 1 443
4) Scan OS-> astsu -sO 192.168.1.1

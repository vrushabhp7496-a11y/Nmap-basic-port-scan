# Nmap baasic port scan :
### In the previous repositry we saw the host discovery without doing port scan now in this epo we will see following points 
- TCP CONNECT SCAN
- TCP SYN SCAN
- UDP SCAN

---

### TCP connect scan : 
- Before seeing tcp scan lets see some states taht cwe need to know after scan results
   1. Open indicates service is listning on port.
   2. closed indicates no service is listning
   3. Filtered means nmap cannot determine port is open or closed as the port is not accessible.
   4. Unfiltered menas nmap cannot determine port is closed or open although is accessible.
   5. Open|Filtered: This means that Nmap cannot determine whether the port is open or filtered.
   6. Closed|Filtered: This means that Nmap cannot decide whether a port is closed or filtered.

---

### TCP Flags ;
- URG indiactes that incoming data is urgent and should be immediatly processed.
- ACK: Acknowledgement flag indicates that the acknowledgement number is significant. It is used to acknowledge the receipt of a TCP segment.
- PSH asks TCP to pass the data to application promptly.
- RST flag is uesd to rest the connection.it also used to indicate that data is sent to host and there is no service running to recieve it.
- SYN is used to initiate TCP 3 way handshake.
- FIN indiactes that sender has no more data to send.that the connection is closed now.

---



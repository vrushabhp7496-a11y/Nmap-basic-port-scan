# > Nmap baasic port scan :
### In the previous repositry we saw the host discovery without doing port scan now in this epo we will see following points 
- TCP CONNECT SCAN
- TCP SYN SCAN
- UDP SCAN

---

### > TCP status : 
- Before seeing tcp scan lets see some states taht cwe need to know after scan results
1. Open indicates service is listning on port.
2. closed indicates no service is listning
3. Filtered means nmap cannot determine port is open or closed as the port is not accessible.
4. Unfiltered menas nmap cannot determine port is closed or open although is accessible.
5. Open|Filtered: This means that Nmap cannot determine whether the port is open or filtered.
6. Closed|Filtered: This means that Nmap cannot decide whether a port is closed or filtered.

---

### > TCP Flags :
- URG indiactes that incoming data is urgent and should be immediatly processed.
- ACK: Acknowledgement flag indicates that the acknowledgement number is significant. It is used to acknowledge the receipt of a TCP segment.
- PSH asks TCP to pass the data to application promptly.
- RST flag is uesd to rest the connection.it also used to indicate that data is sent to host and there is no service running to recieve it.
- SYN is used to initiate TCP 3 way handshake.
- FIN indiactes that sender has no more data to send.that the connection is closed now.

---


### > TCP connect scan :
- TCP connect scan complete by doing TCP 3way handshake.
- TCP connect scan uses command : nmap -sT target.
- When nmap proces this command request with SYN packet is sent to target server
- In response to SYN a closed port replys with RST/ACK flag.
- In response to SYN a open port replys with SYN/ACK flag.this indiactes that TCP 3way handshake is completed.
- Tis scan is used by unprivileaged users and this is 3 way handshake process



---


### > TCP SYN scan :
- It is default scan mod
- Only privilaged user can use SYN scan
- This scan does not require TCP 3 way handshake once reponse is recieved connect closed by nmap by sending RST flag.
- TCP SYN scan command : nmap -sS target


---

### > UDP scan :
- UDP is connectionless protocol
- it does not require any handshake to establish connection
- It is not guranteed that service listning on UDP port will respond.
- If UDP packet is sent to closed port an ICMP unrechable response is obtained.
- UDP scan command : nmap -sU target

---

### > IMPORTANT COMMAND WITH MEANING :
1. TCP connect scan ; nmap -sT target
2. TCP SYN scan : nmap -sS target
3. UDP scan : nmap -sU targ.
4. Scan all ports : -p
5. Scan port from 1 ti 1023 : -p1-1023
6. For 100 most common ports :-F
7. For scan fastest to slowest : -T<0-5>
8. Max Packet rate equal to 50 or less than 50 : --max-rate 50
9. Min packet rate equal to 50 or more than 50 : --min-rate 50
10. At least 100 probes in parallel : --min-parallelism 100


---

Here in this repo i have demonstrated all the necessary command and explanation regarding TCP scan.

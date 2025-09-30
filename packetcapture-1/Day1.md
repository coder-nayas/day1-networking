# DAY 1 – NETWORKING FUNDAMENTALS & PACKET CAPTURE

## 1. Common Ports
- *80 (HTTP)* – web traffic (unencrypted)
- *443 (HTTPS)* – web traffic (encrypted with TLS/SSL)
- *22 (SSH)* – secure remote login
- *53 (DNS)* – domain name system queries
- *25 (SMTP)* – email transfer

## 2. TCP 3-Way Handshake

Client → Server : SYN
Client ← Server : SYN-ACK 
Client → Server : ACK

This process establishes a reliable TCP connection before data transfer.

## 3. Packet Capture

### HTTP (Port 80)
- Captured a *GET request* to testfire.net.
- Response included HTTP *200 OK* with CSS and image files.
- Example shown in screenshot:  
  - Source: 192.168.43.28 → Destination: 65.61.137.117 (port 80)  
  - Request: GET / HTTP/1.1  
  - Server replies with resources like /images/home3.jpg.

### HTTPS (Port 443)
- Captured a *TCP handshake* (SYN, SYN-ACK, ACK) on port 443.  
- Followed by *TLS handshake* packets (Client Hello, Server Hello, Certificate, etc.).  
- This shows how encryption is negotiated before secure data transfer.

## 4. What I Learned
- Understood the role of *common ports* and the *3-way handshake*.  
- Observed differences between HTTP (plaintext) and HTTPS (encrypted).  
- Learned how to filter packets in Wireshark (http, tcp.port == 80, tcp.port == 443). 

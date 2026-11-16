# EX01 Developing a Simple Webserver
## Date:

## AIM:
To develop a simple webserver to serve html pages and display the list of protocols in TCP/IP Protocol Suite.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
~~~
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>TCP/IP Protocol Suite</title>
</head>
<body>

<h1>TCP/IP Protocol Suite</h1>
<p>The TCP/IP protocol suite is a set of communication protocols used to connect devices on the internet. It is organized into four layers.</p>

<h2>Layers and Protocols</h2>
<table border="1" cellpadding="6" cellspacing="0">
  <tr>
    <th>Layer</th>
    <th>Function</th>
    <th>Protocols</th>
  </tr>
  <tr>
    <td>Application</td>
    <td>Provides network services to user programs</td>
    <td>HTTP, HTTPS, FTP, SMTP, POP3, IMAP, DNS, DHCP, Telnet, SSH</td>
  </tr>
  <tr>
    <td>Transport</td>
    <td>End-to-end communication between processes</td>
    <td>TCP, UDP</td>
  </tr>
  <tr>
    <td>Internet</td>
    <td>Addressing and routing of packets</td>
    <td>IP (IPv4, IPv6), ICMP, ARP, IGMP</td>
  </tr>
  <tr>
    <td>Network Access (Link)</td>
    <td>Transmission of frames over physical media</td>
    <td>Ethernet, Wi-Fi, PPP</td>
  </tr>
</table>

<h2>TCP (Transmission Control Protocol)</h2>
<ul>
  <li>Connection-oriented</li>
  <li>Reliable delivery using acknowledgements and retransmission</li>
  <li>Ordered delivery using sequence numbers</li>
  <li>Flow control and congestion control</li>
  <li>Connection setup using a three-way handshake</li>
</ul>

<h3>Three-Way Handshake</h3>
<ol>
  <li>SYN: client asks to open a connection</li>
  <li>SYN-ACK: server accepts and replies</li>
  <li>ACK: client confirms, and data transfer begins</li>
</ol>

<h3>TCP Header Fields</h3>
<table border="1" cellpadding="6" cellspacing="0">
  <tr><th>Field</th><th>Size</th></tr>
  <tr><td>Source Port</td><td>16 bits</td
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',880)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
~~~
## OUTPUT:
<img width="1252" height="905" alt="Screenshot 2026-11-14 160347" src="https://github.com/user-attachments/assets/ebf731dc-21f2-499d-a28d-f4a73ab3ec86" />

<img width="900" height="276" alt="Screenshot 2026-11-14 160845" src="https://github.com/user-attachments/assets/9a187f88-7739-4a15-9e9c-4756bb347c67" />



## RESULT:
The program for implementing simple webserver is executed successfully.


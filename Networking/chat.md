# Mini Chat Application using 2 Terminals
---
<br></br>

## Using Netcat to establish the connection between client and server using Loopback Interface
---
**Creating Server using Netcat:**<br>
*command:* <code> nc -l 12345 </code>
![Server](https://github.com/safiuddin786/zemosolabs/blob/master/Screenshots/Networking/serverstart.png?raw=true)<br></br>

**Connecting Client using Netcat:**<br>
*command:* <code> nc localhost 12345 </code>
![Server](https://github.com/safiuddin786/zemosolabs/blob/master/Screenshots/Networking/clientstart.png?raw=true)<br></br>

**Send message via Terminal**<br>
*client:*
![Server](https://github.com/safiuddin786/zemosolabs/blob/master/Screenshots/Networking/client.png?raw=true)<br></br>
*server:*
![Server](https://github.com/safiuddin786/zemosolabs/blob/master/Screenshots/Networking/server.png?raw=true)<br></br>

**Ending the Connection Using Ctrl+d or Ctrl+c**<br>
*client:*
![Server](https://github.com/safiuddin786/zemosolabs/blob/master/Screenshots/Networking/clientclose.png?raw=true)<br></br>
*server:*
![Server](https://github.com/safiuddin786/zemosolabs/blob/master/Screenshots/Networking/serverclose.png?raw=true)<br></br>
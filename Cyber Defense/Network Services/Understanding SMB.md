# Understanding SMB

### What is SMB?

SMB - `Server Message Block Protocol` - is a client-server communication protocol used for sharing access to files, printers, serial ports and other resources on a network.

Servers make file systems and other resources (printers, named pipes, APIs) available to clients on the network. Client computers may have their own hard disks, but they also want access to the shared file systems and printers on the servers.

The SMB protocol is known as a response-request protocol, meaning that it transmits multiple messages between the client and server to establish a connection. Clients connect to servers using TCP/IP (actually NetBIOS over TCP/IP as specified in RFC1001 and RFC1002), NetBEUI or IPX/SPX.

How does SMB work?

![Screenshot 2023-05-30 at 17 50 41](https://github.com/Jawonlaya/TryHackMe-Projects/assets/115058054/4b391859-ce36-4694-8593-6bdb0678f037)

Once they have established a connection, clients can then send commands (SMBs) to the server that allow them to access shares, open files, read and write files, and generally do all the sort of things that you want to do with a file system. However, in the case of SMB, these things are done over the network.

What runs SMB?

Microsoft Windows operating systems since Windows 95 have included client and server SMB protocol support. Samba, an open source server that supports the SMB protocol, was released for Unix systems.

#### Challenge

```markdown

1. What does SMB stand for? - Server Message Block 
2. What type of protocol is SMB? - response-request
3. What do clients connect to servers using? - TCP/IP
4. What systems does Samba run on? - Unix
```

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

# Enumerating SMB

Lets Get Started

Before we begin, make sure to deploy the room and give it some time to boot. Please be aware, this can take up to five minutes so be patient!

## Enumeration

Enumeration is the process of gathering information on a target in order to find potential attack vectors and aid in exploitation.

This process is essential for an attack to be successful, as wasting time with exploits that either don't work or can crash the system can be a waste of energy. Enumeration can be used to gather usernames, passwords, network information, hostnames, application data, services, or any other information that may be valuable to an attacker.

## SMB

Typically, there are SMB share drives on a server that can be connected to and used to view or transfer files. SMB can often be a great starting point for an attacker looking to discover sensitive information — you'd be surprised what is sometimes included on these shares.



### Port Scanning

The first step of enumeration is to conduct a port scan, to find out as much information as you can about the services, applications, structure and operating system of the target machine.


## Enum4Linux

Enum4linux is a tool used to enumerate SMB shares on both Windows and Linux systems. It is basically a wrapper around the tools in the Samba package and makes it easy to quickly extract information from the target pertaining to SMB. It's installed by default on Parrot and Kali, however if you need to install it, you can do so from the official github.

The syntax of Enum4Linux is nice and simple: "enum4linux [options] ip"

```markdown

TAG            FUNCTION

-U             get userlist
-M             get machine list
-N             get namelist dump (different from -U and-M)
-S             get sharelist
-P             get password policy information
-G             get group and member list

-a             all of the above (full basic enumeration)

Now we understand our enumeration tools, let's get started!
```

#### Challenge

```markdown
1. Conduct an nmap scan of your choosing, How many ports are open? - 3
2. What ports is SMB running on? - 
3. Let's get started with Enum4Linux, conduct a full basic enumeration. For starters, what is the workgroup name? - Workgroup
4. What comes up as the name of the machine? - POLOSMB
5. What operating system version is running? - 6.1
6. What share sticks out as something we might want to investigate? - profiles
```

## Exploiting SMB


Coming soon!

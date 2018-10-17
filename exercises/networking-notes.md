## Introduction to Networking Notes
“Before you can tackle any relevant security issue on a network, you’ll need a basic understanding of networking.”

### Networks 
The basic history goes a little something as follows:

In the 1970s and 1980s, people working at universities around the world wanted to send each other data and messages using their computer-to-computer connections. 
Since the cost for each connection was so high and increased with distance, computers generally only had connections to other nearby computers. 
But if the computer that you were connected to was connected to another computer and that computer in turn was connected to another computer, and so on, you could send a message a long distance as long as each of the computers along the route of the message agreed to store and forward your message.

The most important innovation that allowed messages to move more quickly across a multi-hop network was to break each message into small fragments and send each fragment individually. In networking terms, these pieces of messages are called “packets”

However,

In order to send messages quicker and more efficiently, computers began storing messages in smaller pieces called packets.
Breaking the message into packets greatly reduced the amount of storage needed on the computers in the middle
As networks moved away from the store-and-forward approach, they started to include special-purpose computers that specialized in moving packets.

These were called IMP’s but, later these computers dedicated to communications were called “routers” because their purpose was to route the packets they received towards their ultimate destination
To connect any computer to the network, now all you needed to do was connect it to one router and then the rest of the communication details were handled by the other routers.

As the story goes,

Now that multiple computers at one location can be wired together (LAN), you could connect a router to it. By sending data through the router, all the computers on the local area network could send data across the “Wide Area Network” (or WAN).
The core of the Internet is a set of cooperating routers that move packets from many sources to many destinations at the same time. Each computer or local area network is connected to a router that forwards the traffic from its location to the various destinations on the Internet.

The term “Internet” comes from the idea of “internetworking”, which captures the idea of connecting many networks together. Our computers connect to local networks and the Internet connects the local networks together so all of our computers can talk to each other.

#### Networking devices
* Router
* Wireless Router
* Switch
* Hub
* Modem
* Firewall
* IDS/IPS
* DMZ

#### Cabling
* Coaxial
* Console
* Unshielded Twisted Pair (UTP)
 * Crossover
 * Straight-through
 

#### OSI Model
Open System Interconnection (OSI) model 

Defines a networking framework to implement protocols in seven layers. 
The OSI model is a layered model that describes the steps to be used to transfer data over a transmission medium from one networked device to another.

It conceptually divides computer network architecture into 7 layers in a logical progression.
Think of the seven layers as the assembly line in the computer.  

At each layer, certain things happen to the data that prepare it for the next layer.


### IP Addresses

[Original request for comment documenting the creating of IP](https://tools.ietf.org/html/rfc791)
- 4th version of the Internet Protocol but the first deployed
- 32 bit value that uniquely identifies the system on the network.
- Looks similar to 192.168.1.0
- Connectionless protocol or Best effort – Which means it does not guarantee delivery  but uses protocols like TCP to guarantee delivery
- 4,292,967,296 possible addresses

Terminology
- Bit- one digit either a 1 or 0
- Byte- 8 bits
- Octet- 8 bit binary number (used interchangeably with byte)
- Network address- address router uses to send packets to 
- Broadcast address- Used by all applications and hosts to send information to all hosts on a network 
- Network ID and Host ID – parts of the IP address
- Subnet Mask – determines the number of bits that make up the Network ID & the Host ID


Public and Private
10.0.0.0 /8 or 10.0.0.0 to 10.255.255.255
172.16.0.0 /12 or 172.16.0.0 to 172.31.255.255
192.168.0.0 /16 or 192.168.0.0 to 192.168.255.255

Network Address
The network address represents all the devices on the same network
Always the first IP address in the range
192.168.1.0
Every machine on the network shares the network address as part of its individual IP address

Broadcast Address 
Always the last address in the range.
192.168.255.255
An IP Address that allows information to be sent to all machines on a given subnet rather than a specific machine


Binary -> Decimal

11011000.00111010.11000011.01001110

216 .58.195.78

01001000. 11110111. 11110100. 01011000

72.247.244.88

Decimal -> Binary 

192.168.254.1

11000000.10101000. 11111110. 00000010

172.217.11.174

10101100. 11011001. 00001011. 10101110



Resources:
[Network+ Book](https://drive.google.com/drive/folders/1k8wXbwzGgxt4mYBR40X9S3MRj4huRluk?ogsrc=32)
[Presentation]
[IP address practice](https://drive.google.com/drive/folders/1k8wXbwzGgxt4mYBR40X9S3MRj4huRluk?ogsrc=32)


#### Subnetting
Now that we know how to define networks we need to learn how to take one network address and create multiple networks from it.

Subnetting:
- Reduces network traffic
- Divides up a network into smaller parts for faster and easier communication
- Easier management (It is easier to isolate issues in small networks than one gigantic one and It also enables an administrator to implement security policies such as which subnets are allowed or not allowed to communicate together.)

Answer these 5 questions:

1. How many subnets does the chosen subnet mask produce?
2^x (x=1)
2. How many valid hosts per subnet are available?
2^y – 2  (y=0)
3. What are the valid subnets?
4. What’s the broadcast address of each subnet?
5. What are the valid hosts in each subnet?


Example:
Subnet `192.168.10.0/25`
1. Write out subnet mask
`The last byte = 10000000 
255.255.255.128 = Subnet Mask 
192.168.10.0 = Network Address`
2. How many Subnets are ther (2^x x=1’s)
`2^1 = 2 subnets`
3. How many hosts per subnet (2^y – 2 y=0’s)
`2^7 = 126 hosts`
4. What are valid subnets (256 – B B= last byte)
`256-128 = 128
So the blocks are going to be 0, 128`
5. What is the broadcast address for each?
`The number right before the next subnet
127 and 255`
6.	What are valid hosts?
`0-127 and 128-255
1-126 and 129 – 254`

Subnet		0	128
First host	1	129
Last Host	126	254
Broadcast 	127	255



#### Ports
* Both TCP and UDP must use port numbers to communicate with the upper layers becuase they are what keeps track of different simultaneous conversations by the local host.
* Ports numbered 0-1024 are the most common ports and are reserved
* Ports > 1034 are generally free to be used and are often used by the higher layers


#### Protocols
 There are 4 main groups the protocols can be broken down into:
  - Connectivity
  - Encryption
  - Application
  - Email

**UDP**
Resolves hostnames – specifically, internet names such as www.develague.com to the corresponding IP address

   
#### Wireshark
Wireshark is a network protocol analyer and monitors traffic on your network. 

#### Command Line Tools
We can find out a lot of networking information now that we know so much, using the command line.

Windows Comamnds 

- arp / dig
- getmac - gves you the mac address
- ipconfig / ifconfig
- netstat - Used to show any protocol connection information
 - netstat -ano
- net statistics workstation 
- net session - Display the computers that are connected to your system through Windows file sharing
- netcat
- nslookup
- ping
- pathping
- tasklist - monitors the processes running on the system
- taskkill - used to kill processes
 - taskkill /IM notepad.exe /F
- tracert
- tcpdump
- whoami - Find out who you are logged in as







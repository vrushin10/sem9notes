### TCP/ip protocol suit
![[Pasted image 20231003020656.png]]
**physical layer** - this layer defines the physical characteristic of the transmission as data rate and signal encoding and scheme
**Datalink Layer** - this layer defines the protocols to manage the links , establish links, transferring data to upper layers and to disconnect the link
there 2 sub layers 
	- medium access control(MAC) layer
	- Logical link control(LLC) layer
Transport layer - provides end to end data transfer service between 2 systems .there are 2 types 
	- tcp(Transmition Control Protocol) - for secure application and is connection oriented 
	- udp(User Datagram Protocol) - for application that require less over head like voice over IP
application layer consists of the applications using the communication over the internet like voice over ip

### tcp vs udp
![[Pasted image 20231003021407.png]]

### FTP vs TFTP
![[Pasted image 20231003021445.png]]

### source code vs object code
![[Pasted image 20231003021513.png]]


### big vs small endian

Little and big endian are two ways of storing multibyte data-types ( int, float, etc). In little endian machines, last byte of binary representation of the multibyte data-type is stored first. On the other hand, in big endian machines, first byte of binary representation of the multibyte data-type is stored first

### ping port 
**ping does not have a port number.** Ping uses the Internet Control Message Protocol (ICMP), which is a different protocol than TCP and UDP, which are the protocols that use port numbers.

instead of port a uinque pid is used to identify ping process, client can use this pid to match with the reply of the request  


### Programing model of 8085
![[WhatsApp Image 2023-10-02 at 19.13.49_ca9d98f7.jpg]]


### what is network byte order
Ports and addresses are usually specified by calls using the network byte ordering convention. Network byte order is also known as big endian byte ordering, where the high order byte defines significance. Network byte ordering allows hosts using different architectures to exchange address information. Use accept(), bind(), htonl(), htons(), ntohl(), and ntohs() for more information on network byte order.


### )What is the difference between $ ping 127.0.0.1 and C:// ping 127.0.0.1
**Windows:**

- The default ping size is 32 bytes.
- The ping command sends four packets by default.
- The ping command uses the ICMP protocol, but it does not use any specific ICMP message type.

**Linux:**

- The default ping size is 64 bytes.
- The ping command sends continuous packets by default until it is stopped.
- The ping command uses the ICMP echo request and echo reply messages.


### What is null modem 
a null modem is a special type of cable or adapter that allows two computers or devices to communicate directly over a serial connection without the need for modems or other communication equipment. It "crosses over" transmit and receive lines to enable direct data exchange. It's often used for data transfer, serial communication, debugging, and console connections in networking and IT.


### How to store multibyte 
To store multi-byte data, use arrays, data structures, or serialization libraries, depending on your programming language and data format. When working with binary data, consider endianness for consistent storage. In databases, use appropriate data types for multi-byte data storage. Ensure proper memory management when necessary. For text data, consider character encoding like UTF-8.

### 0.0.0.0 vs 127.0.0.1(Localhost)
0.0.0.0 is multicast address that binds to all the network adaptors
127.0.0.1 is is a unicast address and does not bind to any network adaptor

y, "0.0.0.0" is used for routing and binding to all available network interfaces, while "127.0.0.1" is the loopback address for local network communication, testing, and running network services locally


intel HEX format 
![[Pasted image 20231003023051.png]]
:LLAAAATTDDDDDDCC

L = length in the number of bytes(1 byte)
A = Start Address(2 byte)
T = Type(1 byte)
D = Data to be loaded(1 or >)
C = check sum(2 byte)
Intel HEX file format is a text-based format that is used to store and transfer binary data.
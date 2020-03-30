# PPP
Point to Point Protocol == dial up access (DSL) from client to ISP uisng PPPoE || PPPoA

PPP provides data-link connection between 2 routers, it can provide authentication, encryption, and compression.

# LCP

LCP, Link Control Protocol to establish, configure, and test the link as well as negotiate settings, options and the use of features.

# Establishment of PPP in Physical Network

- [x] Serial Cable or Phone Line

- [x] Smart Phone

- [x] SONET (optical fiber)

- [x] Special Radio Link

# Life Cycle

1. dead

2. establish

3. auth

4. data transport while the network protocol invoked.

5. terminate

# Auth

Peer routers exchange auth messages. Two auth choices are Password Authentication Protocol (PAP) and Challenge Handshake Authentication Protocol (CHAP). 

Auth's Work Principle

https://github.com/QueenieCplusplus/DataStorage_Hadoop#key-in-session-加密的安全通訊技術


# Encrypto 

https://github.com/QueenieCplusplus/Cipher_Crypto

# Compression

Increases the effective throughput on PPP connections by reducing the amount of data in the frame that must travel across the link. Then decompress at destination.

# PPP frame (within datagrame)

* Structure


|    flag   |broadcast_addr|    control     |  protocol |  info  | pad| Checksum|      
|-----------|--------------|----------------|-----------|--------|----|---------|
|begin & end|      0xFF    |                |  PPP ID   |datagram| opt|         |


* Encapsulation

|    flag   |    addr    |    control     |     protocol |  info  | pad| Checksum|      
|-----------|------------|----------------|--------------|--------|----|---------|
|           |            |                |              |        |    |         |

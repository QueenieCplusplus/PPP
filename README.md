# PPP
Point to Point Protocol == dial up access (DSL) from client to ISP uisng PPPoE || PPPoA

PPP provides data-link connection between 2 routers, it can provide authentication, encryption, and compression.

And PPTP (point to point tunneling protocol) is for hosts, not for 2 routers ~

# LCP (Layer2) to establish Link

LCP, Link Control Protocol to establish, configure, and test the link as well as negotiate settings, options and the use of features.

# Layer3 config

* IPCP, Internet Protocol Control Protocol 

* IPXCP, Internetwork Packet Exchange Control Protocol 

* ATCP, AppleTalk Control Protocol

* IPv6CP, Internet Protocol Version 6 Control Protoco will see extended use in the future (when IPv6 replaces IPv4 as the dominant layer-3 protocol).

# Establishment of PPP in Physical Network

- [x] Serial Cable or Phone Line

- [x] Smart Phone

- [x] SONET (optical fiber)

- [x] Special Radio Link

# Life Cycle

1. dead

2. establish

3. auth using PAP

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


|    flag   |broadcast_addr|    control |  protocol |  info  | pad| Checksum| flag |      
|-----------|--------------|------------|-----------|--------|----|---------|------|
|begin & end|      0xFF    |            |  PPP ID   |datagram| opt|         |      |


* Encapsulation

|    flag   |broadcast_addr    |    control     |     protocol |  info  | pad| fcs|      
|-----------|------------------|----------------|--------------|--------|----|----|
|           |                  |                |              |        |    |    |

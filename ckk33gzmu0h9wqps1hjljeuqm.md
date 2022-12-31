# The Web: TCP, UDP

## Introduction
According to  [Wikipedia](https://en.wikipedia.org/wiki/World_Wide_Web) , The World Wide Web (WWW), commonly known as the Web, is an information system where documents and other web resources are identified by Uniform Resource Locators (URLs, such as https://google.com/ ), which may be interlinked by hypertext, and are accessible over the Internet.
The Web is everywhere. You are reading this article on the web, when you tweet, you are accessing the web, when you access you email, you are accessing the web.
## Goal
By the end of this article you should be able to understand how the web works in relation to TCP and UDP
## Let’s delve in
For the devices on the internet to communicate, all the devices have to be uniquely identifiable and this is done using the IP (Internet Protocol)
Internet Protocol
An IP address is a label attributed to a device on the internet that allows the device to be uniquely identifiable and hence able to communicate with other devices on the internet. An example of an IP address is 66.249.66.213. The IP is responsible for transmitting data from one device to another but it is not responsible for checking if the data is sent correctly, such functionality is handled either by the following:
## Transmission Control Protocol (TCP)
This is a standard that ensures that the data transmitted by the IP is correct. The TCP specifies how data is transmitted and ensures that the transmitted is in the right order and complete, so you don’t send “Computer” and the receiver receives “Compu” or “oCertmup”.Simply put the protocol establishes a connection between sender and receiver before data is transmitted till after it is transmitted.
## User Datagram Protocol (UDP)
The UDP, is a communication protocol used across the Internet for especially time-sensitive transmissions such as video playback or DNS lookups. It speeds up communications by not formally establishing a connection before data is transferred. This allows data to be transferred very quickly, but it can also cause data to become lost in transit
## Hypertext Transfer Protocol (HTTP)
HTTP is a protocol which allows the fetching of resources, such as HTML documents. It is the foundation of any data exchange on the Web and it is a client-server protocol, which means requests are initiated by the recipient, usually the Web browser. A complete document is reconstructed from the different sub-documents fetched, for instance text, layout description, images, videos, scripts, and more.
## Quick UDP Internet Connections (QUIC)
QUIC is a new encrypted-by-default Internet transport protocol, that provides a number of improvements designed to accelerate HTTP traffic as well as make it more secure, with the intended goal of eventually replacing TCP on the web.
## WebSockets
The WebSocket Protocol enables two-way communication between a client running untrusted code in a controlled environment to a remote host that has opted-in to communications from that code. The security model used for this is the origin-based security model commonly used by web browsers. The protocol consists of an opening handshake followed by basic message framing, layered over TCP. The goal of this technology is to provide a mechanism for browser-based applications that need two-way communication with servers that does not rely on opening multiple HTTP connections.
## gRPC
gRPC is a technology for implementing RPC APIs that uses HTTP 2.0 as its underlying transport protocol. You might expect that gRPC and HTTP would be mutually exclusive, since they are based on opposite conceptual models. gRPC is based on the Remote Procedure Call (RPC) model, in which the addressable entities are procedures, and the data is hidden behind the procedures. HTTP works the inverse way. In HTTP, the addressable entities are “data entities” (called “resources” in the HTTP specifications), and the behaviors are hidden behind the data — the behavior of the system results from creating, modifying, and deleting resources.
## What’s next
Now that we have understand the protocols that specifies how devices on a network are identified and data transmitted, I will explain how that data is stored on the internet — web servers in the next article, I will explain what web servers are and how they work.
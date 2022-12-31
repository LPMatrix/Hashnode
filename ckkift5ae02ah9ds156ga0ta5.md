# The Web: Proxies

## Introduction
In the  [previous article](https://matrix.hashnode.dev/the-web-web-servers) , I explained web servers and how they work, since we have understood the storage and exchange of data on a network, I will explain how that  process can be made faster, more secure  and resilient-  **proxies**.

## Goal
By the end of this article you should be able to understand proxies, load balancer and load balancing algorithms.
## Let's delve in
### Proxy server (forward proxy)
This is a web server that acts as a gateway between a client application, for example, a browser, and the real server. It makes requests to the real server on behalf of the client or sometimes fulfills the claim itself. 
### Reverse Proxies
A reverse proxy server is a type of proxy server that typically sits behind the firewall in a private network and directs client requests to the backend server. 

*The difference between a forward and reverse proxy is subtle but important. A forward proxy sits in front of a client and ensures that no origin server ever communicates directly with that specific client. On the other hand, a reverse proxy sits in front of an origin server and ensures that no client ever communicates directly with that origin server.*

**A use case for a reverse proxy is load balancing**

#### Load balancing
Load balancing refers to efficiently distributing incoming network traffic across a group of backend servers, also known as a server farm or server pool.

#### Load balancer
A load balancer distributes incoming client requests among a group of servers, in each case returning the response from the selected server to the appropriate client.

**Deploying a load balancer makes sense only when you have multiple servers, it often makes sense to deploy a reverse proxy even with just one web server or application server.**

### Load Balancing Algorithm
#### Round Robin
This technique involves a simple method of load balancing servers. Multiple identical servers are used to deliver the same services. Each one is configured to use the same internet domain name, but they’re given unique IP addresses. A DNS server stores all the IP addresses and the corresponding domain name. When requests for the IP address associated with the domain name is received, the address is returned in a rotating sequential manner.

#### Least Connections
New connections are sent to the server that currently has the least number of outstanding concurrent connections. 

#### Source IP hash
Combines the source and destination IP address in a request to generate a hash key, which is then designated to a specific server. This lets a dropped connection be returned to the same server originally handling it.

*The list of load balancing algorithms above is non-exhaustive*

## What's next
Now that we have understand how information are stored on the internet, I will explain how the process of the client requesting data from the server could be made faster  -  **caching**.

# The Web: Web Servers

## Introduction
In the  [previous article](https://matrix.hashnode.dev/the-web-tcp-udp) , I explained IP and its protocols and since we have understood the protocols that specifies how devices on a network are identified and data transmitted, I will explain how that data is stored on the internet - web servers.

## Goal
By the end of this article you should be able to understand how the web works in relation to web servers.
## Let's delve in
A web server is a computer hardware or software or combination of both that runs websites. It distributes web pages as they are requested. The basic objective of the web server is to store, process and deliver web pages to the users. This intercommunication is done using Hypertext Transfer Protocol (HTTP). A web server also supports SMTP (Simple Mail transfer Protocol) and FTP (File Transfer Protocol) protocol for emailing and for file transfer and storage respectively. Common examples of web servers include Apache, Ngnix and IIS.

A web server **listens **on a **port **for a **request **sent via a **transfer protocol** and sends a **response **containing the requested **resource**

Contents from the web server can either be **static **or **dynamic**.
### Static Content
Static contents don't change - same thing is shown to all users, e.g about us page and contact page. These pages are usually html only, with no database.

### Dynamic Content
Dynamic contents, like the name suggests change based on certain condition such as content changing based on user logged in, e.g profile page and ecommerce order page. These pages usually load different data from the database.

The language (protocol) spoken between the web server and the web browser is the  [HTTP](https://matrix.hashnode.dev/the-web-tcp-udp) and for efficiency sake the number of requests sent to the server should be reduced, hence the need for **HTTP E-Tags**

### HTTP E-Tag
Entity tags (E-Tags) are used in HTTP headers to manage web caching behavior. They provide a way for web clients to determine if their cache content matches the content on the web server. If the E-Tag for a particular resource (such as a html file) do not match, the web client sends a request to the server to download the most recent version.

As discussed earlier, one usually need a database to serve dynamic content. A database could either be SQL(relational) or NoSQL.

### SQL (relational)
Relational database are table-based i.e they contain rows and columns. An example is  [MySQL](https://www.mysql.com/) 

### NoSQL
These are document-based or graph-based or key-value based. They don't use tables to store data. An example is  [MongoDB](https://www.mongodb.com/) 

To create a functional and reliable database, some guidelines must be followed and this is called ACID, a mnemonic for **Atomicity**, **Consistency**, **Isolation**, **Durability**

A database transaction symbolizes a unit of work performed within a database management system against a database, and treated in a coherent and reliable way independent of other transactions.

### Atomicity
The "all or nothing" property of transactions. A transaction will either commit or abort. If a transaction commits, all of its effects remain; if it aborts, all of its effects are undone.

### Consistency
A transaction always transforms the state of the system from one consistent state to another. As a result, any single transaction (or any sequence of transactions) leaves the system in a consistent state.

### Isolation
The isolation portion of the ACID Properties is needed when there are concurrent transactions. Concurrent transactions are transactions that occur at the same time. The safeguards used by a database to prevent conflicts between concurrent transactions are a concept referred to as isolation.

### Durability
This ensures that once a transactions is completed successfully, it will be stored onto a server/hard disk and will persist.

## What's next
Now that we have understand how information are stored and served on the internet, I will explain how the process of the client requesting data from the server could be speed up and made secure - proxies.

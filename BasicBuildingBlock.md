# IP 

* IP stands for Internet Protocol
* To connect any web app we need IP address
* IANA(internet assigned numbers authority) created IP address
* There are two type of IP Address

    * IPv4 
    * IPv6

`IPv4 is very popular in networking.IPv6 was 128 bit and difficult to remember so very less adopatation happened`

## Classification of IPv4

1. Class A

    * It Ranges from 0 - 127 (0.0.0.0 - 127.255.255.255)
    * It is reserved for local system. It means (10.0.0.0 - 10.255.255.255 is local network and cannot expose outside the network (e.g - LAN Network))

1. Class B

    * It Ranges from 128 - 191 and used for Internet

1. Class C
 
    * It Ranges from 192-223
    * (192.168 is local network)

1. Class D

    * It Ranges from 224-239 (Not used / Reserved)

1. Class E

    * It Ranges from 240 -255 (not used)


## Port

* It is entry point to the application
* We have 65535 numbers of port

| Port | Description |
|------|-------------|
|0-1023| They are reserved port by System |
|1024 - 49150 | Application Port - you can run your application using anyone of this port. (3000-9999) is used by node application |
|49151 -65535 | Open port |

`We need IP address and port to connect any application e.g 102.203.229.255:5542`

## Web Port

* http use port 80 this is default.
* https use port 443.

## Http Verbs

1. Get - Job of get is to fetch data
1. Post - Job of post is to send data to server
1. Put - Job of post is to send data to server to update or create a resource.
1. Delete - Delete the resource at specific url
1. Option - query
1. Head - query

## HTTP Header

 Any request which sends to server or any request that comes from server will have header.

 <b>Request Header</b> - This type of headers contains information about the fetched request by the client.
 <br>
<b>Response Header</b> - This type of headers contains the location of the source that has been requested by the client.

## HTTP Ports

|port number| Description|
|-----------|------------|
|100||
|200| All the successful request and response show this (200,201,202 series)|
|300| For any kind of migration we use this port (301,302,..)|
|400| It is use for user authentication or user check (for eg :- 404 Page not found)|
|500| It means server has some issue |

## Software License

* Any software development cannot happen without license
* Apache 2.0
* MIT
* BSD
* GPL
* Mozilla

## Database

* Collection of information that can be store, update and delete. There are two type:-
1. Relational - use table format

    * MySql
    * Postgre Sql
    * Maria BD

1. Non Relational - use schema (or simple team structure)

    * Mongo DB
    * Redis
    * Cassandra
    * NeoJS
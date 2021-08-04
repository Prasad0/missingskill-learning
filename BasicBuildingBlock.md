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


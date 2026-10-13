Routing Analysis



Objective = the objective of this lab is to understand how a computer decides where to send network traffic.



I will inspect the routing table and identify the default gateway and directly connected networks.



Environment



* Operating System: Windows
* Tool: Command Prompt, route print
* Command: route print
* Protocol: Routing





The routing table contains information that helps Windows choose where to send network packets.



Results



After using the command "route print" in Command Prompt, a routing table appeared with every active route of IPv4 connections showing: network destionation, netmask, gateway, interface and metric. Below a sanitized example of a default route:



Parameter           |  Value



Network destination | 0.0.0.0

Netmask             | 0.0.0.0

Gateway             | 192.168.10.1

Interface           | 192.168.10.50

Metric              | 35





The command also displayed IPv6 routes. This shows that Windows maintains routing information for both IPv4 and IPv6, depending on the network configuration.



Analysis



The routing table helps Windows decide where to send network packets.The default route uses 0.0.0.0 as the network destination and 0.0.0.0 as the netmask. It is used when no more specific route matches the destination. The gateway is the next device that receives packets when traffic needs to leave the local network. There are several routes displayed on the routing table, some of them have an "on-link" route which means that the destination is directly reachable through a local network interface. The route print command makes it possible to inspect these routes and understand how Windows handles network traffic.



Conclusion



In this lab, I used the route print command to inspect the routing table on Windows. I identified the default route and learned how the default gateway is used to send traffic outside the local network, after analyzing all the other routes displayed. I also learned that On-link routes are used for destinations that Windows considers directly reachable through a local interface.The command displayed both IPv4 and IPv6 routing information, which shows that Windows can maintain separate routing information for both protocols.




TCP and UDP Analysis



Objective= the objective of this lab is to check TCP and UDP information on a Windows computer and understand the difference between these two protocols.



Environment



* Operating System: Windows



* Tools: PowerShell, Get-NetTCPConnection, Get-NetUDPEndpoint



* Protocols: TCP and UDP



Result 



After using the command Get-NetTCPConnection, a list of various TCP Connections appeared, showing the local address, local port, the remote address and remote port and, finally, the state of the connection of each. I chose an established connection state with sanitized data as an example of my representation:



Parameter      |    Value



Local Address  |    192.168.10.50

Local Port     |   52000

Remote Address |   203.0.113.25

Remote Port    |  443

State          |  Established Internet







After using the command Get-NetUDPEndpoint, the result must be a list of local addresses and local ports. A local UDP endpoint was found using an IPv6 link-local address. The sanitized example below:





Parameter    |    Value



Local Address|  fe80::1234:5678:abce%4

Local Port   | 53000





Analysis



The Get-NetTCPConnection command showed an established TCP connection:



* The local port was 64947.



* The remote port was 443.



* The Established state means that the TCP connection was established.



Port 443 is commonly used for HTTPS traffic. However, the port number alone does not identify the exact website or application. The local port is used by the computer, while the remote port belongs to the remote endpoint. TCP establishes a connection and provides mechanisms for reliable data delivery. 



The Get-NetUDPEndpoint command showed a local UDP endpoint using an IPv6 link-local address.A link-local IPv6 address is used for communication on the local network link.The command displays local UDP endpoints, but it does not show the remote destination for every endpoint. UDP does not require a TCP connection.



TCP and UDP both use port numbers in order to identify the services associated with network traffic.



Conclusion



In this lab, I used Powershell to inspect both TCP and UDP connections. I identified local and remote ports, overviewing all the states of every connection of my result (not only established but also TimeWaite, Listen, Bound, etc.). 


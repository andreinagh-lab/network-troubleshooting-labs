IP Configuration Analysis



Objective



The objective of this lab is to analyze a device's IPv4 network configuration and understand the role of the IP address, subnet mask, default gateway, DHCP server, and DNS servers.



Environment



* Operating System: Windows



* Tools: PowerShell, Command Prompt



* Network type: Local Area Network (LAN)





To inspect the local network configuration, the following command was used using the above mentioned tools: 



ipconfig /all



This command displays detailed information about the network interfaces configured on the system, including IPv4 addressing, subnet masks, default gateways, DHCP configuration, and DNS servers.



Results: 



The following values represent a sanitized example of the network configuration observed during the lab:



Parameter       | Value 



IPv4 Address    | 192.168.10.50

Subnet Mask     | 255.255.255.0

Default Gateway | 192.168.10.1

DHCP Server     | 192.168.10.1

DNS Servers     |8.8.8.8



The values above are sanitized for documentation purposes and do not represent the actual network configuration of the system used during the lab. Of course, there are other data shown in the results other than what was mentioned. I only picked some of the most important to represent.





## Analysis



IPv4: The IPv4 address identifies the device within the local network. In this representation, the address I used is 192.168.10.50. The address belongs to a private IPv4 range and is therefore intended for use inside a local network.



Subnet mask: The subnet mask is 255.255.255.0, which corresponds to /24. This means that the first 24 bits identify the network, while the remaining 8 bits are available for host addresses.



The resulting network is: 192.168.10.0/24



Default gateway: Then we have the default gateway which is 192.168.10.1. The device uses the default gateway when communicating with destinations outside its local subnet.



DHCP: The DHCP server is 192.168.10.1. DHCP can automatically provide the device with network configuration such as an IP address, subnet mask, default gateway, and DNS server information.



DNS: The DNS server is 8.8.8.8. DNS is responsible for translating domain names, such as google.com, into IP addresses that network devices can use for communication.





Those configurations work together to provide - what is called - network connectivity. In other words, I described some aspects that can be inspected and interpreted while using the prompt ipconfig /all in Powershell while searching for informations on a Windows network connectivity. 




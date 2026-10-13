ARP Analysis



Objective= the objective of this lab is to examine how ARP maps IPv4 addresses to MAC addresses on a local network and to understand how devices identify the next-hop hardware address when communicating within the LAN.



Environment



* Operating System: Windows
* Tool: Powershell, arp -a
* Protocol analyzed: ARP
* Network type: Local Area Network (LAN)



We use the following command such as mentioned in Powershell: arp -a

The command displays IPv4 addresses, their associated MAC addresses, and the type of ARP entry stored by the system.



Result



Parameter      |    Value



IPv4 Address   |    192.168.10.1

Mac address    |   00-11-22-33-44-55

Entry Type     |  dynamic





The MAC address shown above is a sanitized example and does not represent the actual hardware address observed during the lab.



Analysis



The ARP cache showed a dynamic mapping between the default gateway's IPv4 address and its MAC address. When a device needs to communicate with a destination outside its local subnet, routing determines that the default gateway should be used as the next hop. The device then needs the gateway's MAC address to deliver the Ethernet or Wi-Fi frame on the local network.

ARP maps an IPv4 address to the corresponding MAC address.



The destination IP address remains the address of the final destination, while the destination MAC address on the local network identifies the next hop. This demonstrates how Layer 3 addressing (IP) and Layer 2 addressing (MAC) work together during network communication.



Practical Verification



A connectivity test was performed against the default gateway: In powershell was used ping 192.168.8.1



The gateway responded successfully.



The ARP cache was then inspected again using: In powershell, again the command arp -a



The gateway continued to have a dynamic ARP entry, confirming that the system maintained an IPv4-to-MAC mapping for the local next hop.



This demonstrates how ARP information supports local network communication.





Conclusion



The ARP cache was inspected to identify the MAC address associated with the default gateway. A connectivity test confirmed communication with the gateway, while the ARP table showed that the corresponding mapping was maintained as a dynamic entry. Moreover, we also have a clear representation of how ARP works with IP addressing and routing: ARP provides the MAC address required in order to deliver the frame on the local network while routing identifies the next hop.


Network Troubleshooting



Objective= the objective of this lab is to check network connectivity step by step and identify possible causes of common network problems.



Environment



* Operating System: Windows



* Tools: Command Prompt



* Commands: ipconfig, ping, nslookup



Troubleshooting Method



I will check the network configuration, test connectivity, and then check DNS resolution. This approach helps identify where a network problem may be occurring.



Results



I used the "ipconfig" command in Command Prompt and identified an IPv4 address and a default gateway. Then, I ran the command "ping 192.168.9.1" (not the actual def. gateway, I used a sanitiezed version just for this lab) and the test returned 4 replies with 0 packets lost, this means that an external IP address responded to the ping test. After that, I ran the command "nslookup example.com" and as a result I got 4 IP addresses for the domain, so the DNS resolution worked too for this test.



Analysis



The network configuration showed that the computer had a valid IPv4 address and a default gateway, which indicated that the basic network settings were configured correctly. The first ping test to the local gateway was successful, with no packets lost, confirming that the computer could communicate with the router. I then tested connectivity to an external IP address, 8.8.8.8, and received the same result, showing that the external address was reachable during the test.



Finally, I used nslookup to check DNS resolution for example.com. The command returned four IP addresses, indicating that the domain name was successfully resolved. Based on these results, all the checks were successful, and no connectivity issues were identified during the test. By combining these commands, I was able to check the network configuration, verify local and external connectivity, and confirm that DNS resolution was working.





Conclusion



In this lab, I used ipconfig, ping, and nslookup to check network connectivity. I verified the network configuration, tested communication with the default gateway, checked an external IP address, and tested DNS resolution. All tests were successful. In conclusion, this helped me understand how to check network connectivity step by step and how each command provides different information.




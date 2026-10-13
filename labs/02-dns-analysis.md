DNS Analysis



Objective = the objective of this representation is to analyze DNS resolution, identify the DNS resolver being used, inspect DNS records, and understand how domain names are translated into IP addresses.



Environment



* Operating System: Windows
* Tools: Powershell, nslookup
* Protocol analyzed: DNS
* Test domain: Google.com



Command used in Powershell: nslookup Google.com





As a result, we have the domain name which in this case is Google.com and the IP addresses associated with the requested domain name. For documentation purposes, the resolver information has been sanitized:



Parameter        Value

DNS Resolver  |  192.168.10.1



Resolver Address  | 192.168.10.1



Query   |    google.com



Result  |  IP addresses returned successfully







Analysis



The DNS lookup showed us that the local system uses a DNS rezolver to translate the domain name (in this case Google.com) into an IP address. Other than that, it also may return a cached response or query other DNS servers when the requested info is not available. When we get a successful response, it's a confirmation that DNS resolution is functioning correctly for the tested domain . The DNS resolver's role is to translate domain names into IP addresses that the device can use to establish a network communication.



Alternative DNS Test



A second DNS lookup was performed using Google Public DNS: nslookup google.com 8.8.8.8



The response identified the DNS server as dns.google, confirming that the query was handled by Google Public DNS. This test demonstrates that a DNS query can be sent to a specific resolver instead of relying on the DNS server configured automatically by the local network. Using an alternative DNS resolver can be useful when troubleshooting DNS-related connectivity problems.



Troubleshooting Scenario



A DNS-specific troubleshooting scenario was considered:



* ping 8.8.8.8 succeeds



* nslookup google.com has a TIMEOUT result



* nslookup google.com 8.8.8.8 succeeds



Diagnosis



This pattern indicates that general Internet connectivity is working, while the DNS resolver configured by the local network may be unavailable or malfunctioning. Testing an alternative DNS resolver helps isolate the problem and confirms whether DNS resolution is the source of the failure.



Verification



The successful response from Google Public DNS confirms that DNS resolution itself is working and that the issue is likely related to the default DNS resolver rather than general network connectivity.



Conclusion



This lab demonstrated how DNS translates domain names into IP addresses and how a DNS resolver acts as an intermediary between a device and the wider DNS infrastructure.



The nslookup command was used to inspect DNS resolution and identify the resolver handling the query. An additional test using Google Public DNS demonstrated how an alternative resolver can be used for troubleshooting.



The lab also demonstrated how DNS failures can be isolated from general network connectivity problems by comparing DNS queries with direct IP connectivity tests.


HTTP and HTTPS Analysis



Objective= the objective of this lab is to understand the difference between HTTP and HTTPS and learn how TLS helps protect network communication.



Environment



* Operating System: Windows



* Tools: Command Prompt



* Protocols: HTTP and HTTPS



Results



After using the command "nslookup example.com" on Command Prompt for this lab, we have as a result an IP address for the domain (example.com). This shows that the domain name could be resolved using DNS. After, I ran the command " curl -I https://example.com" and the response started with the following: HTTP/1.1 200 OK. The status code 200 means that the request was successful. The response included HTTP headers, which contain information about the server's reply. I also run another test using the command "curl -I http://example.com", and the response was the same "HTTP/1.1 200 OK". This means that the server returned a successful respons to the HTTP request and that it was not redirected to HTTPS.



Analysis



The "nslookup" command returned an IP address for the domain. This showed that DNS resolution worked for this test. Both HTTP and HTTPS requests returned "200 OK", this means that the server responded successfully to both requests. HTTP does not encrypt data by itself. HTTPS uses TLS to protect data during transmission and help verify the server's identity. In this test, the HTTP request returned "200 OK" instead of redirecting to HTTPS.

The status code showed that the request was successful, but it did not provide details about the TLS connection.





Conclusion



In this lab, I used nslookup to check DNS resolution and curl to test HTTP and HTTPS requests. Both requests returned 200 OK, which showed that the server responded successfully. I learned that HTTP and HTTPS can return the same status code, but HTTPS provides additional protection through TLS. I also learned that an HTTP response does not always mean that the server redirects the request to HTTPS.


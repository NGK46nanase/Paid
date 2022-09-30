# Client Identification and Cookies

| Header name | header type | Description | Usaege |
| ---- | ---- | ---- | ---- |
| From | Request | User's email address |  few browsers send From headers, due to worries of unscrupulous servers collecting email addresses and using them for junk mail distribution | 
| User-Agent | Request | User's browser software | tells the server information about the browser the user is using, including the name and version of the program, and often information about the operating system |
| Referer | Request | Page User came from by following link | provides the URL of the page the user is coming from |
| Authorization | Request | Username and password |  |
| client-ip | Extension(Request) | Client's IP address |.  | 
| X-Forwarded-For | Extension (Request) | Client's IP address |.  | 
| Cookie | Extension (Request) | Server-generated ID label |    |

## Client IP Address

Limits 
- To enhance security and manage scarce addresses, many users browse the Internet through Network Address Translation (NAT) firewalls. These NAT devices obscure the IP addresses of the real clients behind the firewall, converting the actual client IP address into a signle , shared firewall IP address ( and different port numbers). 
- HTTP  proxies and gateways typically open new TCP connections to the origin server. The web server will see the IP address of the proxy server instead of that of the client. Some proxies attempt to work around this problem by adding special Client-ip or X-Forwarded-For HTTP extension headers to preserve the original IP address. But not all proxies support this behavior.





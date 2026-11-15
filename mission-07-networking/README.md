# Mission 7 — How Computers Communicate

## 1. Task / objective

Understand basic network types and communication concepts.
Explore connectivity and DNS lookup tools, and explain what
happens when a website opens.

## 2. Work completed

### Task 7.1 — Network Concepts

| Concept | Explanation | Example |
|---------|-------------|---------|
| LAN | A Local Area Network connects devices across a small area, such as a home, lab, or office. | Computers connected to a college lab network. |
| MAN | A Metropolitan Area Network connects networks across a city or metropolitan area. | A city-wide network connecting municipal offices. |
| WAN | A Wide Area Network connects networks over large geographical distances. | A company's network connecting offices in different countries. |
| DNS | The Domain Name System resolves domain names to information such as IP addresses. | Looking up the address associated with example.com. |
| Router | A device that forwards packets between networks. | A home router forwarding traffic between the local network and an internet provider. |
| Protocol | An agreed set of rules for communication. | HTTPS governs secure communication between a browser and a web server. |
| Packet switching | Data is carried in packets that share network links. Packets can be forwarded separately and reassembled as needed. | Website data travelling through several network devices. |
| Client-server | A model in which a client requests a service and a server responds. | A browser requesting a page from a web server. |

### Task 7.2 — Observe Network Information

**Connectivity test**

ping -c 4 example.com

On macOS, `-c 4` limits the test to four requests.
Ping sends ICMP Echo Requests and reports replies, response times,
and packet-loss information.

**What does a connectivity test help check?**

It helps check whether a destination responds to this type of
network traffic. Replies indicate that ICMP communication worked
during the test.

A missing reply does not necessarily mean the website is unavailable.
Some systems block ICMP while still serving web pages. Ping also
does not confirm that an HTTPS service is working.

**Illustrative result 

four received, and 0% packet loss. 

**DNS lookup**

nslookup example.com


This asks the configured DNS resolver for information about
example.com. 


**What information does a DNS lookup display?**

It displays DNS lookup results, such as IPv4 or IPv6 addresses
associated with the requested name. Results can vary by time,
location, resolver, and service configuration.

**What role does DNS play when opening a website?**

DNS helps the browser obtain an address for a domain name.
It lets people use names instead of remembering numeric addresses.
A browser may reuse a cached result rather than perform a new
lookup every time.

**Observation status**

The expected purpose of both commands is documented.

### Task 7.3 — What Happens When a Website Opens?

1. I enter an HTTPS website address into the browser. The browser
   acts as the client and identifies the requested domain and path.

2. The browser checks whether it already has usable information,
   such as a cached page, DNS result, or existing connection.
   If necessary, DNS resolves the domain to an IP address.

3. The computer sends traffic toward the destination through the
   network. For a server outside the local network, this normally
   passes through a router and the internet provider.

4. If a new connection is needed, the browser establishes a secure
   connection using the protocols supported by the service.
   HTTPS uses TLS protection; HTTP/1.1 and HTTP/2 commonly use TCP,
   while HTTP/3 uses QUIC over UDP.

5. The browser sends an HTTP request identifying the resource it
   wants. The server processes the request and sends a response
   containing a status and, when appropriate, page content.

6. The browser processes the returned HTML, requests additional
   resources such as stylesheets, images, and scripts as needed,
   and renders the page. Scripts may update the page or request
   more information.

## 3. Commands / tools used

- Terminal: Provides the interface for network commands.
- `ping -c 4 example.com`: Tests ICMP responsiveness using four requests.
- `nslookup example.com`: Looks up DNS information for the domain.
- Google Chrome: Acts as a web client when opening websites.
- Visual Studio Code: Edits this README.
- Markdown: Formats the table, headings, and explanations.

## 4. My understanding

Networks allow devices to exchange data. LAN, MAN, and WAN describe
networks covering different geographical scales.

DNS helps translate a domain name into information needed to reach
a service. Routers forward packets between networks, and protocols
define how devices communicate.

A browser is a client requesting resources from a server.
Opening a website involves name resolution, network communication,
secure protocols, requests, responses, and rendering.

Connectivity tests and DNS lookups answer different questions.
Ping checks responsiveness to ICMP traffic, while a DNS lookup
checks name-resolution information.

## 5. Difficulties faced

No actual network-test errors have been recorded.

Concepts requiring care include distinguishing DNS from connectivity
testing and recognising that a failed ping does not by itself prove
a website is unavailable.

## 6. How I resolved them

I separated the purposes of the tools:

- DNS lookup identifies information associated with a domain name.
- Ping checks whether the destination responds to ICMP requests.
- Opening an HTTPS website checks a different service using
  different protocols.

## 7. Evidence / files

- README.md: Contains the network-concepts table, tool explanations,
  and six-step website explanation.

## 8. Commit details

Planned commit message:
Explain networking concepts and website communication

Actual commit and push status: 

Mission status: 
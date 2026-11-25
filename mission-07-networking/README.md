# Mission 7 - How computers communicate

## 1. Task / objective
The objective of this mission was to define core computer networking concepts with real-world examples, perform basic connectivity and DNS lookup tests from the Terminal while keeping personal network information private, and explain step-by-step how a browser loads a website.

## 2. Work completed

### Task 7.1 - Explain network concepts
| Concept | Explain it in your own words | Example |
| :--- | :--- | :--- |
| LAN | A network covering a small local area, such as a home, lab, or office. | A home Wi-Fi network connecting a laptop, smartphone, and printer to the same router. |
| MAN | A network covering a city or large campus area. | A university campus network linking multiple academic blocks and hostel buildings across a city. |
| WAN | A network covering large geographical areas across cities, countries, or continents. | The global Internet connecting regional ISPs and data centers worldwide. |
| DNS | Translates a human-readable domain name into a numerical IP address. | Resolving `example.com` into its public IP address so a browser knows where to connect. |
| Router | Connects separate networks together and forwards data packets between them along the best path. | A home Wi-Fi router forwarding traffic between local devices and an ISP's external network. |
| Protocol | A standardized set of rules that devices follow to format, transmit, and receive data reliably. | HTTPS for secure web browsing, or TCP/IP for reliable packet delivery. |
| Packet switching | Data is broken into small, addressed packets that travel independently across a network and reassemble at the destination. | Streaming a video or loading a webpage where data arrives in small chunks rather than one continuous stream. |
| Client-server | A communication model where a client requests a service or resource and a server processes and delivers it. | A web browser (client) requesting a webpage from a remote web server. |

### Task 7.2 - Observe network information
- **Connectivity test (`ping -c 4 example.com`):**
  - **Observed result:** Sent 4 test packets to `example.com` and received 4 replies (`0.0% packet loss`) with round-trip times recorded in milliseconds.
  - **What a connectivity test checks:** It verifies whether a remote host is reachable over the network, checks if packets are being dropped, and measures network latency (round-trip delay).
- **DNS lookup (`nslookup example.com`):**
  - **Observed result:** Local DNS server address `[redacted]` resolved `example.com` to its public IPv4 (`93.184.215.14` / authoritative edge IPs) and IPv6 addresses.
  - **What a DNS lookup displays:** It shows the DNS resolver server handling the query along with the domain's mapped IPv4 (`A` record) and IPv6 (`AAAA` record) network addresses.
- **Role of DNS when opening a website:** Computers communicate over networks using numerical IP addresses rather than English words. When you type a website name into a browser, DNS acts like an internet phonebook by translating that domain name into the target server's IP address so your device can establish a connection.

### Task 7.3 - What happens when you open a website?
1. **User enters URL in the client:** You type a web address (such as `https://example.com`) into your web browser, which acts as the **client**.
2. **DNS resolution:** The browser checks its local cache and queries a **DNS** server to translate the human-readable domain name into the destination web **server's** numerical IP address.
3. **Packet routing through the local network:** Your computer breaks the request into small data packets addressed to that IP and sends them through your local **router** out onto the wider internet.
4. **Protocol handshake:** The client and server establish a connection using standard networking **protocols**—TCP ensures reliable packet delivery, while HTTPS (HTTP over TLS) sets up an encrypted session.
5. **HTTP request sent to server:** Over that secure protocol connection, the browser sends an HTTP `GET` request asking the **server** for the webpage's HTML, CSS, and media files.
6. **Server processes and responds:** The remote web **server** receives the request, locates or generates the requested resources, and sends the webpage data back in packets across the network.
7. **Browser renders the webpage:** Your client browser receives the response packets, reassembles them, and renders the visual webpage on your screen.

## 3. Commands / tools used
- `cd`: Navigated into `mission-07-networking`.
- `ping -c 4 example.com`: Tested network reachability and measured round-trip packet latency to a public domain.
- `nslookup example.com`: Queried DNS records to inspect how a domain name resolves to IP addresses.
- **VS Code**: Used to document the networking tables, redacted diagnostic observations, and step-by-step communication flow in `README.md`.
- `git add`, `git commit`, `git push`: Staged, committed, and pushed Mission 7 documentation to GitHub.

## 4. My understanding
I understood how everyday web browsing relies on multiple layers working together: DNS translates names into IP addresses, routers forward packets across local and wide-area networks, and standardized protocols like TCP/IP and HTTPS ensure reliable, secure client-server communication.

## 5. Difficulties faced
Running `ping example.com` without a count flag initially caused the command to run continuously in macOS Terminal, and the raw `nslookup` output exposed my local router's private DNS gateway address.

## 6. How I resolved them
I stopped the continuous ping with `Ctrl + C` and re-ran it with `-c 4` to limit the test to four packets, and I replaced my local DNS server IP address with `[redacted]` before documenting the results in `README.md`.

## 7. Evidence / files
- `mission-07-networking/README.md` (Network concepts table, privacy-safe `ping` and `nslookup` observations, and 7-step website loading explanation).

## 8. Commit details
- **Commit message:** `Explain networking concepts and website communication`
- **Status:** Committed and pushed to GitHub (`main` branch).
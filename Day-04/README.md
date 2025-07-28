Day-4 Cyber Security Notes
Date:25-07-2025

🧠 Network Fundamentals
🌐 What is a Network?
A network is a collection of interconnected devices (such as computers, servers, routers, etc.) that communicate and share resources. Networks can range from a simple connection between two computers to the global scale of the Internet.

🧩 What is a Subnet?
A subnet (short for subnetwork) is a logical division of an IP network. It helps network administrators organize a large network into smaller, manageable segments, which enhances:

Performance by reducing congestion

Security by isolating segments

Efficiency by limiting broadcast traffic

🔁 What is Port Forwarding?
Port forwarding redirects incoming network traffic on a specific port to a different internal IP and port. It's commonly used to allow external access to services within a private network (e.g., accessing a home server remotely).

Example:
Public IP:Port → Internal IP:Port
203.0.113.1:8080 → 192.168.0.10:80

🔐 Antivirus Limitations
⚠️ Note: Antivirus software typically cannot scan password-protected or encrypted files, such as ZIP archives or encrypted documents.

Aspect	Description
Limitation	Antivirus can't access encrypted/password-protected files
Risk	Malware may be hidden inside such protected files
Detection	Antivirus may miss threats in these files
User Advice	Avoid opening such files from unknown sources
Recommendation	Use layered security (e.g., endpoint protection, behavior monitoring)

🛡️ User Account Control (UAC)
User Account Control (UAC) is a Windows security feature that prevents unauthorized system changes. It limits application privileges unless explicitly approved by the user.

Feature	Description
Purpose	Prevent unauthorized system changes
Behavior	Prompts for admin credentials when changes are attempted
Default Action	Runs apps with standard user rights

🔧 UAC Notification Levels:
Level	Description
Always Notify	Prompt for every change
Notify only when apps try to make changes	Default option, prompts only for apps
Same as above (no dimming)	Does not dim desktop during prompt
Never Notify (Not Recommended)	Disables UAC protection completely

🔍 Have I Been Pwned?
Have I Been Pwned (HIBP) is a free online tool created by Troy Hunt to check if your personal data has been exposed in data breaches.

Feature	Description
Email check	See if your email was in a breach
Password check	Check if a password is compromised (uses k-anonymity for privacy)
Paste search	Find personal data in public data dumps
Domain monitoring	Track breaches affecting an entire domain
Developer API	Access breach data programmatically
Website	haveibeenpwned.com

🕰️ Wayback Machine
The Wayback Machine, by the Internet Archive, lets users view and retrieve historical snapshots of websites.

Feature	Description
Purpose	Archive and retrieve past versions of web pages
Archive Size	Over 700 billion pages (dating back to 1996)
Use Cases	Research, content recovery, fact verification, SEO insights
Developer Access	Public API available
Website	archive.org/web

🔄 API (Application Programming Interface)
An API allows different software systems to communicate by defining a set of rules and formats for requests and responses.

Category	Description
Purpose	Enable interaction between applications
Common Uses	Web apps, third-party integration, mobile apps, microservices
Authentication	Often required (API keys, OAuth, etc.)
Rate Limiting	Controls the number of requests an app can make

🧪 Types of APIs
Type	Description
REST	HTTP-based, stateless, widely used
GraphQL	Flexible queries, efficient data fetching
SOAP	Protocol-based, used in enterprise systems
WebSocket	Real-time, two-way communication

⚙️ .env (Environment Variables)
A .env file stores environment variables, often used for configuration and sensitive data such as API keys and passwords.

Feature	Description
Use Case	Manage app settings outside the source code
Environment Separation	Support for development, staging, production
Best Practices	Do not commit .env to version control
Tool Support	Use libraries like dotenv to load variables

🗡️ Nmap Flags – (Kali Linux)
Nmap is a powerful network scanning and reconnaissance tool used for security auditing and discovery.

🔧 Common Nmap Flags
Flag	Description
-Pn	Skip host discovery, treat all hosts as up
-A	Enable OS detection, version detection, script scanning, traceroute
-sV	Detect service versions
-O	OS detection
-oN	Save output in normal format
--script	Run specific Nmap Scripting Engine (NSE) scripts
-vv	Very verbose output
-p-	Scan all 65,535 ports
-p	Scan specific ports (e.g., -p 80,443)
-sS	TCP SYN scan (stealth scan)
-sT	TCP connect scan (less stealthy)

🔍 Scan Examples
nmap -A -p- target.com → Full scan of all ports with OS detection

nmap -sS -p 80,443 target.com → SYN scan of specific ports

nmap -O -sV target.com → OS and version detection

nmap --script vuln target.com → Scan for known vulnerabilities

📡 TCP vs UDP – Comparison
Feature	TCP	UDP
Type	Connection-oriented	Connectionless
Reliability	✅ Guaranteed delivery	❌ No guarantee
Order	✅ In-order packet delivery	❌ Packets may arrive out of order
Error Handling	✅ Built-in error correction	❌ Basic error checking only
Speed	❌ Slower (more overhead)	✅ Faster (minimal overhead)
Header Size	20–60 bytes	8 bytes
Flow Control	✅ Yes	❌ No
Congestion Control	✅ Yes	❌ No
Use Cases	Web, email, file transfer	Streaming, DNS, VoIP
Example Protocols	HTTP, HTTPS, FTP, SMTP	DNS, DHCP, RTP, VoIP

🧭 When to Use:
TCP → Reliability > Speed (Web, file transfer, database)

UDP → Speed > Reliability (Streaming, gaming, real-time apps)

🌐 IPv4 vs IPv6 – Comparison
Feature	IPv4	IPv6
Address Length	32-bit	128-bit
Format	Dotted decimal (e.g., 192.168.1.1)	Hexadecimal (e.g., 2001:0db8::1)
Address Space	~4.3 billion addresses	~340 undecillion addresses
Header Size	20 bytes (variable)	40 bytes (fixed)
Security	Optional	Built-in IPsec support
Configuration	Manual or DHCP	Supports auto-configuration
Mobility	Limited	Native support
Header Checksum	Included	Removed (for efficiency)
Broadcast Support	Yes	Replaced by multicast
Use Cases	Legacy systems, current internet	IoT, future-proof networks

🖥️ MAC Address – Overview
Feature	Description
Purpose	Unique hardware identifier for network interfaces
Format	6-byte (48-bit) hex (e.g., 00:1A:2B:3C:4D:5E)
Assignment	Assigned by device manufacturer
Uniqueness	Globally unique (in theory)
Uses	Device identification, ARP resolution, access control
Security	Can be spoofed, limited built-in protection
Validation	CRC (Cyclic Redundancy Check) used for error detection

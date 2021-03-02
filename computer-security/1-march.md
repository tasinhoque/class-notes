Chapter 1, Page 4, Introduction to Computer Security

Bangladesh Data Center Company Ltd. (BDCCL)

SQL attack

Forensic Lab/Counter Terrorism & Transnational Crime (CTTC) can recover deleted files

Anti-forensic tools help nullify the hard-disk entries

Hard Disk Hash

### Integrity tools

- Backup
- Data Collecting

TCP Syn Attack

---

[Taken from [Imperva](https://www.imperva.com/learn/ddos/syn-flood/)]

<div style="flex: 1; display: flex; justify-content: center;">
  <img src="https://www.imperva.com/wp-content/uploads/sites/13/2020/03/diagram-52@3x.png" width="300px">
</div>

### What is a SYN flood attack

TCP SYN flood (a.k.a. SYN flood) is a type of Distributed Denial of Service (DDoS) attack that exploits part of the normal TCP three-way handshake to consume resources on the targeted server and render it unresponsive.

Essentially, with SYN flood DDoS, the offender sends TCP connection requests faster than the targeted machine can process them, causing network saturation.

### Attack description

When a client and server establish a normal TCP “three-way handshake,” the exchange looks like this:

- Client requests connection by sending SYN (synchronize) message to the server.
- Server acknowledges by sending SYN-ACK (synchronize-acknowledge) message back to the client.
- Client responds with an ACK (acknowledge) message, and the connection is established.
- In a SYN flood attack, the attacker sends repeated SYN packets to every port on the targeted server, often using a fake IP address. The server, unaware of the attack, receives multiple, apparently legitimate requests to establish communication. It responds to each attempt with a SYN-ACK packet from each open port.

The malicious client either does not send the expected ACK, or—if the IP address is spoofed—never receives the SYN-ACK in the first place. Either way, the server under attack will wait for acknowledgement of its SYN-ACK packet for some time.

During this time, the server cannot close down the connection by sending an RST packet, and the connection stays open. Before the connection can time out, another SYN packet will arrive. This leaves an increasingly large number of connections half-open – and indeed SYN flood attacks are also referred to as “half-open” attacks. Eventually, as the server’s connection overflow tables fill, service to legitimate clients will be denied, and the server may even malfunction or crash.

While the “classic” SYN flood described above tries to exhaust network ports, SYN packets can also be used in DDoS attacks that try to clog your pipes with fake packets to achieve network saturation. The type of packet is not important. Still, SYN packets are often used because they are the least likely to be rejected by default.

<img src="https://www.imperva.com/learn/wp-content/uploads/sites/13/2019/01/syn-flood.jpg.webp" width="500px">

---

[Taken from [Varonis](https://www.varonis.com/blog/what-is-a-proxy-server/)]

### What’s a Proxy Server?

A proxy server acts as a gateway between you and the internet. It’s an intermediary server separating end users from the websites they browse. Proxy servers provide varying levels of functionality, security, and privacy depending on your use case, needs, or company policy.

If you’re using a proxy server, internet traffic flows through the proxy server on its way to the address you requested. The request then comes back through that same proxy server (there are exceptions to this rule), and then the proxy server forwards the data received from the website to you.

If that’s all it does, why bother with a proxy server? Why not just go straight from to the website and back?

Modern proxy servers do much more than forwarding web requests, all in the name of data security and network performance. Proxy servers act as a firewall and web filter, provide shared network connections, and cache data to speed up common requests. A good proxy server keeps users and the internal network protected from the bad stuff that lives out in the wild internet. Lastly, proxy servers can provide a high level of privacy.

### How Does a Proxy Server Operate?

Every computer on the internet needs to have a unique Internet Protocol (IP) Address. Think of this IP address as your computer’s street address. Just as the post office knows to deliver your mail to your street address, the internet knows how to send the correct data to the correct computer by the IP address.

A proxy server is basically a computer on the internet with its own IP address that your computer knows. When you send a web request, your request goes to the proxy server first. The proxy server then makes your web request on your behalf, collects the response from the web server, and forwards you the web page data so you can see the page in your browser.

When the proxy server forwards your web requests, it can make changes to the data you send and still get you the information that you expect to see. A proxy server can change your IP address, so the web server doesn’t know exactly where you are in the world. It can encrypt your data, so your data is unreadable in transit. And lastly, a proxy server can block access to certain web pages, based on IP address.

---

Class taken by Sohrab sir

Sessional class on computer security today from 2:30 PM

Textbook: [Introduction to Computer Security by Goodrich][goodrich]

[Slides][slides]

There is no central authority of the internet.

MAC address can be counterfeit.

Internet is inherently vulnerable.

We don't want to introduce unnecessary delay in the network due to security protocol.

Network protocols like TCP/IP are very lightweight and not very secure.

At first, internet was invented in order to connect four machines. At that time, they assumed that internet wouldn't get any complex than that.

### Man in the Middle Attack

Alice -> Trudy -> Bob  
Alice <- Trudy <- Bob

Password attack tool: John the ripper, Cain & Abel

Kali linux is used for ethical hacking

Denial of Service Attack

---

[Taken from [Palo Alto Networks][palo alto]]

A Denial-of-Service (DoS) attack is an attack meant to shut down a machine or network, making it inaccessible to its intended users. DoS attacks accomplish this by flooding the target with traffic, or sending it information that triggers a crash. In both instances, the DoS attack deprives legitimate users (i.e. employees, members, or account holders) of the service or resource they expected.

Victims of DoS attacks often target web servers of high-profile organizations such as banking, commerce, and media companies, or government and trade organizations. Though DoS attacks do not typically result in the theft or loss of significant information or other assets, they can cost the victim a great deal of time and money to handle.

There are two general methods of DoS attacks: flooding services or crashing services. Flood attacks occur when the system receives too much traffic for the server to buffer, causing them to slow down and eventually stop. Popular flood attacks include:

Buffer overflow attacks – the most common DoS attack. The concept is to send more traffic to a network address than the programmers have built the system to handle. It includes the attacks listed below, in addition to others that are designed to exploit bugs specific to certain applications or networks.  
ICMP flood – leverages misconfigured network devices by sending spoofed packets that ping every computer on the targeted network, instead of just one specific machine. The network is then triggered to amplify the traffic. This attack is also known as the smurf attack or ping of death.  
SYN flood – sends a request to connect to a server, but never completes the handshake. Continues until all open ports are saturated with requests and none are available for legitimate users to connect to.  
Other DoS attacks simply exploit vulnerabilities that cause the target system or service to crash. In these attacks, input is sent that takes advantage of bugs in the target that subsequently crash or severely destabilize the system, so that it can’t be accessed or used.

---

Security Goals:

- Confidentiality
- Integrity: Maintaining the promises.
- Availability

Encryption and decryption using HTTP

When the encryption and decryption keys are same, the cryptography is called symmetric cryptography.  
Shared secret key  
Key exchange protocol  
Hidden protocol: Military communication

### Tolls for Confidentiality

- Access Control
- Authentication
- Authorization
- Physical Security

[goodrich]: https://drive.google.com/drive/folders/1WL26VnB2V2l6jzXWxyHzP68LMf7CQFQp
[slides]: https://sites.google.com/site/securitybook1/home/presentations?authuser=0
[palo alto]: https://www.paloaltonetworks.com/cyberpedia/what-is-a-denial-of-service-attack-dos

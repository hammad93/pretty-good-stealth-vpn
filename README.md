# pretty-good-stealth-vpn
A repository detailing research and development on VPN technologies including a survey of different methodologies. The intention for this repository is to protect the privacy of users and to prevent the internet from advancing surveillance technology. This repository was released to report how some spam, scammers, and hackers are utilizing stealth to be dishonest.

## Experiments on different types of VPN

Consider a scenario where you want to get a letter from the mail but hide your real address from the sender. A VPN is similar to a solution where we setup a decoy address and then forward letters from it to the intended address. In addition, the VPN scrambles the letter before sending it to the intended address and when it arrives, we unscramble it. This process is known as encryption and decryption. A scenario where multiple people use the same decoy address to receive letters at their own address can increase privacy.

### Popular VPN Providers
- Overview
    - Popular VPN provider’s are often the first choice for choosing a VPN solution because of the accessibility and choice of server location. Although requiring technical setup, they are also some of the easiest to configure. However, because it is popular, it is the easiest to detect. 
- Speed & Performance
    - Each VPN provider is different and the speeds can vary by your location because of latency. In general, speeds are best when connecting to a domestic server, or a server located in the same country. Often, the bottleneck is not the server response but the latency. However, if you are using these providers by default and set to block non-VPN traffic, they suffer from unpredictable downtime and surges in latency. 
- Privacy
    - This option provides the most privacy because the traffic is shared amongst many users. However, this applies to web applications that receive large amount of traffic with the highest likelihood with more than one user on the same VPN and server; or identical IP’s. The most popular VPN’s are also the “dirtiest” with high number of spam and illegal activity reports from the IP. This causes many web applications to easily identify if a user is under a VPN because other user’s on the same server are causing enough trouble for centralized spam reporters to identify and report.
- Encryption
    - These VPN’s claim to use encryption but because they are also corporations they are unlikely to be transparent. Numerous hacks and other exploits cause concern and none of the most popular providers are immune. Although many claim that there are no logs, an apparent contradiction is billing and many of the most popular providers do not accept a privacy coin. 
### Dedicated VPN Instances from VPN Providers
- Overview
    - A dedicated VPN instance is a server that only you have access to in theory. After trying out some of these and analyzing IP records, I have not yet found one that fulfilled the marketing. What it is meant to solve is the problem of detection of a VPN, where it is more difficult to know it is a VPN if you’re the only one on the server. While this might have been true in the past, current spam and cybersecurity threat detection utilize IP ranges instead of a strict whitelist that knows if the sever is part of a VPN or data center.  
- Speed & Performance
    - Download and upload speeds may or may not be faster given the CPU, RAM, and HDD speeds of the instance compared to a shared server that may have more resources. When measuring reliability and uptime, this option is better than shared because it is dedicated. Regardless, there was still significant downtime from the provider and because the IP of the dedicated instances are often flagged as spam or a threat.
- Privacy
    - This provides less privacy for cases where a shared IP would provide obscurity. If a user is sending traffic that would draw attention from authorities, this is the most dangerous option because there is a 1 to 1 match, beyond reasonable doubt, hosted by a corporation that only needs to sell the perception of privacy instead of rigorously proving it. These instances are less easy to detect because the application needs an interface that flags IP ranges instead of hardcoded VPN server IP’s.
- Encryption
    - Data is just as encrypted as shared servers but most of the known leaks or hacks have not targeted them as far as we know. This is likely the best option for a user who has no traffic that can draw attention and wants to hide their traffic from their internet provider.
### Self Hosted VPN from Popular Cloud Hosting Providers
- Overview
    - What if we want to create our own VPN server, does this make it less detectable? The answer is yes, and there are other benefits including cost and performance. When choosing the protocol to host our VPN, both OpenVPN and WireGuard were tested on a virtual machine hosting Ubuntu. However, WireGuard results indicated better performance in terms of download speed and uptime.  
- Speed & Performance
    - A self-hosted VPN from a cloud service provider was the best performing of the options tested. When measuring the speeds, the cloud providers matched already available benchmarks, including burst network speeds. Uptime is mainly reliant on the cloud hosting provider and their specific hosting plan. WireGuard did not cause any downtime.
- Privacy
    - This option allowed for levels of privacy similar to other options. The protocol also allowed for changing of IP addresses on a routine basis to further mask the requests, something that the dedicated VPN instances from a 3rd party did not have. For anonymous browsing on sites with a high amount of internet traffic, privacy was the same as using an infrastructure without a VPN.
- Encryption
    - Self-hosting the machine allows for control and validating of encryption or logs. The protocol keeps no internet traffic logs and offers variable encryption strength with no significant performance differences between 256 bit and 4096 bit. Bit encryption strength of 4096 is the minimum required due to advancements in brute force mechanisms.
- Detection
    - Although this method was less detectable compared to popular VPN providers, a small proportion of applications flagged the requests because they were coming from a data center. This was not because it detected encrypted traffic but as a spam and bot filter, applications denied or throttled these requests.
### Self Hosted VPN from home
- Overview
    - This option is preferred for travel when it makes sense to utilize your own IP. The encryption was done through a tunnel after the modem using a WireGuard server. A specialized router was bought with these capabilities already installed. It is possible to utilize any router with sufficient CPU and RAM. 
- Speed & Performance
    - 
- Privacy
- Encryption

Detection of VPN by corporate firewalls
  Data Centers
  Whitelisted providers
  Location providers
Detection of VPN by governments
  Similar solutions offered from corporations


Bottlenecks
- Server upload speeds
- VPN Server throughput 
- Ethernet cable throughput
- Home upload speeds
- VPN Protocol

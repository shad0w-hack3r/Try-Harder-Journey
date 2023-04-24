# Section 6: Active Reconnaissance

Introduction to DNS: 
    If you do not know what DNS is or how it works, 
    [here](https://www.digitalocean.com/community/tutorials/an-introduction-to-dns-terminology-components-and-concepts) is a great guide that I used to better understand it from Digital Ocean. 
    If you think you have a good understanding of what DNS is then you will also need to understand how to perform forward and reverse lookups. In addition, you should also know how zone transfers work and how to perform them. Performing these tests will certainly help you better understand what your targets are in the lab. For more information about these techniques check out this article [here](https://resources.infosecinstitute.com/dns-enumeration-techniques-in-linux/):

Tools for DNS Enumeration:

[Dnsrecon Created by Darkoperator](https://github.com/darkoperator/dnsrecon)

Network Scanning:

Nmap: 
	A tool that you should 100% totally learn about. You will probably use this everyday (If not most of the time while you are in the lab). I highly recommend you take some time to learn what the tool does, how each command switch works, each scanning technique you can run, and any other capabilities. Nmap is a powerful tool that has the ability to determine what hosts are online, what services they are running, what operating system is running on that host, and dozens of characteristics. In addition, one of the most powerful features that you should also learn is the Nmap Scripting Engine (NSE). With NSE scripts you have the ability automate a wide variety of networking tasks for your scans including vulnerability detection and exploitation. Here are my resources that I used to learn more about Nmap:

    Nmap Official Guide: I used this more than the man pages. I highly recommend purchasing the full book since the official guide is missing a few chapters, such as “Detecting and Subverting Firewalls and Intrusion Detection Systems”, “Optimizing Nmap Performance”, “Port Scanning Techniques and Algorithms”, “Host Discovery (Ping Scanning)”, and more. https://nmap.org/book/toc.html
    Link for Nmap Network Scanning Book (if you want to purchase it): https://www.amazon.com/Nmap-Network-Scanning-Official-Discovery/dp/0979958717
    Nmap Scripting Engine (NSE): https://nmap.org/book/man-nse.html
    ZephrFish’s Nmap Blog: https://blog.zsec.uk/nmap-rtfm/

Masscan: 
	A powerful tool that can be used to scan a set of requested ports against your targets. As Robert Graham says “this can be done in less than 6 minutes at around 10 million packets per second”.

        1. [Daniel Miessler guide to using Masscan](https://danielmiessler.com/study/masscan/)

Service Enumeration:

There are a variety of services running on so many systems…take the time to understand them! Do not just scan them and move on. Take some time to look at each of them because they could be a key for you to obtain shell access on a system!

Abatchy provided a link from 0day security that gave me a lot of ideas and things to look for that I may have missed when I skipped some the of the services in the lab. The original link is dead but you can find copies of it on the wayback machine: https://web.archive.org/web/20200309204648/http://0daysecurity.com/penetration-testing/enumeration.html

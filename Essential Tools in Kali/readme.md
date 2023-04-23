1. Netcat: The TCP/IP Swiss Army tool. Experiment with this tool and understand what it does because you will be using this almost every day during your course and beyond.

SANS Netcat Cheatsheet: https://www.sans.org/posters/netcat-cheat-sheet/
    Netcat Cheatsheet Reference: https://quickref.me/nc

2. Ncat: A better version of netcat in my opinion. Supports SSL communication and it is part of Nmap.

3. Socat: A command line based utility that establishes two bidirectional byte streams and transfers data between them. However, it has the ability to to allow multiple clients listen on a port and to reuse connections.

    Socat Man Page: https://linux.die.net/man/1/socat

4. PowerShell and PowerCat:

PowerShell is a cross-platform scripting language built by Microsoft that can is used for task automation and configuration management. PowerShell consists of running in a shell or a command-line environment. Unlike most shells, which accept and return text, PowerShell is built on top of the .NET Common Language Runtime (CLR), and accepts and returns .NET objects. PowerShell is a very powerful tool that pentesters use as it is installed Default on Windows and it can also be installed on Linux systems as well.

5. Resources to learn more about PowerShell:

    PowerShell Learning Resources: https://docs.microsoft.com/en-us/powershell/scripting/learn/more-powershell-learning?view=powershell-7
    PowerShell for Pentesting In Kali Linux: https://www.offensive-security.com/offsec/kali-linux-powershell-pentesting/

Books:

    Windows PowerShell CookBook: https://www.amazon.com/Windows-PowerShell-Cookbook-Scripting-Microsofts/dp/1449320686
    Windows PowerShell Reference Book: https://www.amazon.com/Windows-PowerShell-Pocket-Reference-Scripters-dp-1449320961/dp/1449320961/
    Learn PowerShell in a Month of Lunches: https://www.amazon.com/Learn-Windows-PowerShell-Month-Lunches/dp/1617294160/

Hands on Challenges for learning PowerShell:

    underthewire.tech: https://underthewire.tech/wargames.htm
    codewars: https://www.codewars.com/

PowerCat: A powershell version of netcat. The script can be downloaded onto a Windows target to transfer files, return a shell, or create payloads that we can call back from our target. https://github.com/besimorhino/powercat

TCPDump: Command line base Network Analysis Tool. Very useful and good to know if you are on a system that does not have a GUI. Here is a good cheat sheet I used for tcpdump when I needed to troubleshoot my exploits: https://www.andreafortuna.org/technology/networking/tcpdump-a-simple-cheatsheet/

    Daniel Miessler TCPDump Guide: https://danielmiessler.com/study/tcpdump/

Wireshark: GUI based Network Analysis tool. There a lot of free PCAP samples online that you can use to understand how Wireshark works. Be careful with downloading some of these PCAP files because they may have malware in them; make sure you read where the PCAP is from before playing :D

PCAP Samples:

    Netresec: https://www.netresec.com/?page=pcapfiles
    Malware Traffic Analysis: https://www.malware-traffic-analysis.net/
    Packettotal (Just like virustotal but for PCAP Analysis): https://packettotal.com/
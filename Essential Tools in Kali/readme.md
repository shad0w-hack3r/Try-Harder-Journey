# Essentials Tools in Kali Linux

1. Netcat: The TCP/IP Swiss Army tool. Experiment with this tool and understand what it does because you will be using this almost every day during your course and beyond.

   1. [SANS Netcat Cheatsheet](https://www.sans.org/posters/netcat-cheat-sheet/)
   2. [Netcat Cheatsheet Reference](https://quickref.me/nc)

2. Ncat: A better version of netcat in my opinion. Supports SSL communication and it is part of Nmap.

3. Socat: A command line based utility that establishes two bidirectional byte streams and transfers data between them. However, it has the ability to to allow multiple clients listen on a port and to reuse connections.

    [Socat Man Page](https://linux.die.net/man/1/socat)

4. PowerShell and PowerCat:

    PowerShell is a cross-platform scripting language built by Microsoft that can is used for task automation and configuration management. PowerShell consists of running in a shell or a command-line environment. Unlike most shells, which accept and return text, PowerShell is built on top of the .NET Common Language Runtime (CLR), and accepts and returns .NET objects. PowerShell is a very powerful tool that pentesters use as it is installed Default on Windows and it can also be installed on Linux systems as well.

   1. Resources to learn more about PowerShell:

       1. [PowerShell Learning Resources](https://docs.microsoft.com/en-us/powershell/scripting/learn/more-powershell-learning?view=powershell-7)
       2. [PowerShell for Pentesting In Kali Linux](https://www.offensive-security.com/offsec/kali-linux-powershell-pentesting/)

   2. Books:

       1. [Windows PowerShell CookBook](https://www.amazon.com/Windows-PowerShell-Cookbook-Scripting-Microsofts/dp/1449320686)
       2. [Windows PowerShell Reference Book](https://www.amazon.com/Windows-PowerShell-Pocket-Reference-Scripters-dp-1449320961/dp/1449320961/)
       3. [Learn PowerShell in a Month of Lunches](https://www.amazon.com/Learn-Windows-PowerShell-Month-Lunches/dp/1617294160/)

   3. Hands on Challenges for learning PowerShell:

      1. [underthewire.tech](https://underthewire.tech/wargames.htm)
      2. [codewars](https://www.codewars.com/)

5. [PowerCat](https://github.com/besimorhino/powercat): A powershell version of netcat. The script can be downloaded onto a Windows target to transfer files, return a shell, or create payloads that we can call back from our target.

6. TCPDump: Command line base Network Analysis Tool. Very useful and good to know if you are on a system that does not have a GUI. Here is a good [cheat sheet](https://www.andreafortuna.org/technology/networking/tcpdump-a-simple-cheatsheet/) I used for tcpdump when I needed to troubleshoot my exploits.

    1. [Daniel Miessler TCPDump Guide](https://danielmiessler.com/study/tcpdump/)  


7. [Wireshark](https://www.wireshark.org/download.html): GUI based Network Analysis tool. There a lot of free PCAP samples online that you can use to understand how Wireshark works. Be careful with downloading some of these PCAP files because they may have malware in them; make sure you read where the PCAP is from before playing :D

    PCAP Samples:

    1. [Netresec](https://www.netresec.com/?page=pcapfiles)
    2. [Malware Traffic Analysis](https://www.malware-traffic-analysis.net/)
    3. [Packettotal (Just like virustotal but for PCAP Analysis)](https://packettotal.com/)
## Sec-01 Network detection

NMap (Network Mapper)

Nmap is an scanning tool for security auditing and mapping of networks. 

Nmap allows network admins to find which devices / live hosts are running on their network, OS detection, version detection, discover open ports (port scanning) and services, and detect vulnerabilities.

Nmap uses the raw IP address in order to detect various available hosts on the network, the services they’re offering, the version of operating system they’re running, and the type of firewall they are using, . Whenever we’re having connectivity issues of network or firewall configuration, the first thing we check is which ports are open.

There are several commands available to check open ports and scan them on your system. Nmap is the most used tool for this purpose. 


Nmap helps you to quickly map out a network without sophisticated commands or configurations. It also supports simple commands (for example, to check if a host is up) and complex scripting through the Nmap scripting engine.

Other features of Nmap include:

* Ability to quickly recognize all the devices including servers, routers, switches, mobile devices, etc on single or multiple networks.

    Scanning the list of active devices on a network is the first step in network mapping. There are two types of scans you can use for that:

    Ping scan — Scans the list of devices up and running on a given subnet.

    > nmap -sp 192.168.1.1/24
    Scan a single host — Scans a single host for 1000 well-known ports. These ports are the ones used by popular services like SQL, SNTP, apache, and others.

    Port Scanning
    Port scanning is one of the most fundamental features of Nmap. You can scan for ports in several ways.

    Using the -p param to scan for a single port
    > nmap -p portnr ---.----.--.-- (ip address)

    > nmap scanme.nmap.org

    * Helps identify services running on a system including web servers, DNS servers, and other common applications. Nmap can also detect application versions with reasonable accuracy to help detect existing vulnerabilities.

    * Nmap can find information about the operating system running on devices. It can provide detailed information like OS versions, making it easier to plan additional approaches during penetration testing.

    Scan to Find out OS Information

    nmap -A ---.----.--.-- (ip address)

    Add in the -A flag on your Nmap command, you can discover the operating system information of the hosts that are mapped. The -A flag can be used in combination with other Nmap commands.

    nmap -O ---.----.--.-- (ip address)

    Using the -O flag on your Nmap command will reveal further operating system information of the mapped hosts. The -O flag enables OS detection.

    To do a version scan, use the ‘-sV’ command. Nmap will provide a list of services with its versions.

    > nmap -sV scanme.nmap.org

    Find Host Interfaces, Routes, and Packets
    It may become necessary to find host interfaces, print interfaces, and routes to debug.

    To do this, use the iflist command:

    nmap --iflist

    The “–iflist” command will produce a list of the relevant interfaces and routes.

    nmap --packet-trace

    Similarly, “–packet-trace” will show packets sent and received, providing similar value for debugging.

    Identify Hostnames
    There are a few ways you can implement host discovery through Nmap. The most common of which is through -sL. For example:

    nmap -sL ---.----.--.-- (ip address)


* During security auditing and vulnerability scanning, you can use Nmap to attack systems using existing scripts from the Nmap Scripting Engine.
* Nmap has a graphical user interface called Zenmap. It helps you develop visual mappings of a network for better usability and reporting.




***
## Key terminology

NMap
WireShark



***
## Exercise






***
### Sources

https://phoenixnap.com/kb/how-to-install-nmap-ubuntu-18-04

https://phoenixnap.com/kb/nmap-command-linux-examples

https://www.freecodecamp.org/news/what-is-nmap-and-how-to-use-it-a-tutorial-for-the-greatest-scanning-tool-of-all-time/

https://tecadmin.net/scanning-open-ports-with-nmap/






***
### Overcome challenges


***
### Results

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
    > nmap scanme.nmap.org

* Helps identify services running on a system including web servers, DNS servers, and other common applications. Nmap can also detect application versions with reasonable accuracy to help detect existing vulnerabilities.
* Nmap can find information about the operating system running on devices. It can provide detailed information like OS versions, making it easier to plan additional approaches during penetration testing.
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

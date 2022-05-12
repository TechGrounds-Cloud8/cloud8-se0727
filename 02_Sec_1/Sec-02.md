## Sec-02 Firewalls
***
What is a Firewall?

Firewalls are hardware and/or software systems which protect end users from malicious traffic on the Internet. When data is sent over the Internet, it comes packaged with information about where it is coming from and where it is supposed to go, as well as an indication as to what application the data is for.

Firewalls accomplish this control by inspecting data packets. The data within the packets can be inspected by the firewall to see if it contains threats. Part of this process involves checking how the data should connect to and move through the network. 


stateful firewalls vs stateless firewalls

#### What is a stateful firewall?

**state** means the last known or current status of a process, and managing state refers to keeping track of the process

A stateful firewall inspects everything inside data packets, the characteristics of the data, and its channels of communication. Stateful firewalls examine the behavior of data packets, and if anything seems off, they can filter out the suspicious data. Also, a stateful firewall can track how the data behaves, cataloging patterns of behavior. 

If a data packet examination reveals suspicious behavior—even if that kind of behavior has not been manually inputted by an administrator—the firewall can recognize it and address the threat. A stateful firewall can be used at the edge of a network or within, as is the case with an internal segmentation firewall (ISFW), which protects specific segments of the network in the event malicious code gets inside.

These firewalls can integrate encryption or tunnels, identify TCP connection stages, packet state and other key status updates.

This firewall is situated at Layers 3 and 4 of the Open Systems Interconnection (OSI) model. As the name suggests, a stateful firewall always keeps track of the state of network connections. Once a particular kind of traffic has been approved by a stateful firewall, it is added to a state table. The state table entries are created for TCP (Transmission Control Protocol) streams or UDP (User Datagram Protocol) datagrams that are allowed to communicate through the firewall in accordance with the configured security policy.  If no traffic is seen for a specified time (implementation dependent), the connection is removed from the state table.

#### What is a stateless firewall?

Stateless firewalls make use of a data packet's source, their origin i.e, IP address, port number, destination IP  parameters to figure out whether the data presents a threat. These parameters have to be entered by either an administrator or the manufacturer via rules they set beforehand. 

If a data packet goes outside the parameters of what is considered acceptable, the stateless firewall protocol will identify the threat and then restrict or block the data housing it.

Stateless firewalls don't look beyond the header of packet contents to determine if traffic is authorized.

The stateless firewalls are designed to protect networks based on static information such as source and destination.




***
## Key terminology

* Firewall
    De verschillende types firewall\
        * stateful / stateless\
        * hardware / software


***
## Exercise and Results


* Installeer een webserver op je VM.
* Bekijk de standaardpagina die met de webserver geïnstalleerd is.
* Stel de firewall zo in dat je webverkeer blokkeert, maar wel ssh-verkeer toelaat.
* Controleer of de firewall zijn werk doet.



***
### Sources

https://www.geeksforgeeks.org/stateless-vs-stateful-packet-filtering-firewalls/

https://sandstormit.com what-is-a-firewall-and-why-do-i-need-one/

https://www.fortinet.com/resources/cyberglossary/stateful-vs-stateless-firewall





***
### Overcome challenges



***
### 
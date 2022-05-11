## IP adressen

* IP address
An IP address is a numeric address: it is an identifier for a computer or device on a network. Every device has to have an IP address for communication purposes.

* Public en Private IPs

There are two different types of IP addresses:
        * Public
        * Private

Public IP address: when u want a connection to the Internet, yuo will need a internet service provider. They will assign a modem/router in your place with a public IP address.
* This public IP address is what's registered on the internet and gives you access to the world wide web (Internet). IF u do not have a public IP address, u cannot access the Internet.
* Public IP addresses are unique (there are no duplicates in the world)

When the IPv4 addresses were created the engineers did not realise how big the internet would become. Although there are over 4 billion IP version 4 addresses available, due to th e xplosive growth of the Internet they almost are running up. So in order to prevent a shortage of IP4 addresses engineers developed Private IP addresses.

Private IP address: These are not publicly registered on the Internet.
* So u cannot access the Internet using a Private IP address.
* When u have a device with a Private IP address and u wish to access the Internet, this Private IP address has to be converted to a Public IP address.
* Private IP addresses are only used internally, (home or business).
The DHCP server (service) inside your Router is what assigns your internal devices a Private IP.
A home or business has multiple devices with their own Private IP adresses that need access to the Internet. These Private IP addresses will be translated to the one Public IP Address that we have been given by the ISP.
And the service that translates this is called NAT. 


    * NAT (Network Address Translation)

        NAT is a service built into our router.It translates private to public and also public to private. Because when a computer on the Internet wants to communicate with a computer on your private network (LAN) the public IP address needs to be translated bu NAT to the private IP address for that computer.
                

Private IP addressess have three different classes and these classes have different ranges.

Class | IP Address Range          | Default Subnet Mask
----- | :-------------------------: | :-------------------:
A | 10.0.0.0 -10.255.255.255 | 255.0.0.0
B | 172.16.0.0. - 172.31.255.255 | 255.255.0.0.
C | 192.168.0.0. - 192.168.255.255 | 255.255.255.0

* Class A starts with the number 10 and is typically used by large organisations.
* Class B starts with 172 and is typically used by medium-sized organisations.
* Class C starts with 192 and is used in small organizations and homes. This Class is the mostly used.


Public IP | Private IP
--------- | ----------
Unique | Non-Unique. Can be used on other networks.
Publicly registered on the internet | Not publicly registered
Used externally | Used Internally
Assigned by a ISP | Assigned by a Router (pool with numbers)
Not free | Free
Not Secure (use VPN) | More secure

CIDr nog uitleggen


* DHCP (Dynamic Host Configuration Protocol)
Every computer or device on a network has to have an IP adddress to communicate. An IP address identifies a computer / device on a network. There are two ways that a computer can be assigned an IP address: 

* Static IP or Dynamic IP.

         * A Static IP is where an user assigns a computer or device an IP address ** Manually**






* Statische en dynamische adressen
 IPv4 en IPv6


***
## Key terminology

* IP adressen
* IPv4 en IPv6
* Public en Private IPs
* NAT
* CIDR
* Statische en dynamische adressen




***
## Exercise



***
### Sources

https://www.youtube.com/watch?v=ddM9AcreVqY

https://www.youtube.com/watch?v=XQ3T14SIlV4







***
### Overcome challenges



***
### Results

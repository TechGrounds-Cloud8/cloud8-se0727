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

Static IP or Dynamic IP.

A Static IP is where an user assigns a computer or device an IP address   *Manually*:
So for each computer on the network you had to open up the computer network configuration page and manually type in the IP address, subnetmask, default gateway and DNS server. When u want to add an another computer to the network you would have to do the same thing on that computer. This is a lot of work.

There is a better and easier way to assign an IP address to a computer and this is called an Dynamic IP.

A Dynamic IP is where a compter gets an IP Address automatically from a DHCP server. A DHCP server automatically assigns a computer with an IP address. And also subnetmask, default gateway and DNS server.

The DHCP server assigns the IP address as a lease. A lease is the amount of time an IP address is assigned to a computer.
The lease is to help make sure the DHCP server does not run out of IP addresses in its pool/scope.

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

* Ontdek wat je publieke IP adres is van je laptop en mobiel op wifi.

![alt text](../00_includes/NTW/Public%20IP%20Laptop.PNG)


* Zijn de adressen hetzelfde of niet? Leg uit waarom.

Public IP address are the same, because both devices belongto the LAN network and uses thee default gateway of the Router to connect to the Internet.(Public IP address of the Router)

* Ontdek wat je privé IP adres is van je laptop en mobiel op wifi.

![alt text](../00_includes/NTW/Private%20IP%20via%20cmd%20prompt.PNG)
![alt text](../00_includes/NTW/verbonden%20app%20%20met%20private%20ip%20address.PNG)

* Zijn de adressen hetzelfde of niet? Leg uit waarom.

Private addresses zijn op een paar digits niet hetzelfde. Every device has its own Private IP address.


* Verander het privé IP adres van je mobiel naar dat van je laptop.  Wat gebeurt er dan?


![alt text](../00_includes/NTW/veranderen%20ip%20add%20laptop%20en%20mobiel.PNG)

* Probeer het privé IP adres van je mobiel te veranderen naar een adres buiten je netwerk. Wat gebeurt er dan?

![alt text](../00_includes/NTW/ping%20nu%20website.PNG)


![alt text](../00_includes/NTW/veranderen%20ip%20address%20mobiel%20nr%20nu%20website.PNG)


Tip: vergeet niet je instellingen weer terug te zetten wanneer je klaar bent met de opdracht.


***
### Sources

https://www.youtube.com/watch?v=ddM9AcreVqY

https://www.youtube.com/watch?v=XQ3T14SIlV4







***
### Overcome challenges



***
### Results

## Sec-02 Firewalls
***
What is a Firewall?

Firewalls are hardware and/or software systems which protect end users from malicious traffic on the Internet. When data is sent over the Internet, it comes packaged with information about where it is coming from and where it is supposed to go, as well as an indication as to what application the data is for.

Firewalls accomplish this control by inspecting data packets. The data within the packets can be inspected by the firewall to see if it contains threats. Part of this process involves checking how the data should connect to and move through the network. 


### stateful firewalls vs stateless firewalls

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


### hardware firewalls vs software firewalls

The main difference between a hardware firewall and a software firewall is that the hardware firewall runs on its own physical device, while a software firewall is installed on another machine. A common example of a software firewall is the firewall built into most operating systems like Windows and macOS. 

Difference between Hardware and Software firewall : 

Software Firewall |	Hardware Firewall
----------------- | ------------------
Software Firewall operates on the system. |	Hardware Firewall do not operate on the system.
Configuration of software firewall is easy.	| Configuration of hardware firewall is not easy.
It is more expensive. | It is cheaper than software firewall.
It is flexible i.e., you can choose which application has to be installed. |	It is not flexible like software firewall.
It is installed inside the individual system. |	It is installed outside the system.
It protects the one system at a time. |	It protects a whole network at a time.
It makes the performance of computers slows down.| It doesn’t affects the performance of the computer.
It has needed to be installed on every individual system on a network. |	It needs only one hardware to be installed for a whole network.



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

How Do I Know If Apache Is Installed?
You can enter http://server-ip:80 on your web browser as the address for an Apache web server. You should see the statement that your Apache server is functioning properly. Clicking this command will enable you to confirm whether or not Apache is running.


* Stel de firewall zo in dat je webverkeer blokkeert, maar wel ssh-verkeer toelaat.
* Controleer of de firewall zijn werk doet.



***
### Sources

https://www.geeksforgeeks.org/stateless-vs-stateful-packet-filtering-firewalls/

https://sandstormit.com what-is-a-firewall-and-why-do-i-need-one/

https://www.fortinet.com/resources/cyberglossary/stateful-vs-stateless-firewall

https://www.checkpoint.com/cyber-hub/network-security/what-is-firewall/what-is-a-hardware-firewall/#:~:text=The%20main%20difference%20between%20a,systems%20like%20Windows%20and%20macOS.

https://opensource.com/article/18/9/linux-iptables-firewalld

https://linuxhint.com/open-port-80-centos/

https://linuxconfig.org/ubuntu-20-04-open-http-port-80-and-https-port-443-with-ufw

https://linuxize.com/post/how-to-setup-a-firewall-with-ufw-on-ubuntu-18-04/#check-ufw-status


https://www.delftstack.com/howto/linux/configuring-the-apache-web-server-on-ubuntu-and-debian/

https://www.delftstack.com/howto/linux/configuring-the-apache-web-server-on-ubuntu-and-debian/




***
### Overcome challenges

Check UFW Status
Once the installation is completed you can check the status of UFW with the following command:
sudo ufw status verbose
Copy
UFW is disabled by default. If you never activated UFW before, the output will look like this:

Status: inactive

UFW Default Policies
By default, UFW will block all of the incoming connections and allow all outbound connections. This means that anyone trying to access your server will not be able to connect unless you specifically open the port, while all applications and services running on your server will be able to access the outside world.
The default polices are defined in the /etc/default/ufw file and can be changed using the sudo ufw default <policy> <chain> command.

Allow SSH Connections
Before enabling the UFW firewall we need to add a rule which will allow incoming SSH connections. If you’re connecting to your server from a remote location, which is almost always the case and you enable the UFW firewall before explicitly allow incoming SSH connections you will no longer be able to connect to your Ubuntu server.

To configure your UFW firewall to allow incoming SSH connections, type the following command:

sudo ufw allow ssh
Output:
Rules updated
Rules updated (v6)

f you changed the SSH port to a custom port instead of the port 22, you will need to open that port.

For example, if your ssh daemon listens on port 4422, then you can use the following command to allow connections on that port:
sudo ufw allow 55813/tcp

Enable UFW
Now that your UFW firewall is configured to allow incoming SSH connections, we can enable it by typing:
sudo ufw enable
Output:
Command may disrupt existing ssh connections. Proceed with operation (y|n)? y
Firewall is active and enabled on system startup
You will be warned that enabling the firewall may disrupt existing ssh connections, just type y and hit Enter.

Allow connections on other ports

Depending on the applications that run on your server and your specific needs you’ll also need to allow incoming access to some other ports.

Below we will show you a few examples on how to allow incoming connections to some of the most common services:

Open port 80 - HTTP
HTTP connections can be allowed with the following command:
sudo ufw allow http
instead of http you can use the port number, 80:
sudo ufw allow 80/tcp  to allow HTTP connections.
or sudo ufw allow http  to allow HTTP connections.


Access Web Server Through a Browser
We can now access the webserver through the browser.

Open the browser of your choice. We have used Firefox in this tutorial and typed the localhost IP address.

The notation should look like the following.

http://your_server_ip

In our case, we have typed http://18.196.32.244:55813 and pressed Enter. This should take you to the Apache default page.

If you see the Apache default page, it means you have successfully installed the Apache webserver on your system.


Denying connections
The default policy for all incoming connections is set to deny, and if you haven’t changed it, UFW will block all incoming connections unless you specifically open the connection.

Writing deny rules is the same as writing allow rules; you only need to use the deny keyword instead of allow.

sudo ufw deny from http or 80/tcp



Deleting UFW Rules
There are two different ways to delete UFW rules by rule number, and by specifying the actual rule.

Deleting rules by rule number is easier, especially when you are new to UFW. To delete a rule by a rule number first, you need to find the number of the rule you want to delete. To get a list of numbered rules, use the ufw status numbered command: sudo ufw status numbered
Output
Status: active

     To                         Action      From
     --                         ------      ----
[ 1] 22/tcp                     ALLOW IN    Anywhere
[ 2] 80/tcp                     ALLOW IN    Anywhere
[ 3] 8080/tcp                   ALLOW IN    Anywhere

To delete rule number 3, the one that allows connections to port 8080, you would enter: sudo ufw delete 3
Output: see list above without 3






***
https://linuxize.com/post/how-to-setup-a-firewall-with-ufw-on-ubuntu-18-04/

https://phoenixnap.com/kb/configure-firewall-with-ufw-on-ubuntu#ftoc-heading-5


***
### 
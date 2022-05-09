# NTW-01  OSI Stack

OSI stands for Open System Interconnection Model.

The OSI model was made for connecting open systems. These systems are created/designed to be open for communication with almost any other system.

The OSI model defines internetworking in terms of a vertical stack of seven layers to explain the flow of information. The OSI model can be used as a guide for how data is transmitted over the network (an abstract representation of the data pathway).

The upper layers of the OSI model represent software that implements network services like encryption and connection management. 
The lower layers of the OSI model implement hardware-oriented functions like routing, addressing, and flow control.

![alt text](../00_includes/NTW/OSI-model%20overview.PNG)

The following are the 7 OSI layers:

* Layer 7 – Application Layer
The application layer is the layer where application and users interaction will take place like outlook, File Explorer, Chrome, or some other applications using different protocols HTTP (web communication), HTTPS (Secured web communication), SMB (file transfer).

* Layer 6 – Presentation Layer
This layer formats the data so (helps to Encrypt or Decrypt) that the receiving application can understand the data. One example is SSL (encryption) communication requirements for an application.


* Layer 5 – Session Layer
The session layer handles/manages the opening and closing of a session between application processes. Like RPC (remote procedure calls).

* Layer 4 – Transport Layer
The transport layer in the OSI model takes care of data transfer between different networks. It establishes connection between two machines (unlike lower layers which aids in establishing connection)!!
TCP and UDP are the most common data transfer protocols used. Data is divided in segments and reassembled into a data stream.

* Layer 3 – Network Layer
The network layer is where the route of your data transfer from one computer to another machine is handeld. The physical device attached to this network layer are Layer 3 Switches and Routers.
Source and Destination IP addresses are added to the data in the network layer. The Network layer sends Packets between peer network layers.


* Layer 2 – Data Link Layer
 The Data link layer in the OSI model defines the protocol to make/create and terminate a connection between two physically connected devices.
 There are two sub-layers as part of the Data link layer.
    * Medium access control (MAC) layer (MAC address)
    * Logical link control (LLC) layer
 The devices which are part of Data link: Switches and Bridges
 Source and Destination MAC addresses are added to the data in the Data Link Layer. The Data Link layer sends Frames between peer data link layers.
 
* Layer 1 – Physical Layer
Transmission and reception data between a device and a physical medium. As the name implies the physical layer is all about the Bluetooth, Optical Cable, Ethernet cable, and USB. Hubs and Repeaters are also considered as devices function at the physical layer.
The Physical layer sends Bits between peer physical layers

Data Encapsulation and Data De-Encapsulation gives a good overview how and in which format and whith what added information the data is processed and send.

Data Encapsulation happens when data is transmitted from the application layer to the physical layer of the OSI reference model.



Following the data stream on the figure above:

Alphanumeric user input is converted to data for transmission on the network (At the upper layers)

Data is converted to segments, which allow hosts to reliably communicate (At the Transport Layer)

Segments are converted to packets or datagrams with a source and destination logical address (At the Network layer)

Packets or datagrams are converted to frames for transmission over an interface to the network (At the Data Link Layer)

Frames are converted to bits, and uses a synchronization and clocking function (At the Physical Layer)

Again, data encapsulation occurs when going from layer 7 to layer 1 of the OSI reference model.










***
## Key terminology

OSI Model
TCP/IP Model
Data Encapsulation




***
## Exercise


***
### Sources

https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/

https://www.javatpoint.com/osi-model

https://www.geeksforgeeks.org/layers-of-osi-model/

https://www.guru99.com/layers-of-osi-model.html

https://www.anoopcnair.com/it-support-osi-model-troubleshooting/

https://www.guru99.com/tcp-ip-model.html

https://www.certificationkits.com/cisco-certification/cisco-ccna-640-802-exam-certification-guide/cisco-ccna-the-osi-model/



### Overcome challanges
[Give a short description of your challanges you encountered, and how you solved them.]

### Results
[Describe here the result of the exercise. An image can speak more than a thousand words, include one when this wisdom applies.]

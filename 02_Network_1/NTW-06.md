## NTW-06 SubNetting

IP Address Strcuture

10|0|0|0
--|--|--|--

Octet 1 | Octet 2 | Octet 3 | Octet 4
------- | ------- | ------- | -------

1|1|1|1|1|1|1|1    -------- 8 bits binary values
-|-|-|-|-|-|-|-


128 | 64 | 32 | 16 | 8 | 4 | 2 | 1  --------- Decimal Values
--- | --- | -- | -- | -- | -- | -- | --


Each octet range will be between 0-255

Each octet size is 8 bits, total octet size will be 32 in IPv4 address space.

#### Available IPs Depends on NW prefix

Example: 192:168:0.0 /16

Formula:

Total available Host bits = Total Bits -/- NW prefix

32 bits - 16 bits = 16

Total available IPs = 2^ Total available host bits

2^16 = 65536 IPs

#### How many subnets: 

2n -2, 

Where the exponent n is equal to the number of bits left after subnet bits are borrowed.

we can calculate how many bits will be required so that each subnet has 30 host addresses. 25 -2 =30, so 5 bits atleast must be available for host addressing and the remaining can be borrowed to create subnet addresses. The -2 in the formula accounts for two addresses the subnetwork address and the broadcast address which cannot be assigned to hosts.

Example: requirement of 200 IP and want to allocate 100 IP in subnet 1 and 100 ip in subnet 2
Note: always make sure that subnet prefix must be greater than its Virtual Network above.
VNET of 192.168.0.0 /24 (256 IPs)
SUbnet1 needs 100 IPs
Subnet2 needs 100 IPs

2^n-2=100
2^n = 102
2^7 =102 (2^6 = 64)

So 32-7 = 25 are used for network, 7 bits are used for hosts. So, n is 7, 7 bits are left after subnet bits (1) are borrowed. 25 bits are part of Network IP address so prefix of subnet is /25

#### Find Start IP and End IP range for subnet1

1111 111 . 1111 1111 . 1111 1111 . 1000 0000 

25 bits are part of Network IP address so prefix of subnet is /25

7 bits are part of the host IP address

128 | 64 | 32 | 16 | 8 | 4 | 2 | 1  
--- | --- | -- | -- | -- | -- | -- | --
1 | 0 | 0 | 0 | 0 | 0 | 0 | 0

So first bit of last octet is part of Network, So there are 64+32+16+8+4+2+1 is 127 hosts, with 127 as End range.

128 is also Magic Number, so each subnet starts after 128 hosts.

Start Range is  192.168.0.0 is reserved for Router
LAst ip address i first Subnet is reserved for broadcasting 192.168.0.127

192.168.0.0 /24

So Subnet 1 Range : 192.168.0.1 /25 - 192.168.0.126 /25

(192.168.0.0 /25 Router,  192.168.0.127 Broadcast))

So Subnet 2 Range : 192.168.0.129 /25 - 192.168.0.254 /25

(192.168.0.128 Router, 192.168.0.255 Broadcast).


















***
## Key terminology

IPv4 Address
Mask
Subnet
Double 
Magical Number 



***
## Exercise and Results

The requirement is to perform subnetting such that we create as many subnets as we can with 30 hosts in each subnet.

Our First step will be to determine how many bits do we need to borrow from the host portion such that the requirement of minimum 30 hosts per subnet is fulfilled. Using the formula below

2n -2, 

Where the exponent n is equal to the number of bits left after subnet bits are borrowed.

we can calculate how many bits will be required so that each subnet has 30 host addresses. 25 -2 =30, so 5 bits atleast must be available for host addressing and the remaining can be borrowed to create subnet addresses. The -2 in the formula accounts for two addresses the subnetwork address and the broadcast address which cannot be assigned to hosts.

The network 192.168.116.0/24 has 8 bits for host portion and we will reserve 5 bits for the new host portion, the 3 bits remaining can now be used for creating subnets. To determine how many subnets we can

create, use the following formula:

2n = number of subnets

where the exponent n is bits borrowed from the host portion.

Thus in this case we can create 23 =8 subnets



***
### Sources

https://cidr.xyz/

https://www.certificationkits.com/cisco-certification/ccna-articles/cisco-ccna-network-layer-conceptslayer-3/calculate-hosts-in-a-subnet-networks-in-a-subnet-a-range-of-ips/




***
### Overcome challenges

Understanding the concept of CIDR notation and calculating 
network adress, first usuable ip an dlast uasable ip address, the number of subnets available etc.



***
### 

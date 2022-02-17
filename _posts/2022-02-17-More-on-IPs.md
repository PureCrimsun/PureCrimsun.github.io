              **************Notes for the day**************
Every single board has a Mac address that is different 
IPs can be changes Mac addresses "can't"
ARP maps IPs to Mac addresses

each number in a IPv4 has to be between 0 and 255
each numbber is actaully a 8 bit binary number. That is why they are limmited to 0-255
octet=binary number. 

Bit 1 = 128
Bit 2 = 64
Bit 3 = 32
Bit 4 = 16
Bit 5 = 8
Bit 6 = 4
Bit 7 = 2
Bit 8 = 1
          192.168.1.1
128+64=192 making the first part of the IP in binary "11000000"
1 in Binary is 00000001

IPv4 addresses can not end in 0 or 255. Those are reserved for Network addresses and broadcast addresses
every host must have its own IP address
Since IP addresses cant be shared IPv4 has a problem of only being able to have 4 billion unique address
NAT-Network Address Translation is one of the ways around this problem
NAT routers use a registered IP address to be connected to the internet. The IP addresses on the other side of the router (your own net work) Use unregistered addresses. 
NAT takes all off the addresses in the network and translates them into the 1 registered IP address.

Reserved IP address ranges (private IP addresses)
10.0.0.0 - 10.255.255.255
172.16.0.0 - 172.31.255.255
192.168.0.0 - 192.168.255.255
these addresses have not been registered with anyone in the world
These addresses are non-routable and will not work without a NAT router.

sub net mask
IP addresses assigned to a host are split into 2 parts 
Network and Node The node is specific to the device on the network.
192.168.1.1 
192.168.1 is the network portion of the address
---.---.-.1 is the node portion of the address
Every host on the same network must have exactly the same numbers in the network portion of their IP address. Conversely, they must have unique numbers in the node portion.
Think of this a houses built on a street. The Network portion is the street name while the Node portion is the house number. 
*** The amount of the address that is used for the network and the amount that is used for the node address can change, depending upon what the address is. ***
There are three default subnet masks 255.0.0.0, 255.255.0.0, and 255.255.255.0. 
Any octet with a 255 in it for a default subnet mask indicates that that is the network portion of the address. 
Any octet with 0 indicates that is the host, or node, portion of the address.
The subnet mask is used to 

IP addresses are divided into five different default classes, and each address class has its own default subnet mask.
The important thing to remember about a class A IP address is that the decimal value of the first octet of that IP address has to be within the range of 1-126.
Using the default subnet mask of 255.0.0.0., that means that only the first octet of the IP address is used for the network address, 
and the last three octets are the node address.

In a class B address, the decimal value of the first octet must be between 128 and 191. subnet= 255.255.0.0

In a class C address, the decimal value of the first octet of the IP address must be between 192 and 223. subnet = 255.255.255.0

CIDR Notation is the short hand for subnet masks. This is done by simply adding a backslash (/) at the end of the IP address followed by the number of bits in the subnet mask. 
The notation referres to the network portion of the subnet mask. 
192.168.1.1/24 is
11111111.11111111.11111111.00000000 or
255.255.255.0 making it a class C address

You can also use only part of an octet for a network address, if you want to. This is called partial subnetting or variable length subnet masking (VLSM).
Using VLSM, we completely ignore all of the default subnet masks

11111111.11111111.111111-00.00000000 (255.255.252.0) Subnet
11000000.10101000.000000-01.00000001 (192.168.1.1) IP


11111111.11000000.00000000.00000000 (255.192.0.0)
![VLSM pic](https://user-images.githubusercontent.com/99808189/154563956-6b8490ec-8f43-4a24-ac06-f59b2f3d55e3.PNG)


![IP classes](https://user-images.githubusercontent.com/99808189/154567298-f2704790-13b5-42c5-85e3-d0030f06ae77.PNG)


![subnetting short cut](https://user-images.githubusercontent.com/99808189/154567490-03989b7e-cebb-47a3-99b7-3ecfe6bd21ae.PNG)






















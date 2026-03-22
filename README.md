# Variable-Length-Subnet-Masks
Designed and implemented a subnetted network using Cisco Packet Tracer by dividing a /24 into multiple LANs and a point-to-point link. Configured IP addressing, assigned gateways, and implemented static routing to enable full connectivity between networks.

## Platforms Leveraged
- Cisco Packet Tracer

##  Scenario

My job is to subnet the 192.168.5.0/24 network to provide sufficient addressing for all four LANs as well as the point-to-point connection between R1 and R2. I will assign the first usable address to the PC in each LAn, then assign the last usable address to the router's interface in each LAN. After that, I will configure the static routes on each router so that all PCs can ping eachother.

<img width="753" height="332" alt="Screenshot 2026-03-21 at 6 23 48 PM" src="https://github.com/user-attachments/assets/cff0b307-69c5-43f1-a90b-ac6f0bed3260" />

---

## Steps Taken

### 1. Assign the largest subnet at the start of the address space. Then assign the second-largest subnet after it. Repeat the process until all subnets have been assigned.

In the lab, the largest subnet is LAN 2 with 64 hosts so this is the first subnet chosen. I borrowed seven bits so all 64 hosts can fit in the subnet. The borrowed hosts came out to 126 hosts, making LAN 2 a /25 subnet. The network address of LAN 2 is 192.168.5.0/25 when you turn all the borrowed bits into zeros. The first usable address is 192.168.5.1/25. The broadcast address is 192.168.5.127/25 because I turned all the borrowed bits into ones. Making the last usable address 192.168.5.126/25.

I repeated the process for the other three LANs including the point-to-point connection. I did the subnetting process in the screenshot below.

![IMG_3201](https://github.com/user-attachments/assets/197a3536-3a59-4fac-b6bf-451fe39e3739)

### 2. Assign the first usable address to the PC in each LAN

<img width="1690" height="1035" alt="Screenshot 2026-03-21 at 11 05 20 PM" src="https://github.com/user-attachments/assets/5ff7ffc0-4156-4de2-bd23-dcf4240ac781" />

### 3. Assign the last usable address to the router's interface in each LAN

<img width="843" height="191" alt="Screenshot 2026-03-21 at 11 13 40 PM" src="https://github.com/user-attachments/assets/885e93bd-6d42-4477-af9f-a3514589e8e0" />



**Query used to locate events:**

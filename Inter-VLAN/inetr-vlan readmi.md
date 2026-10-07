## VLAN Configuration using Cisco Packet Tracer 🌐
### 📌 Project Overview
This project demonstrates Inter-Virtual Local Area Network (IVLANs)using Cisco Packet Tracer. The lab is designed to showcase how to configure VLANs on switches and routers to enable communication between devices across different VLANs. The goal is to familuarize users with VLAN configuration, router-on-a-stick setup, and effective communication between VLANs.
### 🧰 Tools Used
- Cisco Packet Tracer
### 🥅 Network Setup 
- 1 router
- 2 switches 
-Multiples PCs
- Ethernet(Copper straight-through)
-Trunk link between switches
- Trunk link between first switch and router
### 🌐 VLANs Detials
| VLANs ID | departments |
| :--- | ---: |
| VLAN 10 | sales |
| VLAN 20 | marketing |
| VLAN 30 | Finance |
### ⚙ Configuration Details
##### 🔸 VLAN Creation
 enable
config terminal

vlan 10  
name sales  
exit  

vlan 20  
name marketing   
exit 

vlan 30  
name finance   
exit 
### 🔹 Assign Ports to VLANs

interface rang fastethernet 0/1 -2  
switchport switch mode access  
switchport acces vlan 10  
exit

interface range fastehernet 0/3 -4  
switchport mode access   
switchprot access vlan 20  
exit

interface rang fastethernet 0/5 -6  
switchport mode access  
switchport access vlan 30  
exit  
### Configur to Router(Roter-on-a-stick)
##### a. Access the router CLI
enable  
config terminal 
interface gigabitethernet 0/1  
no shutdown  
exit  
##### b. created sub-interfaces for each VLAN   
interface gigabitethernet 0/1.1    
encapsulation dot1q 10  
ip address 192.168.10.10/24    
exit  

 interface gigabitethernet 0/1.2  
 encapulation dot1q 20  
 ip address 192.168.20.10/24  
 exit  

 interface gigabitethernet 0/1.3  
 encapsulation dot1q 30  
 ip address 192.168.30.10/24  
 exit  
### 🔹 Trunk Configuration (between switches)

interface fastethernet 0/23  
switchport mode trunk  
exit    

interface gigabitethernet 0/1  
switchport mode trunk  
exit  
##### 👉 Allow multiple VLAN traffic bewteen switches
### 💻 PC Configuration 
###### Each VLAN uses a diffrent IP rang
| VLAN | EXAMPLE IP | default Gateway |  
| --- | ---| --- |
| VLAN 10 | 192.168.10.x | 192.168.10.10 |
| VLAN 20 | 192.168.20.x | 192.168.20.10 |
| VLAN 30 | 192.168.30.x | 192.168.30.10 |
### 🧪 Testing
- ##### Ping from one VLAN to another 
Test the connectivity by pinging from a PC in  VLAN 10 to a PC in VLAN 20.
if configuration is ciorret, the devices will be able to communicate through the router.
### 🎯 Learning Outcomes  
- Inter-VLAN creation and management
- Network segmentation
- Trunking between switches
- Trunking between switch and router  
- Improved network security and performance
### 📁 Files Included
- Inter-valn.pkt ➡ Packet tracer file
- screenshots of Inter-VLAN topology
### 👨‍💻 Author
 Aamin pinjari
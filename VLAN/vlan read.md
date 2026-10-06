## VLAN Configuration using Cisco Packet Tracer 🌐
### 📌 Project Overview
This project demonstrates the configuration of Virtual Local Area Network (VLANs)using Cisco Packet Tracer. Multiple VLANs are created to logically segment the network into different departments and control communication between devices.
### 🧰 Tools Used
- Cisco Packet Tracer
### 🥅 Network Setup
- 2 switches 
-Multiples PCs
- Ethernet(Copper straight-through)
-Trunk link between switches
### 🌐 VLANs Detials
| VLANs ID | departments |
| :--- | ---: |
| VLAN 10 | sales |
| VLAN 20 | marketing |
| VLAN 30 | Finance |
### ⚙ Configuration Details
##### 🔸 VLAN Creation
 <span style="color:red">enable
config terminal

vlan 10  
name sales  
<span style="color:red">exit  

vlan 20  
name marketing   
<span style="color:red">exit 

vlan 30  
name finance   
<span style="color:red">exit 
### 🔹 Assign Ports to VLANs

interface rang fastethernet 0/1 -2  
switchport switch mode access  
switchport acces vlan 10  
<span style="color:red">exit

interface range fastehernet 0/3 -4  
switchport mode access   
switchprot access vlan 20  
<span style="color:red">exit

interface rang fastethernet 0/5 -6  
switchport mode access  
switchport access vlan 30  
<span style="color:red">exit  
### 🔹 Trunk Configuration (between switches)

interface fastethernet 0/23  
switchport mode trunk  
<span style="color:red">exit  

##### 👉 Allow multiple VLAN traffic bewteen switches
### 💻 PC Configuration 
###### Each VLAN uses a diffrent IP rang
| VLAN | EXAMPLE IP |
| --- | ---|
| VLAN 10 | 192.168.10.x |
| VLAN 20 | 192.168.10.x |
| VLAN 30 | 192.168.30.x |
### 🧪 Testing
- VLAN creation and management
- Network segmentation
- Trunking between switches  
- Improved network security and performance
### 📁 Files Included
- valn.pkt ➡ Packet tracer file
- screenshots of VLAN topology
### 👨‍💻 Author
 Aamin pinjari
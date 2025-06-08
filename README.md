# 🕸️ SMALL OFFICE HOME OFFICE🕸️

---
![image](https://github.com/user-attachments/assets/6acdaed1-e891-4abb-90c1-a0f84bc71d84)

## 🎯 Project Goal
- Design and configure a small office network that supports:
- Internet access
- Segmented departments (using VLANs)
- Central DHCP
- Secure switch/router configurations
- Inter-VLAN communication

## 🖥️ Scenario Overview
We are tasked with setting up a network for a small company with 3 departments:
- HR (VLAN 10)
- IT (VLAN 20)
- Sales (VLAN 30)
Each department has 3-4 PCs. All devices must have dynamic IPs

## 🧱 Network Components

- 1 Router (e.g., Cisco 2911)
- 2 Switches (e.g., 2960)
- 1 Server (DHCP & DNS)
- 1 ISP simulator (another router as ISP)

10 PCs (3–4 per department)

---

## 🔧 Configuration Steps

**1. Assign VLANS**
<br>
On Switch 1 4 PCs were assigned to VLAN 10 and 3 PCs were assigned to VLAN 30. G0/0 was assigned as a trunk port in order to carry VLAN traffic. The same steps were repeated on switch 2 for the cpresponding VLANs and trunk ports.

![image](https://github.com/user-attachments/assets/c8229833-8492-4c95-9ece-2c372da35f07)

---

**2. Configure Inter-VLAN routing**
<br>
On the Router we set up sub-interfaces for each vlan and assigned their respective subnets.

![image](https://github.com/user-attachments/assets/582d6d53-91fa-4bfa-b9b6-98601bdc1a90)

---

**3. Configure DHCP**
<br>
Set the scope for each VLANs (Also set a route to the ISP for external connection *not really neccessary for this lab*)

![image](https://github.com/user-attachments/assets/2a5c6a3b-d09b-4b4e-86d2-21f452cb2bfd)


---

**4. Configure Port Security**
<br>
To ensure no unauthorized devices connect to the switches we will enable port security. Repeat for other switch as well. 

![image](https://github.com/user-attachments/assets/19d15659-6cd6-4be6-8023-5edb2b40bf0d)


---








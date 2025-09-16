# 🔐 Configure PfSense & Set up virtual networking 


## 📖 **Part 1**


- ### ⚙️1 Reset the admin account and password 
 
- ### 🖊2 Assisgn interfaces
    - Set em0 as the Wan 
    - Set static em1 as the LAN address 

- ### ⌨️3 Set interfaces IP address 
  - Set Ip address for the WAN interface 10.0.0.1/24 ( the address should be the hosts' IP address)
  - Set Ip address for the LAN interface 192.168.10.1/24

## 📡 **Part 2** Set up networking 
  - In settings --> network --> adapter --> set Adapter 1 to NAT, Adapter 2 to Homelab, and Adapter 3 to inet.
  - Adapter 1 is set to Nat to keep the VMs isolated, but you can set this to bridged. ( if set to bridged it will get a different IP address than the Host computer has) 
  - Homelab is the name of the internal network.
  - Adapter 3 is set to inet. This will act as the DMV in later projects
 ---
    
   <img width="358" height="78" alt="image" src="https://github.com/user-attachments/assets/ea112b83-03d8-4dfc-bdb6-0f3a1f4845ad" />
   
---
### 🧱1 Set Internal Network
<img width="423" height="117" alt="image" src="https://github.com/user-attachments/assets/508c7e47-539a-4930-a634-1752029e8fec" />


  - Navigate to settings --> network --> Adapter 1 & select " Internal Netowrk".
  - Name your internal network Homelab (same as the internal network name for the fire wall)
  - Do this for each vm you intend to have on the same network as the Firewall
---
## Unsure how to segement the network? [Click Here](/VLAN-Guide.md)

 ### 3 Set IP Addresses for machines 
 - Each device's method for setting an IP may be different.
 - The goal is to create VLANs!
 - Be sure to set the gateway to the IP of PfSense
 
---
> [!IMPORTANT]
> **Once you added the IP, you should be able to ping other devices on network.**


   <img width="496" height="289" alt="image" src="https://github.com/user-attachments/assets/445badc9-41ff-4a01-baca-1ad1749dec49" />

---


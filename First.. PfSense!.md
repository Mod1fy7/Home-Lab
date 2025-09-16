# Configure PfSense
### Set up virtual networking 

## Part 1 

### 1 Reset the admin account and password 

### 2 Assisgn interfaces 

Set em0 as the Wan 
Set static em1 as the LAN address 

### 3 Set interfaces IP address 

Set Ip address for the WAN interface 10.0.0.1/24 ( the address should be the hosts' IP address)
Set Ip address for the LAN interface 192.168.10.1/24

##Part 2 Set up networking 
<img width="358" height="78" alt="image" src="https://github.com/user-attachments/assets/ea112b83-03d8-4dfc-bdb6-0f3a1f4845ad" />

## Do the same for all other VMS 
<img width="423" height="117" alt="image" src="https://github.com/user-attachments/assets/508c7e47-539a-4930-a634-1752029e8fec" />


 Ensure all machines are on the same LAN 
 <img width="496" height="289" alt="image" src="https://github.com/user-attachments/assets/445badc9-41ff-4a01-baca-1ad1749dec49" />

 ## Set static IP address for workstations. Ensuring they are on the same LAN and subnet. 
in this example I set the IP addresses as follows


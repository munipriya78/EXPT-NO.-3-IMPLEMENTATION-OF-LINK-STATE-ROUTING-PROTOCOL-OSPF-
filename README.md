# EXPT NO.3 IMPLEMENTATION OF LINK STATE ROUTING PROTOCOL OSPF
# AIM

To connect computers in multiple networks using Open Shortest Path First Routing Protocol and to verify the connectivity between computers.

# EQUIPMENTS REQUIRED
Desktop Computer
Cisco Packet Tracer 5.0 Software

# IP ASSIGNMENT
<img width="829" height="519" alt="image" src="https://github.com/user-attachments/assets/b24b2e4e-aea0-4a52-982c-8a1f0c5579de" />

# NETWORK DIAGRAM
<img width="678" height="468" alt="image" src="https://github.com/user-attachments/assets/5d7bb16a-81ea-40d8-9ad9-638a7c2a9fd5" />


# PROCEDURE
STEP 1: Open a Packet Tracer Software.
STEP 2: Drag two 2900 Switches, two Cisco 1800 Routers, four PC Terminals from tool bar and drop it in work area.
STEP 3: Connect all the PC Terminals and Routers through Switches as shown in the network diagram using CAT 6 Patch cables.
STEP 4: Configure IP address and Gateway in all PC Terminals.
STEP 5: Configure Delhi router IP address, save configuration and restart Delhi router. STEP 6: Configure Chennai router IP address, save configuration and restart Chennai router. STEP 7: Check the connectivity between the computers in network.
STEP 8: Configure OSPF in Delhi router, Save configuration and restart Delhi router.
STEP 9: Configure OSPF in Chennai router, Save configuration and restart Chennai router.
STEP 10: Verify the connectivity between PC Terminals in different networks using Ping command.
STEP 11: Check the routing table in Delhi router and Chennai router using show ip route command.

## Programm:
## Router 0 Program
```
Router0> enable 
Router0# configure terminal 
Router0(config)# interface FastEthernet0/0 
Router0(config-if)# ip address 192.168.1.1 255.255.255.0 
Router0(config-if)# no shutdown 
Router0(config-if)# exit 
Router0(config)# interface Serial2/0 
Router0(config-if)# ip address 192.168.2.1 255.255.255.0 
Router0(config-if)# clock rate 64000 
Router0(config-if)# no shutdown 
Router0(config-if)# exit 
Router0(config)# router ospf 1 
Router0(config-router)# router-id 1.1.1.1 
Router0(config-router)# network 192.168.1.0 0.0.0.255 area 0 
Router0(config-router)# network 192.168.2.0 0.0.0.255 area 0 
Router0(config-router)# exit 
Router0# write memory
```

## Router 1 Program
```
Router1> enable 
Router1# configure terminal 
Router1(config)# interface FastEthernet0/0 
Router1(config-if)# ip address 192.168.3.1 255.255.255.0 
Router1(config-if)# no shutdown 
Router1(config-if)# exit 
Router1(config)# interface Serial2/0 
Router1(config-if)# ip address 192.168.2.2 255.255.255.0 
Router1(config-if)# no shutdown 
Router1(config-if)# exit 
Router1(config)# router ospf 1 
Router1(config-router)# router-id 2.2.2.2 
Router1(config-router)# network 192.168.3.0 0.0.0.255 area 0 
Router1(config-router)# network 192.168.2.0 0.0.0.255 area 0 
Router1(config-router)# exit 
Router1# write memory
```

# OUTPUT
## Router 0 Table
<img width="1161" height="462" alt="image" src="https://github.com/user-attachments/assets/f72c0cd3-cbb2-449e-ae6b-803cd040728d" />

## Router 1 Table
<img width="755" height="349" alt="image" src="https://github.com/user-attachments/assets/3de388df-9b86-4734-909b-6727a4dfec2f" />


# RESULT
Thus the computers in multiple networks using Open Shortest Path First Routing Protocol is connected and the connectivity between the computers is verified.


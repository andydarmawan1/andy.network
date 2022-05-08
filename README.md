#DHCP RELAY

STEP 1
Open the Cisco simulator software and create a network topology for the DHCP as follows

<img width="577" alt="Screen Shot 2022-05-08 at 20 41 54" src="https://user-images.githubusercontent.com/37010734/167299026-79350413-f1b7-4be7-84af-6d1e5f62e516.png">


STEP 2
Open the Cisco Router R1 CLI command prompt and configure the Router’s GigabitEthernet interfaces as follows

<img width="434" alt="image" src="https://user-images.githubusercontent.com/37010734/167299055-20ed9192-3e3c-439c-b569-72c634afc19d.png">



STEP 3
Configure the DHCP server on the router as follows.
Here, the purpose of enabling DHCP is to see the difference between Relay Agent. Then we will try to get the IP address from a different location by cancelling DHCP.

<img width="463" alt="image" src="https://user-images.githubusercontent.com/37010734/167299068-58f588bb-2314-4400-be5c-a4d860aa7cef.png">

STEP 4
Ping the connection form the PCI command prompt to the default gateway.

<img width="468" alt="image" src="https://user-images.githubusercontent.com/37010734/167299126-50c4fc3c-cae9-47cd-9043-f0fa43730e6b.png">


STEP 5
Configure the IP Address configuration of PC1 to DHCP and PC1 successfully retrived TCP/IP information from the DHCP server configured on the Router
 
<img width="468" alt="image" src="https://user-images.githubusercontent.com/37010734/167299119-c6b44708-e5e0-4b65-9a2b-7cb6f176765e.png">


STEP 6
Configure the server you added to the 192.168.10.0/24 network as follows and click the Add button to add the configuration to the list. After making sure that the DHCPRELAY pool is added to the list, proced to the next step

<img width="468" alt="image" src="https://user-images.githubusercontent.com/37010734/167299148-b596f647-e2a6-4dc8-a8f7-5567a8f8e27d.png">


STEP 7
Delete the DHCP pool with the no ip dhcp pool LAN command, and then execute the ip helper-address command on the interface that will act as AGENT.

<img width="468" alt="image" src="https://user-images.githubusercontent.com/37010734/167299164-3a5ea1e2-d677-4405-b92c-f2e9ac893c2c.png">


STEP 8
Please wait while obtaining the IP address

<img width="468" alt="image" src="https://user-images.githubusercontent.com/37010734/167299178-c707e48f-5562-4b0c-995d-7385475b21c4.png">


As you can see in the image below, PC1 received its TCP/IP settings from the DHCP Server with IP address 192.168.10.10. You can also see that it receives the IP address from block 192.168.5.150 – 192.168.5.200 in the DHCP pool configured as Agent.
 

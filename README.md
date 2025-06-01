Step1: set up pfsense network adapters 1st WAN 2nd Host-Only(LAN1) 3RD Host-Only

Step2: configure the WAN with dhcp and lan by default takes 192.168.1.1 (preferred to keep as it is ) can be changed but if not needs to change LAN subnet from virtual network editor.
![image](https://github.com/user-attachments/assets/80279be6-9571-4d84-bef1-a3551addcfed)
Step3: edit kali’s network adapeter to vmnet1 (LAN1)

Step4: opens kali and go to 192.168.1.1 (if subnet not changed , if changed go to the subnet gateway)

Step5: login with username admin and password pfsense 
![image](https://github.com/user-attachments/assets/cd839e38-3f51-41be-b2ec-3565a23b3403)
Step6: enter interfaces -> add -> opt1 

Step7: go to opt1 from interfaces and configured it’s static ip

Step8: edit meta’s network adapeter to vmnet2 (LAN2)

Step9: opens Metasploit machine and go to network configuration and add mahine’s static ip and gateway (the opt1 gateway ip)
![image](https://github.com/user-attachments/assets/bc7870d0-3e71-4fab-be97-3422afec4fde)
Step10: in pfsense go to rules -> opt1 add rule to open any protocol from opt1 to any destintation (like LAN default rules)
![image](https://github.com/user-attachments/assets/cbb51bca-2417-4b3a-8b6c-949a92568138)
Step11: ping from every machine to another to make sure every thing is fine 

Step12: scan with nmap from kali to Metasploit 
![image](https://github.com/user-attachments/assets/d55a7f3d-6bf0-4aac-adf7-f3027041d378)
Step13: exploit open ports like ftp and telnet
![image](https://github.com/user-attachments/assets/2adc38a0-24ef-44fc-802c-57d938bb8c08)
Step14: edit LAN rules to prevent attack on the ports (like ftp 21 ,telnet 23)
![image](https://github.com/user-attachments/assets/0294cd5e-6c01-4d00-a1f7-d7ef52944570)
Step15: try rexploit to make sure rules are preventing  
![image](https://github.com/user-attachments/assets/8fa338cb-a326-4b70-b741-9aee9bc68298)
![image](https://github.com/user-attachments/assets/738fb07f-879d-48b6-8fee-b322a61e323a)
![image](https://github.com/user-attachments/assets/6f599c2c-6dbc-4717-9bfe-d149e822af1d)

# Forest-Security
Forest Security is an application designed for Polish National Forests in order to monitor safety of entry gates, as well as configuring sensors for detecting gates states in the real time.

# Description
Application collects data from gates, which are rotation sensors and triggers notification or marker change. These functionalities allow Polish National Forests Employees to track gates states, making forest free from unauthorized access threats.

![11](https://github.com/user-attachments/assets/156314a3-fe27-46a0-a1aa-09a05df6bfc4)

![8](https://github.com/user-attachments/assets/58f9a029-57c3-4860-8f96-bf3111b90717)


Application works in 2 modes - Forester and Installer. In both of them different features are enabled. 

Forester:
❌ Set Device
✔️ Deactivate Device
❌ Set Geolocation
❌ Change Device Config
✔️ Exit and listen for changes

![5](https://github.com/user-attachments/assets/5a6d7a0a-eefc-4606-a274-0da5d4d1b2d3)

Installer:
✔️ Set Device
✔️ Deactivate Device
✔️ Set Geolocation
✔️ Change Device Config
❌ Exit and listen for changes

![4](https://github.com/user-attachments/assets/858cd9d9-401f-4f00-96b6-b7d9a9447119)

1. Set Device - enables form to add new sensor or update existing sensor setting - API endpoint decides what action is performed.
   
   ![7](https://github.com/user-attachments/assets/cee0cb72-7c1d-4dd5-b8f2-42ef500aa98f)
   
a) Device ID - uniue device id which is retrieved by scanning QRCode by phone's camera
b) Latitude - location derrives from Android GPS 
c) Longitude - location derrives from Android GPS
d) Refresh Time - interval in secons by which device should send confirmation of it's continuity of work to MQTT Broker
e) Forest ID - autofilled - installer is assigned to the particular forest
f) additional info
g) is initially closed - is gate (rotation sensor) initially closed
h) Restart
   
3. Deactivate Device - Forester or Installer can make sensor unvulnerable for rotation changes for a specified time
   
   ![6](https://github.com/user-attachments/assets/d057336e-141c-4b26-b9c9-90a600cc7a6c)
   
5. Set Geolocation - allows to update geoloc configuration without affecting other parameters of device
   
   ![9](https://github.com/user-attachments/assets/804f7add-b304-4d97-acc3-95158e7a3e32)
   
7. Change Device Config - designed to modify device's confirmation sending frequency etc.
   
   ![10](https://github.com/user-attachments/assets/4a0941b9-7a7b-4f7a-a7dd-43df902f3442)

9. Exit and listen for changes - closes app but it remains in the background to keep forester posted if any gate state change occurs.
    

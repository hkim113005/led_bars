# led_bars
## 1. Setting up WLED
### Install WLED on DigQuad
Use https://install.wled.me/ to install latest version of WLED with Ethernet support on the board.
### Access through WLED AP
Connect to the WLED AP through WiFi. The default password should be `wled1234`.
### Configure network
- Set static IP address to `192.168.100.2` or any arbitrary IP address of choice. 
- Set subnet mask to `255.255.255.0`, which should be default, or match to subnet mask to that of FPP.
- Set gateway IP address to the static IP address of the FPP (`192.168.100.1`)
### Configure LEDs
- Set LED count

Repeat these steps as many times to create WLED controllers, note static IP address down for later us in XLights
## 2. Setting up FPP
### Flash FPP on Raspberry Pi
Use the Raspberry Pi imager to flash FPP (https://www.raspberrypi.com/software/)
### Access through WiFi tethering
Connect to FPP through WiFI. The default password should be `Christmas`.
### Configure network
- Set WiFi tethering to always on.
- Set `eth0` static IP address to `192.168.100.1` or whatever you previously set in WLED as the FPP IP address.
- Set `eth0` subnet mask to `255.255.255.0` or whatever you previously set in WLED as the subnet mask.
- Set `eth0` gateway IP address to be blank.
## 3. Setting Up XLights
### Add ethernet controller
Fill in details as necessary. Use static IP address of WLED controller(s). Leave FPP Proxy blank.
### Create layout and sequence
Create layout and sequence. Assign to WLED controller through `Visualize...`
### FPP Connect and upload
While connected to the WiFi tether for FPP use `FPP Connect` to find the FPP and upload sequences to FPP.
# OAK-D-IoT-75 | DM1098OBC_WiFi DepthAI USB3C Baseboard

![image](https://user-images.githubusercontent.com/32992551/110514833-f0649100-80c4-11eb-8e2c-6c164f2d9f48.png)
![image](https://user-images.githubusercontent.com/32992551/110514872-fce8e980-80c4-11eb-95f7-552f1ff6fdf7.png)

Size comparison to BW1092, DepthAI Pi CM4, and OAK-SOM-IoT below:
![image](https://user-images.githubusercontent.com/32992551/110514940-12f6aa00-80c5-11eb-9789-baccb00740ea.png)

# Project Stage

This design is validated and is now in mass production.  It is ready to be used in downstream designs and/or customizations.

# Overview

This repository contains open hardware designed by Luxonis, and meant to be used as a baseboard for the [Luxonis](https://www.luxonis.com/depthai) OAK-SOM-IoT. The BW1098OBC_WIFI baseboard has three on-board cameras which implement stereo and RGB vision, piped directly into the DepthAI SoM for depth and AI processing. The data can be then output to a host via USB 3.1 Gen1 (Type-C) or via ESP32 Wi-Fi interface. 

## Repository structure:
* `PCB` contains the packaged Altium project files
* `Docs` contains project output files
* `Images` contains graphics for readme and reference
* `3D Models` contains generated 3D models of the board

# Key features
* Support for on-board stereo and RGB camera modules
* Interface for Luxonis DepthAI SoM
* USB 3.1 Gen1 Type-C
* Integrates ESP32-WROOM-32D (Wi-Fi 2.4 GHz to 2.5 GHz)
* Micro USB interface for serial communication with ESP32 
* Pads for DepthAI SoM / ESP32 3.3V SPI (refer to schematic for pinout)
* Pads for ESP32 3.3V AUX GPIOs (refer to schematic for pinout) 
* QWIIC connector for ESP32 I2C 
* 5V barrel jack input
* Support for 5V fan
* Design files produced with Altium Designer 20


# Board layout & dimensions

![](https://github.com/luxonis/depthai-hardware/blob/master/DM1098OBC_DepthAI_USB3C_WIFI/Images/DM1098OAKW_R0M0E0_SIDE_AllComponents.png?raw=true)

![](https://github.com/luxonis/depthai-hardware/blob/master/DM1098OBC_DepthAI_USB3C_WIFI/Images/DM1098OAKW_R0M0E0_BOT_AllComponents.png?raw=true)

![](Images/DM1098OAKW_R0M0E0_Dimensions.jpg)

# Enclosure
We are working on an enclosure for the OAK-D-IoT-75.  In fact it is in the process of tooling being finished as of this writing (November 2021).  Once it is done, it will be orderable from shop.luxonis.com, and future OAK-D-IoT-75 will come with enclosures.  Below is a pre-production sample:
![image](https://user-images.githubusercontent.com/32992551/140240240-d899ba86-bbda-480c-bd99-5082f49bdfdf.png)
![image](https://user-images.githubusercontent.com/32992551/140240364-c21e00df-2075-4872-92b2-b752a1730164.png)

Meanwhile, it's worth noticing excellent cases designed by our community members.
* T Kamoi design https://www.thingiverse.com/thing:4876999
* Thomas Höfler design https://www.thingiverse.com/thing:4880485
* Xplicator (Gerrit Kolb) design https://www.thingiverse.com/thing:4879233
* Carlos Alvarenga design https://www.thingiverse.com/thing:4876354

# Getting started
The DM1098OBC_WIFI accepts 5V (+/-10%) from a 5.5m x 2.5mm barrel jack or via USB 3.1 Gen1 Type-C.

Interfacing with the DepthAI SoM is also possible with DM1098OBC_WIFI connector pads J5, and J6. These pads are designed for the [Molex/53047-0810](https://octopart.com/search?q=53047-0810&currency=USD&specs=0) or equivalent. Please refer to the schematics for pinout information.

The reset button resets the Luxonis DepthAI SoM only. 

The 5V LED indicates 5V power is present on the DM1098OBC. The PG LED indicates "power good" from the DepthAI SoM. The "RUN" LED indicates that the DepthAI SoM is not in reset.  


# Revision info
These files represent the R0M0E0 revision of this project. Please refer to schematic page, `Project_Information.SchDoc` for full details of revision history.

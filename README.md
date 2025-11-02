#  GNSS Basestation
<img width="510" height="183" alt="miner_ohneBG" src="https://github.com/user-attachments/assets/7aa2d497-d174-43aa-8f2b-47c93be2a783" />

## with UM980 GNSS Module, Raspberry Pi Zero 2WH & 3D Printable Case

This repository contains a 3D-printable case specifically designed for the **UM980 GNSS module**.<br>
It’s part of a DIY GNSS miner setup for the onocoy project.

## 🧩 Features
- Ethernet port
- Custom fit for the **UM980 GNSS module**
- Space for two **3008 cooling fan** 
- no soldering



# 📄 Part List

- Raspberry Pi Zero 2 WH – where the "H" officially stands for "pre-soldered headers"  
https://www.raspberrypi.com/products/raspberry-pi-zero-2-w/
<img width="250" height="174" alt="RASP_PI_ZERO2_WH" src="https://github.com/user-attachments/assets/80a5c816-0b8b-43cc-b90f-1bcd15385148" />

- UM980 GNSS Module
Exampple:  https://witmotion-sensor.com ; https://www.gns-electronics.de/ ; https://aliexpress.com/
<img width="184" height="250" alt="um980" src="https://github.com/user-attachments/assets/c81fc6bb-e565-4fdf-b510-cbfd57153f90" />

- USB-A (Male) to USB-C (Male) OTG
Example: https://aliexpress.com/item/1005002301799896.html
<img width="229" height="250" alt="usb otg" src="https://github.com/user-attachments/assets/11d13eb0-989e-42bb-b893-fa8c28c4eb26" />

- Ethernet / USB HUB HAT 
https://www.waveshare.com/product/raspberry-pi/hats/interface-power/eth-usb-hub-hat-b.htm?___SID=U 
<img width="250" height="172" alt="eth_hat" src="https://github.com/user-attachments/assets/4e4fce9b-29e2-4b4d-b333-94443c3f791a" />

- 2x Fan 30x30x08 5V/3V
Example: https://aliexpress.com/item/32813594463.html
<img width="250" height="251" alt="fan" src="https://github.com/user-attachments/assets/6ebe6f5f-afcc-4d9b-934c-0be6bb307f4d" />

- Raspberry Pi Micro USB Power Supply
https://www.raspberrypi.com/products/micro-usb-power-supply
<img width="250" height="250" alt="microusb-51v-25a-netzteil-fur-raspberry-pi-3b-3a-3b-2b-zero-zero-2-original-weiss" src="https://github.com/user-attachments/assets/1b6409c5-2805-414e-88f5-0d3cbac5ee8e" />

- MicroSD card (at least 8GB,max 32GB, Class 10 recommended)
<img width="250" height="187" alt="sd_card" src="https://github.com/user-attachments/assets/3d729816-15c2-4d2f-ae81-a434106245fd" />


# To complete your setup, you will need the following components:

- GNSS Antenna  Recommend: Beitian BS-800S
Example: https://www.aliexpress.us/item/3256808846936564.html
<img width="450" height="200" alt="antenna" src="https://github.com/user-attachments/assets/d12811f0-edee-4f7d-b358-3e0ba1650b81" />

- LM400 cable SMA - TNC
Example: https://www.aliexpress.us/item/3256808997745754.html
Connector Compatibility Note:
The antenna requires a TNC-K connector — not a standard TNC.
Why this matters:
Standard TNC and TNC-K have different sizes.
Recommended Practice:
To guarantee compatibility, buy the antenna and cable as a bundle from the same supplier.
<img width="250" height="203" alt="cable" src="https://github.com/user-attachments/assets/951e0954-a507-4edb-8514-e76a244d78f3" />

- A mounting bracket
Example: https://aliexpress.com/item/1005006425749599.html
<img width="220" height="220" alt="bracket" src="https://github.com/user-attachments/assets/06ec4d4b-1815-4322-8d41-9627abb804f4" />




## 🚀 Installation Guide

### Prerequisites:

- A computer for initial SD card flashing.
- Internet access for downloads and configuration.
- You can 3D print the case yourself from the provided STL files, utilize a 3D printing service, or purchase a pre-printed case if available.



## 1. Print the Case
### 🖨️ Print Instructions

- Recommended material: **PETG**,**ASA** or **PLA+**
- Orientation: print flat (bottom side down)
- Supports: **not required**
- Infill: 20-40%

### 2. Assemble the Main Board
![main_board](https://github.com/user-attachments/assets/bd724068-8737-407b-b39b-44f12837400d)


(The photo shows the 2W version with pins added by the user)

- Assemble the Ethernet Hub and Raspberry Pi Zero: Carefully connect the Ethernet hub and the Raspberry Pi Zero, referring to their respective manuals for detailed instructions.
- Attach the USB-A to USB-C OTG Adapter: Insert the USB-A to USB-C OTG adapter into the designated port on the right side of the Raspberry Pi Zero.
- Connect the UM980 GNSS Board: Attach the UM980 GNSS board to the USB-C OTG adapter.
- Mount the Assembled Board: Carefully place the fully assembled board into the case.
- Secure the Board: Use the provided screws to fix the board firmly to the case.
- Install the Antenna Plug: Guide the antenna plug through the designated hole in the case and secure it by screwing it into place.
- Attach the Fans: Slide the two fans into their designated slots on the lid of the case.
- Connect the Fans: Connect the fan cables to the appropriate GPIO pins on the Raspberry Pi Zero. ( https://github.com/airtkey/UM980-diy-/blob/main/pictures/raspberry-pi-zero-pinout.png )
<img width="349" height="100" alt="fan_lid" src="https://github.com/user-attachments/assets/a89f288a-bcf6-4063-950f-05d9efbf2443" />
<br>  
<img width="417" height="162" alt="insode" src="https://github.com/user-attachments/assets/d0f15523-a58e-4c8d-8413-0b1c4c0dbbf2" />


### 1. Flash the OS
Download and flash **Raspberry Pi OS Lite (64-bit)** in the **Debian Bookworm** version to your microSD card using Raspberry Pi Imager. Enable SSH and Wi-Fi before proceeding. For more detailed information on flashing and setup, please refer to: https://www.raspberrypi.com/documentation/computers/getting-started.html#installing-the-operating-system.

### 2. Connect via SSH
Insert the SD card into your Raspberry Pi and power it up.  
Then connect using an SSH client like **PuTTY**:


### 3. Update and Reboot

Run the following commands:

sudo apt update
sudo apt upgrade
sudo reboot



   ```bash
   wget https://github.com/GNSSOEM/ELT_RTKBase/raw/main/install.sh
   chmod +x install.sh
   ./install.sh


### 5. Install the ELT_RTKBase Software

Open a terminal (ssh with putty) on the Pi and run two times:

"wget https://github.com/GNSSOEM/ELT_RTKBase/raw/main/install.sh
chmod +x install.sh
./install.shlol

The script will install the required software and drivers, and start the dashboard (usually accessible at http://raspberrypi.local:3000).

💡 After installation, you can configure your receiver and connect it to a network like Onocoy directly from the web dashboard.

## 🖨️ Print Instructions

- File format: `.stl`
- Recommended material: **PETG** or **PLA+**
- Orientation: print flat (bottom side down)
- Supports: **not required**
- Infill: 15–30%

## 🧰 Assembly

1. Place the UM980 module inside the case.
2. Mount the **3010 fan** above the chip – connect power directly to the module pins *(or skip if using a passive heatsink)*.
3. Route the USB-C and antenna cables through the side cutouts.
4. Close the lid – some variants support screw or snap-fit.

## 🔀 Splitter Variant

The "Splitter" case version has space to install a **GNSS splitter**, allowing you to run the UM980 module **in parallel with another GNSS miner** (e.g. for multimining with Geodnet + Onocoy).

> 🛠️ Important: Be sure to use an **active splitter** with power passthrough if your antenna needs voltage.

## 📷 Preview
  
(https://github.com/airtkey/onominer-raspi-version/blob/main/IMG_20250618_121334.jpg)

## 🔗 Related Links

- [Onocoy Network](https://onocoy.com)
- [UM980 Base Setup (ELT_RTKBase)](https://github.com/GNSSOEM/ELT_RTKBase)


## 📬 Contact

Questions? Ideas?  
Feel free to:
  
- Reach out via [YouTube](http://www.youtube.com/@airtkey)  
- Message me on **Discord** – you’ll find me in the **Onocoy server**   as alex_multimining.
- Or on **X (Twitter)**: [@alex_multimining](https://x.com/AlexMultiMining)

---


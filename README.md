#  UM980 GNSS Module with a Raspberry Pi Zero 2WH & 3D Printable Case

This repository contains a 3D-printable case specifically designed for the **UM980 GNSS module**. It’s part of a DIY GNSS miner setup and is ideal for projects such as Onocoy.


## 🧩 Features
- Ethernet port
- Custom fit for the **UM980 GNSS module**
- Space for two **3010 cooling fan** 
- no soldering



# 📄 Part List

- Raspberry Pi Zero 2 WH – where the "H" officially stands for "pre-soldered headers"  
https://www.raspberrypi.com/products/raspberry-pi-zero-2-w/

- UM980 GNSS Module
  https://witmotion-sensor.com

- USB-A (Male) to USB-C (Male) OTG
Example: https://aliexpress.com/item/1005002301799896.html

- Ethernet / USB HUB HAT 
https://www.waveshare.com/product/raspberry-pi/hats/interface-power/eth-usb-hub-hat-b.htm?___SID=U 

- 2x Fan 30x30x08 5V/3V
Example: https://aliexpress.com/item/32813594463.html

- Raspberry Pi Micro USB Power Supply
https://www.raspberrypi.com/products/micro-usb-power-supply

- MicroSD card (at least 8GB, Class 10 recommended)


# To complete your setup, you will need the following components:

- GNSS Antenna  Recommend: Beitian BS-800S
Example: https://www.aliexpress.us/item/3256808846936564.html

- LM400 cable SMA - TNC
Example: https://www.aliexpress.us/item/3256808997745754.html
Connector Compatibility Note:
The antenna requires a TNC-K connector — not a standard TNC.
Why this matters:
Standard TNC and TNC-K have different sizes.
Recommended Practice:
To guarantee compatibility, buy the antenna and cable as a bundle from the same supplier.

- A mounting bracket
Example: https://aliexpress.com/item/1005006425749599.html




## 🚀 Installation Guide

### Prerequisites:

- A computer for initial SD card flashing.
- Internet access for downloads and configuration.
- You can 3D print the case yourself from the provided STL files, utilize a 3D printing service, or purchase a pre-printed case if available.



### 1. Print the Case

### 2. Assemble the Main Board

- Assemble the Ethernet Hub and Raspberry Pi Zero: Carefully connect the Ethernet hub and the Raspberry Pi Zero, referring to their respective manuals for detailed instructions.
- Attach the USB-A to USB-C OTG Adapter: Insert the USB-A to USB-C OTG adapter into the designated port on the right side of the Raspberry Pi Zero.
- Connect the UM980 GNSS Board: Attach the UM980 GNSS board to the USB-C OTG adapter.
- Mount the Assembled Board: Carefully place the fully assembled board into the case.
- Secure the Board: Use the provided screws to fix the board firmly to the case.
- Install the Antenna Plug: Guide the antenna plug through the designated hole in the case and secure it by screwing it into place.
- Attach the Fans: Slide the two fans into their designated slots on the lid of the case.
- Connect the Fans: Connect the fan cables to the appropriate GPIO pins on the Raspberry Pi Zero.

### 1. Flash the OS
Download and flash **Raspberry Pi OS (Lite)** to your microSD card using [Raspberry Pi Imager](https://www.raspberrypi.com/software/).  
Enable SSH and Wi-Fi before booting (you can create an empty `ssh` file and a `wpa_supplicant.conf` in the boot partition).

### 2. Connect via SSH
Insert the SD card into your Raspberry Pi and power it up.  
Then connect using an SSH client like **PuTTY**:

Default credentials (recommended to change later):
Username: admin
Password: admin

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


##### Component Summary Table



| Component                  | Description (from README)                                                                 | Quantity | Est. Price (USD) | Recommended Sources                                                                 | Notes/Alternatives |
|----------------------------|-------------------------------------------------------------------------------------------|----------|------------------|-------------------------------------------------------------------------------------|---------------------|
| **Raspberry Pi Zero 2 WH** | Core single-board computer for GNSS data processing (quad-core, Wi-Fi/BT, headers included). | 1        | $15–$20         | - Official: [Raspberry Pi Store](https://www.raspberrypi.com/products/raspberry-pi-zero-2-w/)<br>- Amazon: [Search: Pi Zero 2 WH](https://www.amazon.com/s?k=raspberry+pi+zero+2+wh)<br>- AliExpress: [Pi Zero 2 WH](https://www.aliexpress.com/w/wholesale-raspberry-pi-zero-2w-h.html) | Ensure "H" variant (pre-soldered headers). Alternative: Pi Zero W (add headers manually for ~$5 savings). |
| **Ethernet / USB HUB HAT** | Waveshare HAT for Ethernet connectivity and USB expansion on Pi Zero.                     | 1        | $15–$20         | - Official: [Waveshare](https://www.waveshare.com/product/raspberry-pi/hats/interface-power/eth-usb-hub-hat-b.htm)<br>- Amazon/AliExpress/Local stores. | Pogo-pin design for easy stacking; essential for stable network in remote setups. |
| **UM980 GNSS Module**      | Multi-constellation RTK-capable receiver (supports RTCM/NMEA via UART/USB). Key for basestation corrections. | 1        | $90–$130        | - [Witmotion](https://witmotion-sensor.com/)<br>- [GNS-Electronics](https://www.gns-electronics.de/)<br>- AliExpress (verify seller quality). | Select compact board as shown in README pictures; UART connection to Pi pins 8/10. |
| **USB-A (Male) to USB-C (Male) OTG** | Short OTG adapter cable for USB connectivity (e.g., to HAT or external devices).          | 1        | $3–$10          | - Amazon/AliExpress/Local electronics stores.                                        | Match format in README pictures; ensures OTG mode for Pi Zero. |
| **GNSS Antenna**           | Multi-band (L1/L2) active antenna for high-precision RTK signals (e.g., mushroom-style with magnetic mount). | 1        | $100            | - [Beitian BS-800S](https://store.beitian.com/collections/best-selling/products/beitian-high-gain-high-precision-gnss-antenna-provide-stability-and-reliability-gnss-signal-for-positioning-applications-bt-800s)<br>- AliExpress: [RTK GNSS Antenna](https://www.aliexpress.com/w/wholesale-rtk-gps-antenna.html) | **Critical for Accuracy:** Choose multi-band active model like BS-800S to minimize multipath and ensure SNR >35 dB. Magnetic mount recommended for flexible placement; poor antennas degrade RTK fixes. |
| **MicroSD Card**           | 8GB+ storage for OS and RTKLIB software.                                                  | 1        | $5–$8           | - Amazon/AliExpress/Local stores (verified brands like SanDisk).                     | Class 10 or higher for reliable booting; pre-flash with Raspberry Pi OS. |
| **Fan 30x30x08 5V/3V**     | Compact cooling fans for Pi and module (prevents thermal throttling in enclosures).       | 2        | $3–$10          | - Amazon/AliExpress/Local electronics stores.                                        | 5V for Pi GPIO power; mount via adhesive for passive airflow. |
| **RF Cable SMA - TNC**     | Coaxial cable for connecting GNSS antenna (SMA male) to receiver (TNC-K female).          | 1        | <$20            | - Amazon/AliExpress: [SMA to TNC Cable](https://www.aliexpress.us/item/3256808997745754.html)<br>- Local stores. | **Compatibility:** Use TNC-K (not standard TNC) for antenna fit. Buy bundle with antenna to avoid mismatches; RG174 type for low loss (<0.5 dB/m). |
| **Power Supply & Wires**   | 5V/2A micro-USB adapter and jumper wires for stable Pi powering.                          | 1 set    | $10–$20         | - Amazon/AliExpress/Local stores.                                                    | **Strongly Recommended:** Official Raspberry Pi supply to avoid undervoltage/instability. Skip generic phone chargers; include female-to-male jumpers for GPIO. |
| **Enclosure**              | Weatherproof 3D-printed case (STLs in `print_files/`; protects outdoor setup).            | 1        | $5–$15          | - Services: [Shapeways](https://www.shapeways.com/) or [Treatstock](https://www.treatstock.com/) (upload files). | Materials: ASA/PLA+/PETG for UV resistance; local makerspaces for cheap prints. |



#### Regional Sourcing Options (India & Brazil)
To make RTKit more accessible, here are local alternatives for key components.  

| Region                  | Shops                          |
|----------------------------|---------------------------------------------------------------------|
| **Brazil** | [TNT](https://www.tntferramentas.com.br/) <br>[mercadolivre](https://www.mercadolivre.com.br/) |
| **India** | [Robu.in](https://robu.in/) <br>[Fab.to.Lab](https://www.fabtolab.com/) <br>[Thinkrobotics](https://thinkrobotics.com/) <br>[Robokits India](https://robokits.co.in/) |


**Tips for Regional Users:** 
- **India:** Use UPI payments on Robu.in for discounts; watch for GST-inclusive pricing.
- **Brazil:** Mercado Livre offers free shipping on many items; factor in ICMS taxes.
- If links change, update via issues/PRs—community contributions welcome!



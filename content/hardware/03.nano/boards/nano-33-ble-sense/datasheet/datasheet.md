---
identifier: ABX00031
title: Arduino® Nano 33 BLE Sense
variant: 'Datasheet'
type: maker
author: Elizabeth Esparza
---

![](assets/featured.jpg)

# Description 

<p style="text-align: justify;">Arduino® Nano 33 BLE Sense is a miniature sized module containing a NINA B306 module, based on Nordic nRF52480 and containing an Arm® Cortex®-M4F, a crypto chip which can securely store certificates and pre shared keys and a 9 axis IMU. The module can either be mounted as a DIP component (when mounting pin headers), or as a SMT component, directly soldering it via the castellated pads</p>

# Target areas:

Maker, enhancements, IoT application 

# Contents

## Application Examples
<div style="text-align:justify;">

**Onboard Sensors for Rapid Prototyping:** Equipped with a wide range of built-in sensors (IMU, microphone, temperature, humidity, pressure, color, and gesture), it lets you test multiple applications without additional hardware, accelerating the initial development phase.

**AI at the Edge:** Leverage the powerful Arm® Cortex®-M4F processor to run TinyML models directly on the board. Perform tasks such as speech recognition, anomaly detection, or gesture classification locally, enabling intelligent, standalone applications without needing constant cloud connectivity.

**Wireless Communication and IoT Projects:** With integrated Bluetooth® Low Energy 5, you can seamlessly connect your projects to smartphones, other BLE devices, or gateways. Build robust IoT sensors that leverage long-range mode or create interactive peripherals for a truly wireless experience.

**Secure IoT Device Prototyping:** Implement robust security for your connected projects using the dedicated ATECC608A cryptographic chip. This module is perfectly suited for securely connecting to the Arduino IoT Cloud or other platforms by handling secure key storage and encrypted communication.

**Wearable Technology and Miniaturized Devices:** The ultra-compact form factor, low power consumption, and 9-axis IMU make it an excellent choice for developing wearable tech, such as fitness trackers, motion controllers, or other portable electronics.

**Scalable Development**  Start small with simple sensor demos and grow into complex, secure IoT systems. The familiar Nano form factor ensures compatibility with a vast ecosystem of shields, breadboards, and community resources.

**Cross compatibility:** Its BLE capabilities and comprehensive sensor suite make it ideal for creating end-to-end solutions that integrate with mobile apps, cloud dashboards, or other smart devices, enabling rapid prototyping of complete systems.
</div>

## Features
### General Specifications Overview

<p style="text-align: justify;">The Nano 33 BLE Sense is a significant leap forward from the classic 8-bit AVR-based Nano boards, bringing a powerful 32-bit Arm® Cortex®-M4 processor and a complete suite of integrated sensors. It maintains the beloved Nano form factor, ensuring compatibility with a vast ecosystem of shields and projects while opening the door to advanced applications in AI and IoT. </p>

<p style="text-align: justify;"> The board is built around the NINA-B306 module, which provides robust wireless connectivity and substantial computational resources. Compared to its predecessors, it features a massive increase in memory and processing power, alongside integrated sensors for motion, sound, and environmental sensing.</p>

| Feature               | Description                                                                                               |
| --------------------- | --------------------------------------------------------------------------------------------------------- |
| Microcontroller       | 64-bit Arm® Cortex®-M4F (nRF52840)                                                                        |
| Internal Memory       | 1 MB Flash / 256 KB RAM                                                                                   |
| Power Supply          | Various options for easily powering the board: USB connector (5V), VIN pin (5-18V), or direct 3.3V supply |
| USB Connectivity      | Micro-USB port for power and data                                                                         |
| Power                 | Input voltage (VIN): 3.3-18 V / Power via Micro-USB at 5 V                                                |
| Digital Inputs        | GPIO (14x - All exposed I/O can be used as digital), PWM (5x)                                             |
| Analog Inputs         | 12-bit ADC (8x)                                                                                           |
| Communication         | UART (1x), I2C (1x), SPI (1x)                                                                             |
| Dimensions            | 18 mm x 45 mm                                                                                             |
| Operating Temperature | -40 °C to +85 °C                                                                                          |

### Microcontroller
<div style="text-align:justify;">
The Nano 33 BLE Sense is based on the nRF52840 system-on-chip from Nordic Semiconductor, which is integrated into the u-blox NINA-B306 module. It features a powerful 64 MHz Arm® Cortex®-M4F microprocessor.

On the Nano 33 BLE Sense, the operating voltage for I/O pins is 3.3 V. It is not 5V tolerant, so care must be taken when interfacing with components or shields designed for 5V logic.
</div>

| Component          | Details                         |
| ------------------ | ------------------------------- |
| nRF52480 Processor | Arm® Cortex®-M4 at up to 64 MHz |
| Flash Memory       | 1 MB of Flash Memory            |
| Programming Memory | 256 kB of RAM                   |
| ADC                | Yes (12-bit)                    |
| DAC                | Yes (12-bit)                    |

<div style="text-align:justify;">

For more technical details on this microcontroller, visit [Nordic - nRF52480 series official documentation](https://www.nordicsemi.com/Products/nRF52840).

Most of its pins are connected to the external headers, however some are reserved for internal communication with the wireless module and the on-board internal I2C peripherals (IMU and Crypto).

**NOTE**: As opposed to other Arduino Nano boards, pins A4 and A5 have an internal pull up and default to be used as an I2C Bus so usage as analog inputs is not recommended.

</div>

### Micro-USB Connector

<p style="text-align: justify;">The Nano 33 BLE Sense has one Micro-USB port, used to power and program your board as well as send and receive serial communication. </p>

<div style="background-color: #FFFFE0; border-left: 6px solid #FFD700; margin: 20px 0; padding: 15px;">
You should not power the board with more than <strong>5 V</strong> via the USB-Micro port.
</div>

| Pin | **Function** | **Type**     | **Description**                                                                        |
| --- | ------------ | ------------ | -------------------------------------------------------------------------------------- |
| 1   | VUSB         | Power        | Power Supply Input. If board is powered via VUSB from header this is an Output **(1)** |
| 2   | D-           | Differential | USB differential data -                                                                |
| 3   | D+           | Differential | USB differential data +                                                                |
| 4   | ID           | Analog       | Selects Host/Device functionality                                                      |
| 5   | GND          | Power        | Power Ground                                                                           |


### Digital Analog Converter (DAC)

<p style="text-align: justify;">The Nano 33 BLE Sense has a DAC with up to 12-bit resolution attached to the A0 analog pin. A DAC is used to convert a digital signal to an analog signal.</p>

### Board Actuators

<p style="text-align: justify;">The Nano 33 BLE features an RGB LED and single color built-in LED, both can be controlled through the Nano 33 BLE Sense GPIOs. See the [pinout](#pinout) section for a detailed overview.</p>

### Related Products

- Nano 33 BLE Sense (ABX00069)

## Ratings

### Recommended Operating Conditions

<p style="text-align: justify;">
The table below provides a guideline for the optimal use of the Nano 33 BLE Sense board, outlining typical operating conditions and design limits. The operating conditions of the Nano 33 BLE Sense are largely a function based on its component's specifications.</p>

|    **Symbol**   |        **Description**        | **Min** | **Typ** | **Max** | **Unit** |
|:---------------:|:-----------------------------:|:-------:|:-------:|:-------:|:--------:|
|  V<sub>IN</sub> |    Input voltage (VIN pin)    |   5.0   |   7.0   |   18.0  |    VDC   |
| V<sub>USB</sub> | Input voltage (USB connector) |   4.8   |   5.0   |   5.5   |    VDC   |
|  T<sub>OP</sub> |     Operating temperature     |   -40   |    25   |    85   |    °C    |

<div style="background-color: #FFFFE0; border-left: 6px solid #FFD700; margin: 20px 0; padding: 15px;"><p style="text-align: justify;"><strong>Note:</strong> V<sub>DD</sub> Nano 33 BLE Sense only supports 3.3V I/Os and is **NOT** 5V tolerant so please make sure you are not directly connecting 5V signals to this board or it will be damaged. Also, as opposed to Arduino Nano boards that support 5V operation, the 5V pin does NOT supply voltage but is rather connected, through a jumper, to the USB power input.</p>
</div>

### Power Options

<p style="text-align: justify;">Power can either be supplied via the VIN pin, or via USB-Micro connector. If power is supplied via VIN, the MP2322GQH Step Down Converter steps the voltage down to 3.3 V.</p>

<div style="background-color: #FFFFE0; border-left: 6px solid #FFD700; margin: 20px 0; padding: 15px;">
When using the 3V3 pin to power external peripherals, notice that above 150 mA the board may become very hot due to LDO regulator functioning basis.
</div>

#### Power Tree

<p style="text-align: justify;">The following diagram illustrates the Nano 33 BLE Sense main system power architecture.</p>

![Arduino Nano 33 BLE Sense Power Tree](assets/powerTree.svg)

**NOTE:** Since V<sub>USB</sub> feeds V<sub>IN</sub> via a Schottky diode and a DC-DC regulator specified minimum input voltage is 4.5V the minimum supply voltage from USB has to be increased to a voltage in the range between 4.8V to 4.96V depending on the current being drawn.

## Functional Overview

### Pinout

<p style="text-align: justify;">The Nano breakout connectors pinout is shown in the following figure. The board exposes two 15 pin connectors which can either be assembled with pin headers or soldered through castellated vias.</p>

![Pinout for Nano 33 BLE Sense](assets/pinout.png)

#### Analog (JP1)

| Pin | Function  | Type         | Description                                   |
| --- | --------- | ------------ | --------------------------------------------- |
| 1   | D13 / SCK | Digital      | Serial Clock; can be used as GPIO             |
| 2   | +3V3      | Power Out    | +3V3 Power Rail                               |
| 3   | AREF      | Analog       | Analog Voltage Reference / GPIO               |
| 4   | A0        | Analog       | Analog pin 0 / ADC in / DAC out / GPIO        |
| 5   | A1        | Analog       | Analog pin 1 / GPIO                           |
| 6   | A2        | Analog       | Analog pin 2 / GPIO                           |
| 7   | A3        | Analog       | Analog pin 3 / GPIO                           |
| 8   | A4        | Analog / SDA | Analog pin 4 / I²C Serial Data (SDA) / GPIO   |
| 9   | A5        | Analog / SCL | Analog pin 5 / I²C Serial Clock (SCL)  / GPIO |
| 10  | A6        | Analog       | Analog pin 6 / GPIO                           |
| 11  | A7        | Analog       | Analog pin 7 / GPIO                           |
| 12  | VUSB      | Power In/Out | Connected to USB power input (via jumper SJ1) |
| 13  | RST       | Digital In   | Active-low Reset input (duplicate of pin 18)  |
| 14  | GND       | Power        | Ground                                        |
| 15  | VIN       | Power        | Voltage Input                                 |

#### Digital (JP2)

| Pin | Function   | Type     | Description                                      |
| --- | ---------- | -------- | ------------------------------------------------ |
| 15  | D12 / MISO | Digital  | Controller In Peripheral Out / SPI (MISO) / GPIO |
| 14  | D11 / MOSI | Digital  | Controller Out Peripheral In / SPI (MOSI) / GPIO |
| 13  | D10 / PWM  | Digital  | Digital pin 10 / GPIO / PWM                      |
| 12  | D9 / PWM   | Digital  | Digital pin 9 / GPIO / PWM                       |
| 11  | D8         | Digital  | Digital pin 8 / GPIO                             |
| 10  | D7         | Digital  | Digital pin 7 / GPIO                             |
| 9   | D6 / PWM   | Digital  | Digital pin 6 / GPIO / PWM                       |
| 8   | D5 / PWM   | Digital  | Digital pin 5 / GPIO / PWM                       |
| 7   | D4         | Digital  | Digital pin 4 / GPIO                             |
| 6   | D3 / PWM   | Digital  | Digital pin 3 / GPIO / PWM                       |
| 5   | D2         | Digital  | Digital pin 2 / GPIO                             |
| 4   | GND        | Power    | Ground                                           |
| 3   | RST        | Internal | Active-low Reset input (duplicate of pin 13)     |
| 2   | D0 / RX    | Digital  | Digital pin 0 / Serial Receiver (RX) / GPIO      |
| 1   | D1 / TX    | Digital  | Digital pin 1 / Serial Transmitter (TX) / GPIO   |

### Debug
<p style="text-align: justify;">On the bottom side of the board, under the communication module, debug signals are arranged as 3x2 test pads with 100 mil pitch with pin 4 removed. Pin 1 is depicted in Figure 3 – Connector Positions</div>

| Pin | **Function** | **Type**   | **Description**                  |
| --- | ------------ | ---------- | -------------------------------- |
| 1   | +3V3         | Power Out  | +3V3 Power Rail                  |
| 2   | SWD          | Digital    | nRF52480 Single Wire Debug Data  |
| 3   | SWCLK        | Digital In | nRF52480 Single Wire Debug Clock |
| 5   | GND          | Power      | Power Ground                     |
| 6   | RST          | Digital In | Active-low Reset input           |


## Board Topology

Top:
![Board topology top](assets/topologyTop.png)

| **Ref.** | **Description**                 | **Ref.** | **Description**                  |
| -------- | ------------------------------- | -------- | -------------------------------- |
| U1       | NINA-B306 Module Bluetooth® Low Energy 5.0 Module | U6       | MP2322GQH Step Down Converter    |
| U2       | LSM9DS1TR Sensor IMU            | PB1      | IT-1185AP1C-160G-GTR Push button |
| U3       | MP34DT06JTR Mems Microphone     | HS-1     | HTS221 Humidity Sensor           |
| U4       | ATECC608A Crypto chip           | DL1      | Led L                            |
| U5       | APDS-9660 Ambient Module        | DL2      | Led Power                        |

Bottom:
![Board topology bot](assets/topologyBot.png)

| **Ref.** | **Description** | **Ref.** | **Description** |
| -------- | --------------- | -------- | --------------- |
| SJ1      | VUSB Jumper     | SJ2      | D7 Jumper       |
| SJ3      | 3v3 Jumper      | SJ4      | D8 Jumper       |

### IMU
<div style="text-align:justify;">Arduino Nano 33 BLE has an embedded 9 axis IMU which can be used to measure board orientation (by checking the gravity acceleration vector orientation or by using the 3D compass) or to measure shocks, vibration, acceleration and rotation speed.

Source code for the Arduino Library that supports the IMU is available **[9]**.
</div>

### Barometer and Temperature Sensor
<div style="text-align:justify;">
The embedded Barometer and temperature sensor allow measuring ambient pressure. The temperature sensor integrated with the barometer can be used to compensate the pressure measurement.

Source code for the Arduino Library that supports the Barometer is available **[10]**.
</div>

### Relative Humidity and Temperature Sensor
<p style="text-align: justify;">

Relative humidity sensor measures ambient relative humidity. As the Barometer this sensor has an integrated temperature sensor that can be used to compensate for the measurement.

Source code for the Arduino Library that supports the Humidity sensor is available **[11]**.

</div>

### Digital Proximity, Ambient Light, RGB and Gesture Sensor
<p style="text-align: justify;">Source code for the Arduino Library that supports the Proximity/gesture/ALS sensor is available **[12]**.</p>

#### Gesture Detection
<p style="text-align: justify;">Gesture detection utilizes four directional photodiodes to sense reflected IR energy (sourced by the integrated LED) to convert physical motion information (i.e. velocity, direction and distance) to a digital information. The architecture of the gesture engine features automatic activation (based on Proximity engine results), ambient light subtraction, cross-talk cancellation, dual 8-bit data converters, power saving inter-conversion delay, 32-dataset FIFO, and interrupt driven I2C communication. The gesture engine accommodates a wide range of mobile device gesturing requirements: simple UP-DOWN-RIGHT-LEFT gestures or more complex gestures can be accurately sensed. Power consumption and noise are minimized with adjustable IR LED timing.</p>

#### Proximity Detection
<p style="text-align: justify;">The Proximity detection feature provides distance measurement (E.g. mobile device screen to user’s ear) by photodiode detection of reflected IR energy (sourced by the integrated LED). Detect/release events are interrupt driven, and occur whenever proximity result crosses upper and/ or lower threshold settings. The proximity engine features offset adjustment registers to compensate for system offset caused by unwanted IR energy reflections appearing at the sensor. The IR LED intensity is factory trimmed to eliminate the need for end-equipment calibration due to component variations. Proximity results are further improved by automatic ambient light subtraction. </p>

#### Color and ALS Detection
<p style="text-align: justify;">The Color and ALS detection feature provides red, green, blue and clear light intensity data. Each of the R, G, B, C channels have a UV and IR blocking filter and a dedicated data converter producing16-bit data simultaneously. This architecture allows applications to accurately measure ambient light and sense color which enables devices to calculate color temperature and control display backlight.</p>

### Digital Microphone
<div style="text-align:justify;">

The MP34DT05 is an ultra-compact, low-power, omnidirectional, digital MEMS microphone built with a capacitive sensing element and an IC interface.

The sensing element, capable of detecting acoustic waves, is manufactured using a specialized silicon micromachining process dedicated to produce audio sensors.

</div>

## Device Operation 

### Getting Started - IDE

<p style="text-align: justify;">If you want to program your Nano 33 BLE Sense while offline you need to install the Arduino® Desktop IDE **[1]**. To connect the Nano 33 BLE Sense to your computer, you will need a Type-C® USB cable, which can also provide power to the board, as indicated by the LED (DL3).</p>

### Getting Started - Arduino Cloud Editor

<p style="text-align: justify;">

All Arduino boards, including this one, work out-of-the-box on the Arduino Cloud Editor **[2]**, by just installing a simple plugin.

The Arduino Cloud Editor is hosted online, therefore it will always be up-to-date with the latest features and support for all boards. Follow **[3]** to start coding on the browser and upload sketches onto your board.
</div>

### Online Resources

<p style="text-align: justify;">Now that you have gone through the basics of what you can do with the board you can explore the endless possibilities it provides by checking exciting projects on Arduino Project Hub **[4]**, the Arduino Library Reference **[5]**, and the online store **[6]**; where you will be able to complement your board with sensors, actuators and more.</p>

### Board Recovery

<div style="text-align:justify;">

All Arduino boards have a built-in bootloader which allows flashing the board via USB. In case a sketch locks up the processor and the board is not reachable anymore via USB, it is possible to enter bootloader mode by double-tapping the reset button right after the power-up.

</div>


## Mechanical Information

### Board Outline and Mounting Holes
<p style="text-align: justify;">The board measures are mixed between metric and imperial. Imperial measures are used to maintain 100 mil pitch grid between pin rows to allow them to fit a breadboard whereas board length is Metric. </p>

![Board layout](assets/outline.png)

## Certifications
### Declaration of Conformity CE DoC (EU)
<p style="text-align: justify;">We declare under our sole responsibility that the products above are in conformity with the essential requirements of the following EU Directives and therefore qualify for free movement within markets comprising the European Union (EU) and European Economic Area (EEA). </p>

### Declaration of Conformity to EU RoHS & REACH 211 01/19/2021
<p style="text-align: justify;">Arduino boards are in compliance with RoHS 2 Directive 2011/65/EU of the European Parliament and RoHS 3 Directive 2015/863/EU of the Council of 4 June 2015 on the restriction of the use of certain hazardous substances in electrical and electronic equipment.</p>

| Substance                              | **Maximum limit (ppm)** |
| -------------------------------------- | ----------------------- |
| Lead (Pb)                              | 1000                    |
| Cadmium (Cd)                           | 100                     |
| Mercury (Hg)                           | 1000                    |
| Hexavalent Chromium (Cr6+)             | 1000                    |
| Poly Brominated Biphenyls (PBB)        | 1000                    |
| Poly Brominated Diphenyl ethers (PBDE) | 1000                    |
| Bis(2-Ethylhexyl) phthalate (DEHP)     | 1000                    |
| Benzyl butyl phthalate (BBP)           | 1000                    |
| Dibutyl phthalate (DBP)                | 1000                    |
| Diisobutyl phthalate (DIBP)            | 1000                    |

Exemptions : No exemptions are claimed. 

<p style="text-align: justify;">Arduino Boards are fully compliant with the related requirements of European Union Regulation (EC) 1907 /2006 concerning the Registration, Evaluation, Authorization and Restriction of Chemicals (REACH). We declare none of the SVHCs (https://echa.europa.eu/web/guest/candidate-list-table), the Candidate List of Substances of Very High Concern for authorization currently released by ECHA, is present in all products (and also package) in quantities totaling in a concentration equal or above 0.1%. To the best of our knowledge, we also declare that our products do not contain any of the substances listed on the "Authorization List" (Annex XIV of the REACH regulations) and Substances of Very High Concern (SVHC) in any significant amounts as specified by the Annex XVII of Candidate list published by ECHA (European Chemical Agency) 1907 /2006/EC.</div>

### Conflict Minerals Declaration 
<p style="text-align: justify;">As a global supplier of electronic and electrical components, Arduino is aware of our obligations with regards to laws and regulations regarding Conflict Minerals, specifically the Dodd-Frank Wall Street Reform and Consumer Protection Act, Section 1502. Arduino does not directly source or process conflict minerals such as Tin, Tantalum, Tungsten, or Gold. Conflict minerals are contained in our products in the form of solder, or as a component in metal alloys. As part of our reasonable due diligence Arduino has contacted component suppliers within our supply chain to verify their continued compliance with the regulations. Based on the information received thus far we declare that our products contain Conflict Minerals sourced from conflict-free areas.</p> 

## FCC Caution
<div style="text-align:justify;">

Any Changes or modifications not expressly approved by the party responsible for compliance could void the user’s authority to operate the equipment.

This device complies with part 15 of the FCC Rules. Operation is subject to the following two conditions: 

(1) This device may not cause harmful interference

 (2) this device must accept any interference received, including interference that may cause undesired operation.

 </div>

**FCC RF Radiation Exposure Statement:**
<p style="text-align: justify;">

1. This Transmitter must not be co-located or operating in conjunction with any other antenna or transmitter.

2. This equipment complies with RF radiation exposure limits set forth for an uncontrolled environment.

3. This equipment should be installed and operated with minimum distance 20cm between the radiator & your body.

English:
User manuals for license-exempt radio apparatus shall contain the following or equivalent notice in a conspicuous location in the user manual or alternatively on the device or both. This device complies with Industry Canada license-exempt RSS standard(s). Operation is subject to the following two conditions:

(1) this device may not cause interference

(2) this device must accept any interference, including interference that may cause undesired operation of the device.

French: 
Le présent appareil est conforme aux CNR d’Industrie Canada applicables aux appareils radio exempts de licence. L’exploitation est autorisée aux deux conditions suivantes :

(1) l’ appareil nedoit pas produire de brouillage

(2) l’utilisateur de l’appareil doit accepter tout brouillage radioélectrique subi, même si le brouillage est susceptible d’en compromettre le fonctionnement.
</div>

**IC SAR Warning:**
<div style="text-align:justify;">

English 
This equipment should be installed and operated with minimum distance 20 cm between the radiator and your body.

French:
Lors de l’ installation et de l’ exploitation de ce dispositif, la distance entre le radiateur et le corps est d ’au moins 20 cm.

**Important:** The operating temperature of the EUT can’t exceed 85℃ and shouldn’t be lower than -40℃.

Hereby, Arduino S.r.l. declares that this product is in compliance with essential requirements and other relevant provisions of Directive 2014/53/EU. This product is allowed to be used in all EU member states.
</div>

| Frequency bands | Maximum output power (ERP) |
| --------------- | -------------------------- |
| 863-870Mhz      | 5.47 dBm                   |

## Company Information

| Company name    | Arduino S.r.l                           |
| --------------- | --------------------------------------- |
| Company Address | Via Andrea Appiani 25 20900 MONZA Italy |

## Reference Documentation

| Reference                              | **Link**                                                     |
| -------------------------------------- | ------------------------------------------------------------ |
| Arduino IDE (Desktop)                  | https://www.arduino.cc/en/software                           |
| Arduino Cloud Editor                   | https://create.arduino.cc/editor                             |
| Arduino Cloud Editor - Getting Started | https://docs.arduino.cc/arduino-cloud/guides/editor/         |
| Arduino Project Hub                    | https://create.arduino.cc/projecthub?by=part&part_id=11332&sort=trending |
| Library Reference                      | https://www.arduino.cc/reference/en/                         |
| Forum                                  | http://forum.arduino.cc/                                     |
| Nina B306                              | https://content.u-blox.com/sites/default/files/NINA-B3_DataSheet_UBX-17052099.pdf |
| ECC608                                 | https://ww1.microchip.com/downloads/aemDocuments/documents/SCBU/ProductDocuments/DataSheets/ATECC608A-CryptoAuthentication-Device-Summary-Data-Sheet-DS40001977B.pdf |
| MPM3610                                | https://www.monolithicpower.com/pub/media/document/MPM3610_r1.01.pdf |
| ECC608 Library                         | https://github.com/arduino-libraries/ArduinoECCX08           |
| LSM6DSL Library                        | https://github.com/adafruit/Adafruit_LSM9DS1                 |
| LPS22HB                                | https://github.com/stm32duino/LPS22HB                        |
| HTS221 Library                         | https://github.com/stm32duino/HTS221                         |
| APDS9960 Library                       | https://github.com/adafruit/Adafruit_APDS9960                |


## Revision History

| Date       | **Revision** | **Changes**                           |
| ---------- | ------------ |-------------------------------------- |
| 25/04/2024 | 3            | Updated link to new Cloud Editor      |
| 03/08/2022 | 2            | Reference documentation links updates |
| 27/04/2021 | 1            | General datasheet updates             |
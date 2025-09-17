---
title: 'Nano 33 BLE Sense User Manual'
difficulty: beginner
compatible-products: [nano-33-ble-sense]
description: 'Learn about the hardware and software features of the Arduino® Nano 33 BLE Sense board.'
tags:
  - Cheat sheet
  - User manual
author: 'Elizabeth Esparza'
hardware:
  - hardware/04.nano/boards/nano-33-ble-sense
software:
  - ide-v1
  - ide-v2
  - iot-cloud
  - web-editor
  - open-mv
---

This user manual provides a comprehensive overview of the Nano 33 BLE Sense board, highlighting its hardware and software elements. With it, you will learn how to set up, configure and use all the main features of the Nano 33 BLE Sense board.

![The Arduino® Nano 33 BLE Sense](assets/Nano33_ble_sense.png)

## Hardware and Software Requirements

### Hardware Requirements

- Nano 33 BLE Sense (x1)
- [USB Micro cable (x1)](https://store-usa.arduino.cc/products/usb-2-0-cable-type-a-micro)
- [Breadboard (x1) (recommended)](https://store.arduino.cc/products/breadboard-400-contacts)
- [Male/male jumper wires (recommended)](https://store.arduino.cc/products/10-jumper-wires-150mm-male?queryID=undefined)

### Software Requirements

- [Arduino IDE 2.0+](https://www.arduino.cc/en/software/) or [Arduino Web Editor](https://create.arduino.cc/editor)
- [Arduino Mbed OS Nano Board Package](https://github.com/arduino/ArduinoCore-mbed).



## Nano 33 BLE Sense Overview



The Arduino Nano 33 BLE Sense represents a significant leap in the Nano family, integrating the powerful Nordic nRF52480 microcontroller with an Arm® Cortex®-M4F core and a comprehensive suite of embedded sensors into the classic, compact form factor. This board is designed to bridge the gap between simple prototyping and advanced IoT development, providing the computational power and connectivity essential for modern applications.

The Nano 33 BLE Sense is built around the NINA-B306 module, featuring Bluetooth® 5 with long-range support and Thread/Zigbee capability. Its defining characteristic is the integrated sensor hub: a 9-axis IMU, humidity, temperature, barometric pressure, gesture, proximity, color, light, and microphone. Coupled with a dedicated cryptographic chip (ATECC608A) for secure communication, it offers an unparalleled out-of-the-box experience for data fusion and AI edge processing. Its miniature size (approx. 45 x 18 mm) and robust feature set make the Nano 33 BLE Sense the ideal choice for projects demanding sophisticated sensing, wireless connectivity, and the security of a modern microcontroller platform.

### Nano 33 BLE Sense Architecture Overview

The Arduino Nano 33 BLE Sense features a robust and certified design, purpose-built for a new generation of intelligent applications, including motion-activated devices, environmental monitoring, gesture control, and secure, low-power IoT edge nodes.

The top view of the Nano 33 BLE Sense board is shown in the image below:

The bottom view of the Nano 33 BLE Sense board is shown in the image below:

Here is an overview of the board's main components shown in the images above:

- Microcontroller: The heart of the NINA-B306 module is the Nordic Semiconductor nRF52480 microcontroller, based on a 64 MHz Arm® Cortex®-M4F processor with a floating-point unit (FPU). It provides 1 MB of Flash memory and 256 KB of SRAM for application development. Important: The board operates at 3.3V, and its I/O pins are not 5V tolerant.

- Micro-USB connector: The board uses a Micro-B USB connector for programming, power supply, and serial communication with a computer or other host device.

- Onboard user LED: The board includes an onboard user-programmable RGB LED to provide visual feedback.

- Power LED: A green power indicator LED (LED_PWR) illuminates when the board is powered.
  
- Integrated Sensor Hub: A defining feature of this board is its comprehensive suite of onboard sensors, including a 9-axis IMU ([LSM9DS1](https://www.st.com/resource/en/datasheet/lsm9ds1.pdf)), a humidity and temperature sensor ([HTS221](https://www.st.com/resource/en/datasheet/lsm9ds1.pdf)), a barometric pressure sensor ([LPS22HB](https://www.st.com/resource/en/datasheet/lps22hb.pdf)), a digital microphone ([MP34DT05](https://www.st.com/resource/en/datasheet/mp34dt05-a.pdf)), and a gesture, proximity, color, and light sensor ([APDS-9960](https://content.arduino.cc/assets/Nano_BLE_Sense_av02-4191en_ds_apds-9960.pdf)).

- Castellated Pins: The board's castellated pins allow for surface mounting as a module, facilitating direct integration into custom PCB designs and final products without the need for headers.

- Cryptographic co-processor: The board includes a Microchip ATECC608A secure element, which provides hardware-based secure storage for up to 16 keys, certificates, or data. This enables robust security for IoT applications, supporting ECDH key agreement and AES-128 encryption.

- Wireless communication: The board features Bluetooth® 5 connectivity through the NINA-B306 module, supporting features like 2 Mbps throughput, long-range mode, and advertising extensions. The module also includes an IEEE 802.15.4 radio.

### Board Core and Libraries

The **Arduino Mbed OS Nano Boards** core contains the libraries and examples to work with the Arduino Nano 33 BLE Sense's peripherals and onboard components, such as its nRF52480 microcontroller, advanced wireless capabilities, and the extensive suite of integrated sensors. To install the core for the Nano 33 BLE Sense board, navigate to **Tools > Board > Boards Manager** or click the Boards Manager icon in the left tab of the IDE. In the Boards Manager tab, search for Nano 33 BLE and install the latest Arduino Mbed OS Nano Boards package.

The Arduino Mbed OS Nano Boards core provides support for the following:

- Board control and configuration (reset, pin configuration, and low-power management)

- Wireless communication (Bluetooth® Low Energy)

- Advanced peripheral functions (12-bit ADC, PWM)

- Communication interfaces (UART, I2C, SPI)

- Onboard sensor hub access (IMU, microphone, humidity, pressure, gesture, color, light)

- Cryptographic functions (Secure hardware-based key storage with the ATECC608A)

- Standard Arduino libraries compatibility

### Pinout
![Nano 33 BLE Sense pinout.](assets/pinout.png)

The full pinout is available and downloadable as PDF from the link below:
- [Nano 33 BLE Sense pinout](https://docs.arduino.cc/resources/pinouts/ABX00031-full-pinout.pdf)

### Datasheet
The complete datasheet is available and downloadable as PDF from the link below:
- [Nano 33 BLE Sense datasheet](https://docs.arduino.cc/resources/datasheets/ABX00031-datasheet.pdf)

### Schematics
The complete schematics are available and downloadable as PDF from the link below:
- [Nano 33 BLE Sense schematics](https://docs.arduino.cc/resources/schematics/ABX00031-schematics.pdf)

### STEP Files
The complete STEP files are available and downloadable from the link below:

- [Nano 33 BLE Sense STEP files](https://docs.arduino.cc/resources/schematics/ABX00031-schematics.pdf)

## First Use

### Unboxing the Product

When opening the Nano BLE 33 Sense box, you will find the board and its corresponding documentation. The Nano 33 BLE Sense does not include additional cables, so you will need a USB Micro cable ([available separately here](https://store-usa.arduino.cc/products/usb-2-0-cable-type-a-micro)) to connect the board to your computer.

The Nano 33 BLE Sense is a standalone device that can be programmed directly without requiring additional boards. However, for more complex projects, you can easily combine it with Arduino shields compatible with the Nano family.

### Connecting the Board
The Nano 33 BLE Sense can be connected to your computer using its onboard USB Micro connector. It can also be integrated into larger projects using the following:

- **Direct USB Micro connection:** For programming, power supply and serial communication with the computer

- **Pin connection:** For integration into breadboards or custom PCBs

- **Module mounting:** Using the board's castellated pins for direct soldering to PCBs

Important note: The Nano 33 BLE Sense operates at +3.3 VDC natively. Its I/O pins are not 5V tolerant. When connecting to devices or sensors that operate at +5 VDC, a logic level converter is required to avoid permanently damaging the board.


### Powering the Board

The Nano 33 BLE Sense can be powered in several ways:

- **Via USB Micro connector:** The most common method during development and programming

- **Via VIN pin:** Using an external +4.5-18 VDC power supply that will be internally regulated to +3.3 VDC.

- **Via 3V3 pin:** Directly connecting a regulated +3.3 VDC source.

***The microcontroller on the Arduino Nano 33 BLE Sense operates at 3.3V. You must never apply more than 3.3V to its Digital and Analog pins. Connecting higher voltage signals, like the 5V commonly used with other Arduino boards, will permanently damage the board.***

#### 5V Pin

To maintain the classic Nano form factor while protecting the board, the 5V pin on the header has a special, non-standard behavior:

- **Default Safety Feature:** The 5V pin is not connected by default (factory setting). This is a precaution to draw your attention to the 3.3V compliance requirement.

- **How to Enable 5V Output:** To make the 5V pin active, you must create a solder bridge on the two pads marked VUSB on the bottom of the board.

- **USB Power Only:** Even with the solder bridge, the 5V pin will only output voltage when the board is powered via the USB port. If you power the board from the VIN pin, the 5V pin will remain inactive.

- **Design Recommendation:** The onboard 3V3 pin is always available. We strongly recommend designing your projects to use 3.3V for sensors and actuators, as this is becoming the standard voltage for electronic ICs.

***Important note: The Nano 33 BLE Sense's VIN pin accepts a voltage range of +5-18 VDC. Always verify all connections before applying power.***

#### Internal +3.3 VDC Power Supply

The Nano 33 BLE Sense includes an efficient MPM3610 DC-DC converter that regulates input power to a stable +3.3 VDC supply for the entire board, including:

- nRF52480 Microcontroller: The main processor core and its internal peripherals.

- Integrated Sensor Hub: Powers all onboard sensors (IMU, microphone, humidity, pressure, gesture sensor).

- Cryptographic Co-processor: Powers the ATECC608A secure element.

- I/O Pin Voltage: All digital and analog pins operate at this voltage.

### Onboard Sensors and Peripherals

The board's unique integrated sensor hub is powered by the internal +3.3 VDC supply and includes the following components, which can be accessed through dedicated libraries:

- **9-axis IMU (LSM9DS1)**: For motion and orientation sensing.

- **Digital Microphone (MP34DT05):** For audio capture.

- **Humidity and Temperature Sensor (HTS221):** For environmental monitoring.

- **Barometric Pressure Sensor (LPS22HB):** For weather forecasting and altitude measurement.

- **Gesture, Proximity, Light, Color Sensor (APDS-9960):** For detecting user interaction and ambient light conditions.

### Hello World Example

Let's program the Nano 33 BLE Sense to reproduce the classic `Hello World` example used in the Arduino ecosystem: the `Blink` sketch. We will use this example to verify that the Nano 33 BLE Sense's connection to the computer works correctly, that the Arduino IDE is properly configured, and that both the board and development environment function as expected.

First, connect your Nano 33 BLE Sense to your computer using a USB-C cable, open the Arduino IDE, and make sure that the board is connected correctly. If you are new to the Arduino IDE, please refer to the official Arduino documentation for more detailed information about initial setup. Copy and paste the following example sketch into a new Arduino IDE file:

```arduino
/*
  Blink

  Turns an LED on for one second, then off for one second, repeatedly.

  Most Arduinos have an on-board LED you can control. On the UNO, MEGA and ZERO
  it is attached to digital pin 13, on MKR1000 on pin 6. LED_BUILTIN is set to
  the correct LED pin independent of which board is used.
  If you want to know what pin the on-board LED is connected to on your Arduino
  model, check the Technical Specs of your board at:
  https://docs.arduino.cc/hardware/

  modified 8 May 2014
  by Scott Fitzgerald
  modified 2 Sep 2016
  by Arturo Guadalupi
  modified 8 Sep 2016
  by Colby Newman

  This example code is in the public domain.

  https://docs.arduino.cc/built-in-examples/basics/Blink/
*/

// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);  // turn the LED on (HIGH is the voltage level)
  delay(1000);                      // wait for a second
  digitalWrite(LED_BUILTIN, LOW);   // turn the LED off by making the voltage LOW
  delay(1000);                      // wait for a second
}

```

To upload the sketch to the board, click the **Verify** button to compile the sketch and check for errors, then click the **Upload** button to program the device with the sketch.

![Uploading a sketch to the Nano 33 BLE Sense in the Arduino IDE]()

As shown in the animation below, you should see the built-in orange user LED of your Nano 33 BLE Sense board turn on for one second, then turn off for one second, repeating this cycle continuously. 

![Onboard orange user LED blinking]()

Additionally, you can open the Arduino IDE's Serial Monitor (Tools > Serial Monitor) to see the status messages that the example sketch sends each time the LED state changes.

![Arduino IDE Serial Monitor output for the Blink sketch]()

This example confirms the following:

- The Nano 33 BLE Sense board is correctly connected
- The Arduino IDE is properly configured
- The board is functioning correctly
- USB communication is working
- Digital pins respond to commands

Congratulations! You have successfully completed your first program on the Nano 33 BLE Sense board. You are now ready to explore the more advanced features of this tiny but powerful board.

## LEDs

This user manual section covers the Nano 33 BLE Sense built-in LEDs, showing their main hardware and software characteristics.

### Power LED

The Nano 33 BLE Sense features a green power indicator LED (LED_PWR) that illuminates when the board is powered via USB or an external source.


This LED is controlled by the hardware and cannot be programmed by the user. It serves as a visual confirmation that the board is receiving power.

### RGB LED

The Nano 33 BLE Sense features a built-in RGB LED that can be used as a visual feedback indicator for the user.

![Built-in RGB LED of the Nano 33 BLE Sense board]()

The built-in RGB LED can be accessed through the following macro definitions:

| **Built-in LED** | **Macro Definition** | **Microcontroller Pin** |
| :--------------: | :------------------: | :---------------------: |
|     Red LED      |        `LEDR`        |         `P0.24`         |
|    Green LED     |        `LEDG`        |         `P0.16`         |
|     Blue LED     |        `LEDB`        |         `P0.06`         |


The following example sketch each of the RGB LED colors at an interval of 500 ms:

```arduino
/**
RGB LED Example for the Arduino Nano 33 BLE Sense Board
Name: nano_33_rgb_led.ino
Purpose: This sketch demonstrates how to control the built-in
RGB LED of the Arduino Nano 33 BLE Sense board.

@author Arduino Product Experience Team
@version 1.0 01/06/25
*/

void setup() {
  // Initialize serial communication and wait up to 2.5 seconds for a connection
  Serial.begin(115200);
  for (auto startNow = millis() + 2500; !Serial && millis() < startNow; delay(500));
  
  // Initialize LEDR, LEDG and LEDB as outputs
  pinMode(LEDR, OUTPUT);
  pinMode(LEDG, OUTPUT);
  pinMode(LEDB, OUTPUT);
  
  // Turn off all LEDs initially
  digitalWrite(LEDR, HIGH);
  digitalWrite(LEDG, HIGH);
  digitalWrite(LEDB, HIGH);
  
  Serial.println("- Arduino Nano 33 BLE Sense - RGB LED Example started...");
}

void loop() {
  // Turn on the built-in red LED and turn off the rest
  digitalWrite(LEDR, LOW);
  digitalWrite(LEDG, HIGH);
  digitalWrite(LEDB, HIGH);
  Serial.println("- Red LED on!");
  delay(500);
  
  // Turn on the built-in green LED and turn off the rest
  digitalWrite(LEDR, HIGH);
  digitalWrite(LEDG, LOW);
  digitalWrite(LEDB, HIGH);
  Serial.println("- Green LED on!");
  delay(500);
  
  // Turn on the built-in blue LED and turn off the rest
  digitalWrite(LEDR, HIGH);
  digitalWrite(LEDG, HIGH);
  digitalWrite(LEDB, LOW);
  Serial.println("- Blue LED on!");
  delay(500);
  
  // Turn off all LEDs
  digitalWrite(LEDR, HIGH);
  digitalWrite(LEDG, HIGH);
  digitalWrite(LEDB, HIGH);
  Serial.println("- All LEDs off!");
  delay(500);
}
```

You should now see the built-in RGB LED cycling through red, green, and blue colors, followed by a brief moment with all LEDs off, repeating this pattern continuously.

![Onboard RGB user LED blinking]()

Additionally, you can open the Arduino IDE's Serial Monitor (Tools > Serial Monitor) to see the status messages that the example sketch sends each time the RGB LEDs state changes.

![Arduino IDE Serial Monitor output for the RGB LED example sketch]()

### User LED

The Nano 33 BLE Sense also features a built-in orange user LED that can be used for basic status indications and debugging purposes.

![Built-in user LED of the Nano 33 BLE Sense board]()


The built-in user LED can be accessed through the following macro definition:

| **Built-in LED** | **Macro Definition** | **Microcontroller Pin** |
| :--------------: | :------------------: | :---------------------: |
| Orange User LED  |    `LED_BUILTIN`     |         `P0.13`         |

The following example sketch demonstrates how to control the built-in user LED:

```arduino
/**
User LED Example for the Arduino Nano 33 BLE Sense Board
Name: nano_r4_user_led.ino
Purpose: This sketch demonstrates how to control the built-in
user LED of the Arduino Nano 33 BLE Sense board.

@author Arduino Product Experience Team
@version 1.0 01/06/25
*/

void setup() {
  // Initialize serial communication and wait up to 2.5 seconds for a connection
  Serial.begin(115200);
  for (auto startNow = millis() + 2500; !Serial && millis() < startNow; delay(500));
  
  // Configure LED_BUILTIN pin as output
  pinMode(LED_BUILTIN, OUTPUT);
  
  // Turn off LED initially
  digitalWrite(LED_BUILTIN, LOW);
  
  Serial.println("- Arduino Nano 33 BLE Sense - User LED Example started...");
}

void loop() {
  // Turn on the built-in user LED
  digitalWrite(LED_BUILTIN, HIGH);
  Serial.println("- User LED on!");
  delay(1000);
  
  // Turn off the built-in user LED
  digitalWrite(LED_BUILTIN, LOW);
  Serial.println("- User LED off!");
  delay(1000);
}
```

You should now see the built-in orange user LED blinking on and off at 1-second intervals, repeating this pattern continuously.

![Onboard RGB user LED blinking]()

Additionally, you can open the Arduino IDE's Serial Monitor (Tools > Serial Monitor) to see the status messages that the example sketch sends each time the user LED state changes.

![Arduino IDE Serial Monitor output for the orange LED example sketch]()

## Pins

This user manual section provides comprehensive information about the Nano 33 BLE Sense's pin capabilities and functionality. Understanding the board's pins capabilities and configurations is important for making the most of your projects.


### Pins Overview

The Nano 33 BLE Sense features a total of **20 accessible pins** arranged in the classic Nano form factor, maintaining compatibility with existing Nano shields and breadboard layouts. These pins provide various functionalities including digital I/O, analog input, PWM output and several communication protocols.

![Nano 33 BLE Sense pinout overview]()

### Pins Specifications and Characteristics

The Nano 33 BLE Sense's pins are organized into the following categories:

|   **Pin Type**   | **Count** |      **Pin Numbers**      |               **Primary Functions**                |
| :--------------: | :-------: | :-----------------------: | :------------------------------------------------: |
| **Digital Pins** |    14     |       `D2` - `D13`        |        Digital I/O, PWM (5 pins), SPI, UART        |
| **Analog Pins**  |     8     |        `A0` - `A7`        |     Analog input, Digital I/O, I2C, DAC (`A0`)     |
|  **Power Pins**  |     4     | `VIN`, `5V`, `3V3`, `GND` |              Power supply and ground               |
| **Special Pins** |     3     |  `RESET`, `AREF`, `VUSB`  | System control, reference, and power configuration |


***Please note: Pins A4 and A5 have internal pull-ups and are dedicated to the onboard I2C bus by default. Their use as analog inputs is not recommended.***


The following table shows the electrical specifications and operating limits for all pins on the Nano 33 BLE Sense board:

|    **Specification**    |  **Value**   |            **Notes**             |
| :---------------------: | :----------: | :------------------------------: |
|  **Operating Voltage**  |   +3.3 VDC   | Logic level for all digital pins |
| **Input Voltage Range** | 0 - +3.3 VDC |    Not 5 VDC tolerant inputs     |
| **Max Current per Pin** |              |    Source/sink current limit     |
|  **Max Total Current**  |              |  Combined current for all pins   |
|  **Analog Reference**   |   +3.3 VDC   |      Default `AREF` voltage      |

**Important safety considerations when working with the Nano 33 BLE Sense pins:**

- Never exceed +3.3 VDC on any I/O pin. The board is NOT 5V TOLERANT.

- The +5V pin is an INPUT only when the VUSB solder jumper is bridged and the board is powered by USB. It is never an output.

- Always use logic level converters when interfacing with 5V devices.


### Digital Pins

The Nano 33 BLE Sense features 14 digital pins (`D2` to `D13`, `RX`, `TX`) that can be configured as either digital inputs or digital outputs. These pins operate at +3.3 VDC logic levels. Digital pins are the foundation of most Arduino projects, allowing you to control LEDs, read button states, interface with sensors and communicate with other devices.

The Nano 33 BLE Sense digital pins provide the following functionality:

| **Arduino Pin** | **Microcontroller Pin** | **Additional Functions** |             **Special Features**              |
| :-------------: | :---------------------: | :----------------------: | :-------------------------------------------: |
|      `RX`       |         `P1.10`         |         UART RX          |             Serial communication              |
|      `TX`       |         `P1.03`         |         UART TX          |             Serial communication              |
|      `D2`       |         `P1.11`         |            -             |                  Digital I/O                  |
|      `D3`       |         `P1.12`         |           PWM            |                  Digital I/O                  |
|      `D4`       |         `P1.15`         |            -             |                  Digital I/O                  |
|      `D5`       |         `P1.13`         |           PWM            |                  Digital I/O                  |
|      `D6`       |         `P1.14`         |           PWM            |                  Digital I/O                  |
|      `D7`       |         `P0.23`         |            -             |                  Digital I/O                  |
|      `D8`       |         `P0.21`         |            -             |                  Digital I/O                  |
|      `D9`       |         `P0.27`         |           PWM            |                  Digital I/O                  |
|      `D10`      |         `P1.02`         |           PWM            |               SPI communication               |
|      `D11`      |         `P1.01`         |      SPI MOSI, PWM       |               SPI communication               |
|      `D12`      |         `P0.08`         |         SPI MISO         |               SPI communication               |
|      `D13`      |         `P0.13`         |         SPI SCK          | SPI communication, Built-in LED (LED_BUILTIN) |

***__Important note:__  Pins `RX` and `TX` are used for serial communication (UART) and should be avoided for general digital I/O when using Serial communication. Pins `D11` (COPI), `D12` (CIPO), and `D13` (SCK) are used for SPI communication.***


The Nano 33 BLE Sense's digital pins offer the following specifications:

|  **Specification**   |   **Value**   |                     **Notes**                     |
| :------------------: | :-----------: | :-----------------------------------------------: |
|    Logic Voltage     |   +3.3 VDC    |           `HIGH` and `LOW` logic levels           |
|    Input Voltage     | 0 to +3.3 VDC |                Not 5 VDC tolerant                 |
| Max Current (Source) |               |        Recommended per pin source current         |
|  Max Current (Sink)  |               |         Recommended per pin sink current          |
|  Total Max Current   |               | Recommended combined for all GPIO and 3V3 pin use |
|    Digital `HIGH`    |               |            Minimum voltage for `HIGH`             |
|    Digital `LOW`     |               |             Maximum voltage for `LOW`             |

Digital pins can be configured and controlled using the following basic Arduino functions.

You can configure a pin's mode using the `pinMode()` function:

```arduino
pinMode(pin, mode);
```

To write a digital value to an output pin, use the `digitalWrite()` function:

```arduino
digitalWrite(pin, value);
```

To read the state of a digital input pin, use the `digitalRead()` function:

```arduino
digitalRead(pin);
```

The available pin modes are `OUTPUT` for digital output, `INPUT` for digital input with high impedance, and `INPUT_PULLUP` for digital input with the internal pull-up resistor enabled. Digital output values can be `HIGH` (+3.3 VDC) or `LOW` (0 VDC), and digital input readings will return `HIGH` or `LOW` based on the voltage level detected on the pin.

***The following example demonstrate basic digital pin functionality using simple connections that you can easily test with the Nano 33 BLE Sense board.*** 

The following example demonstrates using both digital input and output simultaneously by reading a button and controlling the built-in LED of the board:

```arduino
/**
Combined Digital I/O Example for the Arduino Nano 33 BLE Sense Board
Name: nano_r4_digital_io_combined.ino
Purpose: This sketch demonstrates reading a button input and toggling
the built-in LED state each time the button is pressed.
*/

// Pin definitions
const int buttonPin = 2;            // Button input on D2
const int ledPin = LED_BUILTIN;     // Built-in LED

// Variables to store button and LED state
int buttonState = 0;
int lastButtonState = HIGH;
bool ledState = false;

void setup() {
  // Initialize serial communication and wait up to 2.5 seconds for a connection
  Serial.begin(115200);
  for (auto startNow = millis() + 2500; !Serial && millis() < startNow; delay(500));
  
  // Configure pins
  pinMode(buttonPin, INPUT_PULLUP);
  pinMode(ledPin, OUTPUT);
  
  // Turn off LED initially
  digitalWrite(ledPin, LOW);
  
  Serial.println("- Arduino Nano 33 BLE Sense - Combined Digital I/O Example started...");
  Serial.println("- Press button to toggle the built-in LED");
}

void loop() {
  // Read current button state
  buttonState = digitalRead(buttonPin);
  
  // Check if button was just pressed (state change from HIGH to LOW)
  if (buttonState == LOW && lastButtonState == HIGH) {
    // Button press detected - toggle LED state
    ledState = !ledState;
    digitalWrite(ledPin, ledState);
    
    Serial.print("- Button pressed! LED is now ");
    if (ledState) {
      Serial.println("ON");
    } else {
      Serial.println("OFF");
    }
    
    // Simple debounce delay
    delay(50);  
  }
  
  // Save current button state for next iteration
  lastButtonState = buttonState;
  
  // Small delay for stability
  delay(10);
}
```

To test this example, connect a push button to the Nano 33 BLE Sense board as follows:

- Connect one leg of a push button to pin `D2`
- Connect the other leg of the push button to `GND`
- No external components needed (using built-in LED and internal `INPUT_PULLUP`)

![Digital pins test circuit on the Nano 33 BLE Sense board]()

You should now see the built-in LED toggle on and off each time you press the button. The LED will stay in its current state until you press the button again. Additionally, you can open the Arduino IDE's Serial Monitor (Tools > Serial Monitor) to see messages indicating when the button is pressed and the current LED state.

![Arduino IDE Serial Monitor output for the combined digital I/O example sketch]()

### Analog Pins

The Nano 33 BLE Sense features 8 analog input pins (`A0` to `A7`) that can be read using the `analogRead()` function. These pins allow you to measure continuously varying voltages, making them perfect for reading sensors like potentiometers, light sensors, temperature sensors and other analog components and devices. The analog-to-digital converter (ADC) built into the nRF52840 microcontroller of the Nano 33 BLE Sense board converts the analog voltage into a digital value that your sketch can process.

The Nano 33 BLE Sense analog pins provide the following functionality:

| **Arduino Pin** | **Microcontroller Pin** | **Additional Functions** | **Special Features** |
| :-------------: | :---------------------: | :----------------------: | :------------------: |
|      `A0`       |         `P0.04`         |       Digital I/O        |          -           |
|      `A1`       |         `P0.05`         |       Digital I/O        |          -           |
|      `A2`       |         `P0.30`         |       Digital I/O        |          -           |
|      `A3`       |         `P0.29`         |       Digital I/O        |          -           |
|      `A4`       |         `P0.31`         |  SDA (I2C), Digital I/O  |  I2C communication   |
|      `A5`       |         `P0.02`         |  SCL (I2C), Digital I/O  |  I2C communication   |
|      `A6`       |         `P0.28`         |      Analog In Only      | No digital function  |
|      `A7`       |         `P0.03`         |      Analog In Only      | No digital function  |

***__Important note:__ Pins `A4` and `A5` are dedicated to I2C communication (SDA and SCL respectively) and have internal pull-up resistors enabled by default. Pins `A6` and `A7` are analog-only and cannot be used as digital pins.***


The Nano 33 BLE Sense's analog pins offer the following specifications:

| **Specification**  |   **Value**   |          **Notes**          |
| :----------------: | :-----------: | :-------------------------: |
|   Input Voltage    | 0 to +3.3 VDC | Maximum safe input voltage  |
| Default Resolution |    10-bit     |        Values 0-1023        |
| Maximum Resolution |    12-bit     |        Values 0-4095        |
| Default Reference  |   +3.3 VDC    |        AREF voltage         |
|    Sample Rate     |   200 kSPS    |   Maximum sampling speed    |
|      Accuracy      |    ±2 LSB     | Typical conversion accuracy |

You can read analog values using the `analogRead()` function:

```arduino
value = analogRead(pin);
``` 

The default reference voltage of these pins is +3.3 VDC. The default resolution is set to 10-bit, but it can be updated to 12-bit resolution using the analogReadResolution() function in the setup() of your sketch.

***The following examples demonstrate basic analog pin functionality using simple connections that you can easily test with the Nano 33 BLE Sense board.***

The following example demonstrates how to read an analog value and display it on the Serial Monitor:

```arduino
/**
/**
Analog Input Example for the Arduino Nano 33 BLE Sense Board
Name: nano_33_ble_sense_analog_input.ino
Purpose: This sketch demonstrates how to read an analog input
and display the value on the Serial Monitor.
*/

// Analog input pin
const int analogPin = A0;

void setup() {
  // Initialize serial communication and wait up to 2.5 seconds for a connection
  Serial.begin(115200);
  for (auto startNow = millis() + 2500; !Serial && millis() < startNow; delay(500));
  
  Serial.println("- Arduino Nano 33 BLE Sense - Analog Input Example started...");
  Serial.println("- Reading analog values from pin A0");
}

void loop() {
  // Read the analog value (0 - 1023 with 10-bit resolution)
  int analogValue = analogRead(analogPin);
  
  // Convert to voltage (0 to +3.3 VDC)
  float voltage = analogValue * (3.3 / 1023.0);
  
  // Display the results
  Serial.print("- Analog Value: ");
  Serial.print(analogValue);
  Serial.print(" | Voltage: ");
  Serial.print(voltage, 2);
  Serial.println(" VDC");
  
  // Wait half a second before next reading
  delay(500);  
}
```

To test this example, connect a potentiometer to the Nano 33 BLE Sense board as follows:

- Connect the middle pin of a potentiometer to `A0`
- Connect one outer pin of the potentiometer to `3V3`
- Connect the other outer pin of the potentiometer to `GND`

***Important: Never connect more than 3.3V to analog pins***

![ADC test circuit on the Nano 33 BLE Sense board]()

You can open the Arduino IDE's Serial Monitor (Tools > Serial Monitor) to see the real-time analog values and voltage measurements as you adjust the potentiometer. As you turn the potentiometer, the values will range from 0 to 1023, with corresponding voltage readings from 0 to +3.3 VDC.

![Arduino IDE Serial Monitor output for the analog input example sketch]()

The following example demonstrates how to use 12-bit resolution for more precise analog readings; **use the same potentiometer connection from the first example**:

```arduino
/**
/**
High-Resolution Analog Input Example for the Arduino Nano 33 BLE Sense Board
Name: nano_33_ble_sense_analog_high_res.ino
Purpose: This sketch demonstrates how to use 12-bit resolution
for precise analog input measurements.
*/

// Analog input pin
const int analogPin = A0;

void setup() {
  // Initialize serial communication and wait up to 2.5 seconds for a connection
  Serial.begin(115200);
  for (auto startNow = millis() + 2500; !Serial && millis() < startNow; delay(500));
  
  // Set analog read resolution to 12-bit (0 - 4095)
  analogReadResolution(12);
  
  Serial.println("- Arduino Nano 33 BLE Sense - High-Resolution Analog Input Example started...");
  Serial.println("- Using 12-bit resolution (0 - 4095)");
}

void loop() {
  // Read the analog value (0 - 4095 with 12-bit resolution)
  int analogValue = analogRead(analogPin);
  
  // Convert to voltage (0 - +3.3 VDC)
  float voltage = analogValue * (3.3 / 4095.0);
  
  // Calculate percentage (0 - 100%)
  float percentage = (analogValue / 4095.0) * 100.0;
  
  // Display the results
  Serial.print("- Analog Value: ");
  Serial.print(analogValue);
  Serial.print(" | Voltage: ");
  Serial.print(voltage, 3);
  Serial.print(" VDC | Percentage: ");
  Serial.print(percentage, 1);
  Serial.println(" %");
  
  // Wait half a second before next reading
  delay(500);
}
```

You can open the Arduino IDE's Serial Monitor (Tools > Serial Monitor) to see the high-resolution analog values, voltage measurements and percentage calculations as you adjust the potentiometer. With 12-bit resolution, the values will range from 0 to 4095 instead of the standard 0 to 1023, providing higher precision for sensitive measurements.

![Arduino IDE Serial Monitor output for the high-resolution analog input example sketch]()


### PWM (Pulse Width Modulation)

The Nano 33 BLE Sense board features multiple pins with PWM capability that can be used to generate analog-like output signals. PWM works by rapidly switching a digital output between `HIGH` and `LOW` states, where the ratio of `HIGH` time to the total period determines the effective analog voltage output.

The Nano 33 BLE Sense board provides PWM functionality on the following pins:

| **Arduino Pin** | **Microcontroller Pin**  | **Primary Function**  |
| :-------------: | :---------------------:  | :-------------------: |
|      `D3`       |         `P1.12`          |      Digital I/O      |
|      `D5`       |         `P1.13`          |      Digital I/O      |
|      `D6`       |         `P1.14`          |      Digital I/O      |
|      `D9`       |         `P1.27`          |      Digital I/O      |
|      `D10`      |         `P1.02`          |  Digital I/O, SPI CS  |
|      `D11`      |         `P1.01`          | Digital I/O, SPI MOSI |


***__Important note:__ The Nano 33 BLE Sense does not have a true Digital-to-Analog Converter (DAC). For analog output, PWM is the primary method. Pins `A4` and `A5` (I2C) and `D11`, `D12` (SPI) are not recommended for PWM as they are primarily used for communication buses.***


You can use PWM pins as analog output pins with the `analogWrite()` function:

```arduino
analogWrite(pin, value);
```

By default, the resolution is 8-bit (0 to 255). You can use analogWriteResolution() to change this, supporting up to 12-bit (0 to 4095) resolution: 

```arduino
analogWriteResolution(resolution);
```

***The following PWM examples use the built-in orange user LED (`LED_BUILTIN`) of the Nano 33 BLE Sense board, which supports PWM for brightness control. This eliminates the need for external components and allows you to test PWM functionality immediately.***

The following example demonstrates how to control the brightness of the built-in orange user LED using PWM:

```arduino
/**
PWM Example for the Arduino Nano 33 BLE Sense Board
Name: nano_33_ble_sense_pwm_led.ino
Purpose: This sketch demonstrates how to use PWM to control
the brightness of the built-in user LED.

@author Arduino Product Experience Team
@version 1.0 01/06/25
*/

// Built-in LED pin (supports PWM)
const int ledPin = LED_BUILTIN;

void setup() {
  // Initialize serial communication and wait up to 2.5 seconds for a connection
  Serial.begin(115200);
  for (auto startNow = millis() + 2500; !Serial && millis() < startNow; delay(500));
  
  Serial.println("- Arduino Nano 33 BLE Sense - PWM LED Example started...");
  Serial.println("- Built-in LED will fade in and out continuously");
}

void loop() {
  // Fade in (0 to 255)
  for (int brightness = 0; brightness <= 255; brightness++) {
    analogWrite(ledPin, brightness);
    delay(5);
  }
  
  Serial.println("- LED at maximum brightness");
  delay(500);
  
  // Fade out (255 to 0)
  for (int brightness = 255; brightness >= 0; brightness--) {
    analogWrite(ledPin, brightness);
    delay(5);
  }
  
  Serial.println("- LED turned off");
  delay(500);
}
```

You should now see the built-in orange user LED of your Nano 33 BLE Sense board gradually fade in and out, creating a smooth breathing effect that repeats continuously.

![Onboard RGB user LED fading](assets/pwm-1.gif)

Additionally, you can open the Arduino IDE's Serial Monitor (Tools > Serial Monitor) to see the status messages that the example sketch sends at key brightness levels.

![Arduino IDE Serial Monitor output for the PWM example sketch](assets/pwm-2.png)

The following example demonstrates how to use a 12-bit PWM resolution for more precise control of the built-in orange user LED:

```arduino
/**
High-Resolution PWM Example for the Arduino Nano 33 BLE Sense Board
Name: nano_33_ble_sense_pwm_high_res.ino
Purpose: This sketch demonstrates how to use 12-bit PWM resolution
for precise control of the built-in orange user LED brightness.

@author Arduino Product Experience Team
@version 1.0 01/06/25
*/

// Built-in LED pin (supports PWM)
const int pwmPin = LED_BUILTIN;

void setup() {
  // Initialize serial communication and wait up to 2.5 seconds for a connection
  Serial.begin(115200);
  for (auto startNow = millis() + 2500; !Serial && millis() < startNow; delay(500));
  
  // Set PWM resolution to 12-bit (0-4095)
  analogWriteResolution(12);
  
  Serial.println("- Arduino Nano 33 BLE Sense - High-Resolution PWM Example started...");
  Serial.println("- Using 12-bit resolution (0-4095) with built-in LED");
}

void loop() {
  // Generate a smooth sine wave using 12-bit PWM
  for (int i = 0; i < 360; i++) {
    // Calculate sine wave value and map to 12-bit range
    float sineValue = sin(i * PI / 180.0);
    int pwmValue = (int)((sineValue + 1.0) * 2047.5);  // Map -1 to 1 → 0 to 4095
    
    analogWrite(pwmPin, pwmValue);
    
    // Print current values every 30 degrees
    if (i % 30 == 0) {
      Serial.print("- Angle: ");
      Serial.print(i);
      Serial.print("°, PWM Value: ");
      Serial.println(pwmValue);
    }
    
    delay(10);
  }
  
  Serial.println("- Sine wave cycle completed");
  delay(1000);
}
```

This high-resolution example creates a smooth sine wave pattern with the built-in LED brightness, demonstrating the precision available with a 12-bit PWM resolution. You should see a very smooth transition in the LED brightness following a sine wave pattern. Additionally, you can open the Arduino IDE's Serial Monitor (Tools > Serial Monitor) to see the angle and PWM value outputs that demonstrate the precise 12-bit control values being used.

![Arduino IDE Serial Monitor output for the high-resolution PWM example sketch]()

### 5V

The microcontroller on the Arduino Nano 33 BLE Sense runs at 3.3V, which means that you must never apply more than 3.3V to its Digital and Analog pins. Care must be taken when connecting sensors and actuators to assure that this limit of 3.3V is never exceeded. Connecting higher voltage signals, like the 5V commonly used with the other Arduino boards, will damage the Arduino Nano 33 BLE Sense.

To avoid such risk with existing projects, where you should be able to pull out a Nano and replace it with the new Nano 33 BLE Sense, we have the 5V pin on the header, positioned between RST and A7 that is not connected as default factory setting. This means that if you have a design that takes 5V from that pin, it won't work immediately, as a precaution we put in place to draw your attention to the 3.3V compliance on digital and analog inputs.

5V on that pin is available only when two conditions are met: you make a solder bridge on the two pads marked as VUSB and you power the Nano 33 BLE Sense through the USB port. If you power the board from the VIN pin, you won't get any regulated 5V and therefore even if you do the solder bridge, nothing will come out of that 5V pin. The 3.3V, on the other hand, is always available and supports enough current to drive your sensors. Please make your designs so that sensors and actuators are driven with 3.3V and work with 3.3V digital IO levels. 5V is now an option for many modules and 3.3V is becoming the standard voltage for electronic ICs.

![Soldering the VUSB pins.](assets/Nano33_ble_sense_vusb.png)


## UART Communication

The Nano 33 BLE Sense board features built-in UART (Universal Asynchronous Receiver-Transmitter) communication that allows your projects to communicate with other devices through serial data transmission. UART is implemented within the nRF52840 microcontroller and provides two separate hardware serial ports: one connected to the USB Micro connector for computer communication, and another available on pins `RX` and `TX` for external device communication.

UART is one of the most used device-to-device communication protocols, allowing asynchronous serial communication where the data format and transmission speed are configurable. The protocol sends data bits one by one, from the least significant to the most significant, framed by start and stop bits. Embedded systems, microcontrollers, and computers use UART as a form of device-to-device hardware communication that requires only two wires for transmitting and receiving data.

The Nano 33 BLE Sense's UART interface offers the following technical specifications:

|   **Parameter**   |  **Value**  |      **Notes**       |
| :---------------: | :---------: | :------------------: |
|    Baud Rates     |             | Common: 9600, 115200 |
|     Data Bits     |             | Standard data width  |
|   Communication   | Full-duplex |  Simultaneous TX/RX  |
|  Hardware Ports   |      2      | USB Serial + Serial1 |
|     UART Pins     | `RX`, `TX`  | RX, TX respectively  |
| Operating Voltage |  +3.3 VDC   |   TTL logic levels   |
|   Flow Control    |  Software   |  XON/XOFF supported  |

The Nano 33 BLE Sense board uses the following pins for UART communication:

| **Arduino Pin** | **Microcontroller Pin** | **UART Function** | **Description** |
| :-------------: | :---------------------: | :---------------: | :-------------: |
|      `RX`       |         `P1.10`         |      Receive      |  Receive Data   |
|      `TX`       |         `P1.03`         |     Transmit      |  Transmit Data  |

You can communicate via UART using the built-in `Serial` and `Serial1` objects. The `Serial` object is connected to the USB Micro port for computer communication, while `Serial1` is connected to pins `RX` and `TX` for external device communication.

The following example demonstrates basic UART communication patterns:

```arduino
/**
/**
UART Basic Example for the Arduino Nano 33 BLE Sense Board
Name: nano_33_ble_sense_uart_basic.ino
Purpose: This sketch demonstrates basic UART communication
using both USB Serial and hardware Serial1.

@author Arduino Product Experience Team
@version 1.0 01/06/25
*/

void setup() {
  // Initialize USB serial communication at 115200 baud
  Serial.begin(115200);
  for (auto startNow = millis() + 2500; !Serial && millis() < startNow; delay(500));
  
  // Initialize hardware serial on RX/TX pins at 9600 baud
  Serial1.begin(9600);
  
  Serial.println("- Arduino Nano 33 BLE Sense - UART Basic Example started...");
  Serial.println("- USB Serial (Serial): 115200 baud");
  Serial.println("- Hardware Serial (Serial1): 9600 baud on RX/TX");
  Serial.println("- Connect external device to RX and TX pins");
  Serial.println("- Type messages in Serial Monitor to send via Serial1");
  Serial.println();
}

void loop() {
  // Check for data from USB Serial (computer)
  if (Serial.available()) {
    String message = Serial.readString();
    message.trim(); // Remove newline characters
    
    if (message.length() > 0) {
      Serial.print("- USB received: \"");
      Serial.print(message);
      Serial.println("\"");
      
      // Send the message via Serial1 (RX/TX)
      Serial1.print("- Message from USB: ");
      Serial1.println(message);
      
      Serial.println("- Message sent via Serial1 (RX/TX)!");
    }
  }
  
  // Check for data from Serial1 (external device on RX/TX)
  if (Serial1.available()) {
    String response = Serial1.readString();
    response.trim(); // Remove newline characters
    
    if (response.length() > 0) {
      Serial.print("- Serial1 received: \"");
      Serial.print(response);
      Serial.println("\"");
    }
  }
  
  // Send periodic test data via Serial1
  static unsigned long lastSend = 0;
  if (millis() - lastSend > 3000) {
    lastSend = millis();
    
    // Send test data with timestamp
    Serial1.print("Test data: ");
    Serial1.print(millis());
    Serial1.println(" ms");
    
    Serial.println("- Periodic test data sent via Serial1!");
  }
  
  delay(10);
}
```

***To test this example, connect an external UART device to the `RX` and `TX` pins. The code will demonstrate UART communication patterns that can be observed with a logic analyzer or by connecting another serial device.***

You can open the Arduino IDE's Serial Monitor (Tools > Serial Monitor) to interact with the USB serial port and observe the communication patterns.

![Arduino IDE Serial Monitor output for the UART example sketch](assets/uart-1.png)


The Nano 33 BLE Sense board provides two distinct UART communication channels, giving you the flexibility to handle multiple communication tasks simultaneously. The first channel is the USB Serial (`Serial`), which is your primary interface for programming and debugging. This channel offers several key features:

- Connected to the onboard USB Micro connector
- Used for programming and debugging
- Typically runs at 115200 baud
- Automatic baud rate detection
- No external connections required 

The second channel is the Hardware Serial (`Serial1`), which is dedicated to external device communication. This channel provides robust connectivity for your project peripherals:

- Connected to pins `RX` and `TX`
- Used for external device communication
- Configurable baud rate.
- TTL voltage levels (0 VDC/+3.3 VDC)
- Requires external device connection

Here is a practical example of reading incoming data from an external UART device::

```arduino
// Example: Reading data from external UART device
void readUARTData() {
  String incoming = "";
  
  while (Serial1.available()) {
    delay(2);  // Small delay for stability
    char c = Serial1.read();
    incoming += c;
  }
  
  if (incoming.length() > 0) {
    Serial.print("Received: ");
    Serial.println(incoming);
  }
}

// Example: Sending data to external UART device
void sendUARTData() {
  Serial1.write("Hello world!");
}
```

When working with UART on the Nano 33 BLE Sense, there are several key points to keep in mind:
- Voltage Levels: The UART operates at 3.3V TTL levels (0V for LOW, 3.3V for HIGH). Never connect 5V devices directly without a level shifter.

- Baud Rate Matching: Ensure both devices use the same baud rate, data bits (typically 8), stop bits (typically 1), and parity (typically none).

- Connection Pattern: Remember that TX connects to RX and RX connects to TX (crossover connection) when connecting two devices.

- Asynchronous Protocol: UART is asynchronous, meaning there's no clock signal. The baud rate must be identical on both transmitting and receiving devices.

- Dual Channel Advantage: Unlike some older Arduino boards, the Nano 33 BLE Sense has separate channels for USB and hardware UART, allowing simultaneous debugging and external communication.

## SPI Communication

The Nano 33 BLE Sense board features built-in SPI (Serial Peripheral Interface) communication that allows your projects to communicate with external devices like sensors, displays, memory cards, and other microcontrollers. SPI is implemented within the nRF52840 microcontroller and uses dedicated pins to provide high-speed synchronous serial communication.

SPI is particularly useful when your project needs to communicate with external components at high speeds. While I2C is suitable for simple sensor communication and UART for basic serial data exchange, SPI excels at high-speed communication with devices like SD cards, TFT displays, wireless modules, or external memory chips. SPI can achieve faster data rates than I2C and can handle multiple devices on the same bus through individual chip select lines.

The Nano 33 BLE Sense's SPI interface offers the following technical specifications:

|   **Parameter**   |           **Value**            |          **Notes**          |
| :---------------: | :----------------------------: | :-------------------------: |
|    Clock Speed    |                                |    Maximum SPI frequency    |
|   Data Transfer   |                                |     Standard data width     |
|   Communication   |          Full-duplex           |  Simultaneous send/receive  |
|     SPI Pins      | `D11`, `D12`, `D13` + any GPIO | `COPI`, `CIPO`, `SCK`, `CS` |
| Multiple Devices  |           Supported            |   Via different `CS` pins   |
| Operating Voltage |            +3.3 VDC            |        Same as board        |
| Protocol Support  |                                |   All SPI modes available   |

The Nano 33 BLE Sense board uses the following pins for SPI communication:

| **Arduino Pin** | **Microcontroller Pin** | **SPI Function** |        **Description**        |
| :-------------: | :---------------------: | :--------------: | :---------------------------: |
|      `D11`      |         `P1.01`         |      `COPI`      | Controller Out, Peripheral In |
|      `D12`      |         `P1.08`         |      `CIPO`      | Controller In, Peripheral Out |
|      `D13`      |         `P0.13`         |      `SCK`       |         Serial Clock          |
|    Any GPIO     |            -            |       `CS`       | Chip Select (any digital pin) |

***Note: The signal names have been updated from the traditional MOSI/MISO/SS to the modern COPI/CIPO/CS terminology for better clarity.***

You can communicate via SPI using the dedicated `SPI.h` library, which is included in the Arduino Mbed OS Nano Boards core. The library provides simple functions to initialize the bus, send and receive data and manage multiple devices.

The following example demonstrates how to use SPI communication:

```arduino
/**
SPI Basic Example for the Arduino Nano 33 BLE Sense Board
Name: nano_r4_spi_basic.ino
Purpose: This sketch demonstrates how to use SPI communication
to send and receive data.

@author Arduino Product Experience Team
@version 1.0 01/06/25
*/

#include <SPI.h>

// Chip Select pin for SPI device
const int CS_PIN = 10;

void setup() {
  // Initialize serial communication and wait up to 2.5 seconds for a connection
  Serial.begin(115200);
  for (auto startNow = millis() + 2500; !Serial && millis() < startNow; delay(500));
  
  Serial.println("- Arduino Nano 33 BLE Sense - SPI Basic Example started...");
  
  // Set CS pin as output and set it HIGH (inactive)
  pinMode(CS_PIN, OUTPUT);
  digitalWrite(CS_PIN, HIGH);
  
  // Initialize SPI communication
  SPI.begin();
  
  // Configure SPI settings
  // - Clock speed: 1 MHz (1000000 Hz)
  // - Data order: Most Significant Bit first
  // - Data mode: Mode 0 (Clock polarity = 0, Clock phase = 0)
  SPI.beginTransaction(SPISettings(1000000, MSBFIRST, SPI_MODE0));
  
  Serial.println("- SPI initialized successfully");
  Serial.println("- Ready to communicate with SPI devices");
  
  // Example: Send some test data
  sendSPIData();
}

void loop() {
  // Send a counter value every 2 seconds
  static int counter = 0;
  
  // Select the device (CS LOW)
  digitalWrite(CS_PIN, LOW);
  
  // Send counter value
  byte response = SPI.transfer(counter);
  
  // Deselect the device (CS HIGH)
  digitalWrite(CS_PIN, HIGH);
  
  // Display results
  Serial.print("- Sent: ");
  Serial.print(counter);
  Serial.print(" | Received: ");
  Serial.println(response);
  
  // Increment counter and wrap around at 255
  counter++;
  if (counter > 255) {
    counter = 0;
  }
  
  delay(2000);
}

void sendSPIData() {
  Serial.println("- Sending test data...");
  
  // Select the device
  digitalWrite(CS_PIN, LOW);
  
  // Send a sequence of test bytes
  for (int i = 0; i < 5; i++) {
    byte testData = 0x10 + i;  // Send 0x10, 0x11, 0x12, 0x13, 0x14
    byte response = SPI.transfer(testData);
    
    Serial.print("  Sent: 0x");
    if (testData < 16) Serial.print("0");
    Serial.print(testData, HEX);
    Serial.print(" | Received: 0x");
    if (response < 16) Serial.print("0");
    Serial.println(response, HEX);
    
    delay(100);
  }
  
  // Deselect the device
  digitalWrite(CS_PIN, HIGH);
  
  Serial.println("- Test data transmission complete");
}
```

***To test this example, connect an SPI-compatible device. Without a connected device, the received data will typically be `0xFF` or random values.***

You can open the Arduino IDE's Serial Monitor (Tools > Serial Monitor) to see the SPI communication in action.

![Arduino IDE Serial Monitor output for the SPI example sketch](assets/spi-1.png)

For connecting multiple SPI devices, you can use different digital pins as Chip Select (`CS`) lines while sharing the `COPI`, `CIPO`, and `SCK` pins:

```arduino
// Multiple SPI device example
const int DEVICE1_CS = 10;  // First SPI device
const int DEVICE2_CS = 9;   // Second SPI device
const int DEVICE3_CS = 8;   // Third SPI device

void setup() {
  SPI.begin();
  
  // Configure all CS pins as outputs
  pinMode(DEVICE1_CS, OUTPUT);
  pinMode(DEVICE2_CS, OUTPUT);
  pinMode(DEVICE3_CS, OUTPUT);
  
  // Set all CS pins HIGH (inactive)
  digitalWrite(DEVICE1_CS, HIGH);
  digitalWrite(DEVICE2_CS, HIGH);
  digitalWrite(DEVICE3_CS, HIGH);
}

void communicateWithDevice(int csPin, byte address, byte data) {
  digitalWrite(csPin, LOW);    // Select device
  SPI.transfer(address);
  SPI.transfer(data);
  digitalWrite(csPin, HIGH);   // Deselect device
}
```

When working with SPI on the Nano 33 BLE Sense, there are several key points to keep in mind:

Voltage Levels: The SPI operates at 3.3V logic levels. Never connect 5V SPI devices directly without a level shifter.

- **Chip Select Management:** Only one device should be selected (`CS LOW`) at a time. Always deselect devices after communication.

- **Device Compatibility:** Different SPI devices may require specific clock speeds, modes, and protocols. Always consult your device's datasheet.

- **Synchronous Protocol:** SPI is synchronous, meaning data is transferred in both directions simultaneously with each clock pulse.

- **Flexible CS Pins:** Unlike some Arduino boards, you can use any digital pin as a Chip Select pin, providing flexibility for multiple devices.

- **Modern Terminology:** Use COPI (Controller Out, Peripheral In) instead of MOSI, and CIPO (Controller In, Peripheral Out) instead of MISO.

## I2C Communication

The Nano 33 BLE Sense board features built-in I2C (Inter-Integrated Circuit) communication that allows your projects to communicate with multiple devices using just two wires. I2C is implemented within the nRF52840 microcontroller and uses two dedicated pins to provide reliable serial communication with sensors, displays, memory modules, and other microcontrollers. This makes it perfect for projects that need to connect several devices without using many pins.

I2C is particularly useful when your project needs to communicate with multiple sensors and devices in a simple way. While SPI is excellent for high-speed communication and UART for basic serial data exchange, I2C excels at connecting many devices with minimal wiring. Multiple I2C devices can share the same two-wire bus, each with its own unique address, making it ideal for sensor networks, display modules, and expandable systems.

The Nano 33 BLE Sense's I2C interface offers the following technical specifications:

|   **Parameter**   |  **Value**  |        **Notes**        |
| :---------------: | :---------: | :---------------------: |
|    Clock Speed    |             |                         |
|   Data Transfer   |             |   Standard data width   |
|   Communication   | Half-duplex | One direction at a time |
|     I2C Pins      | `A4`, `A5`  |  SDA, SCL respectively  |
| Device Addressing |             |                         |
| Operating Voltage |  +3.3 VDC   |      Same as board      |

The Nano 33 BLE Sense uses the following pins for I2C communication:

| **Arduino Pin** | **Microcontroller Pin** | **I2C Function** |  **Description**  |
|:---------------:|:-----------------------:|:----------------:|:-----------------:|
|       `A4`      |          `P0.31`         |        SDA       |  Serial Data Line |
|       `A5`      |          `P0.02`         |        SCL       | Serial Clock Line |

You can communicate via I2C using the dedicated `Wire.h` library, which is included in the Arduino UNO R4 Boards core. The library provides simple functions to initialize the bus, send and receive data and manage multiple devices.

The following example demonstrates basic I2C communication patterns:

```arduino
/**
I2C Basic Example for the Arduino Nano 33 BLE Sense Board
Name: nano_r4_i2c_basic.ino
Purpose: This sketch demonstrates basic I2C communication
patterns for protocol analysis.

@author Arduino Product Experience Team
@version 1.0 01/06/25
*/

#include <Wire.h>

// Example device address
const int DEVICE_ADDRESS = 0x48;

void setup() {
  // Initialize serial communication and wait up to 2.5 seconds for a connection
  Serial.begin(115200);
  for (auto startNow = millis() + 2500; !Serial && millis() < startNow; delay(500));
  
  Serial.println("- Arduino Nano 33 BLE Sense - I2C Basic Example started...");
  
  // Initialize I2C communication as master
  Wire.begin();
  
  Serial.println("- I2C initialized successfully");
  Serial.println("- Connect protocol analyzer to A4 (SDA) and A5 (SCL)");
  Serial.println("- Starting I2C communication patterns...");
  
  delay(2000);
}

void loop() {
  // Write a single byte
  Serial.println("- Writing single byte (0xAA) to device 0x48...");
  Wire.beginTransmission(DEVICE_ADDRESS);
  Wire.write(0xAA);
  Wire.endTransmission();
  
  delay(1000);
  
  // Write multiple bytes
  Serial.println("- Writing multiple bytes (0x10, 0x20, 0x30) to device 0x48...");
  Wire.beginTransmission(DEVICE_ADDRESS);
  Wire.write(0x10);
  Wire.write(0x20);
  Wire.write(0x30);
  Wire.endTransmission();
  
  delay(1000);
  
  // Request data from device
  Serial.println("- Requesting 2 bytes from device 0x48...");
  Wire.requestFrom(DEVICE_ADDRESS, 2);
  
  // Read any available data
  while (Wire.available()) {
    int data = Wire.read();
    Serial.print("Received: 0x");
    if (data < 16) Serial.print("0");
    Serial.println(data, HEX);
  }
  
  delay(2000);
  Serial.println("---");
}
```
***To test this example, no external I2C devices are required. The code will generate I2C communication patterns that can be analyzed with a protocol analyzer. Without devices connected, read operations will typically return `0xFF`.***

You can open the Arduino IDE's Serial Monitor (Tools > Serial Monitor) to see the I2C operations being performed. Connect a protocol analyzer to pins `A4` (SDA) and `A5` (SCL) to observe the actual I2C protocol signals.

![Arduino IDE Serial Monitor output for the I2C example sketch](assets/i2c-1.png)

***The I2C protocol requires pull-up resistors on both SDA and SCL lines. __The Nano 33 BLE Sense board does not have internal pull-ups on `A4` and `A5` to avoid interference with their analog input functionality, so external 4.7kΩ pull-up resistors to +5 VDC are required for proper I2C operation__.***

One of the main advantages of I2C is the ability to connect multiple devices to the same bus. Here is how to connect multiple I2C devices:

```arduino
// Example: Communicating with multiple I2C devices
void communicateWithMultipleDevices() {
  // Device addresses (examples)
  const int SENSOR_ADDRESS = 0x48;    // Temperature sensor
  const int DISPLAY_ADDRESS = 0x3C;   // OLED display
  const int EEPROM_ADDRESS = 0x50;    // External EEPROM
  
  // Read from temperature sensor
  Wire.beginTransmission(SENSOR_ADDRESS);
  Wire.write(0x00);  // Register to read
  Wire.endTransmission();
  
  Wire.requestFrom(SENSOR_ADDRESS, 2);
  if (Wire.available() >= 2) {
    int tempHigh = Wire.read();
    int tempLow = Wire.read();
    Serial.print("Temperature: ");
    Serial.println((tempHigh << 8) | tempLow);
  }
  
  // Send data to display
  Wire.beginTransmission(DISPLAY_ADDRESS);
  Wire.write(0x40);  // Data mode
  Wire.write(0xFF);  // Sample data
  Wire.endTransmission();
  
  // Write to EEPROM
  Wire.beginTransmission(EEPROM_ADDRESS);
  Wire.write(0x00);  // Memory address
  Wire.write(0x55);  // Data to write
  Wire.endTransmission();
}
```

When working with I2C on the Nano 33 BLE Sense board, there are several key points to keep in mind for successful implementation:

- Each I2C device must have a unique address on the bus, so check device datasheets to avoid address conflicts.
- Keep in mind that I2C is a half-duplex protocol, meaning data flows in only one direction at a time. The master device (your Nano 33 BLE Sense board) controls the clock line and initiates all communication.
- When connecting multiple devices, simply connect all SDA pins together and all SCL pins together, along with power and ground connections.
- The Nano 33 BLE Sense board can communicate with up to 127 different I2C devices on the same bus, making it perfect for complex sensor networks and expandable systems.

## LSM9DS1 Sensor

IMU stands for: inertial measurement unit. It is an electronic device that measures and reports a body's specific force, angular rate and the orientation of the body, using a combination of accelerometers, gyroscopes, and oftentimes magnetometers.

![The LSM9DS1 sensor](assets/Nano33_ble_sense_imu.png)

The LSM9DS1 is a system-in-package featuring a 3D digital linear acceleration sensor, a 3D digital angular rate sensor, and a 3D digital magnetic sensor.

To access the data from the LSM9DS1 module, we need to install the LSM9DS1 library, which comes with examples that can be used directly with the Nano 33 BLE Sense.

It can be installed directly from the library manager through the IDE of your choice. To use it, we need to include it at the top of the sketch:

```arduino
#include <Arduino_LSM9DS1.h>
```
And to initialize the library, we can use the following command inside `void setup()`.

```arduino
  if (!IMU.begin()) {
    Serial.println("Failed to initialize IMU!");
    while (1);
  }
```
### Accelerometer
An accelerometer is an electromechanical device used to measure acceleration forces. Such forces may be static, like the continuous force of gravity or, as is the case with many mobile devices, dynamic to sense movement or vibrations.

The accelerometer data can be accessed through the following commands:

```arduino
  float x, y, z;

  if (IMU.accelerationAvailable()) {
    IMU.readAcceleration(x, y, z);
  }
```
Here is an example of using the accelerometer as a "level" that will provide information about the position of the board. With this application we will be able to read what the relative position of the board is as well as the degrees, by tilting the board up, down, left or right:

```arduino
/*
  Arduino LSM9DS1 - Accelerometer Application

  This example reads the acceleration values as relative direction and degrees,
  from the LSM9DS1 sensor and prints them to the Serial Monitor or Serial Plotter.

  The circuit:
  - Arduino Nano 33 BLE Sense

  Created by Riccardo Rizzo

  Modified by Jose García
  27 Nov 2020

  This example code is in the public domain.
*/

#include <Arduino_LSM9DS1.h>

float x, y, z;
int degreesX = 0;
int degreesY = 0;

void setup() {
  Serial.begin(9600);
  while (!Serial);
  Serial.println("Started");

  if (!IMU.begin()) {
    Serial.println("Failed to initialize IMU!");
    while (1);
  }

  Serial.print("Accelerometer sample rate = ");
  Serial.print(IMU.accelerationSampleRate());
  Serial.println("Hz");
}

void loop() {

  if (IMU.accelerationAvailable()) {
    IMU.readAcceleration(x, y, z);

  }

  if (x > 0.1) {
    x = 100 * x;
    degreesX = map(x, 0, 97, 0, 90);
    Serial.print("Tilting up ");
    Serial.print(degreesX);
    Serial.println("  degrees");
  }
  if (x < -0.1) {
    x = 100 * x;
    degreesX = map(x, 0, -100, 0, 90);
    Serial.print("Tilting down ");
    Serial.print(degreesX);
    Serial.println("  degrees");
  }
  if (y > 0.1) {
    y = 100 * y;
    degreesY = map(y, 0, 97, 0, 90);
    Serial.print("Tilting left ");
    Serial.print(degreesY);
    Serial.println("  degrees");
  }
  if (y < -0.1) {
    y = 100 * y;
    degreesY = map(y, 0, -100, 0, 90);
    Serial.print("Tilting right ");
    Serial.print(degreesY);
    Serial.println("  degrees");
  }
  delay(1000);
}
```
In order to get a correct reading of the board data, before uploading the sketch to the board hold the board in your hand, from the side of the USB port. The board should be facing up and "pointing" away from you. The image below illustrates the board's position and how it works:

![Interacting with the X and Y axes.](./assets/nano33BS_02_illustration.png)

Now, you can verify and upload the sketch to the board and open the Monitor from the menu on the left.  

If you tilt the board upwards, downwards, right or left, you will see the results printing every second according to the direction of your movement!

Here is a screenshot of the sketch returning these values:

![Printing out the "tilt condition" of the board.](./assets/nano33BS_02_printing_values.png)


## Support

If you encounter any issues or have questions while working with your Nano 33 BLE Sense board, we provide various support resources to help you find answers and solutions.

### Help Center

Explore our Help Center, which offers a comprehensive collection of articles and guides for Nano family boards. The Help Center is designed to provide in-depth technical assistance and help you make the most of your device.

- [Nano family help center page](https://support.arduino.cc/hc/en-us/sections/360004605400-Nano-Family)

### Forum

Join our community forum to connect with other Nano family board users, share your experiences, and ask questions. The Forum is an excellent place to learn from others, discuss issues, and discover new ideas and projects related to the Nano 33 BLE Sense.

- [Nano category in the Arduino Forum](https://forum.arduino.cc/c/official-hardware/nano-family/87)

### Contact Us

Please get in touch with our support team if you need personalized assistance or have questions not covered by the help and support resources described before. We're happy to help you with any issues or inquiries about the Nano family boards.

- [Contact us page](https://www.arduino.cc/en/contact-us/)
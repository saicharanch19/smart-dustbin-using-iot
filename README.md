The SMART DUSTBIN WITH GARBAGE LEVEL INDICATOR has been developed using the following sensor and equipment:
1.	NodeMCU ESP8266 : The NodeMCU ESP8266 is a popular development board that integrates the ESP8266 Wi-Fi chip. It's widely used in IoT (Internet of Things) projects due to its low cost, small size, and built-in Wi-Fi capabilities, making it suitable for applications like the Smart Dustbin with Garbage Level Indicator.
2.	Ultrasonic Sensor : measures the distance to an object using ultrasonic sound waves.
3.	Arduino UNO : The Arduino Uno is an open-source microcontroller board based on the Microchip ATmega328P microcontroller
4.	IR Sensor : Detects the motion of the object
5.	servo motor : is a rotary actuator that allows for precise control of angular position.





3.1	Block Diagram
A block diagram is a diagram of a system in which the principal parts or functions are represented by blocks connected by lines that show the relationships of the blocks. A block diagram is used to represent a control system in diagram form.
 
 

In the above Figure 2 shows a block diagram that covers the general flow of the system. An ultrasonic sensor was used to detect distance and height on a trashcan, and an NodeMCU ESP8266 was utilised to programme the uploading of a code for Wi-Fi connectivity. The data monitored and obtained from the NodeMCU ESP8266 is can be seen on Blynk Cloud. Also the second diagram in the above figure shows how the Ir sensor and Servo motor are Interfaced with Arduino uno to make the trashcan lid opening mechanism automatic.







3.2	Flow Diagram
A flowchart is a graphical representation of a process. It is a type of diagram that represents a workflow or process. A flowchart can also be defined as a diagrammatic representation of an algorithm, a step-by-step approach to solving a task. The flowchart shows the steps as boxes of various kinds, and their order by connecting the boxes with arrows.
 










































In the above Figure 3 shows a flow diagram in which the system monitors the garbage bin and informs about the level of the garbage collected in the trash bin.
 
3.3	Sequence Diagram
A sequence diagram represents object collaboration and is used to define event sequences between objects for a certain outcome. It is an essential component used in processes related to analysis, design and documentation























3.4	Data Flow Diagram
A data-flow diagram is a way of representing a flow of data through a process or a system. It utilizes characterized images like square shapes, circles, and bolts, in addition to short text marks, to show information inputs, yields, capacity focuses and the courses between every objective. It portrays the interface between the other components and is shown with arrows, typically labeled with a short data name. A DFD model uses a number of notations to represent flow of data:


A DFD model uses a number of notations to represent flow of data:
1.	External Entity
2.	Data Flow
3.	Process
4.	Data store
 
 







 
CHAPTER 4 SYSTEM REQUIREMENT

Hardware Requirements
We will need the following hardware to accomplish our project.
1.	Ultrasonic Sensor (HC-SR04)
2.	NodeMCU esp8266
3.	Arduinno UNO
4.	IR Sensor
5.	Servo Motor
6.	Bread Board
7.	Jumper Wires
8.	Dustbin


4.1	Ultrasonic Sensor (HC-SR04)
The Ultrasonic Sensor is a device that uses ultrasonic sound waves to determine the distance to the garbage. It has a transducer that helps in the transmission and reception of ultrasonic pulses dependent on the closeness of the item. It detects items as well as trash stuff. HC-SR04 is an ultrasonic sensor which is used for measuring the distance between the top of the lid to the top of the garbage.


Table 1: Pin Number and Function of Ultrasonic sensor

 
 






The ultrasonic sensor uses sonar to determine the distance to an object. Here’s how it works:
•	The ultrasound transmitter (trig pin) emits a high-frequency sound (40 kHz).
•	The sound travels through the air. If it finds an object, it bounces back to the module.
•	The ultrasound receiver (echo pin) receives the reflected sound (echo).


4.2	ESP8266 Node MCU :
The NodeMCU (Node MicroController Unit) is an open-source software and hardware development environment built around an inexpensive System-on-a-Chip (SoC) called the ESP8266. The ESP8266, designed and manufactured by Espressif Systems, contains the crucial elements of a computer: CPU, RAM, networking (WiFi), and even a modern operating system and SDK.
 
 


Figure 9 : ESP8266 NodeMCU

•	Power Pins There are four power pins. VIN pin and three 3.3V pins.
•	VIN can be used to directly supply the NodeMCU/ESP8266 and its peripherals. Power delivered on VIN is regulated through the onboard regulator on the NodeMCU module – you can also supply 5V regulated to the VIN pin
•	3.3V pins are the output of the onboard voltage regulator and can be used to supply power to external components.
•	GND are the ground pins of NodeMCU/ESP8266
•	I2C Pins are used to connect I2C sensors and peripherals. Both I2C Master and I2C Slave are supported. I2C interface functionality can be realized programmatically, and the clock frequency is 100 kHz at a maximum. It should be noted that I2C clock frequency should be higher than the slowest clock frequency of the slave device.

•	GPIO Pins NodeMCU/ESP8266 has 17 GPIO pins which can be assigned to functions such as I2C, I2S, UART, PWM, IR Remote Control, LED Light and Button programmatically. Each digital enabled GPIO can be configured to internal pull-up or pull-down, or set to high impedance. When configured as an input, it can also be set to edge-trigger or level-trigger to generate CPU interrupts.

•	ADC Channel The NodeMCU is embedded with a 10-bit precision SAR ADC. The two functions can be implemented using ADC. Testing power supply voltage of VDD3P3 pin and testing input voltage of TOUT pin. However, they cannot be implemented at the same time.

•	UART Pins NodeMCU/ESP8266 has 2 UART interfaces (UART0 and UART1) which provide asynchronous communication (RS232 and RS485), and can communicate at up to 4.5 Mbps. UART0 (TXD0, RXD0, RST0 & CTS0 pins
 
can be used for communication. However, UART1 (TXD1 pin) features only data transmit signal so, it is usually used for printing log.
•	SPI Pins NodeMCU/ESP8266 features two SPIs (SPI and HSPI) in slave and master modes. These SPIs also support the following general-purpose SPI features:
•	4 timing modes of the SPI format transfer
•	Up to 80 MHz and the divided clocks of 80 MHz
•	Up to 64-Byte FIFO
•	SDIO Pins NodeMCU/ESP8266 features Secure Digital Input/Output Interface (SDIO) which is used to directly interface SD cards. 4-bit 25 MHz SDIO v1.1 and 4-bit 50 MHz SDIO v2.0 are supported.

•	PWM Pins The board has 4 channels of Pulse Width Modulation (PWM). The PWM output can be implemented programmatically and used for driving digital motors and LEDs. PWM frequency range is adjustable from 1000 μs to 10000 μs (100 Hz and 1 kHz).
•	Control Pins are used to control the NodeMCU/ESP8266. These pins include Chip Enable pin (EN), Reset pin (RST) and WAKE pin.
•	EN: The ESP8266 chip is enabled when EN pin is pulled HIGH. When pulled LOW the chip works at minimum power.
•	RST: RST pin is used to reset the ESP8266 chip.
•	WAKE: Wake pin is used to wake the chip from deep-sleep.
•	 Control Pins are used to control the NodeMCU/ESP8266. These pins include Chip Enable pin (EN), Reset pin (RST) and WAKE pin.
•	EN: The ESP8266 chip is enabled when EN pin is pulled HIGH. When pulled LOW the chip works at minimum power.
•	RST: RST pin is used to reset the ESP8266 chip.
•	WAKE: Wake pin is used to wake the chip from deep-sleep.
4.3	Jumper Wires
Jumper wires are simply wires that have connector pins at each end, allowing them to be used to connect two points to each other without soldering. Jumper wires are typically used with breadboards and other prototyping tools in order to make it easy to change a circuit as needed.


 
4.4	IR Sensor
Infra-Red Sensor commonly known as IR Sensor is nothing but a combination of IR source and a light detector called photo diode and it work on principal of transmitting light and receiving it and comparing the received amount of light with the help of a comparator LM358. IR Sensors are commonly used in detecting object and obstacles; it can also detect color.

Figure 11:  IR sensor
4.5	Breadboard
A breadboard is a rectangular plastic board with a bunch of tiny holes in it. Most electronic components in electronic circuits can be interconnected by inserting their leads or terminals into the holes and then making connections through wires where appropriate. The breadboard has strips of metal underneath the board and connects the holes on the top of the board. A breadboard allows for easy and quick creation of temporary electronic circuits or to carry out experiments with circuit design. Breadboards enable developers to easily connect components or wires thanks to the rows and columns of internally connected spring clips underneath the perforated plastic enclosure.



 
4.6	Arduino UNO
Arduino UNO is based on an ATmega328P microcontroller. It is easy to use compared to other boards, such as the Arduino Mega board, etc. The board consists of digital and analog Input/Output pins (I/O), shields, and other circuits.

The Arduino UNO includes 6 analog pin inputs, 14 digital pins, a USB connector, a power jack, and an ICSP (In-Circuit Serial Programming) header. It is programmed based on IDE, which stands for Integrated Development Environment. It can run on both online and offline platforms.





o	ATmega328 Microcontroller- It is a single chip Microcontroller of the ATmel family. The processor code inside it is of 8-bit. It combines Memory (SRAM, EEPROM, and Flash), Analog to Digital Converter, SPI serial ports, I/O lines, registers, timer, external and internal interrupts, and oscillator.
o	ICSP pin - The In-Circuit Serial Programming pin allows the user to program using the firmware of the Arduino board.
 
o	Power LED Indicator- The ON status of LED shows the power is activated. When the power is OFF, the LED will not light up.
o	Digital  I/O  pins-  The  digital pins have the value HIGH or LOW.  The  pins numbered from D0 to D13 are digital pins.
o	TX and RX LED's- The successful flow of data is represented by the lighting of these LED's.
o	AREF- The Analog Reference (AREF) pin is used to feed a reference voltage to the Arduino UNO board from the external power supply.
o	Reset button- It is used to add a Reset button to the connection.
o	USB- It allows the board to connect to the computer. It is essential for the programming of the Arduino UNO board.
o	Crystal Oscillator- The Crystal oscillator has a frequency of 16MHz, which makes the Arduino UNO a powerful board.
o	Voltage Regulator- The voltage regulator converts the input voltage to 5V.
o	GND- Ground pins. The ground pin acts as a pin with zero voltage.
o	Vin- It is the input voltage.
o	Analog Pins- The pins numbered from A0 to A5 are analog pins. The function of Analog pins is to read the analog sensor used in the connection. It can also act as GPIO (General Purpose Input Output) pins.





4.7	Servo Motor SG90

Servo motors are devices that can rotate to a specific angle or position. They can be used to move robotic arms, steering wheels, camera gimbals, etc. Servo motors have three wires: power, ground and signal. The power wire is usually red and should be connected to the 5V pin on the Arduino board. The ground wire is usually black or brown and should be connected to a ground pin on the board. The signal wire is usually yellow or orange and should be connected to a PWM pin on the board.

A servo is generally composed of the following parts: case, shaft, gear system, potentiometer, DC motor, and embedded board.
 
 

 
CHAPTER 5 SOFTWARE REQUIREMENTS
5.1	Software implementation

The software required is the Arduino IDE.



5.2. Arduino IDE

The open-source Arduino Software (IDE) makes it easy to write code and upload it to the board. It runs on Windows, Mac OS X, and Linux. The environment is written in Java and based on Processing and other open-source software. This software can be used with any Arduino board. The Arduino development environment contains a text editor for writing code, a message area, a text console, a toolbar with buttons for common functions, and a series of menus. It connects to the Arduino hardware to upload programs and communicate with them. Software written using Arduino are called sketches. These Sketches are written in the text editor. Sketches are saved with the file extension.ino. It has features for cutting/pasting and for searching/replacing text. The message area gives feedback while saving and exporting and also displays errors. The console displays text output by the Arduino environment including complete error messages and other information. The bottom right-hand corner of the window displays the current board and serial port. The toolbar buttons allow you to verify and upload programs, create, open, and save sketches, and open the serial monitor.

 
5.3	Blynk

Blynk is a platform that allows to quickly build interfaces for controlling and monitoring the hardware projects from iOS and Android device. After downloading the Blynk app, we can create a project dashboard and arrange buttons, sliders, graphs, and other widgets onto the screen. There are three major components in the platform:

▪	Blynk App - allows to create amazing interfaces for projects using various widgets we provide.

▪	Blynk Server - responsible for all the communications between the smart phone and hardware.

▪	Blynk Libraries - for all the popular hardware platforms - enable communication with the server and process all the incoming and out coming commands.



5.4	Program EPS8266 NodeMCU with Arduino IDE

1.	From the Menu select |File|Preferences| (Picture 1)
2.	For the “Additional Boards Manager URLs”, in the "Preferences" dialog set one of the following:
If you want to use the stable release of the ESP8266 libraries: http://arduino.esp8266.com/stable/package_esp8266com_index.json
3.	If you want to use the latest staging version of
the ESP8266 libraries: http://arduino.esp8266.com/staging/package_esp8266co m_index.json

4.	Select the Board and Upload the code


 
5.5	Program Arduino UNO with Arduino IDE
1.	Download & install the Arduino environment (IDE) ...
2.	Launch the Arduino IDE. ...
3.	If needed, install the drivers. ...
4.	Connect the board to your computer via the USB cable. ...
5.	Select your board.
6.	Select your serial port.
7.	Upload the program.





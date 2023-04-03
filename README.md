# Arduino-RFID-Attendance

## INTRODUCTION

* This project aims to provide an efficient and secure way to record attendance in organizations, colleges, and schools using RFID technology. The traditional paper-based attendance system can be prone to errors and proxy attendance, but an RFID-based system can help eliminate these issues.

* This system is designed to be used at different educational institutions, corporate offices, government offices, and other organizations. It uses RFID tags attached to ID cards to uniquely identify each employee or student and record their attendance. The communication is wireless using electromagnetic and electrostatic coupling.

* The system is deployed using an Arduino Uno and other microcontrollers. It provides an effortless, quicker, and secure way to record attendance compared to the conventional method of signing on a paper. With this system, institutional authorities can easily monitor attendance and reduce the risk of errors and fraudulent activities.

This repository contains the source code and documentation for the RFID attendance system. 

## ABSTRACT

This project proposes an RFID-based attendance system as an efficient and secure alternative to traditional paper-based attendance systems. The system is designed to be used in various educational institutions, corporate offices, and government offices. It uses RFID tags attached to ID cards to uniquely identify each employee or student and record their attendance. The system is deployed using an Arduino Uno and other microcontrollers, and it communicates wirelessly using electromagnetic and electrostatic coupling. The system provides an effortless, quicker, and secure way to record attendance, reducing the risk of errors and fraudulent activities such as proxy attendance.

## COMPONENTS REQUIRED

* Arduino Uno R3 CH340G ATmega328p
* Mini Micro SD Card Reader Module 
* Tiny RTC Real Time Clock DS1307 I2C IIC
* Transparent 400 Points Solderless Breadboard 
* Ai Thinker ESP01S ESP8266 WiFi Module 
* Jumper cables

## COMPONENTS DESCRIPTION

 -**ARDUINO UNO**
 
 
This is a microcontroller board based on the ATmega328p microcontroller. It has 14 digital input/output pins, 6 analog inputs, and supports serial communication via USB. The CH340G chip is used to convert USB signals to serial signals, allowing it to communicate with the computer.



 -**Transparent 400 Points Solderless Breadboard** 

This is a breadboard that allows you to prototype electronic circuits without soldering. It has 400 points and a transparent design that makes it easy to see the connections.

 -**Jumper cables** 

These are cables with male-to-male, male-to-female, and female-to-female connectors that are used to connect the components together. They come in various lengths and colors to help keep the connections organize


## CIRCUIT DIAGRAM

<img src="https://github.com/kartik5106/Arduino-RFID-Attendance/blob/main/circut_diagram.png" width="800" height= "900">  

## FLOW CHART 

<img src="https://github.com/kartik5106/Arduino-RFID-Attendance/blob/main/flow_chart.png" width="800" height= "900">

## WORKING
This code uses an RFID module (MFRC522) to read RFID tags/cards and give access based on their UID. The UID of authorized cards is stored in the code and checked against the UID of the card that is scanned.

The code initializes the RFID module and sets up the pins for LED and buzzer. Then it enters the main loop where it checks if there is a new card present using the function mfrc522.PICC_IsNewCardPresent(). If a new card is not present, it displays a message on the LCD screen to show that the system is ready to scan a new card. If a new card is present, it reads the card's UID using mfrc522.PICC_ReadCardSerial(). The UID is then printed on the serial monitor and stored in a string variable 'content'.

Next, the code checks if the scanned card's UID matches the authorized UIDs stored in the code. If the UID matches, it displays a success message on the LCD, turns on a green LED, and beeps the buzzer. If the UID does not match, it displays an error message on the LCD, turns on a red LED, and beeps the buzzer.

The serial monitor is used to print the UID of the scanned card, as well as the name and ID of the authorized user who presented the card. This is useful for debugging and keeping track of who is accessing the system.

Overall, this code is a simple example of how to use an RFID module to control access to a system based on RFID tags/cards.

<img src="https://github.com/kartik5106/Arduino-RFID-Attendance/blob/main/serial_monitor.jpeg" width="800" height= "600">
This is a sample working of the project. 

## FUTURE SCOPE

This project can be further improved by adding features like a user interface for easy monitoring of attendance, integration with cloud-based systems for remote access to attendance data, and automatic notification to concerned authorities in case of absence or delay. The system can also be made more secure by implementing advanced encryption techniques to protect the attendance data from unauthorized access. Additionally, the system can be made more flexible by incorporating support for multiple RFID readers and customized check-in times for different groups of users. These enhancements can make the system more effective and user-friendly, providing better attendance management and monitoring capabilities for organizations and institutions.

## CONCLUSION

In conclusion, this program for an RFID attendance system provides an efficient and convenient way of taking attendance in educational institutions or organizations. The system uses an MFRC522 RFID reader, an SD card module, and an RTC DS1307 module to log the UID and the date and time of check-in for each employee or student. The system also checks if the user is late for check-in based on a predefined check-in time and displays a corresponding message and LED indicator.




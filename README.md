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




 -**Mini Micro SD Card Reader Module**
 
 This is a small module that allows you to read and write data to microSD cards. It has a built-in level shifter, so it can be used with both 3.3V and 5V systems.

 -**Tiny RTC Real Time Clock DS1307 I2C IIC**
 
This is a real-time clock (RTC) module that uses the DS1307 chip. It communicates via I2C and provides accurate timekeeping even when the power is off.


 -**Transparent 400 Points Solderless Breadboard** 

This is a breadboard that allows you to prototype electronic circuits without soldering. It has 400 points and a transparent design that makes it easy to see the connections.

 -**Ai Thinker ESP01S ESP8266 WiFi Module** 

This is a small WiFi module based on the ESP8266 chip. It can be used to connect the system to the internet and enable remote monitoring and control.

 -**Jumper cables** 

These are cables with male-to-male, male-to-female, and female-to-female connectors that are used to connect the components together. They come in various lengths and colors to help keep the connections organize


## CIRCUIT DIAGRAM

<img src="https://github.com/kartik5106/Arduino-RFID-Attendance/blob/main/circut_diagram.png" width="800" height= "900">  

## FLOW CHART 

<img src="https://github.com/kartik5106/Arduino-RFID-Attendance/blob/main/flow_chart.png" width="800" height= "900">

## WORKING
This is a program for an RFID attendance system that uses an MFRC522 RFID reader, an SD card module, and an RTC DS1307 module. The program reads the UID of a RFID tag when it is presented, logs the UID and the date and time to an SD card file named "DATA.txt", and checks if the user is late for check-in based on a predefined check-in time.

The program begins with the inclusion of the required libraries, which are MFRC522.h for the RFID, SPI.h for the RFID and SD card module, SD.h for the SD card, and RTClib.h for the RTC. The RFID reader's chip select and reset pins are defined as CS_RFID and RST_RFID, respectively. The SD card's chip select pin is defined as CS_SD. An instance of the MFRC522 class is created, and a String variable called uidString is defined to store the UID of the RFID tag. An instance of the RTC_DS1307 class is also created.

Next, the setup function initializes the serial port with a baud rate of 9600, initializes the SPI bus, and initializes the MFRC522 reader. The setup function also initializes the SD card module, and if initialization fails, an error message is printed. If initialization succeeds, a message indicating successful initialization is printed. The setup function also initializes the RTC and sets the date and time to the date and time the sketch was compiled. If the RTC is not running, an error message is printed.

The loop function continuously checks for new RFID cards using the PICC_IsNewCardPresent function. If a new card is detected, the readRFID function is called. The readRFID function reads the card's UID and stores it in the uidString variable. The logCard function is then called to log the UID and the date and time to the SD card and get the check-in time. Finally, the verifyCheckIn function is called to check if the user is late for check-in.

The readRFID function reads the UID of the RFID tag using the PICC_ReadCardSerial function. The function then concatenates the four bytes of the UID into a String variable called uidString. 

The logCard function first enables the SD card's chip select pin, opens the "DATA.txt" file in write mode, and checks if the file opened successfully. If the file opened successfully, the function prints the UID and the date and time to the file in the format "UID, YYYY/MM/DD, HH:MM". The function then prints the date and time to the serial monitor and closes the file. Finally, the function stores the check-in time in the userCheckInHour and userCheckInMinute variables. If the file did not open successfully, the function prints an error message to the serial monitor.

## FUTURE SCOPE

This project can be further improved by adding features like a user interface for easy monitoring of attendance, integration with cloud-based systems for remote access to attendance data, and automatic notification to concerned authorities in case of absence or delay. The system can also be made more secure by implementing advanced encryption techniques to protect the attendance data from unauthorized access. Additionally, the system can be made more flexible by incorporating support for multiple RFID readers and customized check-in times for different groups of users. These enhancements can make the system more effective and user-friendly, providing better attendance management and monitoring capabilities for organizations and institutions.

## CONCLUSION

In conclusion, this program for an RFID attendance system provides an efficient and convenient way of taking attendance in educational institutions or organizations. The system uses an MFRC522 RFID reader, an SD card module, and an RTC DS1307 module to log the UID and the date and time of check-in for each employee or student. The system also checks if the user is late for check-in based on a predefined check-in time and displays a corresponding message and LED indicator.




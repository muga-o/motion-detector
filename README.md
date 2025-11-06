PIR Motion Sensor LED Indicator
Project Overview
This project uses an Arduino Uno board to interface with a PIR (Passive Infrared) motion sensor. It detects motion and visually indicates the status using two LEDs — a red LED to indicate motion detected and a green LED to indicate no motion. The system is built on a breadboard for easy prototyping and testing.

Components Used
Component

Description

Arduino Uno

Microcontroller board to read sensor and control LEDs

PIR Motion Sensor

Detects infrared motion and outputs HIGH/LOW signal

Breadboard

To connect components without soldering

Red LED

Lights up when motion is detected

Green LED

Lights up when no motion is detected

220Ω Resistors

Current limiting resistors for LEDs

Jumper wires

Connect components and Arduino pins

Power Supply

Arduino powered via USB cable

Circuit Connections
Device

Arduino Pin / Breadboard Connection

PIR Sensor VCC

Arduino 5V pin

PIR Sensor GND

Arduino GND pin

PIR Sensor OUT

Arduino Digital Pin 2

Red LED Anode

Arduino Digital Pin 13 through 220Ω resistor

Red LED Cathode

Breadboard GND rail

Green LED Anode

Arduino Digital Pin 12 through 220Ω resistor

Green LED Cathode

Breadboard GND rail

Breadboard GND Rail

Connected to Arduino GND

How It Works
The PIR motion sensor continuously monitors for motion.
When motion is detected (digitalRead returns HIGH on pin 2), the Arduino turns ON the red LED (pin 13) and turns OFF the green LED (pin 12).
When no motion is detected (digitalRead returns LOW), the Arduino turns ON the green LED and turns OFF the red LED.
The system provides a visual indication of the current motion detection status.
Arduino Code
cpp
32 lines
Copy code
Download code
Click to expand
// Pin Definitions
const int pirPin = 2; // PIR sensor output pin
...
Usage Instructions
Build the circuit exactly as per the connections table above.
Upload the Arduino code to your Arduino Uno board using the Arduino IDE.
Open the Serial Monitor (baud rate 9600) to view real-time motion detection status messages.
Walk in front of the PIR sensor to trigger motion detection and observe the LED changes.
Troubleshooting Tips
Verify LED polarity: longer leg = anode (+), shorter leg = cathode (–).
Ensure resistors are properly connected in series with LEDs to prevent damage.
Confirm all grounds (GND) share a common connection.
Test the PIR sensor separately if motion is not detected.
Double-check wiring to Arduino pins (pin 2 for PIR, pins 12 and 13 for LEDs).
Use Serial Monitor output to help diagnose sensor detection issues.
Project Purpose and Applications
This project demonstrates a basic motion detection and indication system, useful for:

Security alarm prototypes
Automated lighting systems
Learning sensor interfacing with Arduino
Home automation triggers

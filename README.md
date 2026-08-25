# web-controlled-car
# Basic design:
A four wheeled car driven by four DC motors
The motors and wheels are neatly arranged inside the chassis and held in place via nuts and bolts and exposed keyed shafts as well as output shafts
The battery holder is mounted on top of the chassis kit, at the edge of the car with the motor driver and ESP32 expansion board next to it
The ESP32 is mounted on top of its expansion board
The ultrasonic sonar is attached on top of a servo motor at the other end of the chassis kit
The breadboard is placed in front of the ESP32 expansion board and behind the servo motor
Three red LEDs, a buzzer, three resistors, three four pin push buttons and and a light dependent resistor are connected to the breadboard
All the connections between the components are made using male to female jumper wires and male to male jumper wires
# Features: 
The car is connected to a web browser via wifi 
The web browser has buttons which can be clicked/tapped to allow the car to start moving, stop moving, travel left, right, backwards and forwards
The web browser also contains an automatic obstacle avoiding mode 
When switched on, the obstacle avoiding mode allows the car to move away from obstacles upon detecting them
The buzzer automatically switches on when an obstacle is detected by the ultrasonic sonar 
The car contains three LEDs which can be manually switched on and off using three four pin push buttons
The light dependent resistor automatically switches the three LEDs on when it detects low light intensities
The three LEDs are automatically switched off when the light dependent resistor detects high light intensities
The three resistors ensure that the circuit is safe and excess current does not flow through it
# Connections:
Motor wires and motor driver:
     -The two red wires of the two motors on the right to output-3 of the motor driver
     -The two black wires of the two motors on the right to output-4 of the motor driver
     -The two black wires of the two motors on the left should to output-1 of the motor driver
     -The two red wires of the two motors on the left should to output-2 of the motor driver
Motor driver and ESP32: 
     -IN1 to GPIO14
     -IN2 to GPIO27
     -IN3 to GPIO26
     -IN4 to GPIO25
     -ENA to GPIO33
     -ENB to GPIO32
     -5V terminal to 5V pin
     -GND terminal to GND pin
Ultrasonic sensor and ESP32:
     -VCC to 5V
     -TRIG to GPIO4
     -ECHO to GPIO5
     -GND terminal to GND pin
Servo motor and ESP32:
     -Yellow wire to GPIO13
     -Red wire to 5V pin
     -Brown wire to GND
Battery holder and motor driver:
     -positive wire to 12V IN
     -negative wire to GND
Buzzer and ESP32:
     -positive terminal to D23
     -negative terminal to GND
Buttons and ESP32:
     -Button-1 to GPIO12 and GND 
     -Button-2 to GPIO13 and GND
     -Button-3 to GPIO14 and GND 
LEDs and ESP32:
     -LED-1 to GPIO25
     -LED-2 to GPIO26
     -LED-3 to GPIO27
LDR and ESP32:
     -one end of LDR to 3V 
     -opposite end of LDR to GND
     
# Why it follows all the rules:

Mechanical and actuation:
1. Even though it is web operated, it can still move about automatically when the automatic obstacle avoiding mode is switched on
2. The DC motors are used to allow the wheels to move. The mini servo motor allows the ultrasonic sensor to rotate and enables it to detect obstacles. 
3. We will design a basic model of the project using fusion and upload it to GitHub
4. We will make the project as close to the model as possible 

Embedded system+IOT:
1. The code will enable the robot to both be controlled remotely via a web browser and also automatically. Moreover, it automatically switches the LEDs on when the light intensity is low. And it automatically starts a buzzer when it encounters an obstacle. 
2. The car will have its own power source
3. Ultrasonic sensors will detect obstacles whereas  an LDR detects light intensity
4. The car has three buttons which can be used to turn the LEDs on and off 
5. The car will be powered by batteries
6. A buzzer starts the moment the car detects an obstacle and LEDs turn on the moment the light intensity detected by the LDR is low
7. The entire car can be controlled via a web browser

Rules and bans:
1. This project does not contain any sharp objects/weapons
2. The power source has a maximum voltage of 11.1 V




 

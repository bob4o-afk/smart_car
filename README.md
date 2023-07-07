# Smart Car Obstacle Avoidance

This GitHub repository contains the code for a smart car that can autonomously navigate and avoid obstacles. The car is controlled using an Arduino board and various external components.

## Features
- Uses ultrasonic sensors to detect obstacles and determine their distance.
- Utilizes four DC motors to control the movement of the car.
- Implements a servo motor for the rotation of the ultrasonic sensor.
- Employs the Adafruit Motor Shield library to control the DC motors.
- Requires the installation of the NewPing and Servo libraries.

## Hardware Requirements
- Arduino board
- Adafruit Motor Shield
- Ultrasonic sensor
- DC motors (4)
- Servo motor

## Installation
1. Install the necessary libraries by following these steps:
   - Download the AFMotor library from [Adafruit Motor Shield Library](https://learn.adafruit.com/adafruit-motor-shield/library-install) and add it to the Arduino IDE.
   - Download the NewPing library from [Arduino-NewPing](https://github.com/livetronic/Arduino-NewPing) and add it to the Arduino IDE.
   - Download the Servo library from [arduino-libraries/Servo](https://github.com/arduino-libraries/Servo.git) and add it to the Arduino IDE.
2. Connect the Arduino board to the required hardware components (DC motors, servo motor, and ultrasonic sensor) based on the provided pin connections in the code.
3. Upload the code to the Arduino board.

## Usage
1. After uploading the code, the smart car will perform an initialization process.
2. Once initialized, the car will continuously monitor the environment for obstacles.
3. When an obstacle is detected within 15 centimeters, the car will stop and initiate the obstacle avoidance routine.
4. The car will move backward for 300 milliseconds, then stop for 200 milliseconds.
5. The ultrasonic sensor will rotate to the right and left to determine the distances in those directions.
6. Based on the detected distances, the car will turn right or left to avoid the obstacle.
7. If no obstacle is detected within 15 centimeters, the car will move forward.

## Note
- Adjustments to the maximum speed and distance thresholds can be made by modifying the corresponding constants in the code.
- Additional customization can be done by modifying the motor control and sensor rotation routines.

Feel free to contribute to this repository by adding enhancements or addressing any issues you encounter. Enjoy building your own smart car that can navigate through obstacles autonomously!
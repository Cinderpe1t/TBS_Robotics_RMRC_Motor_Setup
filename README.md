# TBS_Robotics_RMRC_Motor_Setup
TBS Robotics RMRC 2022 Motor Setup
## Items to prepare
- Laptop
- Servo motor (Robotics Dynamixel XL430-W270-T)
- U2D2
- U2D2 power hub
## Type of motors
### DC motor
Pure electro-magnetic motor
### Step motor
- Control rotation by going through step(s)
- No encoder - can miss a step
### Servo motor
- Each motor has motor, gear(s), encoder, and controller (a small computer)
- Internal control to achieve control goals
- Position mode vs. velocity mode
- Communicate with controller through serialized data packets
### Learn more
https://learn.adafruit.com/adafruit-motor-selection-guide
## Motor control with Raspberry Pi
- Use motor control hat over RPi
- Controls large current provided to motor(s)
- For DC motor: Pulse Width Modulation to control amount of current, and speed as a result
- For stepper motor: step rotation signal is provided
- Good documentation for RPi: https://learn.adafruit.com/adafruit-dc-and-stepper-motor-hat-for-raspberry-pi
### Motor control with Arduino
- https://learn.adafruit.com/adafruit-arduino-lesson-13-dc-motors
- https://learn.adafruit.com/adafruit-arduino-lesson-16-stepper-motors 
- https://learn.adafruit.com/adafruit-arduino-lesson-14-servo-motors
### Servo motor system of our choice
- Robotis Dynamixel XL430-W270-T, https://www.robotis.us/dynamixel-xl430-w250-t/
- U2D2: USB controller to exchange data with servo motor(s), https://www.robotis.us/u2d2/ 
- U2D2 Power Hub Board Set: motor power driver, https://www.robotis.us/u2d2-power-hub-board-set/
- ROBOTIS has good eManual documents, drivers, CAD drawing and file, etc
### Set up DYNAMIXEL Wizard
- Manual: https://emanual.robotis.com/docs/en/software/dynamixel/dynamixel_wizard2/
- Download Wizard: http://en.robotis.com/service/downloadpage.php?ca_id=10
- Connect U2D2 to computer laptop USB port
- Connect power source (DC adapter or 8x 1.5V battery pack) to U2D2 power hub
- Connect servo motor and power hub using Robot Cable X3P
- Connect single servo motor for the first test
- Confirm motors power on red LED light is on
### Servo motor test drive with DYNAMIXEL Wizard 2.0 
- Search motor
  - Make sure the motor has the latest firmware installed first
  - Need to scan all protocol, all speed and ID’s if motor is not easily found
- Upgrade firmware
- Detect or assign ID
- Setup communication data rate speed (baud rate, or bit rate)
- Test drive operations
- Assign design-specific and unique ID number to each servo motor for later programming
### Understand servo motor control
- Study servo motor manual at https://emanual.robotis.com/docs/en/dxl/x/xl430-w250/
- Q: What is EEPROM?
- Q: how can we set a motor to keep a position? What is the unit of position in angle?
- Q: how can we set a motor to keep a constant rotation?
- Q: how can we run a motor backward?
- Q: how can we know motor’s actual speed?
- Q: how can you read motor’s error message?
- Q: how can you recover the motor from error or fail status?




# FireBeetle Covers-DC Motor&Stepper Driver
<img width="442" height="523" src="https://raw.githubusercontent.com/DFRobot/binaryfiles/master/DFR0508/DFR0508svg1.png"/>

## DFRobot_Motor Library for Arduino
---------------------------------------------------------

This library is used to control dc motors and stepper motors.Including positive spin, reverse, speed adjustment, stop control


### Open dc motor and stepper motor drive hardware, read the information.
   
    void init();
	
### Turn off dc motor and stepper motor drive hardware
   
    void shutdown();
	
### Motor stop rotation
   
    void stop();
	
### The dc motor sets the direction and begins to rotate
	
	void start(uint8_t dir);
	* This function can be used to start the motor
	* dir: Set Orientation       CW or CCW
	
### Step motor rotation Angle, speed, direction control, And it starts spinning.
	
	void start(float angle, uint16_t speed, uint8_t dir);
	* This function can be used to start the motor
	* angle: Set the Angle       Min:0°(If the Angle is equal to 0°,The motor will not stop spinning)
	* speed: Set the speed       Min:8
	* dir: Set Orientation       CW or CCW
		
### Speed control of dc motor and stepper motor

	void speed(uint16_t val);
	* This function is used to set the motor speed
	* val: Set the speed       motor:0<=val<=4096  stepper:8<=val
	
### Obtain current motor rotation direction
	
	getDir();

## Compatibility

MCU                | Tested Works | Doesn't Work | Not Tested  | Notes
------------------ | :----------: | :----------: | :---------: | -----
FireBeetle-ESP32  |      X       |             |            | 
FireBeetle-ESP8266  |      X       |             |            | 
FireBeetle-BLE4.1 |      X       |             |            | 
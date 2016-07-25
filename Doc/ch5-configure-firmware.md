# Configure and Compile Marlin Firmware

So you have assembled your hardware and wired your electronics. Now you need to program the firmware in to RAMPS electronics to bring it to life. In this how to make guide we will see how to configure, compile and program Marlin firmware into RAMPS electronics. 

##Download Marling Firmware 

Firmware is the software that will run inside the RAMPS elections, though there are many firmwares like Repetier, Marlin, etc. We will use Marlin firmware for our Guide. 

- Download Marlin from [https://github.com/MarlinFirmware/Marlin](https://github.com/MarlinFirmware/Marlin)
- Select the ***Download Zip*** button on the right side of the screen.
- Unzip the Zip file

   
##Configure Marlin Firmware for RAMPS and Prusa i3

To get started with Customizing and Configuring Marlin for RepRap Prusa i3 3D Printer, use these general configuration as a starting point and fine tune the setting until you get best prints. 

In the extracted source, open Marlin/Configuration.h file with editor

### Set the baudrate

```
#define BAUDRATE 115200
```

###Set the MOTHERBOARD define to RAMPS

This will configure the RAMP boards with 1xExtruder, 1xFan, 1xBed, see Marlin/boards.h file for more configuration

```
#ifndef MOTHERBOARD
#define MOTHERBOARD BOARD_RAMPS_13_EFB
#endif
```

###Set Name and UUID (Optional)

This is optional, uncomment and set below defines values
```
#define CUSTOM_MENDEL_NAME "Prusa i3"
#define MACHINE_UUID "12941deb-3b62-4c18-8d53-10fcd7338bf3"
```

###Set no. of extruder's

This defines the number of extruders

```
#define EXTRUDERS 1
```

###Set the thermistor

```
#define TEMP_SENSOR_0 11
#define TEMP_SENSOR_1 0
#define TEMP_SENSOR_2 0
#define TEMP_SENSOR_BED 11
```

###Set MAX temperature limits

When temperature exceeds max temp, your heater will be switched off. This feature exists to protect your hotend from overheating accidentally, but *NOT* from thermistor short/failure!. You should use MINTEMP for thermistor short/failure protection.

```
#define HEATER_0_MAXTEMP 230
#define HEATER_1_MAXTEMP 230
#define HEATER_2_MAXTEMP 230
#define BED_MAXTEMP 150
```

###Set PID values

Later you can recalculate the values by running PID tuning

```
#define DEFAULT_Kp 26.88
#define DEFAULT_Ki 1.57
#define DEFAULT_Kd 114.95
```

###Endstops settings
Sets direction of endstops when homing; 1=MAX, -1=MIN

```
#define X_HOME_DIR -1
#define Y_HOME_DIR -1
#define Z_HOME_DIR -1
```

### Set the direction of XYZ and E axis Stepper Motor

```
#define INVERT_X_DIR true
#define INVERT_Y_DIR false
#define INVERT_Z_DIR true
#define INVERT_E0_DIR false
```

### Travel limits after homing

```
#define X_MAX_POS 200
#define X_MIN_POS 0
#define Y_MAX_POS 200
#define Y_MIN_POS 0
#define Z_MAX_POS 200
#define Z_MIN_POS 0
```

###Feedrate and acceleration settings

```
#define HOMING_FEEDRATE {50*60, 50*60, 2.5*60, 0} // set the homing speeds (mm/min)

#define DEFAULT_AXIS_STEPS_PER_UNIT {80, 80, 4000, 100.52} // steps per unit for Solid Cube Direct Drive Extruder
#define DEFAULT_MAX_FEEDRATE {500, 500, 2, 25} // (mm/sec)
#define DEFAULT_MAX_ACCELERATION {4000,4000,100,1000} // X, Y, Z, E maximum start speed for accelerated moves.


#define DEFAULT_ACCELERATION          1000    // X, Y, Z and E max acceleration in mm/s^2 for printing moves
#define DEFAULT_RETRACT_ACCELERATION  3000   // X, Y, Z and E max acceleration in mm/s^2 for retracts
```

###Jerk values
```
#define DEFAULT_XYJERK                20.0 // (mm/sec)
#define DEFAULT_ZJERK                 0.4     // (mm/sec)
#define DEFAULT_EJERK                 2.0    // (mm/sec)
```

## Download and Install Arduino IDE

Since Arduino is a popular board we will not go detail into this topic, there are plenty of articles, how to, youtube video, books, etc. just do a google and find it yourself. 

- [Download the Arduino IDE](https://www.arduino.cc/en/Main/Software)
- [Arduino - Getting Started](http://arduino.cc/en/Guide/HomePage)

## Program Marlin firmware to the RAMPS

- Start Arduino IDE
- Open file **Marlin/Marlin.ino** in Arduino IDE, then press compile and upload button in the IDE tool bar.

Wait till the Marlin firmware is uploaded
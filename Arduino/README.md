### Arduino
Consider the following setup: a joystick lever is connected on the pin A2 of an Arduino Uno board, which is connected on the Serial port with a servomotor. The Arduino board controls the position of the motor using the position of the joystick (when the joystick is in its lowest position the motor is in the lowest position and vice versa). The board communicates with the motor on the Serial port with a baud rate of 19200 Baud using the following protocol: the board sends a byte which represent an instruction and then the parameter on two bytes. 

Write a complete Arduino sketch, named `MotorArduino.ino` which implements the control of the servomotor. The board should sample the value of the joystick with with a period of 100 ms. The joystick produces a low voltage to the board when it is in its lowest position. The instruction code, limit positions of the servomotor and the codec used for the position can be obtained by the following image:

![Motor Goal position](image.png)

To test your sketch we provided an implementation of some Arduino functions. To compile your sketch you will need a posix environment, gcc/g++ and make (on Windows we suggest using WSL or a Virtual Machine). 

Run `make` in the directory containing the makefile to obtain the executable `motorMain`. If it crashes it means that some requirements are not met. If your code satisfies all the requirements you will see the following positions 818, 818, 818, 788, 758, 743, 728, 665, 593, 511, 511, 511, 511, 593, 638, 668, 758, 788, 818, 818




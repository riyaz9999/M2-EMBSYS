
# High Level Requirements
HLR1 : The sensor Detects the light intensity and also the speed velocity and automatically sends the input to the MCU - Implemented.

HLR2 :This process continues till the sensor on vehicle is in affinity of sheet. But as the vehicle crosses the sheet the intensity of light on LDR increasys hence resistance of LDR decreases hence LDR will not be able to send signals of adequate strength to controller. So the controller stops counting.The microcontroller has a default value of count pre-define on it with the help of programming. Now as soon as microcontroller stops counting it start its another function i.e comparing the practical count to default count. When controller start comparing the practical count to default count, there exist two conditions

HLR3 : Condition 1- default count <practical count
Then the speed of vehicle is more.
Condition 2-default count > practical count
Then the speed of vehicle is normal.In condition 1, since the speed of vehicle is more than anticipated, speed of vehicle need to be lowered down.In order to control the speed of vehicle, the controller signify either by continuous beep or any other mean to driver, if driver doesn't respond then controller take over the control from driver and it automatically neutralizes the speed of vehicle with the help of PWM in atmega16 AVR controller. After some duration of time controller automatically resets.
In condition 2, since the speed of vehicle is normal so there is no need to control the speed by controller. We need to install two or more than two sheets if the accident prone area are in quick succession in order to prevent the further loss by accidents. In this model we can add Ultra sonic sensors in front of car in order to prevent collision of vehicles and control its speed due to brakers or any other obstacles.

# Low Level Requirements
LLR1: when sensor detects the light and approch signals the controller gets stopped -Implemented.

LLR2: Sometimes the speed doesnt change for itself and can cause problems - Implemented.

LLR3: Accidents do happen even with precautions unless some applications need to be installed- Implemented.
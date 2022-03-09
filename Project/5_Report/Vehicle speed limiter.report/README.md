## VEHICLE SPEED LIMITER

## Table of Contents

# 1.0 Introduction.

# 2.0 Requirements

# 2.1 Swot Analysis

# 2.2 Components Used In Solar Tracker

# 2.3 5w's And 1H

# 2.4 Table Of Requirements.

# 3.0 Architecture.

# 4.0 Simulation and Output.

# 5.0 Advantages and Usage.

# 6.0 Applications and Scope.

# 7.0 Conclusion.

# VEHICLE SPEED LIMITER-

A speed limiter is an Intelligent speed assistance (ISA) system that prevents a car from travelling over a set speed. This is not the same concept as cruise control as the car does not maintain this set speed. The driver can still use the accelerator, but the speed limiter prevents the car from going faster if the car reaches the limited speed.
A speed limiter is a governor used to limit the top speed of a vehicle. For some classes of vehicles and in some jurisdictions they are a statutory requirement, for some other vehicles the manufacturer provides a non-statutory system which may be fixed or programmable by the driver.

# WORKING 

A sheet is being placed on left side of road in traffic prone areas like schools. colonies, hospitals, four ways etc. This is an ordinary sheet which is being made up of any material like aluminum, plastic etc, beside being used in this project this sheet can be utilized for commercial purposes as any brand can commercialize their product through advertisement on it. The length of sheet is taken in such a way that the vehicle of any size is able to cross it easily.The vehicle has IR sensor and controller installed on it. The IR sensor is installed on left side of the car. It sends Infrared signals which strikes the sheet and gets reflected back to the LDR in IR sensor, now the resistor of LDR increases and sends some values to microcontroller. The microcontroller automatically converts these signals into Digital signals and if controller receives a signal of adequate intensity only then it will start counting.

# HIGH LEVEL AND LOW LEVEL REQUIREMENTS

# HIGH LEVEL REQUIREMENTS.
* RF Module Transmitter.
* Atmega  Microcontroller.
* RF receiver ,DC motor.
* Motor driver IC.
* 9V Battery.
* Transformer,Rectifier,Regulator.

# LOW LEVEL REQUIREMENTS.
* Diode.
* Antenna.
* Switch.
* Decoder and encoder.

# COMPONENTS REQUIRED

* HARDWARE:
IR sensor
L293D
Atmega 16 (microcontroller)
Line Follower Robot
DC Motors
AVR programmer

* SOFTWARES:
BASCOM AVR 
PROTEUS
AVR loader
USB ASP driver

# 5 w's and 1H:
* WHO:
  Almost every person can have an access to use these speed controllers in their own vehicles ,This is mainly used by the police department to check the limitations of the speed of a particular vehicle and this note downs the reading and automatically detects the speed and sends a warn alarm.Although most vehicles come with a built-in speed limiter, you will need to remove it if you want to replace it with an aftermarket device that further reduces speed.

* WHAT:
  A speed limiter is an Intelligent speed assistance (ISA) system that prevents a car from travelling over a set speed. This is not the same concept as cruise control as the car does not maintain this set speed. The driver can still use the accelerator, but the speed limiter prevents the car from going faster if the car reaches the limited speed.

* WHEN:
  Vehicle speed limiters are used in the vehicles ,they are commonly used during to check the speeds of their cars when given to others or to take the safety measures of their own children or themselves.Plan well ahead before overtaking. Be aware that a speed limiter may cause you difficulties when overtaking another vehicle, particularly when climbing a hill.\

* WHY:
  Speed limiters are being implemented in the hope that they will revolutionise road safety. The European Transport Safety Council (ETSC) says the limiters would reduce collisions by 30%, and save around 25,000 lives within 15 years . All vehicles in the EU would be fitted with ISA systems to stop drivers from breaking the speed limit. This relieves drivers from having to constantly check their speedometer and means you are less likely to speed and receive penalty points or fines. Moreover, it is thought that these measures will result in benefits for drivers, including higher fuel efficiency, a reduction in CO2 emissions and lower insurance premiums.

* WHICH:
  In all the recent cars the limiters have been as in-built functions from the company,Many recent Ford, Mercedes-Benz, Peugeot and Renault models already use ISA systems. Volvo will be the first manufacturer to implements ISA systems in all of their car models.

* HOW:
  Put simply, sensors in your car detect how fast you are going, then this information is communicated to the engine’s computer. When the pre-determined speed is met, the computer restricts the flow of fuel and air to the engine. Therefore, as a driver, you will not be able to exceed the pre-determined top speed. However, all speed limiters can be overridden. If there is a need to speed up quickly, pushing down hard on the accelerator will work. Further, it should be made clear that this system does not affect the car’s braking system.

  # SWOT ANALYSIS

# STRENGTHS:
* Reduced travel time and Time efficient.
* Equitable allocation of road space policy can be implemented.
* Smooth flow of traffic.
* Decrease the percentage of accidents and brings awareness.

# WEEKNESS:
* An internal electrical fault may occurs.
* Transmission problems.
* Monitaring may be incomplete.
* Limited speed range operations.

# OPPORTUNITIES:
* Prevents vehicle to go for over speed.
* Technology gets matured enough and comes to excistance.
* Control of theoritical research may provide more efficient terms and advantages.

# THREATS:
* Delay in adaptation.
* Cost management.
* Inattention and poor mapping.
* Variance happens and production of older motors gets decreased.

# IMPLEMENTATION:

This process continues till the sensor on vehicle is in affinity of sheet. But as the vehicle crosses the sheet the intensity of light on LDR increasys hence resistance of LDR decreases hence LDR will not be able to send signals of adequate strength to controller. So the controller stops counting.The microcontroller has a default value of count pre-define on it with the help of programming. Now as soon as microcontroller stops counting it start its another function i.e comparing the practical count to default count. When controller start comparing the practical count to default count, there exist two
conditions:
Condition 1- default count <practical count
Then the speed of vehicle is more.
Condition 2-default count > practical count
Then the speed of vehicle is normal.In condition 1, since the speed of vehicle is more than anticipated, speed of vehicle need to be lowered down.In order to control the speed of vehicle, the controller signify either by continuous beep or any other mean to driver, if driver doesn't respond then controller take over the control from driver and it automatically neutralizes the speed of vehicle with the help of PWM in atmega16 AVR controller. After some duration of time controller automatically resets.
In condition 2, since the speed of vehicle is normal so there is no need to control the speed by controller. We need to install two or more than two sheets if the accident prone area are in quick succession in order to prevent the further loss by accidents. In this model we can add Ultra sonic sensors in front of car in order to prevent collision of vehicles and control its speed due to brakers or any other obstacles.

# APPLICATIONS:

* Alert the nearby police department or the caretaker.
* These can be used in all the types of motor vehicles like bus,lorry,motor bikes and all the cars.
* They can more generally be used to limit the rotational speed of the internal combustion engine or protect the engine from     damage due to excessive rotational speed.
* The governor is a device which is used to controlling the speed of an engine based on the load requirements. Basic governors sense speed and sometimes load of a prime mover and adjust the energy source to maintain the desired level.
* It helps in safe guarding the passengers and also doesnt allow the vehicle to cross the high speed level.

# ADVANTAGES:

* To avoid accidents.
* To maintain maileage.
* Improved fuel efficieny.
* Reduced emissions.

# DIS ADVANTAGES:

* Unintended safety consequences.
* Incresed congestion.
* Loss of profit for small owning operators.
* There are also concerns that speed-limiting technology might lead to added congestion, and the introduction of black-box style data recorders represents a loss of civil liberties.

# CONCLUSION:

Usually people drive very harshly in heavy traffic prone areas as they are in a hurry. but in that hurriedness they often end in loosing either their life or someone other life on road. Our project is based on "Automatic Vehicle Speed Control System", so it has a great significance in termination and reduction of overall accidents and casualties in high traffic prone areas. This project has a system that checks the speed of the vehicle using IR sensors and microcontroller and sends warning signals to driver to lower down the speed if speed is on higher side. Incase driver don't reduce the speed then within seconds our system
will take over the control and will reduce ate speed of vehicle automatically.Hence this project is a great life saving system in heavy traffic areas.

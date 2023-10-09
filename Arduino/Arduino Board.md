*Microcontroller development board, designed to be taken advantage of all the features of a microcontroller*

### **[Components]**
##### [[Microcontroller]]
- Most important component, takes the code -> logic (input -> code -> output) 
![[Pasted image 20231003145047.png]]
##### [[Pins]]
- to be inputs and outputs
- General Purpose Input/Output
- output - adjusting/applying the voltage from the pin
- input - reading the voltage applied to the pin

##### **[[Headers]]**
- each hole makes an electrical connections to the pins to the microcontroller
- you can use wires/components on it
- people often use a breadboard so the wires wont have to be arranged

##### **[[Binary Inputs/pins above]]**
- pin headers labelled with 0-13
- can be used for reading on/off inputs ( button pressed or not), Binary input
- can also act as outputs, can source voltage depending on the number, if u set pin high it will source the volt, can light up devices/leds/buzzers etc
- 0-1, used for communication for usb port (TX,RX) : transmit,receive
- ~ pins capable of pulse modulation : can set voltage high/low at different frequencies 

##### **[[Lower pins]]**
- analog input: has analog to digital converter, useful for sensors like temperature sensors/light sensors. can be used to read the variable voltage and convert it to temperature
- power section:
	- gnd (ground, small voltage)
	- use this for small components which draw not too much currents

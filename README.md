Food Temperature and Humidity Monitoring Using Arduino (Data Aggregation)
1) Data Aggregation
Data aggregation is any process in which information is gathered and expressed in a summary form, for purposes such as statistical analysis

 *Data Aggregation concept*

 Basic Introduction
A project is all about the concept of Data Aggregation.concept is to collect the data from different sensor and give it to controller. first you have to set the sensor value range. because if the sensor value goes high or low compare to set value is has to give some signal this signal is warning to the main server so that the quality is product remain same.for example:if you have one medicine that required 30ºC temperature and 50%RH humidity for that you have to maintain required temp and humidity.for that i build this project which measure the range according you set the ranges.if any value goes high or low it gives warning ths is the concept of Data aggregation 
<img width="423" height="281" alt="image" src="https://github.com/user-attachments/assets/86185d77-89bf-4dac-9054-3cc67312b76f" />

Step 1: Interfacing Humidity Sensor DHT11 to Arduino
<img width="1024" height="561" alt="image" src="https://github.com/user-attachments/assets/1f500ef7-1810-4ab8-bdef-ce91f997216f" />

DHT11 Temperature & Humidity Sensor features a temperature & humidity sensor complex with a calibrated digital signal output.it ensures high reliability and excellent long-term stability.This sensor includes a resistive-type humidity measurement component and an NTC temperature measurement component.extremely accurates,small size, low power consumption.Measurement Range:20-90%RH and 0-50 ℃.DHT11 power supply is 3-5.5V DC Download dht11 data sheet     dht11 lib for arduino

<img width="549" height="305" alt="image" src="https://github.com/user-attachments/assets/42474ae3-94d1-4903-b198-8513d2f2cbc7" />

Step 2: Interfacing Keypad to Arduino

<img width="565" height="685" alt="image" src="https://github.com/user-attachments/assets/ed47c505-5a60-44e0-9397-36e286778c4e" />

Matrix Keypad – reducing the pins from 8 digital to 1 analog on Arduino                         #include
#define analogPin 0
AnalogMatrixKeypad AnMatrixKeypad(analogPin);
void setup(){
Serial.begin(9600);
}
void loop(){
char Key = AnMatrixKeypad.readKey();
if(Key != KEY_NOT_PRESSED)
Serial.println(Key);
}

Step 3: Interface (16*2) LCD to Arduino
<img width="1024" height="566" alt="image" src="https://github.com/user-attachments/assets/1eeb59b3-d079-4d45-a30d-9cd250b1c6f2" />
The LiquidCrystal library allows you to control LCD displays that are compatible with the Hitachi HD44780 driver. There are many of them out there, and you can usually find them by the 16-pin interface.  
Pin 1 to Arduino GND
Pin 2 to Arduino 5V
Pin 3 to GND
Pin 4 to Arduino pin 12
Pin 5 to Arduino GND
Pin 6 to Arduino pin 11
Pin 11 to Arduino pin 5
Pin 12 to Arduino pin 4
Pin 13 to Arduino pin 3
Pin 14 to Arduino pin 2

Step 4: FINAL DATA OF PROJECT 
here is the final data of project it gives A final code and data just watch it and do your project..the .rar file also has the proteus semulation of project and all data of project. one thing keypad sometimes not work properly. and the simulation is perfect only dht11 not working in proteus it work on hardware. the problem behind this i dont no. i try all the possibility but it not work on proteus. project data




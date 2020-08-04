# COMBAT BOTS --- RC ADDON BOARD

##DESCRIPTION
  This code reads the PWM pulse width time coming from channel 1 and channel 2 of the RC receiver,
  then mixes it so that a single joystick can be used to drive a 2 wheeled robot in all directions.
 
##  Pinouts:
 ### Motors: - (This is where the pins go on-board the Combat Bot PCB)
 ```
  Motor 1 - A --> Pin D9  (PB1)
  Motor 1 - B --> Pin D10 (PB2)
  Motor 2 - C --> Pin D5  (PD5)
  Motor 2 - D --> Pin D6  (PD6)
```
###  RGB Pinout: - (This is where the pins go on-board the Combat Bot PCB)
```
  GND --> GND
  RGB --> D4 (PD4)
  +5V --> +5V
  ```

###  2 Channel RC Receiver Input: -
```
  Channel 1 --> D2 (PD2)
  Channel 2 --> D3 (PD3)
  ```

###  Onboard Programming Header: - (This is where the pins go on-board the Combat Bot PCB)
```
  GND  --> GND
  +5V  --> +5V
  CS   --> RST (PC6) Reset
  SCK  --> D13 (PB5)
  Miso --> D11 (PB4)
  Mosi --> D12 (PB3)
  ```

  Programming the PCB can be done by using an Arduino as an isp with the following connections: -

###  Combat PCB    -->   Arduino ISP Programmer
```
         GND  --> GND
         +5V  --> +5V
         CS   --> D10
         SCK  --> D13
         Miso --> D12
         Mosi --> D11
```

  You will also need to add the following URL to the additional Boards Manager URLs List:
 > https://raw.githubusercontent.com/carlosefr/atmega/master/package_carlosefr_atmega_index.json
  Then go to Tools > Board > Board Manager and search for Barebones ATmega chips. Select it and install.
  
  This is a set of config files by Carlos Rodrigues that lets you program a bare MCU without a bootloader or external clock.
  More information can be found here: https://github.com/carlosefr/atmega
  
 ### HOW TO PROGRAM:
  ```
  1)To program the Combat bot pcb you will first need to upload the ARDUINO AS ISP sketch to an arduino uno or nano
  2)Then connect the Arduino to the COMBAT BOT PCB as described above in the programming pinout list.
  3)Under Tools, Change the Board to the new ATMega328/328P option.
  4)Under Tools, Change the Processor to ATMega328p
  5)Under Tools, Change the clock in Internal 8Mhz
  6)Under Tools, Change the Port to the port your arduino is connected to
  7)Under Tools, Change the Programmer to "Arduino as ISP"
  8)Hit Upload and it should then program.
```
 Code and PCB Creator
 by :- Jake Gibson Shaw-Sutton


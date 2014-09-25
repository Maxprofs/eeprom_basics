ssd1306-accelerometer-with-eeprom
============
http://elegantcircuits.com/2014/09/24/reading-and-writing-to-the-avr-eeprom/

A digital accelerometer which measures and displays to the screen the values of accelration in the X, Y and Z axes. Values to be stored in EEPROM 

Runs on Atmega328P AVR Microcontroller at 8MHz (CLKDIV 8 fuse disabled for quicker refresh)

CLK = 8MHZ
avrdude -p atmega328p -P /dev/ttyUSB0 -c avrisp -b 19200 -B 1 -U lfuse:w:0xe2:m -U hfuse:w:0xd9:m -U efuse:w:0xff:m 

Enable CKDIV8 fuse
avrdude -p atmega328p -P /dev/ttyUSB0 -c avrisp -b 19200 -B 1 -U lfuse:w:0x62:m -U hfuse:w:0xd9:m -U efuse:w:0xff:m 

# Arduino_ILI9327_TFT_3.0in
Connect
LCD to STM32F103C8T6
CS > PB8
RS > PB0
WR > PB1
RD > PB7

D0 > PA0
D1 > PA1
D2 > PA2
D3 > PA3
D4 > PA4
D5 > PA5
D6 > PA6
D7 > PA7

TouchScreen
XP=PA6
XM=PB0
YP=PB1
YM=PA7

-----------------------------------------------------------------------------------------------------------
mcufriend_shield.h

#elif defined(ARDUINO_GENERIC_STM32F103C) || defined(ARDUINO_BLUEPILL_F103C8) || defined(ARDUINO_BLUEPILL_F103CB)
#STM32F103C8T6

|D7 |D6 |D5 |D4 |D3 |D2 |D1 |D0 | |RD |WR |RS |CS |RST| //LCD pins     

|PA7|PA6|PA5|PA4|PA3|PA2|PA1|PA0| |PB7|PB1|PB0|PB8|PB9| //STM32 pin 

#include <MCUFRIEND_kbv.h>
MCUFRIEND_kbv tft;       // hard-wired for UNO shields anyway.
#include <TouchScreen.h>

char *name = "Please Calibrate.";  //edit name of shield
const int XP=PA6,XM=PB0,YP=PB1,YM=PA7; //ID=0x9327
const int TS_LEFT=894,TS_RT=128,TS_TOP=915,TS_BOT=80;

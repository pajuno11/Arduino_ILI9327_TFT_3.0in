# Arduino_ILI9327_TFT_3.0in
mcufriend_shield.h

#elif defined(ARDUINO_GENERIC_STM32F103C) || defined(ARDUINO_BLUEPILL_F103C8) || defined(ARDUINO_BLUEPILL_F103CB)
#STM32F103C8T6

//LCD pins     |D7 |D6 |D5 |D4 |D3 |D2 |D1 |D0 | |RD |WR |RS |CS |RST|

//STM32 pin |PA7|PA6|PA5|PA4|PA3|PA2|PA1|PA0| |PB7|PB1|PB0|PB8|PB9|

#include <MCUFRIEND_kbv.h>
MCUFRIEND_kbv tft;       // hard-wired for UNO shields anyway.
#include <TouchScreen.h>

char *name = "Please Calibrate.";  //edit name of shield
const int XP=PA6,XM=PB0,YP=PB1,YM=PA7; //ID=0x9327
const int TS_LEFT=894,TS_RT=128,TS_TOP=915,TS_BOT=80;

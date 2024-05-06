# STM32-ll-I2C-library
It's simple library for STM32. This file have some function for I2C comunication with Slave device.
I used STM32F103, but u can change this device library
#include "stm32f1xx_ll_i2c.h"
#include "stm32f1xx_ll_gpio.h"

Just call this function for 8bit write to slave device like this
I2C_WriteBytesToAddr(I2C2, 0x1a, 0x0b, &reg[0], 1);

Just call this function for read from slave device like this
I2C_ReadData(I2C2, 0x1a, 0x06, ans1, 1);
Also u can read more then byte. Just change last parameter
I2C_ReadData(I2C2, 0x1a, 0x00, ans1, 6);

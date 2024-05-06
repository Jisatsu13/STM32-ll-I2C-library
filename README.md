# STM32-ll-I2C-library
It's simple library for STM32. This file have some function for I2C comunication with Slave device.
I used STM32F103, but u can change this device library
#include "stm32f1xx_ll_i2c.h"
#include "stm32f1xx_ll_gpio.h"

Just call this function for write 8bit into register of slave device like this
I2C_WriteBytesToAddr(I2C2, 0x1a, 0x0b, &reg[0], 1);

Just call this function for read from register of slave device like this
I2C_ReadData(I2C2, 0x1a, 0x06, ans1, 1);
Also u can read more then byte. Just change last parameter
I2C_ReadData(I2C2, 0x1a, 0x00, ans1, 6);

//////////////////////////////////////
Це проста бібліотека для СТМ32. Тут є базові функції для комунікації зі слейвом.
Я використовував STM32F103, але ти можеш замінити оці бібліотеки для свого:
#include "stm32f1xx_ll_i2c.h"
#include "stm32f1xx_ll_gpio.h"

Виклич цю функцію для запису 8 бітів у регістр слейва, як тут
I2C_WriteBytesToAddr(I2C2, 0x1a, 0x0b, &reg[0], 1);

Виклич цю функцію для читання з регістру слейва, як тут
I2C_ReadData(I2C2, 0x1a, 0x06, ans1, 1);
Також можеш змінити останній параметр для читання більше ніж одного байту данних, як тут
I2C_ReadData(I2C2, 0x1a, 0x00, ans1, 6);

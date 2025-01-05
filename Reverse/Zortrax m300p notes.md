# Intro


# Pinouts
## Voltages
### V-IN 
30mA @ 24V only MCU board

### MCU power
3V3

### Reference
#### Extruder Driver
0.4V

#### X, Y drivers
0.6V

#### Z driver
1.0V

## Connectors:

### Power in
- Fits Wurth 691 353 500 004 quite well
- 1 - 24V_IN_P
- 2 - 24V_IN_N
- 3 - 24V_IN_P 
- 4 - 24V_IN_N

### DEBUG:
- 1 - 3V3
- 2 - BOOT0
- 3 - PA9 (U1TX)
- 4 - PA10 (U1RX)
- 5 - PA14 (SWCLK)
- 6 - PA13 (SWDIO)
- 7 - GND
- 8 - NRST

# Components

## Touch
FT6236

## Motor Drivers
 - Input: 44 pin package, potentiometer on pin 21, GND on pin 22
 - Conclusion: LV8729V

## Screen
microtech-lcd.com MTF0397SWI-06XBL
3.97 inch 480 x 800 Pixel Resolution
MIPI Interface TFT LCD Module
Driver: OTM8019A
## Motor Drivers

## MCU
### Conclusion
 - ID: 0x414 -> STM32F1xx (00/01/02/03/05/07)
 - Clock: 72MHz -? STM32F10(3/7)
 - Ethernet: No. -> STM32F103
 - Flahs: 512kB -> ...VE
 - Conclusion: STM32F103VE



### Cube Connect log
  04:05:09 : STM32CubeProgrammer API v2.17.0 | Windows-64Bits 
  04:05:16 : UR connection mode is defined with the HWrst reset mode
  04:05:17 : ST-LINK SN  : 004F00383438510C34313939
  04:05:17 : ST-LINK FW  : V3J3M2
  04:05:17 : Board       : --
  04:05:17 : Voltage     : 3.26V
  04:05:17 : SWD freq    : 8000 KHz
  04:05:17 : Connect mode: Under Reset
  04:05:17 : Reset mode  : Hardware reset
  04:05:17 : Device ID   : 0x414
  04:05:17 : Revision ID : Rev X
  04:05:17 : Debug in Low Power mode is not supported for this device.
  04:05:17 : UPLOADING OPTION BYTES DATA ...
  04:05:17 :   Bank          : 0x00
  04:05:17 :   Address       : 0x4002201c
  04:05:17 :   Size          : 8 Bytes
  04:05:17 :   Bank          : 0x01
  04:05:17 :   Address       : 0x1ffff800
  04:05:17 :   Size          : 16 Bytes
  04:05:17 : UPLOADING ...
  04:05:17 :   Size          : 1024 Bytes
  04:05:17 :   Address       : 0x8000000
  04:05:17 : Read progress:

### Register Log
Peripheral :RCC
Name	Value	Access	Address
CR	0x00005A83	read-write	@ 0x40021000
 HSION	1
 HSIRDY	1
 HSITRIM	0x10
 HSICAL	0x5A
 HSEON	0
 HSERDY	0
 HSEBYP	0
 CSSON	0
 PLLON	0
 PLLRDY	0

CFGR	0x00000000	read-write	@ 0x40021004
 SW	0x0
 SWS	0x0
 HPRE	0x0
 PPRE1	0x0
 PPRE2	0x0
 ADCPRE	0x0
 PLLSRC	0
 PLLXTPRE	0
 PLLMUL	0x0
 OTGFSPRE	0
 MCO	0x0

CIR	0x00000000	read-write	@ 0x40021008
 LSIRDYF	0
 LSERDYF	0
 HSIRDYF	0
 HSERDYF	0
 PLLRDYF	0
 CSSF	0
 LSIRDYIE	0
 LSERDYIE	0
 HSIRDYIE	0
 HSERDYIE	0
 PLLRDYIE	0
 LSIRDYC	0
 LSERDYC	0
 HSIRDYC	0
 HSERDYC	0
 PLLRDYC	0
 CSSC	0

APB2RSTR	0x00000000	read-write	@ 0x4002100C
 AFIORST	0
 IOPARST	0
 IOPBRST	0
 IOPCRST	0
 IOPDRST	0
 IOPERST	0
 IOPFRST	0
 IOPGRST	0
 ADC1RST	0
 ADC2RST	0
 TIM1RST	0
 SPI1RST	0
 TIM8RST	0
 USART1RST	0
 ADC3RST	0
 TIM9RST	0
 TIM10RST	0
 TIM11RST	0

APB1RSTR	0x00000000	read-write	@ 0x40021010
 TIM2RST	0
 TIM3RST	0
 TIM4RST	0
 TIM5RST	0
 TIM6RST	0
 TIM7RST	0
 TIM12RST	0
 TIM13RST	0
 TIM14RST	0
 WWDGRST	0
 SPI2RST	0
 SPI3RST	0
 USART2RST	0
 USART3RST	0
 UART4RST	0
 UART5RST	0
 I2C1RST	0
 I2C2RST	0
 USBRST	0
 CANRST	0
 BKPRST	0
 PWRRST	0
 DACRST	0

AHBENR	0x00000014	read-write	@ 0x40021014
 DMA1EN	0
 DMA2EN	0
 SRAMEN	1
 FLITFEN	1
 CRCEN	0
 FSMCEN	0
 SDIOEN	0

APB2ENR	0x00000000	read-write	@ 0x40021018
 AFIOEN	0
 IOPAEN	0
 IOPBEN	0
 IOPCEN	0
 IOPDEN	0
 IOPEEN	0
 IOPFEN	0
 IOPGEN	0
 ADC1EN	0
 ADC2EN	0
 TIM1EN	0
 SPI1EN	0
 TIM8EN	0
 USART1EN	0
 ADC3EN	0
 TIM9EN	0
 TIM10EN	0
 TIM11EN	0

APB1ENR	0x00000000	read-write	@ 0x4002101C
 TIM2EN	0
 TIM3EN	0
 TIM4EN	0
 TIM5EN	0
 TIM6EN	0
 TIM7EN	0
 TIM12EN	0
 TIM13EN	0
 TIM14EN	0
 WWDGEN	0
 SPI2EN	0
 SPI3EN	0
 USART2EN	0
 USART3EN	0
 UART4EN	0
 UART5EN	0
 I2C1EN	0
 I2C2EN	0
 USBEN	0
 CANEN	0
 BKPEN	0
 PWREN	0
 DACEN	0

BDCR	0x00000000	read-write	@ 0x40021020
 LSEON	0
 LSERDY	0
 LSEBYP	0
 RTCSEL	0x0
 RTCEN	0
 BDRST	0

CSR	0x24000000	read-write	@ 0x40021024
 LSION	0
 LSIRDY	0
 RMVF	0
 PINRSTF	1
 PORRSTF	0
 SFTRSTF	0
 IWDGRSTF	1
 WWDGRSTF	0
 LPWRRSTF	0






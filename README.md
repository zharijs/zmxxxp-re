# What?
Zortrax m200, m300 series reverse engineering to port Klipper.

# Why?
Becuase Zortrax support is non existant and functionality is outdated and was somewhat limited even back wehn it was a new product.

# Where?
 - Here
 - On [EEVblog forum](https://www.eevblog.com/forum/3d-printing/hack-zortrax-driver-board-port-klipper/)

# Todo:
## Demarked / unlabled components
Find demarked or unlabeled electtronics compoennt part numbers
- [x] Motor Drivers `LV8729V`
- [x] MCU `STM32F103VE`
- [x] Display / res / driver / touch `MTF0397SWI-06XBL / 480 x 800 / OTM8019A / FT6236`
- [x] Android processor / module `Alwinner A33 / A33-Core3`

## Demarked / unlabled mechanical parts
Find demarked or unlabeled mechjanical part numbers (for future serviceability)
- [ ] Motors
- [ ] Extruder top fan
- [ ] Extruder Bot Fans
- [ ] Linear bearings
- [ ] Extruder bearing
- [ ] Extruder sprocekt
- [ ] X/Y timing pulleys
- [ ] X/Y timing belts
- [ ] Optical endstops

## Wiring maps
Sketch wiring maps, compare wiring, boards:
- [ ] M200
- [ ] M300
- [ ] M200 plus
- [x] M300 plus
- [ ] M300 dual

## Schematics
Draft importnat parts of board schematics:
- [x] MCU board (M300P)
- [x] MCU board's "WIFI" piggyback (Goes to Android TFT assy)  (M300P)
- [x] MCU board's "DISLPAY" piggyback (Goes to Optical endstops and hosts Buzzer)  (M300P)
- [ ] Original mono display board (M200)
- [ ] Extruder Board (M300P)
- [ ] Android board (M300P)
- [ ] Android level shifter board (M300P)
- [ ] Android Button Board (M300P)
- [ ] Android USB Hub board (M300P)
- [ ] Android Front USB board (M300P)
- [ ] Android USB Ethernet / RJ45 board (M300P)


## MCU pinout
- [ ] M200
- [ ] M300
- [ ] M200 plus
- [x] M300 plus
- [ ] M300 dual

## Port Klipper
- [ ] Start porting it, see what issues come up

## Android board
Evaluate options:
1. It runs on Allwinner A33 - Linux support is somewaht lacking
2. Is bootloader locked / eMMC encrypted?
3. Custom Android instead of linux if possible?
4. Just make a a SOM board with Raspberry Compute, Digi or Variscite SoM to fit same mount and talk to same display and touch?

- [ ] Research the CPU support
- [ ] Evaluate feasability

## Extra mods / changes
- [ ] Add vibration sensor for input shaping
- [ ] Replace ribbon with wire harness and drag chain
- [ ] Bigger motors for 300 series
- [ ] Use native Ethernet, if Android board is changed to somehting else
- [ ] Add magnetic layer to heatplate to use with flexible paltes
- [ ] Add load cells to scan level precisely and without electrical contact (worst design chopice of all M series)
      

# Community announcment
As many of you are swapping out Zortrax HW with BTT and alike, I guess you have OG boards you don't need. 

DM me - I could make some use of those for the greater good

# What?
Zortrax m200, m300 series reverse engineering to port Klipper.

# Why?
Becuase Zortrax support is non existant and functionality is outdated and was somewhat limited even back wehn it was a new product.

# Where?
 - Here
 - On [EEVblog forum](https://www.eevblog.com/forum/3d-printing/hack-zortrax-driver-board-port-klipper/)
 - On [Reddit](https://www.reddit.com/r/3Dprinting/comments/1ia79sl/zortrax_m200_m300_m200p_m300p_motion_board/?utm_source=share&utm_medium=web3x&utm_name=web3xcss&utm_term=1&utm_content=share_button)

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
- [x] Linear guide screws - M5 x 12 countersunk. OG ones are pretty bad with HEX slot. Flat head allows better alignment. I used Torx: `TME: B5X14/BB30503 (https://www.tme.eu/en/details/b5x14_bn368/bolts/bossard/1147315/)`
- [x] Linear guide nuts - M5. OG are hard to handle, can't get any tool in where they are. Changed to M5 square nuts for tiny bit better handling: `TME: B5/BN147 (https://www.tme.com/us/en-us/details/b5_bn147/nuts/bossard/1092634/)`
- [x] Extruder top fan `Both extruder fans are 12v 4010 fans (https://www.aliexpress.com/item/1005006317979634.html)`
- [x] Extruder Bot Fans `Both extruder fans are 12v 4010 fans (https://www.aliexpress.com/item/1005006317979634.html)`
- [ ] Linear bearings
- [ ] Extruder bearing
- [ ] Extruder sprocekt
- [x] X/Y timing pulleys `Standard 20 tooth 2GT Pulley`
- [x] X/Y timing belts `Standard 60cm 2GT belt (https://www.aliexpress.com/item/1005007816768123.html - "2GT-604mm")`
- [ ] Optical endstops `M200 has standard limit switches (https://www.aliexpress.com/item/1005008413626764.html)`
- [x] Z Axis Ball Screw `M200 v3+ and M300 have a 12mm ball screw with a 4mm lead (in klipper rotation distance is 4mm). M200 V2 and eariler had a standard TR8 lead screw (8mm with 8mm lead or in Klipper 8mm rotation distance)`

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
- [ ] Add magnetic layer to heatplate to use with flexible paltes `Ender 3 build plates are a perfect sized fit for the M200 and extremely cheap (https://www.aliexpress.com/item/1005007592437912.html + https://www.aliexpress.com/item/1005007128388830.html 235x235mm`
- [ ] Add load cells to scan level precisely and without electrical contact (worst design chopice of all M series)
      

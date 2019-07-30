# BattGo ArduPilot 
BattGO® is an information exchange system between charging equipment and discharging device.
https://www.battgo.org/

![diagram](https://github.com/domenicopatella/BattGo-ArduPilot-/blob/master/Media/IMG_1.bmp)

BattGo is a battery management system developed by iSDT, basically like a blackbox for your battery.

When you connect the LiPo battery to a BattGo compatible charger or voltage checker, you will be able to access a lot of crucial information about that battery pack, including:

    Battery Brand
    Date of Manufacture
    Battery type and capacity
    Battery C Rating
    Cell voltage
    Remaining capacity
    Temperature
    Discharge cycle
    Error log about overheat, over-discharging and overcharging

This information is all stored inside the battery pack, as well as battery charging preferences and settings such as the charge current, and when to Auto-storage.
That’s right, BattGo batteries can automatically discharge themselves to storage voltage if they are left charged for too long (set by the user). Truly smart batterers.

ISDT sell a development KIT, basically a serial uart converter to comunicate and 4 PCB Smartbattery  (3s/4s/5s/6s)

![diagram](https://github.com/domenicopatella/BattGo-ArduPilot-/blob/master/Media/developmentkit.png) 

I started to write the support for ArduPilot firmware (3.7.0 dev)
https://github.com/DomenicoPatella/ardupilot/tree/Battgo


Mounting small PCB inside the lipo 4S battery 

![diagram](https://github.com/domenicopatella/BattGo-ArduPilot-/blob/master/Media/immagine.png)



I wrote the backend driver and i tested  the firware in SITL mode with BGlinker on the serial port
The protocol is in ASCII mode 
The flight controlloer  send the request with an specific ID command , the smart battery responde with an Ack message
There are several messsages , someone of these require new variables to store the informations. 
At the moment i used the parameters already defined in the program
Battery Voltage
Battery Cells
Serial number 
Current*

![diagram](https://github.com/DomenicoPatella/BattGo-ArduPilot/blob/master/Media/WIndow.png)



# BattGo ArduPilot 
BattGO® is an information exchange system between charging equipment and discharging device.
https://www.battgo.org/

![diagram](https://github.com/domenicopatella/BattGo-ArduPilot-/blob/master/Media/IMG_1.bmp)

BattGo is a battery management system developed by iSDT, basically like a blackbox for your battery.

When you connect the LiPo battery to a BattGo compatible charger or voltage checker, you will be able to access a lot of crucial information about that battery pack, including:

    Battery Brand -tested ok- 
    Date of Manufacture  -supported
    Battery type and capacity - tested ok -
    Battery C Rating  -tested ok  
    Cell voltage -tested ok -
    Remaining capacity  -  support to next release of ISDT pcb- 
    Temperature -tested ok-
    Discharge cycle -tested ok-
    Error log about overheat, over-discharging and overcharging  - supported -

This information is all stored inside the battery pack, as well as battery charging preferences and settings such as the charge current, and when to Auto-storage.
That’s right, BattGo batteries can automatically discharge themselves to storage voltage if they are left charged for too long (set by the user). Truly smart batterers.

ISDT sell a development KIT, there is a tiny serial uart converter to comunicate  and 4 PCB Smartbattery  (3s/4s/5s/6s)

![diagram](https://github.com/domenicopatella/BattGo-ArduPilot-/blob/master/Media/developmentkit.png) 


Example of mounting inside one lipo 4S battery 

![diagram](https://github.com/domenicopatella/BattGo-ArduPilot-/blob/master/Media/immagine.png)


I developed the backend driver and tested  the firware in SITL mode.  The USB Battgo Adapater is used to comunicate on the serial port
The flight controlloer  send the request with an specific ID command , the smart battery responde with an Ack message
There are several messsages , someone of these require new parameters to store the informations. 

Battgo support for ArduPilot firmware (3.7.0 dev)
https://github.com/DomenicoPatella/ardupilot/tree/Battgo

With ALt+F it's possibile to launch a window utilitiy in Mission Planner to read information from smartbatery

![diagram](https://github.com/DomenicoPatella/BattGo-ArduPilot/blob/master/Media/WIndow.png)




Solderless router serial port connector
============
Solderless router serial port connector is designed to enable easy connection to the routers serial port, bypassing the need for soldering headers or wires. This being particularly useful in community wireless networks with the large volume of low-cost wifi routers that may require a serial connection for restoring firmware if something has gone wrong.

![SolRouterSer](https://raw.github.com/IRNAS/SolRouterSer/master/photos/SolRouterSer-2.jpg)
 


### Supported routers
Initially only Tp-Link WR740/741 wifi routers are supported due to their popularity but others may be supported if so requested. Email us about it.

Supported list:
 * WR740N v2
 * WR740N v4
 * WR741ND v2
 * WR741ND v4
 
The listed routers may be easily programmed on OS X with EXPECT scripts found in this repository. Choose the one suitable to your version and familiarise yourself with the manual method of TFTP flashing as published on openwrt wiki.

To flash firmware on WR741ND/740N with scripts in this repository follow these steps:
 * Start a TFTP server
 * Place the firmware int he TFTP folder
 * Assign 192.168.1.100 to the machine
 * Run the script with two arguments, first being the firmware filename in the TFTP folder and second being the UART device, for example `expect flash-wr741nd-v2.expect firmware.bin /dev/tty.SLAB_USBtoUART`
 * Wait and its done.
 
 ![SolRouterSer](https://raw.github.com/IRNAS/SolRouterSer/master/photos/SolRouterSer-3.jpg)
 
### Electronics
The circuit board uses spring loaded test pins to connect to the router. There are LEDs on the serial connections, indicating when the data is being transferred. Unpopulated pads may be used to add pull-up resistors if so required by the USB-UART adapter or the router. 

Email us at (info AT irnas.eu) to preorder the assembled PCB with pre-soldered test pins. 

![SolRouterSer](https://raw.github.com/IRNAS/SolRouterSer/master/photos/SolRouterSer-1.jpg)

For connecting to the computer the use for an USB-UART converter is suggested, FTDI or CP2012 based ones perform very well and are available at low cost.

### Assembly
3D print the SolRouterSer.stl file from this repository and insert the circuit board. Slide it in the cradle, so it aligns with the pins on the router. Firmly press it in position and if required apply slight force to the router circuit board to form a good connection.

### License
![alt text](http://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png "CC-NC-SA")

This work is licensed under [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License] (http://creativecommons.org/licenses/by-nc-sa/4.0/deed.en_US)
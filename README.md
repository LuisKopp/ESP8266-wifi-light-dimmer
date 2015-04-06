# ESP8266-wifi-light-dimmer
Wifi light dimmer based off of the inexpensive ESP8266 wifi modules.

### Circuit design ###
I'm using a dimming circuit by [diy_bloke] (http://www.instructables.com/id/Arduino-controlled-light-dimmer-The-circuit/step1/Arduino-controlled-light-dimmer-The-PCB/).<br />
[Fritzing](http://fritzing.org/) schematics are under the schematics folder.

### Installing ###
1. Download [Arduino-compatible IDE with ESP8266 support] (https://github.com/esp8266/Arduino)
2. Load smartSwitch.ino sketch in Arduino IDE
3. Fill in SSID and password
4. Verify/adjust GPIO pins.
5. Flash sketch ESP

### Control ###
Browse to IP of ESP. Use GET variables to configure settings:
- s = state (0 or 1)
- b = brightness (0-255)
- f = fade (0 or 1)

ex1: View current settings (json): http://ip.of.esp/<br />
ex2: Set brightness to 50% and set state to on: http://ip.of.esp/?s=1&b=128<br />
ex3: Set brightness to 100% and enable dimming: http://ip.of.esp/?b=255&d=1<br />
ex4: Toggle state (on->off or off->on): http://ip.of.esp/?s=t<br />

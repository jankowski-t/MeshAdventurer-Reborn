# MeshAdventurer Reborn
## MeshAdventurer Reborn is my remix of Chris Myers' MeshAdventurer project.
![Original Author's repository](https://github.com/chrismyers2000/MeshAdventurer)
## Features:
### From original project (I removed some things because I didn't need them):
- 1W transmit power for extended range compared to normal Meshtastic hardware (typically 100mW-160mW).
- ~~Wide range voltage input (9-28V), It can be powered by USB or barrel plug making it extremely versitile. You can even power it using a solar panel!~~
- OLED display~~ and rotary encoder with "Canned messages", these are messages pre-programmed by you and can be sent without the need of a smartphone. This is especially useful if your phone dies and you are in an emergency situation~~.
- Optional Temp/Hum/Pressure sensor can send potentially useful data to the rest of your group.
- On-board GPS will keep sending your position even after your phone is disconnected.
- ~~A buzzer to notify you when messages are recieved.~~ 
- Compatible with official Meshtastic Hydra firmware variant so you can stay up to date when new versions are released. No custom firmware needed!
### Added by me:
- All SMD components are no smaller than 1206 for easy hand-soldering.
- Designed to be powered from 1S Li-Ion battery via an additional SM5308 board.
- Two JST PH 2.0 sockets, one is for 5V input from the SM5308 board, the other is for sensing battery voltage.
- The order of VCC and GND pins on OLED display can be selected by soldering jumpers at the top of the board.
## Materials:
- Ebyte E22-900M30S or E22-400M30S LoRa module. The even more powerful E22-XXXM33S modules are likely to work as well but have not been tested.
- ESP32-WROOM-32D. The ESP32 is available with 30 or 38 pins and with various board sizes. This project uses the 38 pin version with 25.4mm distance between the two rows of pins. Some boards are longer than others and have mounting holes in the corners. For this project you need the board where pin headers end right at the board's edge, otherwise the ESP32 will stick past the edge of this board. The WiFi antenna at the other end of the ESP board is not a problem.
- GPS Module: ATGM336H.
- OLED Display: SSD1306, 0.96". Both VCC, GND as well as GND, VCC pin orders can be used - just solder the correct jumpers on this board. Unfortunately the sizes of these displays also vary, so some may not fit well in the enclosure.
- SMA connector: right angle variant. They come with various length of the threaded part. I suggest buying the longest one possible if you want to use the enclosure, so a decent length sticks out for the antenna to thread on.
- Two JST PH 2.0 SMD connectors.
- Button.
- 1206 SMD resistors: 1k x1, 10k x1 and 100k x2 (these form a voltage divider to sense battery voltage; other reasonably high values can be used as long as the voltage applied to ESP's pin is no higher than 3.3 V when battery is full and the ratio is set correctly in firmware).
- 1206 SMD capacitors: 100nF x4.
- 100uF tantalum capacitors, size B, voltage at least 6,3V, x2.
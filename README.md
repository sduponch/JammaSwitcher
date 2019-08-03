# Yet Another Arcade Jamma Switcher

![Switcher Logical Overview](boards/docs/Overview.png?raw=true "Jamma switcher logical overview")

## Component proposal

-RGB Digitalizer :
AD9883A ![AD9883A Documentation](boards/docs/AD9883A.pdf)

RGBH Video Switcher :
TS5V330D ![TS5V330 Documentation](boards/docs/TS5V330.pdf)

RGB DAC :
ADV7125 ![ADV7125 Documentation](boards/docs/ADV7125.pdf) 

Audio Codecs :
ADAU1761 ![ADAU1761 Documentation](boards/docs/ADAU1761.pdf)

Player control switcher :
SN74LVCH16T245 ![SN74LVCH16T245 Documentation](boards/docs/SN74LVCH16T245.pdf)

HDMI Receiver :
ADV7611 ![ADV7611 Documentation](boards/docs/ADV7611.pdf)

HDMI Transmitter :
ADV7511 ![ADV7511 Documentation](boards/docs/ADV7511.pdf)


FPGA SoM :
- MYiR Zinq 7015
- MYiR Zinq 7010 ![MYiR Documentation](boards/docs/MYC-Y7Z010_007S.pdf)* Z7010 has not enought GPIOs

Streaming encoder :
hi3519av100 (IP Camera SoC)*
Zynq 7000 are not powerfull enought to provide 1080p transcoding, all H.264/H.265 IP are designed for Ultrascale or 7035 and above SoC... So an alternate solution is to use an IP Camera SoC like Hisilicon Hi3516 that expose a pcie bus and talk with RGB, HDMI In/Out through this bus via a smaller FPGA .

## Features

Must have features :
- 6 in 1 Jamma Switcher with support of -5, Mono/Stereo audio via RCA, 2/4 Players up to 8 buttons per players.
- USB HID over a virtual USB HUB to allow connection of moderne devices like Raspbery, Xbox, PS4, ect...
- RGBH Downscaller to 15/24/31 kHz on jamma connector to support old cathodic tubes.

Nice to have :
- HDMI In
- HDMI Out
- Multiplayer Netplay via streamming
- Cloudgamming

## Support this project
[![paypal](https://www.paypalobjects.com/en_US/FR/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=UBB56J4T93KZE)

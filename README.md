# ANAVI pHAT - IR automation

## goals

### send IR signals to configure media devices to various presets:

| preset             | HDMI switch | projector | A/V receiver           |
| ------             | ----------- | --------- | ------------           |
| off                | off         | off       | off                    |
| Chromecast (video) | 1, 2.1      | on        | on, "Dolby II (Movie)" |
| Chromecast (audio) | 1, 2.1      | off       | on, "Ext. Stereo"      |
| Switch             | 3, 2.1      | on        | on, "Dolby II (Game)"  |
| PS4                | 4, 5.1      | on        | on, "Direct Surround"  |

For off/on signals (which are the same signal), the pHAT should also listen for these and keep track of the device's state, even if it did not issue the signal. Likewise, the A/V receiver cycles through a series of surround sound settings.

There should be some quick way to recalibrate the rPI's record of the devices' states when they get out of sync (e.g. the device receives a signal that the pHAT misses, or a device's hardware buttons are used, or there is a power outage).

## references

https://www.crowdsupply.com/anavi-technology/infrared-phat

- [User’s manual](http://anavi.technology/files/anavi-infrared-phat.pdf)
- [Instructions for using ANAVI Infrared pHAT with LIRC and Raspbian on Raspberry Pi](http://www.instructables.com/id/Transforming-Raspberry-Pi-Into-a-Remote-Control/)
- [Instructions for controlling and air conditioner](http://www.cnx-software.com/2017/03/12/how-to-control-your-air-conditioner-with-raspberry-pi-board-and-anavi-infrared-phat/)
- [Source code and examples](https://github.com/AnaviTechnology/anavi-examples)

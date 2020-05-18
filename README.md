# rear-view-camera
install a rear view camera in Bru
17 May 2020:
Bench testing the camera. 

- There are two components. Mirror (with display) and Camera.
- Camera has: barrel connector (power, ground); Yellow RCA (video).
- Display has: barrel connector (power, ground); yellow RCA (AV1), white RCA (AV2)
- yellow-yello RCA cable has an extra red wire coming out the back of each connector. No idea why. On automotive amps this is a "remote power-off" wire, for controlling behavior when ignition is in "Accessory" mode. But it doesn't appear to connect to anything in this setup, and doesn't do anything when grounded or energized.

Pyle manual (different but similar) says to supply power via ignition to the display, and via a reverse taillight to the camera. This will make it switch on and off based on whether it's in reverse, you see.

Three buttons on the back of the display change some display settings (brightness, contrast, tint). 

Box sez that it has "input auto-select". We'll see what that means when I connect two sources at the same time. Hopefully it just always prefers AV1, so it would switch to it whenever the reverse camera is triggered. Otherwise I've got to come up with some switching mechanism for AV2 (which could totally be a raspberry pi OBD2 dashboard / video server...)

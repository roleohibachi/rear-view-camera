# rear-view-camera
install a rear view camera in Bru
## 17 May 2020: Bench test

- There are two components. Mirror (with display) and Camera.
- Camera has: barrel connector (power, ground); Yellow RCA (video).
- Display has: barrel connector (power, ground); yellow RCA (AV1), white RCA (AV2)
- yellow-yello RCA cable has an extra red wire coming out the back of each connector. No idea why. On automotive amps this is a "remote power-off" wire, for controlling behavior when ignition is in "Accessory" mode. But it doesn't appear to connect to anything in this setup, and doesn't do anything when grounded or energized.

Pyle manual (different but similar) says to supply power via ignition to the display, and via a reverse taillight to the camera. This will make it switch on and off based on whether it's in reverse, you see.

Three buttons on the back of the display change some display settings (brightness, contrast, tint). 

Box sez that it has "input auto-select". We'll see what that means when I connect two sources at the same time. Hopefully it just always prefers AV1, so it would switch to it whenever the reverse camera is triggered. Otherwise I've got to come up with some switching mechanism for AV2 (which could totally be a raspberry pi OBD2 dashboard / video server...)

Mirror body has two spring-loaded clamps, one of which was broken when I got it. Unscrewed ~10 tiny screws, all of them practically stripped from the factory (tiny screw, soft plastic). Used CA glue to repair the tiny bit of plastic that failed in the clamp. Should work fine now. If it fails again, I'll rip it out and use zip ties!

## 19 May: install
### Mirror
The clamp broke again... but I disassembled it to realize it was the OTHER clamp, not the one I repaired! I repaired this one in the same way, and it seems sturdy. I'll still be careful with it.

Mirror install was straightforward. Remove dome light cover (plastic tabs), remove 2 bolts and dome light housing. There's enough flex inthe headliner that I can push the connectors up into it without further disassembly.

There's an unpopulated header for the OEM "fancy" rear view mirror. It's got 3 wires - power (on its own fuse, labelled "mirror"!), ground, and a reverse indicator. I won't use the reverse indicator here (I'll just wire the camera to the taillight), but it's nice to know it's there in case I change hardware later.

I blew the fuse, though, when I shoved a multimeter probe into that connector from the front. Must have bridged two of the pins. I heard it pop, too! Fortunately it was a 7.5A, so it popped very fast. Lesson learned: probe the male connectors from the rear, so to speak. The plastic housing then protects you from your own imprecision.

Did the splice by neatly twisting, then back-twisting, the wires, then wrapping with electrical tape. Ideally I'd have used crimp connectors, or a dab of solder, but I didn't have any of those things on hand.

### Video wire
This was the hard part. Routed the video wire from the dome light housing, across the front of the headliner just above the windshield. Removed the passenger sun visor, and panels on the A and B pillars. This let me tuck the wire into the headliner from the side, but still route it above the side airbags (out of their way).

Removed a bunch of rear plastic panels, around the C pillar and on the inside of the tailgate. Routed the wire to where a flexible rubber sheath houses cabling into the tailgate. It took a darning needle and a second set of hands to fish the big RCA plug through that spot, but then I was home free to route into the tailgate.

Rather than drill a fresh hole in the bodywork, I carefully analyzed the rear trim. I removed the center trim panel (where the subaru logo is) - it's held on by two weatherproof plastic clips and FOUR bolts! Unnecessary! One of them was even half-hidden behind the rear wiper motor. What a pain in the ass. So I removed that bolt permanently. The bolt hole is protected by the plastic trim - still clean under there after 10 years! That's the spot I'm using to route the camera cabling into the interior. Hogged it out to 1/2" and squeezed the cables through (barely). In the process, I over-drilled the hole, and bound my bit on the wiper motor housing... and the bit snapped off. Dammit.

Spliced the rear power connector to the passenger reverse light (two bare wires, not a cable housing like the driver side). I'm lucky the reverse lights are in the tailgate, and not on the body like the taillights. Were that the case, I'd have to route up and around... yuck.

Plugged in, tested working! Replaced all the panels and had a beer.

TODO: put a raspberry pi on the second video channel. Connect it to OBD2 for an in-flight dashboard. Put some entertainment on there, kinda like a drive-in movie. I'd love to see a shell on my mirror just for nerd cred! TRRS4 to RCA cable is in the mail.

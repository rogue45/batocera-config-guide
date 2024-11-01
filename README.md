# The capcom marvel super heroes arcade cabinet
![arcade_cabinet_edit](https://github.com/user-attachments/assets/b9724977-8186-4dc7-a9c9-66dc8503ef31)

# Batocera usb drive setup
This can be found on youtube. The arcade cabinet has a single usb input. Batocera can be loaded onto a usb as a bootable drive. Essentially when its plugged in the cabinet loads into batocera os.
When its not plugged in, the arcade loads its oem games.

Batocera is essentially an os that lets you select emulators. You can dl and place roms per emulator. We loaded in our fav arcade games and configured as laid out below for a very slick setup.

## Roms placement
```\userdata\roms\<emulator>\<romfile>```
As an example for snes emulator
```\userdata\roms\snes\Pinball Dreams (USA).sfc```

To store an image to display for game selection
I always use png. Not sure if jpg is supported
```\userdata\roms\<emulator>\images```

again as an example using pinball dreasms my image would be stored here:
```\userdata\roms\snes\images\pinballDreams.png```

This path then must be entered into the gamelist file in the emulator director which dictates which roms are shown in the emulators list as well as ties together the rom and the image file
```
	<game>
		<path>./Pinball Dreams (USA).sfc</path>
		<name>Pinball Dreams</name>
		<lang>en</lang>
		<region>us</region>
		<image>./images/pinballDreams.png</image>
	</game>
```
## Game button Remaps
Most the time the button config is good enough by default. But you can do custom remaps per game if you like.
Pinball dreams however used the joystick for left flipper and a button with right flipper

### To make a custom remap for a single game place a remap file for the config dir of the emulator with the filename matching the rom filename but with the .rmp file extension
```\userdata\system\.config\retroarch\config\remaps\Snes9x\Pinball Dreams (USA).rmp```

My cabinet has a joystick to the left and six buttons. From what i have gathered its buttons are configured as follows:

Retroarch on Marvel super heroes arcade cabinet
```
 Y(0)  X(1)  L(2)
 B(3)  A(4)  R(5)
```
Oddly pinbal dreams manual seems to have a typo in button assignments but this config results in
B as my ball plunger, A as left flipper, and R as right flipper which makes the game playable.

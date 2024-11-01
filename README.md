# The arcade cabinet

# Roms placement
\userdata\roms\<emulator>\<romfile>
# As an example for snes emulator
\userdata\roms\snes\Pinball Dreams (USA).sfc

# To store an image to display for game selection
# I always use png. Not sure if jpg is supported
\userdata\roms\<emulator>\images

# again as an example using pinball dreasms my image would be stored here:
\userdata\roms\snes\images\pinballDreams.png

# This path then must be entered into the gamelist file in the emulator director which dictates which roms are shown in the emulators list as well as ties together the rom and the image file
<game>
		<path>./Pinball Dreams (USA).sfc</path>
		<name>Pinball Dreams</name>
		<lang>en</lang>
		<region>us</region>
		<image>./images/pinballDreams.png</image>
	</game>

# Most the time the button config is good enough by default. But you can do custom remaps per game if you like.
# Pinball dreams however used the joystick for left flipper and a button with right flipper

# To make a custom remap for a single game place a remap file for the config dir of the emulator with the filename matching the rom filename but with the .rmp file extension
\userdata\system\.config\retroarch\config\remaps\Snes9x\Pinball Dreams (USA).rmp

# My cabinet has a joystick to the left and six buttons. From what i have gathered its buttons are configured as follows:
# Retroarch on Marvel super heroes arcade cabinet
# Y X L   0, 1, 2
# B A R   3, 4, 5

# Oddly pinbal dreams 

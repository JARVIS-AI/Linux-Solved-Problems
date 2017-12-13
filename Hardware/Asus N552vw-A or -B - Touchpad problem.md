## Touchpad Asus models

Error = Touchpad isn't working !!

  1-i can't tap to click
  2-i can't click right via button
  3-every time i touch, the touchpad the cursor moves to far distance from last position, even if i touch just as close as possible to previous point.
  ...

The TouchPad is Elan
  I installed "elantech-asustouchpad-dkms" from aur, no luck.

The ouput of

```sh
$ xinput list-props "Elan Touchpad"
```

is

```sh
{
Device 'Elan Touchpad':
	Device Enabled (139):	1
	Coordinate Transformation Matrix (141):	1.000000, 0.000000, 0.000000, 0.000000, 1.000000, 0.000000, 0.000000, 0.000000, 1.000000
	Device Accel Profile (267):	0
	Device Accel Constant Deceleration (268):	1.000000
	Device Accel Adaptive Deceleration (269):	1.000000
	Device Accel Velocity Scaling (270):	10.000000
	Device Product ID (259):	1267, 5
	Device Node (260):	"/dev/input/event12"
	Evdev Axis Inversion (271):	0, 0
	Evdev Axis Calibration (272):	<no items>
	Evdev Axes Swap (273):	0
	Axis Labels (274):	"Abs MT Position X" (265), "Abs MT Position Y" (266), "Abs MT Pressure" (295), "Abs Distance" (291), "Abs Tool Width" (292), "Abs MT Touch Major" (293), "Abs MT Touch Minor" (294), "None" (0), "None" (0), "None" (0)
	Button Labels (275):	"Button Left" (142), "Button Unknown" (262), "Button Unknown" (262), "Button Wheel Up" (145), "Button Wheel Down" (146)
	Evdev Scrolling Distance (276):	0, 0, 0
	Evdev Middle Button Emulation (277):	0
	Evdev Middle Button Timeout (278):	50
	Evdev Third Button Emulation (279):	0
	Evdev Third Button Emulation Timeout (280):	1000
	Evdev Third Button Emulation Button (281):	3
	Evdev Third Button Emulation Threshold (282):	20
	Evdev Wheel Emulation (283):	0
	Evdev Wheel Emulation Axes (284):	0, 0, 4, 5
	Evdev Wheel Emulation Inertia (285):	10
	Evdev Wheel Emulation Timeout (286):	200
	Evdev Wheel Emulation Button (287):	4
	Evdev Drag Lock Buttons (288):	0
	Synaptics Palm Detection (518):	1
	Synaptics Tap FastTap (519)
:	1
	Synaptics Edge Scrolling (520):	1, 1, 0
	Synaptics Off (521):	1
}
```

======================================

Just do

```sh
$ sudo modprobe psmouse
```

and reboot.

Enjoy your touchpad :)


## Thanks

Thank you again for follow one of our other solving tut.
If our solving is useful for you come and give me a star, its like a cup of coffee. :)
Thanks.

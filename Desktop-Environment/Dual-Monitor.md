# Dual Monitor

## For Making Dual Monitor in Arch Linux (Laptop Screen 4K + Samsung LED 1366x768)

```sh
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos 120x900
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos 120x9
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos 120x0
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos 120x1
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos -120x0
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos -1367x0
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos -200x0
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos 120x2
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos 0x0
  xrandr --output HDMI-2 --scale 3x3 --mode 1366x768 --pos 0x0
  mons -s
  mons -n left
  mons -e left --dpi 2000
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos -1200x0
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos -1366x0
  xrandr --output HDMI-2 --scale 2.5x2.5 --mode 1366x768 --pos 0x0
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos 120x9
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos 120x0
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos 120x1
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos -120x0
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos -1367x0
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos -200x0
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos 120x2
  xrandr --output HDMI-2 --scale 3x3 --mode 1366x768 --pos 0x0
  mons -s
  mons -n left
  mons -o
  mons -e left --dpi 2000
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos 0x0
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos -1366x0
  xrandr --output HDMI-2 --scale 2x2 --mode 1366x768 --pos -1200x0
  xrandr --output HDMI-2 --scale 2.5x2.5 --mode 1366x768 --pos 0x0
```


  Complete set commands for Dual Monitor (4K + 1366x768 VGA)
  Commands for settings my screen in right location and resolution and DPI
  

# Mirny CPLD code

[Mirny overview](https://github.com/sinara-hw/mirny/wiki)

[Mirny Schematics](https://github.com/sinara-hw/mirny/releases)

## Building

Needs migen and ISE.

```
make
# and then look at/use flash.sh or make flash

# or use fxload and xc3sprog:
/sbin/fxload -t fx2 -I /opt/Xilinx/14.7/ISE_DS/ISE/bin/lin64/xusb_xp2.hex -D /dev/bus/usb/001/*`cat /sys/bus/usb/devices/1-3/devnum` && sleep 10 && \
xc3sprog -c xpc -m /opt/Xilinx/14.7/ISE_DS/ISE/xbr/data -v build/mirny.jed:w
# look for "Verify: Success"
```

# License

GPLv3+

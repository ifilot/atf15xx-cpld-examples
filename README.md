# ATF15XX CPLD Examples

## Purpose

This repository contains a number of examples how to design and program for the
[ATF15XX](https://ww1.microchip.com/downloads/en/DeviceDoc/Atmel-3614-CPLD-ATF15-Overview.pdf)
range of CPLDs.

## Devices

Unless otherwise stated, we make use the [ATF15XX-DK3 development programmer
kit](https://www.microchip.com/en-us/development-tool/atf15xx-dk3-u).

## Programming instructions

Program instructions are provided in the design file, but a brief overview
is also presented here.

* Download and install WinCUPL and ATMISP via 
  [this link](https://www.microchip.com/en-us/products/fpgas-and-plds/spld-cplds/pld-design-resources)
* Open the `.pld` file in WinCUPL
* Do `Run > Device Dependent Compile` or simply hit `F9`: This will generate a
  `.jed` file.
* Open the ATMISP tool and select `File > New`. Number of devices is `1`.
* Select ATF1504AS (or your specific device) for the *Device Name*, select
  `Program / Verify` under *JTAG Instruction* and select the JEDEC file as
  generated in the previous step.
* Click `Run` to place the design on the CPLD. Note that the ATF1502 chip
  needs to have its own 5V power supply. The ATDH1150USB is (apparently)
  unable to provide power to the chip over the JTAG port.
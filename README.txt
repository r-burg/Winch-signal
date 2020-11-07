The unit described was designed and built using strip-board in, as I recall, 2008.

It was built around a PIC16F876 microcontroller, though various other PIC16F devices are suitable and the documents given here refer at times to the PIC16F876 and sometimes the PIC16F877; the PIC16F887 and PIC16F886 should be equally suitable.

The 5 volt power regulator supplies only the microcontroller, which draws only a few milliamps (in the case of the '886 device, a maximum of 3.8 mA as I read the data sheet), and thus it needs no heatsink or other thermal precautions. The relay drive current is draw from the unregulated supply, as are the load currents.

One supplier lists the PIC16F886 at £1.67 one off.

The ULN2803 or ULN2804 driver includes diode protection for inductive loads. To avoid common resistance problems I connected the zero volt line from the battery to the lamps/LEDs separately from the line to the electronics. If LEDs were to be used the current might well be too small for this to be worth bothering with; I used incandescent lamps drawing several amps, and never checked to see if a less cautious layout would be satisfactory.

The sounder was connected between battery positive and the driver output. When I explained that it was included so that the pilot knew what signal was being given, someone responded "you mean the pilot flying overhead?". It was a bit loud... so I put a resistor in series with the sounder, and moved the latter underneath the signal wagon.

I used the following tools etc.:
    Operating system                Ubuntu 16.04 LTS (Linux)
    Compiler                        sdcc
    Assembler, linker etc           gputils
    Simulating debugger             gpsim
    USB programmer                  USBpicrog

While I do not use Windows, I expect the corresponding Windows tool could be used without difficulty. Using the code as it is, you only need burn the hex file to the device.

The files included here need their inconsistencies sorting out; the source is given a 'C' but 'manual-h.doc' says assembler (which it was originally), and there are inconsistencies as to the exact model of microcontroller used. Oops!





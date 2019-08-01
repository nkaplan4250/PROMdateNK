PROGRAMMING THE PROMdate

> > > Plug in PROMdate USB (no need to capture it yet, just power)
> > > Press the button on the Teensy to enter Promgram Mode
> > > Capture PROMdate listed as "Unknown device...." in USB device list
> > > The Teensy gui to the left should change upon capture
> > > In terminal enter the following:

teensy\_loader\_cli -v -w --mcu=at90usb1286 '/home/nk/Desktop/PROMDATE-master/prom.hex'

> > > If successful the PROMdate will now be listed in the USB menu as "Your Name USB Serial \[0100\]"
> > > Disconnect PROMdate from power, attach leads to chip, insert chip into zif socket, connect PROMdate to computer

PROMdate OPERATION AND HEXDUMP

> > > Capture PROMdate
> > > Change the working directory to if you want the files saved somewhere in particular
> > > To launch minicom enter the following:

minicom -D /dev/ttyACM0

> > > copying and pasting from the chip list isn't necessary but to view the list and see current selection press: l
> > > To set the chip make (mCHIP) enter:

mATMega328P

> > > To check that data can be read at a given location (0) enter:

r0

> > > To call command options press:

CTRL-A

> > >         A white row will appear at the bottom of the window. 
> > >         To the right of the word "help" are the settings 
> > >         which should read 115200 8N1 (baud rate, configuration)
> > >         if other press: o (letter not number) to configure Minicom
> > >         select serial port setup and change the setting as needed
> > >         press return to exit to continuation menu and exit to return to minicom

> > > To access the menu/command list press:

z

> > > To "receive" the data as a file press:

r

> > > From the download menu select:

xmodem

> > > Enter a file name with the extension .bin
> > > When prompted hit any key to continue
> > > To quit press CTRL-A then "q" and select "yes"
> > > The file can be viewed without leaving the virtual machine using the Bless Hex Editor application

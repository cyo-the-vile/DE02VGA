# DE02VGA
VGA Card for DE0 and other Terasic Boards


This is a board created to get a 10 bit VGA video output from a DE0 development board by Terasic.  I wasn't satisfied with the limitation of the 4 bit resistor DAC that was included on the DE0 board.  This board solves that problem
Everything routed on the board has taken into account potential clock reflactions so there is a redriver resistor near the DAC for the pixel clock.

In addition, the BLANK line for the DAC must be controlled by the FPGA.  You could just hold it high (3.3V) the entire time or manually manipulate it in your processor design.
Everything was routed to about 60 ohm impedance for most FR4 fabrication processes.  You shouldn't have a problem outputting 1920*1080 resolutions (1080P) from this DAC card. If you will attempt faster pixel clocks and higher resolution video modes, I recommend changing the 33ohm resistor to 22 ohms.

This board uses the ADV7123 3 channel DAC.  The GM7123C is also compatible since that DAC is end of life.  

This card will work with the following Terasic brand development boards:
-DE0
-DE0-CV
-DE10 Nano
-DE2-115 (although redundant as it already has a 10 bit DAC)

This board was made to practice video processor design and the "graduate" card to this one would be an HDMI serializer chip.

To get this card assembled, zip the contents of the gerber folder and take to your preferential fabrication house.  FR4 processes are recommended.

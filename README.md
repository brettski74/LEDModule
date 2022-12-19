# LED Module
This is a design for a simple 3-LED lighting module that I designed for using in my 3D
printer enclosure. It uses CREE J2835 Series LEDs and runs on 11-14V input voltage, so
should run just fine off the 12V supply of many 3D printers.s

The design uses a simple two-transistor current regulator to set the LED current and
hold it steady across the entire input voltage range. The three LEDs are placed in
series and the LED current is set by R2, R3, R4 and R5. Multiple resistors are used to
handle the power dissipation without resorting to more expensive higher power SMD
resistors. Typical setup is to use 3 x 91k resistors for R2, R3 and R4 and leave R5
open. This gives a roughly 30 ohm shunt which gives a roughly 20mA LED current. If you
want to set a different LED current, you can alter the resistors used for R2, R3, R4
and R5, which are placed in parallel and form the shunt resistor of the regulator. The
LED current can be approximated by the formula:

    0.6V / Rshunt


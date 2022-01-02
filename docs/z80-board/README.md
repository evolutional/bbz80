# Z80 CPU Board

A Z80 CPU board for a `RC2014 v1.0` compatible bus.

Loosely based on the [RC2014 Z80 CPU v2.1](https://rc2014.co.uk/modules/z80-cpu-v2-1/) module but using stripboard.

![./z80-board.png](Board image)

The main change is an explicit pullup on the `/RST` pin. The 10nF decoupling capacitor should be wired between pins 11 and 29 on the underside of U1. Alternatively, straddle it across lines 17 and 18 of the bus.

I've gone for using jumper wires on the stripboard rather than a "true" stripboard layout. This makes the board smaller and easier to wire, at the expense of it being uglier and a little more fragile.

The signals for the `RC2014 v2.0` bus are broken out into a separate header row on the top of the board.

The stripboard file is created in [DIY Layout Creator](https://bancika.github.io/diy-layout-creator/). This is my favourite tool for stripboard layouts.

## BOM

Part | Count | Description
--- | --- | ---
R1-R5 | 5 | 10K Ohm wire resistor
H1 | 1 | 40-pin right angled 0.1" SIL pin header
H2 | 1 | 10-pin right angled 0.1" SIL pin header
S1 | 1 | 40-pin 0.6" DIP socket
U1 | 1 | 40-pin Z80 CPU
C1 | 1 | 10nF Ceramic Capacitor


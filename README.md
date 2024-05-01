# "Smart Servo" Protocol
## GoBuila and REV servos
Servos like REV's [Smart Robot Servo](https://www.revrobotics.com/rev-41-1097/) and GoBuilda's [Dual Mode Servo](https://www.gobilda.com/2000-series-dual-mode-servo-25-2-torque/) can be programmed using a programmer like [this one from REV](https://www.revrobotics.com/rev-31-1108/)

Interestingly, these servos can actually send feedback to the programmer, despite only having a single signal wire. This is accomplished through a protocol known as ["Dynamixel 1.0"](https://emanual.robotis.com/docs/en/dxl/protocol1/), which is a simple layer over half-duplex UART.

There are many varients of the Dynamixel protocol, but both the REV and GoBuilda servos appear to be completely compatible with each other. 
They operate at 76923 baud, and appear to use the standard read and write commands to manipulate the control table.

**TODO: Document control table**

| Address | Description | Volatile | Default |
|---------|-------------|----------|---------|
| 0x00    | TODO        | X        | 0x01    |

## Axon servos
Axon servos also use the Dynamixel protocol, but at a different baud rate and apparently using proprietary extension commands to the protocol to allow writing firmware.

**TODO: Document control table and baud rate for Axon servos**

| Address | Description | Volatile | Default |
|---------|-------------|----------|---------|
| 0x00    | TODO        | X        | 0x01    |

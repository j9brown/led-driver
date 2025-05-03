# LED Driver

Drives 4 RGB/W LEDs with PWM for a total of up to 3 A controlled over an I2C bus.

## Design

This design is based around a [PCA9685](https://www.nxp.com/docs/en/data-sheet/PCA9685.pdf) I2C PWM chip with 16 channels.  Each channel drives an N-channel MOSFET low-side switch.  Each group of 4 channels and a positive common rail feeds a JST XH 5-pin connector to which an RGB/W LED lamp may be attached.

The I2C bus must be referenced to the same ground as the negative input.

The board is designed for use with a 12 V nominal power supply but should work with anything from about 5 V to 16 V.  It includes a 3 A polyfuse and transient voltage suppression.  In case of reverse polarity connection, the TVS shunts the power input across the polyfuse.

## Notice

The software, documentation, design, and all copyright protected artifacts are released under the terms of the [MIT license](LICENSE).

The hardware is released under the terms of the [CERN-OHL-W license](hardware/LICENSE).

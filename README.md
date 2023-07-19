# Duofern NRF905 driver
This is a Protocol driver for Rademacher Duofern using a NRF905 chipset

## About
Duofern devices use a Nordic Semiconductor NRF905 chipset for their radio transmission. This project uses such a chipset to communicate with Duofern devices using a Raspberry Pi or any other Linux device with SPI and interrupt GPIOs.

NRF905 chipsets are widely available and cost including shipping around 10 €. A Duofern USB stick or Rademacher Bridge is obsolete.

## Current status
What works is sending and receiving packets from and to Duofern devices. Including Rademacher's own understanding of redundancy checks.
For example, I could turn on and off a switch actor.

Future work is a better understanding of the redundancy checks, which currently with with a hash table. Re-tries and listen-before-send (using the NRF905 carrier detect PIN) are to be implemented.

Emulation for a USB stick would be great. This would allow implementations for Home Assistant and FHEM to work with this project.

Also, there is no support for 10-byte addresses and their encryption.

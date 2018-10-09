# Arduino IR Remote Copier

Copy an Infra Red Remote Signal from Surrounding and Relay it later.

## What is it?

A device that records an IR Remote (TV, A/C, IR Copters, other appliances) that is being used in the surrounding and then transmitts the same signals whenever desired.
You can record multiple signals from various devices.

## Why is it?

With this you can,

1. Copy multiple remotes into one device.
2. Download the codes from [internet](http://www.lirc.org/) and use it if you have lost the device.
3. :)

## How does it work?

The device uses an array of 38kHz IR recievers to recieve single or multi-directional signal._(based on how you arrange them)_.
It stores the data in program/flash memory and them transmittes it back whenever desired using an IR LED's. _You can also use a parallel LED toroid mesh to blash strong signals in all direction._

This uses the Arduino's IRRemote.h library to detect if the recieved IR signals have a known pattern. If so the decoded pattern is short and easier to save.
Else we use the raw value. The raw values are usually big and depending on your device we may not be able to store them in RAM _(I used Nano v3 which had only 2 KB of SRAM)_. But dont worry the raw values can still be stored in Flash memory or buffered serially.

**NOTE:** As of now the read and write are seperate programs, and I am using an Android serial monitor _(there are many in Google play store)_ to read the data. Feel free to merge the 2 codes together if you want.  

## Using Locally

If you want to run this project locally,

### Requirements

1. An Arduino device with a connector.
2. A system to flash the programs.
3. One or more IR LED. _1 Watt or multiple parallel LEDs may may damage the board. Use a driver circuit or alteast a simple load transistor._
4. One or more IR Recievers. _Google TSOP._
5. Connectors.

### Build

**To Do:** Upload Circuit.

## Device

The device using Arduino Nano. You can use any other board too.

![](/docs/ir-packed.jpg)

![](/docs/ir-opening.jpg)

![](/docs/ir-front.jpg)

![](/docs/ir-inside.jpg)

## Licence

Licenced under GNU GENERAL PUBLIC LICENSE v3.0. It is free to copy and distribute.

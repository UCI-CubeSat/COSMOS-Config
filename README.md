# Overview

These are the config files for interfacing with the flight computer. Currently, they include configurations for connecting to the STM32 via a Serial, and reading the IMU packet.

# Usage
First, install Ball Aerospace COSMOS, and follow the getting started guide to get familiar with the tool. Set up a new project, and clone this repository into the config/targets folder. Go into the `cmd_tlm_server.txt` file, and change `com7` to the com port of your USB-Serial converter. Then, connect the STM32 running the flight computer firmware through the USB-Serial converter, and verify that packets are coming in.

# Packets
-IMU Packet - opcode(0x01), roll(uint16), pitch(uint16), yaw(uint16)

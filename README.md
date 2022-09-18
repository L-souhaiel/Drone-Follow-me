# Drone-Follow-me

This repo contains the firmware for a quadcopter (drone) running on esp32 microcontroller.

# Drone System Design

A simple drone has 4 motors (brushless motors), 1 gyroscope, 1 mcu and 1 battery. Those are the basic components to provide simple functionalities like take off, stabilizing, landing etc..
Please note the mcu used (in our case the esp32) needs a wireless communication to command the drone via pc or phone.
For Commanding the drone on top of the esp32, two wireless communication protocols could be used:
* bluetooth(Serial): not recommended for reliability
* Wifi(tcp/ip): recommended and will be used for the firmware
# Drone-Follow-me

This repo contains the firmware for a quadcopter (drone) running on esp32 microcontroller.

# Drone System Design

A simple drone has 4 motors (brushless motors), 1 gyroscope, 1 mcu and 1 battery. Those are the basic components to provide simple functionalities like take off, stabilizing, landing etc..
Please note the mcu used (in our case the esp32) needs a wireless communication to command the drone via pc or phone. 

# Communication with the Drone
For Commanding the drone on top of the esp32, many wireless communication protocols could be used:
* bluetooth(Serial): not recommended for reliability issues
* Wifi(tcp/ip): recommended and will be used for the firmware
* telemetry and RF: will be included in next version

# Esp32 as Web Server
The Esp32 can be used as a webserver to controll the drone.
Two concepts are discussed here:
- 1. host a simple server (no web interface). a client app connect to the server and send commands to drive the drone. (easy solution)
- 2. host a complete web interface for client. the webpage could be opened on a browser from any client connected to the network. (requires front-end (html, css, javascript)) 

# Drone system architecture
For any given solution, the backend design shall remain the same independant from  the frontend and shall be scalable(when adding more ressources) and portable(when switching to other platforms).
From a high level point of of view,  the following design describes a drone:
[simple drone design](ressources/Untitled%20Diagram.drawio.png)
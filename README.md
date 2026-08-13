# Automated Material Sorting System

## Overview

The **Automated Material Sorting System** is an embedded system designed to automatically identify and sort different types of waste.

The system uses an **ESP32 microcontroller** together with inductive, capacitive and ultrasonic sensors to identify materials and control a mechanical sorting mechanism using four servo motors.

The project combines **embedded software, electronics, PCB design and mechanical control** into a single automated system.

## Features

* Automatic material detection
* Metal detection using an inductive sensor
* Non-metal material detection using a capacitive sensor
* Ultrasonic sensing for object detection
* Automated mechanical sorting
* Four servo motors for material routing
* ESP32-based embedded control
* Custom PCB designed using KiCad
* Separate collection compartments for different materials

## System Architecture

```text

                            ^
                            |
          +-----------------+-----------------+
          |                 |                 |
          v                 v                 v
   +-------------+   +-------------+   +-------------+
   |  Inductive  |   | Capacitive  |   |  Ultrasonic |
   |   Sensor    |   |   Sensor    |   |   Sensor    |
   +-------------+   +-------------+   +-------------+
          +-----------------+-----------------+
                            |                 
                            |                                       
                            |
                            v
                  +-------------------+
                  |       ESP32       |
                  |                   |
                  |  Embedded Control |
                  +---------+---------+
                            |
                            v
                   +----------------+
                   | Material       |
                   | Classification |
                   +-------+--------+
                           |
                           v
                  +-------------------+
                  | Servo Actuators   |
                  |                   |
                  |   4 x SG90        |
                  +---------+---------+
                            

     

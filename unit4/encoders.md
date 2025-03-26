---
title: Introduction to Encoders
layout: home
parent: Sensors and Encoders
nav_order: 2
---

# Introduction to Encoders

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## What is it?

An encoder is a device that detects motion and generates an electrical signal to provide feedback on the position, speed, and direction of a system by converting physical movement into electrical pulses.

## How Encoders Works

In the XRP Minibot, a type of encoder is used called a *quadrature encoder*, which uses two signals to track movement accurately.

### Two DIO Ports

*Pulse* — A cycle of alternating high (with voltage) and low (no voltage) electrical signals.

Encoders connect to the robot’s control board using two *Digital Input/Output (DIO)* pins, labeled Channel A and Channel B. Pulses are sent to these channels and the timing and sequence of the high and low pulses help to provide information on position, speed, direction, etc. of a system.

## Initializing Encoders

To use an encoder, you need to initialize it in your code by specifying the two DIO ports it is connected to. For example:

```java
// Initializing an encoder connected to DIO ports 0 and 1
Encoder encoder = new Encoder(0, 1);
```

## Key Methods of Encoders

Encoders offer several useful methods.

- `getDistance()`: 
    - Returns the total distance the robot has traveled, calculated by counting the pulses from the encoder.
  
- `getRate()`: 
    - Returns the minibot's speed in distance per second based on the encoder's pulse rate.
  
- `getStopped()`:
    - Determine if the encoder is stopped.
  
- `getDirection()`: 
    - Returns the direction in which the encoder last moved
  
- `get()`:
    - Returns the current pulse count from the encoder.

- `reset()`: 
    - Reset the Encoder distance to zero. 

## Configuring Encoders

These methods can be used to configure the encoders.

- `setDistancePerPulse(double distancePerPulse)`: 
    - Configures the encoder to return a specific distance for every pulse.
    - Example: `setDistancePerPulse(4.0/256.0)` sets the distance per pulse to 4 units for every 256 pulses.
  
- `setMinRate()`: 
    - Configures the encoder to consider movement stopped if the rate of movement drops below a certain threshold.

## Activity

Look at the `Drivetrain.java` file located in the `subsystems` folder. How are encoders used in the `Drivetrain` subsystem?

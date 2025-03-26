---
title: Drivetrain
layout: home
parent: Arm and Drivetrain
nav_order: 3
---

# Drivetrain

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## What is it?

The main body of the XRP Minibot is called the Drivetrain, as it houses the two powered wheels that enable the robot to move. The robot also features front casters, small swiveling wheels that provide support and aid in maneuverability. These casters are not powered. The XRP robot turns using both skid-steering and differential drive, a method in which the wheels on one side rotate faster or slower than those on the other. This causes the robot to pivot in the direction of the turn, and can result in the wheels and front casters skidding or slipping depending on the friction of the surface.

## Code

In the `subsystems` folder of the XRP Minibot template code, there is a file called `Drivetrain.java`. 

The [encoders](/unit4/encoders.html) and drive motors are initialized in the constructor of the Drivetrain and in the fields. It can be observed in the code that the `Drivetrain` uses differential drive.

The Drivetrain class provides several key methods to control and monitor the robot’s movement. 
- `arcadeDrive(double xaxisSpeed, double zaxisRotate)`  
    - Uses the `xaxisSpeed` for forward/backward movement and `zaxisRotate` for turning left/right. The robot will continue moving and turning based on these inputs until the values change.

- `getLeftEncoderCount()`  
    - Returns the raw encoder count for the left side of the robot.

- `getRightEncoderCount()`  
    - Returns the raw encoder count for the right side of the robot.

- `resetEncoders()`  
    - Resets the encoder counts for both sides of the robot to zero.

- `getLeftDistanceInch()`  
    - Returns the distance traveled by the left wheel in inches.

- `getRightDistanceInch()`  
    - Returns the distance traveled by the right wheel in inches.

- `getAverageDistanceInch()`  
    - Calculates and returns the average of the left and right distances in inches.

- `getAccelX()`  
    - Returns the robot’s acceleration along the X-axis in terms of gravity (G).

- `getAccelY()`  
    - Returns the robot’s acceleration along the Y-axis in terms of gravity (G).

- `getAccelZ()`  
    - Returns the robot’s acceleration along the Z-axis in terms of gravity (G).

- `getGyroAngleX()`  
    - Provides the robot’s orientation around the X-axis in degrees.

- `getGyroAngleY()`  
    - Provides the robot’s orientation around the Y-axis in degrees.

- `getGyroAngleZ()`  
    - Provides the robot’s orientation around the Z-axis in degrees.
    
- `resetGyro()`  
    - Resets the gyro to its default state, useful for recalibrating the robot's orientation.


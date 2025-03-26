---
title: Arm
layout: home
parent: Arm and Drivetrain
nav_order: 2
---

# Arm

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## What is it?

The arm is a type of subsystem in the XRP Minibot.The arm of the minibot is controlled by a servo in the robot, and the angle can be controlled from 0-180 degrees. 

## Code

In the `subsystems` folder of the XRP Minibot template code, there is a file called `Arm.java`. 

```java
/**
* Set the current angle of the arm (0 - 180 degrees).
* @param angleDeg Desired arm angle in degrees
*/
public void setAngle(double angleDeg) {
    m_armServo.setAngle(angleDeg);
}
```

One of the methods in the file is `setAngle(double angleDeg)` which takes in an angle in degrees as a parameter and sets the angle of the arm's servo to the given angle.

Feel free to explore the file to understand it further.
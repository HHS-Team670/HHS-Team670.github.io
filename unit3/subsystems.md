---
title: Subsystems
layout: home
parent: Arm and Drivetrain
nav_order: 1
---

# Subsystems

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Introduction to Subsystems

A subsystem is an abstraction for a collection of robot hardware that operates together as a unit and is designed to handle a specific task. 

## Creating Subsystems

```java
import edu.wpi.first.wpilibj2.command.SubsystemBase;

public class SubsystemExample extends SubsystemBase {
    /** Creates a new SubsystemExample. */
    public SubsystemExample() {}

    @Override
    public void periodic() {
        // This method will be called once per scheduler run
    }
}
```

To create a basic subsystem, a new class must be created that extends `SubsystemBase`. This requires importing `SubsystemBase` from the WPILib library. 

In the constructor of a subsystem, initialize hardware components and set their default states or values.

## Periodic

Subsystems have a `periodic()` method that is called once per scheduler iteration, which is typically every 20 milliseconds. It overrides the `periodic()` method from `SubsystemBase`.

```java
@Override
public void periodic() {
    // This method will be called once per scheduler run
}
```
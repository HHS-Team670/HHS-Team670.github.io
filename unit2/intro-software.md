---
title: Introduction to Software
layout: home
parent: Hardware and Software
nav_order: 5
---

# Introduction to Software

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## AutonomousDistance

The robot is controlled by code that you have cloned from the repository in the previous section. Navigate to the file called AutonomousDistance.java. The path should be `XRPminibots/src/main/java/frc/robot/commands/AutonomousDistance.java`. 

There should be some code in the file, which should look similar to this.

```java
package frc.robot.commands;


import frc.robot.subsystems.Drivetrain;
import edu.wpi.first.wpilibj2.command.SequentialCommandGroup;


public class AutonomousDistance extends SequentialCommandGroup {
  /**
   * Creates a new Autonomous Drive based on distance. This will drive out for a specified distance,
   * turn around and drive back.
   *
   * @param drivetrain The drivetrain subsystem on which this command will run
   */
  public AutonomousDistance(Drivetrain drivetrain) {
    addCommands(
        new DriveDistance(1, 20, drivetrain),
        new TurnDegrees(-1, 90, drivetrain),
        new DriveDistance(2, 15, drivetrain),
        new TurnDegrees(5, 45, drivetrain),
        new DriveDistance(1, 10, drivetrain)
    );
  }
}
```

## Explaining the Code

The `AutonomousDistance` class inherits from `SequentialCommandGroup` because it extends that class. The `SequentialCommandGroup` executes commands in a specific sequence. Inside the `AutonomousDistance` class, a constructor is defined that takes a `Drivetrain` parameter, which controls the robot's movement. Within the constructor, the `addCommands()` method is used to add multiple commands in a sequence.

A method is a block of code that performs certain actions when called. In this case, the `addCommands()` method includes several commands that instruct the Drivetrain to carry out actions in a particular order. The commands will be run in the order they are passed into `addCommands()`. For example, the code first tells the robot to drive a specific distance at a certain velocity, then it commands the robot to turn a set number of degrees with a certain speed, and so on. Each command in the sequence is executed one after the other, guiding the robot through a series of movements.

## Try it Yourself

Now, try to Simulate the Robot Code, and select the Autonomous mode.

<details>
  <summary>What happens?</summary>
  The XRP Minibot should move around on its own, driving forward and turning.
</details>

Feel free to play around with the code and the code inside the parenthesis, or arguments, of `addCommands()`. What changes? 
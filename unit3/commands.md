---
title: Introduction to Commands
layout: home
parent: Arm and Drivetrain
nav_order: 4
---

# Introduction to Commands

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}


## What is it?

The XRP Minibot template code includes many commands to control the Arm and DriveTrain of the robot. For example, an important command for the minibot is called `DriveDistance`, which allows the robot to drive for a specific distance and velocity. 

Commands have various capabilities. For example, commands can run initial autonomous movement, drive the robot a certain distance, and turn the robot for a certain number of degrees or seconds. Using these pre-created commands, you can move the robot’s Drivetrain whichever way you want as long as it’s within the robot’s constraints. Some of these pre-created commands include `DriveDistance`, `DriveTime`, `TurnDegrees`, and `TurnTime`.

There is also the `SequentialCommandGroup`. Classes that extend or inherit from `SequentialCommandGroup` run commands in sequential order. In the constructor of those classes, the method `addCommands()` is called where the commands are passed as arguments and will be run in the exact order they are listed. Some examples of classes that inherit from `SequentialCommandGroup` include `AutonomousDistance` and `AutonomousTime`.


This is a format of a basic command. All commands created extend the Command class, and the methods in the subclass, CommandName, override methods from the superclass Command. For example, the initialize(), execute(), end(), and isFinished() methods can be overridden. Here is a format of a potential command named CommandName.




## Command Structure

```java 
package frc.robot.commands;
import edu.wpi.first.wpilibj2.command.Command;


public class CommandName extends Command {
  public CommandName() {}

  // Called when the command is initially scheduled.
  @Override
  public void initialize() {}

  // Called every time the scheduler runs while the command is scheduled.
  @Override
  public void execute() {}

  // Called once the command ends or is interrupted.
  @Override
  public void end(boolean interrupted) {}

  // Returns true when the command should end.
  @Override
  public boolean isFinished() {}
}
```

This is a format of a basic command. All commands created extend the Command class and inherit its methods. To specify what a command will do in its states, the `initialize()`, `execute()`, and `end()` methods must be overriden. To tell the scheduler when the command has finished execution, the `isFinished()` method should be overriden.

{: .note}
> The `initialize()`, `execute()`, and `end()` methods are defaulted to do nothing, while `isFinished()` is defaulted to return false. This means it will continue to run forever, unless interrupted.

### initialize()

The `initialize()` method is called once when a command is scheduled, setting it up for execution. It prepares the command's state and resources, which should not be done in the constructor, as the constructor is only called once, while the command may be used multiple times.

### execute()

The `execute()` method runs repeatedly while the command is scheduled, typically called every 20 milliseconds in the robot's main periodic method. 

### end(bool interrupted)

The `end(bool interrupted)` method is called once when the command ends, either by completing or being interrupted. It is used to clean up the command's state and reset any necessary values.

## isFinished()

The `isFinished()` method is called repeatedly during execution. The `isFinished()` method checks if the command has completed its task. It runs after the `execute()` method and when it returns true, the command ends, triggering the `end()` method.







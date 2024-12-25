---
title: Running the Minibot
layout: home
parent: Hardware and Software
nav_order: 4
---

# Running the Minibot

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Project

This lesson covers how to run the XRP Minibot and make it move around. To start off, it is important to clone the template code for the XRP Minibot.

### Cloning Template Code

<!---
TODO:
Link to template code repo
-->

To clone the template code, follow these steps.

1. Visit [this repository](https://github.com/HHS-Team670/2024-Minibots).
2. Click the green "Code" button on the screen. 
3. Copy the HTTPS link. 
4. Change the current working directory to the location where you want the cloned directory. You can do this using the `cd` command.
5. Type `git clone`, and then paste the URL you copied earlier and press enter.
> `git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY` 

The code should now be cloned. To access the template code in WPILib VSCode, launch the WPILib VSCode application and click the "File" button in the top left corner. Then, click "Open Folder" and open the folder containing the cloned code. The code should now show up on the screen, ready for editing.

### Turning on/off the Minibot

![XRP Power Switch](https://docs.wpilib.org/en/stable/_images/xrp-power-switch.webp)

To power on the XRP Minibot, find the on/off switch as shown in the image above and slide the knob to the desired position: "on" to power it up or "off" to turn it off.

### Connecting to the Minibot

<!---
TODO:
* Exact WiFi names
* Could work on explaining better
* Images
-->

To communicate with an XRP Minibot, connecting to the minibot's WiFi network is required. For a Team 670 Minibot, the WiFi network is typically named with the Minibot's number (which can be found on the robot) with the password "team670".

### Running the Minibot with a Controller

To run the minibot with an Xbox controller, begin by connecting the Xbox controller to the computer using Bluetooth or a wired connection. Open WPILib VS Code and navigate to the cloned code. Press `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (macOS) to open the command palette, then type and select "WPILib: Simulate Robot Code". After a short time, a simulation window should appear if everything is set up correctly.

In the simulation window, locate the Joysticks[0] item in the interface. Drag Joysticks[0] to the System Joysticks section to establish the controller connection. Next, switch to the teleop mode, which will allow the Xbox controller to manually control the XRP Minibot.

The goal is to maneuver the robot and determine how to move the minibot forward, move it backward, and rotate it.
















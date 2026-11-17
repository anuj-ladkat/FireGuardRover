# FireGuard Rover – Smart Autonomous Firefighting Robot

An intelligent robotic vehicle designed to detect fire and smoke, autonomously navigate towards potential fire sources, and activate a water-based suppression mechanism. The system also integrates GSM-based communication to send emergency SMS alerts and initiate phone calls, enabling faster response to fire incidents.

## Project Overview

Fire accidents can cause significant damage to human life and property, particularly in environments where immediate human intervention is difficult.

**FireGuard Rover** aims to address this challenge through an autonomous firefighting robot equipped with fire and smoke detection sensors, obstacle detection capabilities, a motorized navigation system, and an automatic water-spraying mechanism.

Built around an Arduino Uno microcontroller, the robot continuously monitors its surroundings, detects potential fire hazards, navigates towards the detected source, and activates its suppression mechanism. It also notifies the property owner through GSM-based SMS and call alerts.

## Key Features

- **Fire Detection:** Detects fire using flame sensors.
- **Smoke and Gas Detection:** Monitors the environment for smoke or gas hazards.
- **Autonomous Navigation:** Moves towards detected fire sources.
- **Obstacle Detection:** Uses sensors to identify obstacles and adjust movement.
- **Automatic Fire Suppression:** Activates a water pump to spray water towards the fire.
- **Servo-Controlled Spraying:** Sweeps the water outlet to improve coverage.
- **GSM Communication:** Sends emergency SMS notifications and initiates phone calls.
- **Real-Time Monitoring:** Continuously monitors sensor readings and responds to detected hazards.

## Hardware Components

| Component | Purpose |
|---|---|
| Arduino Uno | Main microcontroller |
| Flame Sensors | Fire detection |
| Gas Sensor | Smoke/gas detection |
| Obstacle Sensors | Obstacle detection |
| DC Motors | Robot movement |
| Motor Driver | Motor control |
| Water Pump | Fire suppression |
| Servo Motor | Controls water-spraying direction |
| GSM Module | SMS and call notifications |
| Robot Chassis | Physical platform |
| Battery | Power supply |

*Note: The component list represents the system architecture. Refer to the actual hardware implementation for exact module models and quantities.*

## System Architecture

The system operates through five primary stages:

1. **Initialization:** Initializes serial communication, GSM module, sensors, motors, and servo motor.
2. **Continuous Monitoring:** Continuously reads sensor values to identify fire, smoke, gas, and obstacles.
3. **Fire Detection and Navigation:** Detects potential fire hazards and controls the motors to navigate towards the target.
4. **Fire Suppression:** Stops the motors, activates the water pump, and moves the servo motor to distribute water.
5. **Emergency Notification:** Sends an SMS alert and initiates a phone call to a predefined contact number.

## Working Principle

```text
       System Initialization
                |
                v
        Initialize Sensors
                |
                v
       Continuous Monitoring
                |
                v
       Fire / Smoke Detected?
           /          \
         No            Yes
         |              |
         v              v
   Continue         Activate
   Monitoring       Navigation
                        |
                        v
                 Navigate Towards
                   Fire Source
                        |
                        v
                 Activate Water
                  Suppression
                        |
                        v
                 Servo-Controlled
                    Water Spray
                        |
                        v
                  Send SMS Alert
                        |
                        v
                   Initiate Call
                        |
                        v
                       End
```

## Control Algorithm

The robot follows a sensor-driven control algorithm:

1. Initialize all sensors and communication modules.
2. Configure motor control pins and servo motor positioning.
3. Continuously monitor sensor readings.
4. Check for obstacles and determine the appropriate motor movement.
5. Detect gas or smoke and send an SMS notification.
6. When fire is detected:
   - Stop the motors.
   - Activate the water pump.
   - Sweep the servo motor to distribute water.
   - Deactivate the pump after the suppression cycle.
   - Send an emergency SMS and initiate a phone call.
7. Continue monitoring the environment.

## Technology Stack

| Technology | Application |
|---|---|
| Arduino Uno | Embedded system control |
| Embedded C/C++ | Robot programming |
| GSM Communication | Emergency notifications |
| Sensor Integration | Fire, gas, and obstacle detection |
| DC Motor Control | Robot movement |
| Servo Control | Water-spraying mechanism |

## Applications

- Industrial fire safety monitoring
- Warehouses and storage facilities
- Residential fire hazard monitoring
- Laboratories and workshops
- Environments requiring remote fire detection
- Preliminary firefighting assistance in hazardous areas

## Future Improvements

Potential enhancements include:

- Integration of computer vision and deep learning for improved fire detection.
- Thermal imaging cameras for detecting heat signatures.
- GPS-based location tracking and remote monitoring.
- IoT dashboard for real-time system status.
- Improved autonomous navigation algorithms.
- Wireless video streaming and remote operation.
- Advanced fire suppression mechanisms for different fire categories.

## Research Publication

This project is based on the research paper:

**Smart Firefighter Robot Car with Automatic Fire Detection and Suppression**

- **Authors:** Anuj Ladkat, Manoj Reddy, Varun Kolte, Yusra Khan, and Nandkumar Kulkarni.
- **Institution:** MIT School of Computing, MIT Art, Design and Technology University, Pune.

## Disclaimer

FireGuard Rover is an academic prototype developed for research and educational purposes. It is not a replacement for certified fire detection systems, professional firefighting equipment, or emergency response services. Its effectiveness depends on sensor accuracy, hardware configuration, environmental conditions, and testing.

## Contributors

- **Anuj Ladkat**
- Manoj Reddy
- Varun Kolte
- Yusra Khan
- Nandkumar Kulkarni

---

If you find this project interesting, consider giving the repository a star.

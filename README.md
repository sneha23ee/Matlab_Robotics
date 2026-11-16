# Matlab_Robotics
Developed a 2-DOF robotic manipulator using MATLAB, Simulink, and Simscape Multibody. Implemented joint motion simulation and forward kinematics to analyze end-effector positioning through coordinate transformations.
# 2-DOF Robotic Manipulator Modeling and Forward Kinematics using MATLAB & Simulink

## Project Overview

This project focuses on modeling and simulating a two-degree-of-freedom (2-DOF) robotic manipulator using MATLAB and Simulink. The robotic mechanism is developed using Simscape Multibody to represent the mechanical structure, joints, links, and end-effector.

The project explores robotic motion through joint-angle inputs and studies the resulting end-effector position using forward kinematics and coordinate transformation techniques.

## Objectives

- Develop a 2-DOF robotic manipulator model using Simscape Multibody.
- Understand the relationship between joint motion and end-effector position.
- Implement forward kinematics to determine end-effector coordinates.
- Analyze the transformation between the robot base and end-effector.
- Simulate joint movements using time-varying input signals.
- Visualize and monitor the robot's motion and output signals.

## System Architecture

The simulation consists of the following main components:

1. **Joint Input Generation:** Sinusoidal signals generate time-varying joint inputs.
2. **Mechanical Modeling:** Simscape Multibody represents the robot's base, links, joints and end-effector.
3. **Joint Configuration:** Joint inputs control the robotic manipulator's movement.
4. **Forward Kinematics:** The end-effector transformation is obtained relative to the robot base.
5. **Coordinate Transformation:** The homogeneous transformation is converted into a translation vector.
6. **Output Monitoring:** Scope blocks are used to observe the simulation signals.

## MATLAB / Simulink Implementation

The model includes:

- Simulink signal generators for joint inputs.
- Simscape Multibody mechanical components.
- Revolute joint connections.
- Mechanism Configuration and Solver Configuration blocks.
- Get Transform block.
- Coordinate Transformation Conversion block.
- Scope-based signal monitoring.

### Joint Input Configuration

| Parameter | Joint 1 | Joint 2 |
|---|---:|---:|
| Input type | Sine wave | Sine wave |
| Amplitude | 1.3 | 0.6 |
| Frequency | Not explicitly specified | 0.7 rad/s |

## Forward Kinematics

Forward kinematics determines the position and orientation of the robotic end-effector based on the joint variables.

For a planar 2-link manipulator, the general position equations are:

\[
x=L_1\cos(q_1)+L_2\cos(q_1+q_2)
\]

\[
y=L_1\sin(q_1)+L_2\sin(q_1+q_2)
\]

Here:

- \(L_1,L_2\): Link lengths
- \(q_1,q_2\): Joint angles
- \(x,y\): End-effector coordinates

*Note: These equations illustrate the general planar 2-link case. The exact coordinate convention and link parameters should be verified against the Simscape model before treating them as its numerical output equations.*

## Technologies Used

- MATLAB
- Simulink
- Simscape
- Simscape Multibody
- Robotics System Toolbox (if used in the development environment)

## Repository Structure

```text
MATLAB-ROS-Robotics-Project/
│
├── README.md
├── MATLAB_Simulink/
│   └── Body.slx
│
├── Images/
│   ├── simulink_model.png
│   ├── robot_mechanism.png
│   └── simulation_output.png
│
├── Results/
│   └── simulation_results/
│
└── Documentation/
    └── Project_Report.pdf
```

## How to Run

1. Clone or download this repository.
2. Open MATLAB.
3. Navigate to the `MATLAB_Simulink` directory.
4. Open `Body.slx`.
5. Ensure the required MATLAB toolboxes and compatible Simscape libraries are installed.
6. Run the Simulink model.
7. Observe the joint motion and end-effector output signals.

## Applications

- Robotic manipulator modeling.
- Industrial automation.
- Robot motion analysis.
- Forward kinematics and coordinate transformations.
- Robotics simulation and control development.

## Future Scope

- Integration of ROS for robotic communication and control.
- Implementation of inverse kinematics.
- Real-time joint control.
- Robot visualization using ROS-compatible tools.
- Hardware implementation using a physical robotic manipulator.

---

**Project Category:** Robotics | MATLAB | Simulink | Forward Kinematics | Simulation

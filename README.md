# 🤖 Autonomous Line Follower Robot

## 📌 Overview

This project presents the design and implementation of an autonomous line follower robot capable of navigating a predefined path using infrared sensing. The robot detects contrast differences between a guiding line and the surrounding surface, enabling real-time path correction through differential motor control.

The system is built around the Arduino Uno microcontroller and integrates a dual-sensor feedback mechanism with a motor driver to control four DC motors. A custom chassis was designed in Autodesk Fusion 360 and fabricated using 3D printing, ensuring a compact, robust, and modular structure.

## 🧰 Hardware Components
-The system consists of the following key components:
-Microcontroller: Arduino Uno
-Sensors: 2 × Infrared (IR) line tracking sensors
-Actuators: 4 × 3–6V DC motors with wheels
-Motor Driver: L298N dual H-bridge module
-Structure: Custom-designed 3D printed chassis (Fusion 360)
-Power Supply: Battery pack
-Interfacing: Jumper wires and connectors

## 🏗️ System Architecture

The robot operates as a feedback-driven embedded system where sensing, processing, and actuation are tightly integrated.
Control Flow:
IR Sensors → Arduino Uno → L298N Motor Driver → DC Motors → Robot Motion
The IR sensors continuously monitor the surface.
Sensor signals are processed by the Arduino.
Based on the input, control signals are sent to the motor driver.
The motor driver regulates motor direction and speed to maintain alignment with the path.

## 🚀 System Features

Real-time line detection and tracking
Differential drive control for smooth navigation
Compact and durable 3D-printed chassis design
Scalable architecture for future enhancements (e.g., PID control, additional sensors)
Energy-efficient and fully portable system

## 🔌 Hardware Integration

IR Sensors to Arduino
Left sensor output → Digital pin (e.g., D2)
Right sensor output → Digital pin (e.g., D3)
Power → 5V and GND
Motor Driver to Arduino
IN1, IN2 → Left motor control
IN3, IN4 → Right motor control
Connected to digital pins (e.g., D8–D11)
Motors to Driver
Left motors → OUT1 & OUT2
Right motors → OUT3 & OUT4
Power Distribution
External battery → L298N (motor supply)
Arduino powered via battery or USB interface

## ⚙️ System Operation

The robot follows a simple yet effective control logic:
The IR sensors detect the presence or absence of the line.
The Arduino processes sensor inputs in real time.
Motion decisions are made based on sensor states:
Both sensors detect the line → Forward motion
Left sensor loses the line → Adjust left
Right sensor loses the line → Adjust right
Both sensors lose the line → Stop or recovery behavior
Control signals are sent to the motor driver.
Motors respond accordingly to maintain path alignment.

## 🎥 Demonstration

Add demonstration video link here.# Line-Follower-IR
A simple line follower robot that uses IR sensors and an L298N motor driver to follow a specific path.

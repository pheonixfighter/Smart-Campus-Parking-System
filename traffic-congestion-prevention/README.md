# Traffic Congestion Prevention

## Module Description
Monitors the vehicle queue at the parking lot entrance. When a queue is detected (vehicles backing up beyond a threshold), this module signals the entrance gate and external traffic systems to stop admitting vehicles, preventing congestion from spilling onto adjacent roads.

---

## Assigned Member
Robert

## Language Used
Arduino C++

## Hardware/Device
An ESP32 S3 

## Sensors/Components
-Two HC-SR04 ultrasonic sensors


---

## FSM States

| State | Description |
|-------|-------------|
| `IDLE` | No queue detected — normal traffic flow allowed |
| `QUEUE_DETECTED` | Queue length exceeds threshold — begin congestion response |
| `STOP` | Halt new vehicle admittance; signal external traffic system to redirect |

### State Transition Diagram

![The State Transition diagram for the traffic congestion prevention unit](./docs/TrafficCongestionPreventionFSMDiagram.drawio)

---

## Interface/Communication
This module sends a DC signal to entrance gate module to tell it to not open when there is a vehicle detected on both sides of the gate

---

## How to Run/Build
### 1. Attatch the following component pins to the following ESP32 pins.  

2. 
2. 
2. 
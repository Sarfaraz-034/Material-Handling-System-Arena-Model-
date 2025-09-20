## Simulation of a Material Handling System using Arena
This project models a manufacturing system that incorporates material handling, developed using Rockwell Arena. The simulation analyzes the flow of parts through processing, quality control, and rework stations, with a focus on the impact of conveyors and transporters on system performance.

## 📝 Problem Statement
Parts enter the system for processing at two sequential stations: a CNC lathe and a CNC milling machine. Upon leaving the milling machine, finished products undergo a quality check.

Successful Quality Check: Products that pass the quality check are transported to a wire house by Transporter 1.

Failed Quality Check: Products that fail are sent to a rework station via Transporter 2.

Post-Rework: After rework, parts are moved to the wire house by Transporter 3.

Material Handling: Parts are moved between the arrival point, lathe, and milling machine by a conveyor. All transporters and the conveyor operate at a velocity of 15 m/min.

The system operates with the following parameters:

Part Inter-arrival Time: Follows an exponential distribution with a mean of 2 minutes (EXP(2)).

### Processing Times (in minutes):

CNC Lathe: Triangular distribution TRIA(7, 9, 11)

CNC Milling: Triangular distribution TRIA(10, 12, 15)

Rework Station: Triangular distribution TRIA(2, 3, 5)

Distances and Material Handling
From Station

To Station

Distance (m)

Material Handling Equipment

Arrival

CNC lathe



Conveyor

CNC lathe

CNC milling



Conveyor

Quality check

Wire house

100 m

Transporter 1

Quality check

Rework

100 m

Transporter 2

Rework

Wire house

100 m

Transporter 3

### 🎯 Project Objectives
The primary goals of this simulation are:

Develop a Model: Construct a comprehensive model of the manufacturing and material handling system using Arena.

Simulate and Visualize: Run the simulation to observe the system's dynamics and visualize the movement of parts.

Analyze Performance: Evaluate key performance measures by running the simulation for a specified number of replications.

### 🛠️ Model Details & System Logic
System Requirements: Windows OS and Rockwell Arena simulation software.

Entities: Parts.

Resources: Lathe operator, Milling operator, Rework operator.

Processes/Machines: CNC Lathe, CNC Milling, Rework.

Stations: Station 1 (and others as required for routing).

Process Action: The core logic for operations is Seize Delay Release.

Queue Discipline: All queues follow a First-Come, First-Served (FCFS) discipline.

### Arena Modules Used
The model is built using a combination of the following Arena modules:

Create

Assign

Station

Leave

Enter

Process

Decide

Dispose

### 🚀 How to Run the Simulation
Ensure you have Rockwell Arena installed on a Windows operating system.

Clone this repository or download the .doe model file.

Open the file in Arena.

Configure the simulation to run for the desired number of replications.

Run the simulation to generate the results report.

### 📊 Results & Analysis
After the simulation completes, Arena will provide a detailed report. This report can be used to analyze performance metrics such as resource utilization, throughput, cycle times, and queue lengths. Analyzing the results across multiple replications will provide statistically significant insights into the system's stability and efficiency.

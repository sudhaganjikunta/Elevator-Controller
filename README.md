# Elevator-Controller
The Elevator Controller is a Finite State Machine (FSM) based digital design that controls the movement of an elevator between multiple floors based on user requests. It receives floor requests, moves the elevator to the requested floor, opens the door for a fixed time, and then waits for the next request.

The design consists of three FSM states:

* IDLE – Waits for floor requests.
* MOVE – Moves the elevator up or down toward the requested floor.
* OPEN – Opens the elevator door for a fixed number of clock cycles before closing it.

The project demonstrates fundamental RTL design concepts such as FSM implementation, sequential logic, request handling, edge detection, register-based storage, and clock-driven control, making it suitable for beginners learning Verilog and digital design.

## Features
🚀 Verilog RTL implementation

🏢 Supports a 5-floor elevator

🔄 Finite State Machine (FSM) based control

⬆️⬇️ Automatic up/down movement

🚪 Automatic door open and close with timer

⏰ Synchronous design with asynchronous reset

🎓 Beginner-friendly RTL project for FPGA and simulation


### Inputs

Signal          	Width             	Description
clk	                1	                System clock
reset	              1	                Asynchronous reset
req               	5               	Floor request inputs (Floor 0–4) 

### Outputs

Signal	          Width	               Description
floor	              3                	Current elevator floor
up	                1	                Elevator moving upward
down	              1	                Elevator moving downward
door	              1	                Door open indicator 

## FSM States
State	Description
* *IDLE*	Waits for incoming requests
* *MOVE*	Moves elevator toward the requested floor
* *OPEN*	Opens the door for a fixed duration

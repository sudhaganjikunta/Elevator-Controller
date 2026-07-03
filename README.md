# Elevator-Controller
The **Elevator Controller** is a Finite State Machine (FSM) based digital design that controls the movement of an elevator between multiple floors based on user requests. It receives floor requests, moves the elevator to the requested floor, opens the door for a fixed time, and then waits for the next request.

The design consists of three FSM states:

* **IDLE** – Waits for floor requests.
* **MOVE** – Moves the elevator up or down toward the requested floor.
* **OPEN** – Opens the elevator door for a fixed number of clock cycles before closing it.

The project demonstrates fundamental RTL design concepts such as FSM implementation, sequential logic, request handling, edge detection, register-based storage, and clock-driven control, making it suitable for beginners learning Verilog and digital design.

---

### Features
🚀 Verilog RTL implementation

🏢 Supports a 5-floor elevator

🔄 Finite State Machine (FSM) based control

⬆️⬇️ Automatic up/down movement

🚪 Automatic door open and close with timer

⏰ Synchronous design with asynchronous reset

🎓 Beginner-friendly RTL project for FPGA and simulation

---

### Inputs

| Signal | Width | Description                                  |
| ------ | ----- | -------------------------------------------- |
| clk    | 1     | System clock used for sequential operation   |
| reset  | 1     | Asynchronous reset signal                    |
| req    | 5     | Floor request inputs from Floor 0 to Floor 4 |

---

### Outputs

| Signal | Width | Description                   |
| ------ | ----- | ----------------------------- |
| floor  | 3     | Current elevator floor number |
| up     | 1     | Indicates upward movement     |
| down   | 1     | Indicates downward movement   |
| door   | 1     | Indicates door open status    |


---
### FSM States
State	Description
* **IDLE**	Waits for incoming requests
* **MOVE**	Moves elevator toward the requested floor
* **OPEN**	Opens the door for a fixed duration

---


### Design Flow
```
Start

↓

Reset System

↓

Wait for Floor Request

↓

Store Request

↓

Move Elevator

↓

Reach Requested Floor

↓

Open Door

↓

Wait for Timer

↓

Close Door

↓

Check Remaining Requests

↓

If Requests Available → Move Again

↓

Else → Return to IDLE
```

---

### Applications

This project can be used as a learning model for several real-world applications, including:

* Residential elevator systems
* Commercial building elevators
* Shopping malls
* Hospitals
* Smart building automation
* Industrial lift systems
* FPGA-based embedded control systems
  
### Learning Outcomes

After completing this project, I will gain practical knowledge of:

* Verilog HDL programming
* RTL coding style
* Finite State Machine (FSM) design
* Sequential logic circuits
* Register-based data storage
* Request queue implementation
* Edge detection techniques
* Timing control using counters
* FPGA simulation and verification


---

### Future Enhancements

The current project can be extended with additional real-world features such as:

* Support for more than five floors
* Priority-based scheduling algorithm
* Simultaneous internal and external floor requests
* Emergency stop button
* Fire alarm mode
* Overload detection using weight sensors
* Floor display using seven-segment displays or LCDs
* Motor speed control
---

## Conclusion

The Elevator Controller using Verilog HDL demonstrates how a real-world control system can be modeled using digital design principles. By combining an FSM, request queue, edge detection, and timer-based door control, the project provides a clear understanding of sequential RTL design. It is well suited for FPGA implementation, academic laboratory exercises, and VLSI interview preparation, while also serving as a strong foundation for building more advanced elevator control systems with additional safety and scheduling features.

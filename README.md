# Microprocessor-Assignment

**Title** - Batch Weighing Machine

Design assignment for **Microprocessor Programming and Interfacing (CS F241)** course (BITS Pilani)

## Software requirements

| Software | Used for |
| --- | --- |
| [Proteus](https://www.labcenter.com/) | Simulating the actual hardware design and running the assembly code on it |
| [emu8086](https://download.cnet.com/Emu8086-Microprocessor-Emulator/3000-2069_4-10392690.html) | Compiling the assembly code to binary (which can be run on Proteus) |

## Report

The report contains -
- Problem statement
- Assumptions
- System Description
- Flowchart of the functioning
- Code
- Limitations
- Screenshots of simulation design

<a href="https://github.com/kunal-mohta/Microprocessor-Assignment/blob/master/report.pdf" target="_blank">View Report</a>

## Problems faced

- **Getting started with Proteus**
  - Due to lack of online resources/tutorials on using Proteus, it is difficult to wrap your head around it.
  - Finding out ways to debug your code while it is running on the hardware simulation, made things a bit easier.
- **Using Hardware Interrupts**
  - As there was never a practical implementation of hardware interrupts shown to us during the course lectures, so it took quite some time to figure out.
  
## Scope of improvements

- Polling is currently being used to wait for the **Read Weight** or **Stop Alarm** signal. This can be changed and made efficient using interrupts.
- As the Load cell components are not available in Proteus by default, potentiometer is used here. But it is not very accurate representation of what the actual structure of Load cell is like, and could be changed 
- When the weight is read again without changing the load, incorrect results are obtained. Debugging revealed it is due to some problem with the 8055 chip. More inspection and trails are needed to solve this.
- The **Read Weight** signal could be completely removed and the machine could be made real time, reading weights as and when the loads are changed.

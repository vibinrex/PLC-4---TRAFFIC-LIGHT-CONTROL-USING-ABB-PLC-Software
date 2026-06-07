# PLC-4---TRAFFIC-LIGHT-CONTROL-USING-ABB-PLC-Software

## Aim
To design and implement a traffic light control system using ABB PLC and ABB Automation Builder software.

## Objective
•	Control Red, Yellow, and Green traffic lights automatically. 
•	Implement a timed sequence for traffic signal operation. 
•	Understand PLC programming using ladder logic and timers. 

## Apparatus Required
•	ABB PLC 
•	ABB Automation Builder Software 
•	PC/Laptop 

## Theory
A traffic light control system regulates vehicle movement at road intersections. The PLC controls the ON/OFF operation of Red, Yellow, and Green lights using timers.
Signal Sequence
1.	Green Light ON – 10 seconds 
2.	Yellow Light ON – 3 seconds 
3.	Red Light ON – 10 seconds 
4.	Repeat the cycle continuously

## Procedure
1.	Open ABB Automation Builder. 
2.	Create a new PLC project. 
3.	Configure the PLC hardware. 
4.	Assign input and output addresses. 
5.	Create ladder logic using timers. 
6.	Compile the program. 
7.	Download the program to the PLC. 
8.	Place the PLC in RUN mode. 
9.	Observe the traffic light sequence.


## I/O Assignment

<img width="468" height="199" alt="image" src="https://github.com/user-attachments/assets/f83052de-bc8a-448c-8659-d7ee9c11a2bd" />

## Timer Configuration

<img width="468" height="142" alt="image" src="https://github.com/user-attachments/assets/8139fb06-8166-415e-93ae-499d7289a606" />

## Control Logic
### Step 1: Green Signal
•	Green lamp ON. 
•	Timer T1 starts. 
•	After 10 seconds, Green lamp OFF. 
### Step 2: Yellow Signal
•	Yellow lamp ON. 
•	Timer T2 starts. 
•	After 3 seconds, Yellow lamp OFF. 
### Step 3: Red Signal
•	Red lamp ON. 
•	Timer T3 starts. 
•	After 10 seconds, Red lamp OFF. 
•	Cycle repeats. 
 
## PROGRAM PLC_PRG
VAR
S3: BOOL;
L2: BOOL;
S2: BOOL;
M: BOOL;
RED: BOOL;
    TIMER1: TON;
delaY: TIME := t#10s60ms;
run_time: TIME;
s1: BOOL;
TIMER2: TOF;
L: TIME := T#10S;
T: TIME;
M2: BOOL;
YELLOW: BOOL;
INP: BOOL;
RESET: BOOL;
COUNT: WORD :=5;
CV: WORD :=0;
C1: CTU;
M5: BOOL;
GREEN: BOOL;
END_VAR


## Ladder Logic Concept
Start PB → T1 (10s) → Green Lamp ON

T1 Done → T2 (3s) → Yellow Lamp ON

T2 Done → T3 (10s) → Red Lamp ON

T3 Done → Return to T1





## Output
<img width="1600" height="825" alt="image" src="https://github.com/user-attachments/assets/860bee81-5aac-4a0c-85b4-28578333cd40" />


<img width="1600" height="859" alt="image" src="https://github.com/user-attachments/assets/77e7a448-a319-492f-8c97-f52af9ccb0f8" />






## Result
The traffic light control system was successfully implemented using ABB PLC software. The Red, Yellow, and Green lights operated automatically according to the programmed timer sequence.


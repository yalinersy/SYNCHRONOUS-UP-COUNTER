### NAME: SRIYALINE R
### REG NO: 24006194
# EXPERIMENT 7: IMPLEMENTATION OF SYNCHRONOUS UP COUNTER
# AIM:

To implement 4 bit synchronous up counter and validate functionality.

# SOFTWARE REQUIRED:

Quartus prime

# THEORY

# 4 bit synchronous UP Counter

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

# PROCEDURE
1: Create a New Project:

Open Intel Quartus Prime

Go to File > New Project Wizard and follow the prompts:

Set the project directory.

Name the project (e.g., Exp7).

Click Finish

2: Write the Verilog Code for the Counter

Create a new Verilog file:

Go to File > New > Design Files > Verilog HDL File.

Write the Verilog code for a 4-bit synchronous up counter.

Save the file with a .v extension (e.g., Exp7.v).

3: Compile the Design:

Go to Processing > Start Compilation or click the Compile button.

Wait for the compilation process to complete and ensure there are no errors.

4: Create the waveform:

Go to File > New > University Program VWF.

Run the waveform inputs in ModelSim with Quartus.

5: Obtain the result.

# PROGRAM
![Screenshot 2024-12-23 110411](https://github.com/user-attachments/assets/0deaef53-46db-47f6-9e40-e5deef4c7049)

# RTL 
![Screenshot 2024-12-23 104915](https://github.com/user-attachments/assets/cea84b74-f792-490b-8c7e-f205e9861313)

# TIMING DIAGRAM 
![Screenshot 2024-12-23 110520](https://github.com/user-attachments/assets/8d262042-023b-44f3-8e31-669913ad654f)

# TRUTH TABLE
![Screenshot 2024-12-23 115233](https://github.com/user-attachments/assets/f754a0de-411a-4bb7-8559-91debc9440bc)

# RESULT
Implementation of 4 bit synchronous up counter is verified and its function is validated.

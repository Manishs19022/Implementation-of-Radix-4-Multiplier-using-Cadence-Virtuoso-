# Implementation-of-Radix-4-Multiplier-using-Cadence-Virtuoso-


# Introduction 

A radix multiplier is a digital circuit designed to perform high-speed 
multiplication by processing multiple bits of the multiplier in each cycle. Unlike 
traditional binary (radix-2) multipliers that handle one bit at a time, radix 
multipliers—such as radix-4, radix-8, or radix-16—group bits to reduce the 
number of partial products, thereby accelerating computation. For instance, 
radix-4 Booth multipliers halve the number of partial products compared to 
radix-2, enhancing performance and efficiency. These multipliers are vital in 
digital signal processing, cryptography, and embedded systems where speed and 
power efficiency are paramount. 
Radix multipliers are integral to modern digital systems, especially in 
applications demanding high-speed arithmetic operations like digital signal 
processing, cryptography, and embedded systems. Their ability to reduce 
computation time and power consumption makes them indispensable in 
designing efficient hardware architectures. As technology advances, hybrid 
approaches combining different radix techniques are being explored to further 
optimize performance and energy efficiency in complex digital circuits. 
The implementation of radix multipliers, particularly using Booth's algorithm, 
has been extensively studied and applied in various hardware designs. For 
example, a study on the implementation of a radix-4 (32-bit) Booth multiplier 
using VHDL demonstrated significant improvements in computation time, 
achieving a delay of 26.32 ns, which is notably lower compared to traditional 
designs. Similarly, the design and comparison of high-speed radix-8 and radix-16 
Booth's multipliers have shown that higher radix implementations can lead to 
further reductions in partial products and improved performance. These 
advancements highlight the importance of radix multipliers in achieving efficient 
and high-speed multiplication in digital systems.

# Literature Survey 

 Design and Implementation of Radix 4 Based Arithmetic Operations,  
Authors:- Saste and A. Sawant , published in 2019. 
Focuses on improving Arithmetic efficiency in Digital Systems 
 Design Of High Performance Configurable Radix-4 Booth Multiplier Using 
Cadence Tools,  
Author:- Dr. T. Esther Rani , published in 2022. 
Designs a configurable Radix-4 Booth multiplier with a Hybrid Adder in 
Cadence, achieving 17.1ns delay (29% faster than Radix-2) and 1.12mW 
power. 
 Modified Booth Encoding Radix-4 8-bit Multiplier,  
Authors:- Da Huang, Afsaneh Nassery, published in 2020. 
Implements an 8-bit Radix-4 Booth multiplier in 0.5µm CMOS, using Booth 
Encoder + CLA,  achieving 0.2092mW power and 38-gate delay. 
 A Fast Multiplier Using Modified Radix-4 Booth Algorithm With Redundant 
Binary Adder For Low Energy Applications ,  
Authors:- R. Mallikarjuna Sharma, K. Raju , published in 2018. 
Proposes a low-energy Radix-4 multiplier using a modified Booth algorithm 
and Redundant Binary Adder, simulated in Cadence (180nm) to reduce power 
and delay

# Objectives: 
 To Understanding the Radix-4 Multiplier Concept:  
 To Implementation of Radix-4 Multiplier in Cadence Virtuoso 
 To analyse the output waveform 
 To verify with the manual calculation  

# Problem Statement: 
The radix multiplier, while effective in handling large-scale multiplications, 
presents several significant challenges in its implementation. Firstly, it requires a 
large area on the chip due to the extensive number of logic gates and components 
involved in its architecture. This substantial area requirement can limit its 
suitability for compact or resource-constrained systems. Secondly, the high 
number of gates also contributes to increased power consumption, making the 
radix multiplier less energy-efficient, especially in battery-powered or low-power 
devices. Lastly, the complexity of the circuit introduces a relatively long delay 
time, as multiple processing stages and operations are required to complete a 
multiplication. These issues—large chip area, high power usage, and longer 
delays—collectively affect the performance and practicality of radix multipliers 
in certain applications

# Block Diagram

<img width="659" height="594" alt="image" src="https://github.com/user-attachments/assets/fbf0590c-d6ad-4be4-89d0-0004068017dd" />

# Manual Calculation
<img width="825" height="860" alt="image" src="https://github.com/user-attachments/assets/ebe52bd9-d3ee-458e-90a3-918c34b9ebd6" />

# Flow Chart
<img width="229" height="553" alt="image" src="https://github.com/user-attachments/assets/77ba4b38-2f9d-454d-8b4c-fd4909a8569d" />


# Results and Discussions 
The output waveform of a Radix-4 multiplier provides valuable insight into the 
functional correctness, timing behavior, and performance of the design. 
Typically, the waveform will show input signals (such as the multiplicand and 
multiplier), control signals (like clock and reset), and the final output product. By 
analyzing the waveform, we can verify whether the output product matches the 
expected value for given inputs. If the partial product generation and addition 
stages are working correctly, the output will stabilize to the correct result within 
a few clock cycles, depending on the implementation. The vdc is provided as 
input for the radix 4 multiplier for both multiplicand and for the booth encoder. 
The voltage for the high input is gives as 1.8V and the voltage for the low input is 
given as 0V for the symbol of the Radix-4 Multiplier. The output is obtained with 
the minimal losses as shown in the waveform.


# Applications: 
1. Digital Signal Processing (DSP) – Used in filters, FFTs, and other DSP 
algorithms. 
2. Graphics Processing Units (GPUs) – For fast arithmetic in image rendering. 
3. Embedded Systems – Where area and power optimization is crucial. 
4. Microprocessors/ALUs – Speeds up multiplication in CPUs. 
5. Communication Systems – Used in encoding/decoding and 
modulation/demodulation. 
6. Control Systems – For real-time mathematical computations. 

# Advantages: 
1. Faster Computation – Reduces the number of partial products (especially in 
Radix-4 or higher). 
2. Efficient for Signed Numbers – Handles 2’s complement arithmetic 
directly. 
3. Lower Hardware Complexity – Compared to full-width multipliers. 
4. Power Efficient – Fewer switching operations due to fewer add/subtract 
stages. 
5. Scalable – Can be extended to higher radix versions (e.g., Radix-8) for 
further speed-up. 

# Outcome: 
 A radix multiplier produces the product of two binary numbers faster and 
with fewer resources than basic multipliers, making it suitable for high
speed arithmetic applications in VLSI and real-time systems.

# Limitations: 
1. Complex Booth Encoding Logic – Higher radix values increase control logic 
complexity. 
2. More Preprocessing Time – Encoding and decoding stages take time. 
3. Design Overhead – Difficult to design and optimize for very high radix 
systems. 
4. Not Ideal for Small Bit-widths – Simpler multipliers may outperform for 
low-bit operations. 

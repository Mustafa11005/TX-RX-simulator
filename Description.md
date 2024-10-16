((Uni-Polar NRZ Transmission Simulation))

This project simulates the transmission and reception of digital data using Uni-Polar Non-Return-to-Zero (NRZ) encoding. It evaluates the impact of noise on signal integrity and calculates the bit error rate (BER). The simulation is performed using MATLAB and also includes a Simulink model with similar functionality.

Overview:

Uni-Polar NRZ Encoding

Uni-Polar NRZ encoding is a straightforward method of representing binary data. In this scheme:

---> 0 is represented by a voltage level of 0V (ground).
---> 1 is represented by a positive voltage level (vcc).

This encoding method ensures that each bit is represented by a constant voltage level throughout its duration, making it simple but susceptible to noise.

Simulation Details:

1- Signal Generation:

- A random stream of bits is generated.

- Each bit is mapped to a voltage level: 0 maps to ground (gnd), and 1 maps to the supply voltage (vcc).

- The bit stream is then converted into a Uni-Polar NRZ signal where each bit is represented for a fixed duration.

2- Noise Addition:

- Gaussian noise with varying levels of standard deviation (sigma) is added to the Uni-Polar NRZ signal. This simulates real-world scenarios where the signal is distorted due to noise.

3- Signal Reception:

- The noisy signal is processed to recover the original bit stream. A threshold is used to determine whether each received signal level corresponds to a 0 or 1.

- The recovered signal is compared to the transmitted signal to evaluate the accuracy of the transmission.

4- Error Calculation:

- The bit error rate (BER) is calculated by comparing the transmitted and received signals. It quantifies the proportion of bits that were incorrectly received due to noise.

MATLAB Script:

The MATLAB script automates the entire process:

- It generates and encodes a bit stream.

- It adds noise to the encoded signal.

- It simulates the reception and decoding of the noisy signal.

- It calculates and displays the BER for different noise levels.

Simulink Model:

A Simulink model replicates the functionality of the MATLAB script:

- Signal Generator: Creates a random bit stream.

- NRZ Encoder: Converts the bit stream into a Uni-Polar NRZ signal.

- Noise Block: Adds Gaussian noise to the signal.

- Receiver: Processes the noisy signal to recover the transmitted bits.

- Error Calculation: Computes and displays the bit error rate.

The Simulink model provides a visual representation of the entire process, making it easier to understand and analyze the effects of noise on signal transmission.

Key Points:

- Uni-Polar NRZ Encoding: Represents binary data with constant voltage levels, susceptible to noise.

- Noise Simulation: Adds Gaussian noise to the signal to mimic real-world conditions.

- Error Measurement: Compares transmitted and received signals to compute the bit error rate.

How to Use?

1- MATLAB Script: Run the MATLAB script to see plots of the transmitted signal, noisy signal, and received signal. The script will output the bit error rate for each noise level.

2- Simulink Model: Open the Simulink model (.slx file) and run the simulation to observe the signal processing and error calculation visually.

Notes:

- Ensure that the Simulink model and MATLAB script are in the same directory or that the Simulink model is properly added to the MATLAB path.

- Adjust parameters such as the number of bits, voltage levels, and noise levels to explore different scenarios and their effects on signal quality.

- You have to run "ErrorSim.mlx" first to get a propper reading of error in the Simulink file (TxRx.slx)
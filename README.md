# BB84 Quantum Key Distribution Simulator

This project is a Python simulation of the BB84 quantum key distribution (QKD) protocol using Qiskit.  
It models secure quantum communication between Alice and Bob, with optional noise and an eavesdropper (Eve), and analyzes the resulting Quantum Bit Error Rate (QBER).

The goal of this project is to demonstrate how quantum mechanics enables secure key exchange and how disturbances (noise or interception) introduce detectable errors.

# Overview

BB84 is a foundational quantum cryptography protocol that relies on:
- Random bit generation
- Random basis selection (X and Z bases)
- Measurement-induced disturbance
- Public basis comparison and key sifting

This simulation implements the full BB84 workflow and compares error rates under different conditions.

# Features

- Full BB84 protocol implementation (Alice, Bob, and optional Eve)
- Random bit and basis generation
- Optional depolarizing noise model
- Optional eavesdropping simulation
- Key sifting and error estimation
- Averaged Quantum Bit Error Rate (QBER) across multiple runs
- Visualization of QBER under different scenarios

# Simulation Scenarios

The program compares four cases:
1. Without noise and eavesdropper  
2. Noise only  
3. Eavesdropper only  
4. Noise + eavesdropper  

The resulting QBER values are displayed in a bar chart for comparison.

# Technologies Used

- Python
- Qiskit
- Qiskit Aer Simulator
- Matplotlib

# How It Works (High Level)

1. Alice generates random bits and random bases and encodes them into qubits.
2. (Optional) Eve intercepts and measures qubits using random bases, introducing disturbance.
3. Bob measures the received qubits using random bases.
4. Alice and Bob publicly compare bases and keep only matching measurements (key sifting).
5. A random subset of the sifted key is compared to estimate the Quantum Bit Error Rate.
6. The protocol is repeated multiple times and the average QBER is calculated.

# SCiMA-Architecture-Framework
SCiMA: A Systolic CiM-Based Accelerator and a Virtual Framework

**A Programmable Systolic Computing-in-Memory Accelerator for CNNs**

## Overview

SCiMA is a configurable and programmable Computing-in-Memory (CiM) accelerator designed for efficient execution of Convolutional Neural Networks (CNNs). The architecture integrates systolic dataflow, in-memory computation, and novel weight mapping techniques to improve data reuse, reduce communication overhead, and enhance computational efficiency.

This repository provides the SCiMA architecture and its associated development and evaluation tools, including a SystemC-based virtual framework, SystemVerilog RTL implementation, Python-based hardware compiler, and SPICE crossbar generation scripts.

The proposed virtual framework supports functional validation, performance evaluation, and power estimation of the SCiMA architecture under different CNN workloads and hardware configurations.

## Repository Contents

### Research Paper

**SCiMA: A Systolic CiM-based Accelerator with a New Weight Mapping for CNNs – A Virtual Framework Approach**

The included PDF contains the research paper published in *IEEE Access*. It presents the proposed architecture, systolic dataflow mechanisms, weight mapping strategies, virtual modeling framework, and experimental evaluation of SCiMA.

### SystemC_SCiMA_Framework.zip

This archive contains the main SystemC-based virtual framework developed for modeling, validating, and evaluating the SCiMA architecture.

The framework includes several SystemC models developed at different abstraction levels to address functional correctness, simulation efficiency, architectural performance, and power consumption.

**SCiMA_Functional**

This implementation provides a complete functional SystemC model of the SCiMA architecture, incorporating its computational components, data movement mechanisms, communication structures, and their interactions.

The primary purpose of this model is to demonstrate the proof of concept of the proposed architecture and verify its functional correctness. It enables validation of the computational operations, systolic dataflow, and communication between architectural components.

**SCiMA_DataMovement_MultiFileConfig, SCiMA_DataMovement_OneFileConfig, and SCiMA_DataMovement_Packetize**

These implementations provide performance-oriented SystemC models of the SCiMA architecture.

To improve simulation speed and enable efficient evaluation of large CNN workloads, the detailed functionality of the computational components is abstracted, while their execution latencies are retained.

Consequently, these models primarily focus on data movement, communication between architectural components, and timing behavior, while accounting for the latency of computational operations.

This abstraction significantly reduces simulation complexity and enables architectural performance evaluation without requiring detailed functional simulation of every computation.

The three implementations provide alternative modeling and configuration approaches, including multi-file configuration, single-file configuration, and packet-based data movement modeling.

**SCiMA_Power_Estimation**

This implementation extends the SystemC-based SCiMA framework with power estimation capabilities.

It enables the evaluation of power and energy consumption associated with the execution of CNN workloads, complementing the performance-oriented models and supporting power-aware architectural analysis.

**Traces**

Contains trace-related resources for analyzing simulation execution, data movement, communication activities, and timing behavior.

### RTL.zip

This archive contains the SystemVerilog RTL implementation of the SCiMA architecture.

The RTL model describes the architecture at the register-transfer level and provides a hardware-oriented implementation for RTL simulation, functional verification, and further hardware development.

### Compiler_Python.zip

This archive contains the Python-based hardware compiler developed for the SCiMA architecture.

The compiler takes CNN applications as input and translates their computational requirements into hardware-specific configuration parameters.

It performs application-to-hardware mapping and generates the configuration information required to execute CNN workloads on the SCiMA accelerator, enabling the programmability of the proposed architecture.

### Python-Spice-Crossbar_Generation.zip

This archive contains Python scripts for automatically generating SPICE netlists of crossbar structures.

The generated SPICE models can be used for circuit-level simulation and electrical characterization of crossbar-based computing-in-memory structures.

## Citation

If you use the SCiMA architecture, SystemC framework, RTL implementation, compiler, or associated tools in your research, please cite the following publication:

**SCiMA: A Systolic CiM-based Accelerator with a New Weight Mapping for CNNs – A Virtual Framework Approach.**

*IEEE Access.*

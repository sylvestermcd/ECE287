# ECE287 Exam 3
## Overview

This module (ex4_wrapper.v) connects different parts and uses a finite state machine (FSM) to control how the system works. It shows how the system interacts with memory, changes states, and handles inputs and outputs.
## Features
**Clock and Reset** : Manages timing and system resets.

**State Machine**: A FSM with clearly defined states, including a new added state (SYSTEM_S_EXTRA) for more functionality.

**Memory Interaction**: Reads and writes data to memory using multiple inputs.

**Input-Output Operations**: Displays the  processed values on the seven-segment display, Accepts inputs through switches, Indicates system status by lighting up LEDs.

**Simple Math Operation**: Adds two inputs and displays the result on the seven-segment display.

**Customizable**: Designed to be modified with/different  new states and features.

## State Machine Details
The FSM follows these states:

SYSTEM_S_START: Initializes the system and resets values.

SYSTEM_S_WAIT: Waits for a user-triggered start signal.

SYSTEM_S_RUN_SYSTEM: Begins the system operation.

SYSTEM_S_GET_IN1: Captures the first input.

SYSTEM_S_GET_IN2: Captures the second input.

SYSTEM_S_RUN_START: Performs the main computation (e.g., addition).

SYSTEM_S_WAIT_RUN_DONE: Waits for the computation to complete.

SYSTEM_S_EXTRA: (New State) Performs additional computations or actions on the result.

SYSTEM_S_DONE: Indicates the operation is complete and returns to the wait state.

## Inputs and Outputs
### Inputs
CLOCK_50: 50 MHz system clock.

KEY[0]: Reset signal.

KEY[1]: Start signal.

SW[9:0]: 10-bit input values for computations.

### Outputs

LEDR[7:0]: State or debug information.

HEX0 to HEX5: Seven-segment display outputs for displaying results.

Getting Started

Setup:

Connect the hardware (e.g., switches, keys, seven-segment displays, and LEDs) based on the  pin assignments.

Load the design onto an FPGA.

Operation:

Reset the system using KEY[0].

Provide inputs using SW[9:0].

Start the computation by pressing KEY[1].

Observe the result on the seven-segment display.



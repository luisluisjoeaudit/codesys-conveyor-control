# I/O List

## Overview

This document lists the variables used in my CODESYS conveyor control project. Variables are grouped under operator inputs, sensor inputs, simulated outputs, and internal variables.

## 1. Operator and Sensor Inputs

| Variable | Expected Type | Purpose |
|---|---|---|
| `Start_PB` | BOOL | Requests conveyor startup. |
| `Stop_PB` | BOOL | Requests a normal conveyor stop. |
| `E_Stop_PB` | BOOL | Simulated emergency-stop input. |
| `Safety_SW` | BOOL | Represents the safety switch status. |
| `Product_Sensor` | BOOL | Detects products passing the conveyor. |
| `PC_Reset` | BOOL | Resets the product counter. |

## 2. Outputs

| Variable | Expected Type | Purpose |
|---|---|---|
| `Siren_Output` | BOOL | Controls the startup warning siren. |
| `Shutdown_Siren` | BOOL | Controls the shutdown warning siren. |
| `Conveyer_Motor_Start` | BOOL | Represents the internal conveyor motor start command. |
| `Conveyer_Motor_OFF` | BOOL | Represents the internal conveyor motor stop state. |
| `Motor_Start_Indication_Light` | BOOL | Indicates the programmed conveyor startup condition. |
| `Motor_OFF_Indication_Light` | BOOL | Indicates the programmed conveyor stopped condition. |
| `Batch_Complete_Indication` | BOOL | Indicates that the product counter has reached its preset. |

## 3. Internal Variables and Function Blocks

| Variable | Expected Type | Purpose |
|---|---|---|
| `System_Run` | BOOL | Maintains the startup/run state. |
| `System_Stop` | BOOL | Maintains the shutdown state. |
| `Startup_Timer` | TON instance | Provides the startup delay. |
| `Stop_Timer` | TON instance | Timer instance for the stop sequence. |
| `Shutdown_Timer` | TON instance | Provides the shutdown delay. |
| `Batch_TON_Indication` | TON instance | Provides the Product_Counter reset. |
| `Product_Counter` | CTU instance | Counts detected products toward a preset value. |

## 4. Configuration

| Setting | Value |
|---|---|
| Startup delay | 5 seconds |
| Normal-stop delay | 5 seconds |
| Product-counter preset | 10 |
| Product-counter reset | 3 seconds|
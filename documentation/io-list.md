# I/O List

## Overview

This document lists the variables used in my CODESYS conveyor control project. Variables are grouped under operator inputs, sensor inputs, simulated outputs, and internal variables.

## 1. Operator and Sensor Inputs

| Variable | Expected Type | Purpose |
|---|---|---|
| `Start_PB` | BOOL | Requests conveyor startup. |
| `Stop_PB` | BOOL | Requests a normal conveyor stop. |
| `E_Stop` | BOOL | Simulated emergency-stop input. |
| `Product_Sensor` | BOOL | Product detection in a short range. |

## 2. Outputs

| Variable | Expected Type | Purpose |
|---|---|---|
| `Siren_Output` | BOOL | Controls the  warning siren. |
| `Conveyor_Motor_Start` | BOOL | Represents the conveyor motor run command. |
| `Motor_Start_Indication_Light` | BOOL | Indicates the programmed conveyor run/start condition. |
| `Batch_Complete_Indication` | BOOL | Indicates that the product counter has reached its preset. |

## 3. Internal Variables and Function Blocks

| Variable | Expected Type | Purpose |
|---|---|---|
| `System_Run` | BOOL | Maintains the startup/run state. |
| `Startup_Timer` | TON instance | Provides the startup delay. |
| `Stop_Timer` | TON instance | Provides the normal-stop delay. |
| `Product_Counter` | CTU instance | Counts number of boxes to a preset value. |
| `PC_Reset` | BOOL | Reset signal for product counter. |

## 4. Configuration

| Setting | Value |
|---|---|
| Startup delay | 5 seconds |
| Normal-stop delay | 5 seconds |
| Product-counter preset | 10 |
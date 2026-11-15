
# OpenDSS Simulation & Analysis Workflow (2,160-Hour Evaluation)

This simulation studies how adding a Solar PV system (`PVSystem.PV675`) affects the performance of the IEEE 13-Bus distribution network over **90 days (2,160 hours)**.

Two operating conditions are compared:

- **Case 1 – Baseline:** IEEE 13-Bus system without Solar PV.
- **Case 2 – With PV:** IEEE 13-Bus system with Solar PV connected at Bus 675.

The main aim is to understand how Solar PV affects power losses and voltage levels throughout the simulation period.

---

## 1. Simulation Workflow

| Step | Process | Description |
|:---:|---|---|
| 01 | Initialization | Connects MATLAB to OpenDSS through the COM interface and loads the IEEE 13-Bus model (`IEEE13Master1.dss`). |
| 02 | Hourly Simulation | Runs power flow calculations for 2,160 hours for both cases to study the network under different operating hours. |
| 03 | Data Collection | Records hourly active power losses, reactive power losses, and bus voltage values. |
| 04 | Result Comparison | Compares both cases to identify changes in power losses and voltage levels. |

## 2. Results & Graphical Analysis

The simulation generates the following graphs to understand the network performance:

- **Active Power Loss Profile:** Shows how much active power is wasted in the distribution lines during each hour (kW).
- **Reactive Power Loss Profile:** Shows the reactive power losses in the network throughout the simulation (kVAR).
- **Final-Hour Voltage Profile:** Displays the voltage levels of different buses and phases at the end of the 2,160-hour simulation.
- **Minimum Voltage Profile:** Tracks the lowest voltage recorded in the network every hour to identify voltage drop conditions and check voltage limit compliance.

## 3. Generated Output Files

The simulation automatically saves the calculated results in the following files:

| File Name | Purpose |
|---|---|
| `Yearly_Losses_Comparison.xlsx` | Contains hourly active and reactive power loss values for both cases. |
| `Total_Yearly_Loss_Comparison.xlsx` | Summarizes the total accumulated energy losses for both cases. |
| `FinalHourVoltageProfile.xlsx` | Stores the voltage values of different buses and phases at Hour 2,160. |
| `IEEE13_YearlyResults.mat` | Stores the complete MATLAB simulation results for future analysis. |

## 4. Key Performance Parameters

- **Active Power Loss (kW):** Measures the real electrical power lost in the distribution network.
- **Reactive Power Loss (kVAR):** Represents reactive power losses in the network.
- **Energy Loss (kWh):** Measures the total active energy lost over the simulation period.
- **Reactive Energy Loss (kVARh):** Measures the accumulated reactive energy losses.
- **Bus Voltage (p.u.):** Indicates the voltage level at each bus compared with its rated voltage.
- **Minimum Voltage:** Identifies the lowest voltage recorded across the distribution network.

## 5. Overall Objective

The 2,160-hour simulation helps evaluate:

- The reduction in active and reactive power losses after Solar PV integration.
- The improvement in voltage profiles across different buses.
- The variation in minimum feeder voltage throughout the simulation.
- The overall impact of Solar PV integration on distribution network performance.

**Tools Used:** MATLAB · OpenDSS · COM Interface · Excel

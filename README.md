# ⚙️ DFT Optimization Tool for Testability Improvement in Combinational Circuits

This project implements an algorithm to identify the **Most Qualified Nodes for Improvement in Testability (MQNI)** in combinational circuits using **SCOAP** metrics. It accepts **Verilog netlists** (e.g., ISCAS'85/89 benchmarks) and outputs suggested Design for Testability (DFT) insertions, maximizing testability with minimal area overhead.

---

## 🧠 Abstract

Fault detection in complex VLSI chips becomes increasingly costly if handled at later stages. This project introduces an algorithm that analyzes a circuit's **testability** and identifies internal nodes where **DFT insertion** will yield maximum improvement. The algorithm calculates **Controllability (CC0, CC1)** and **Observability (CO)** using the SCOAP technique, then computes a **Testability Improvement Factor (TIF)** to rank the best insertion points.

The tool is implemented in C and designed to work directly with gate-level **Verilog netlists**.

---

## 📌 Key Features

- Computes SCOAP testability metrics for all nodes
- Shortlists nodes based on **Total Testability (TT)** and **Fan-Out**
- Calculates **Testability Improvement Factor (TIF)**
- Computes **Area Overhead (AO)** for different DFT insertion strategies
- Applicable to ISCAS benchmark circuits like C17, C432, C499, C880

---

## 🛠️ Technologies Used

- **Language:** C
- **Input Format:** Verilog Netlist (gate-level)
- **Benchmark Circuits:** ISCAS'85 and ISCAS'89
- **Metrics:** SCOAP (CC0, CC1, CO), Fan-Out, TIF, AO

# ⚡ Smart Appliance Scheduling Dataset

## 📌 Project Overview

This repository contains a structured dataset for modeling and analyzing **smart appliance scheduling in energy management systems**.

The dataset categorizes household appliances based on their operational flexibility and defines parameters required for optimization, including power levels, time slots, and dissatisfaction coefficients.

This project can be used for:

* Load scheduling optimization
* Smart grid simulations
* Demand-side energy management research
* Appliance power consumption modeling

---

## 🏷️ Appliance Attributes

Each appliance in the dataset contains the following parameters:

### 1️⃣ Name

The name of the appliance.

Example:

* Washing Machine
* Air Conditioner
* Dishwasher
* Electric Vehicle Charger

---

### 2️⃣ Type

Appliances are categorized into three types based on scheduling flexibility:

| Type   | Description                                                                |
| ------ | -------------------------------------------------------------------------- |
| **NS** | Non-shiftable – Must operate at a fixed time and fixed power level         |
| **PS** | Power-shiftable – Can operate at different power levels                    |
| **TS** | Time-shiftable – Can operate in any time slot within defined working hours |

---

### 3️⃣ Dissatisfaction Coefficient (Diss.Coeff.)

A weighting factor representing user discomfort caused by scheduling deviation.

* For **Power-Shiftable (PS)** appliances:
  Measures dissatisfaction due to deviation from maximum power level.

* For **Time-Shiftable (TS)** appliances:
  Measures dissatisfaction due to waiting time from the earliest available time slot.

Higher coefficient → Higher user discomfort
Lower coefficient → More scheduling flexibility

---

### 4️⃣ Power Rating

Defines the operational power levels of the appliance (in kW or Watts).

Examples:

* Fixed power level (NS): 1.5 kW
* Multiple levels (PS): [0.8 kW, 1.2 kW, 1.8 kW]

---

### 5️⃣ Time Slot

Defines the normal operating window of the appliance.

Example:

* 08:00 – 18:00
* 18:00 – 23:00
* Any time during the day

This parameter is primarily used for time-shiftable scheduling models.

---

## 📂 Example Dataset Structure

```json
{
  "name": "Washing Machine",
  "type": "TS",
  "diss_coeff": 0.7,
  "power_rating": 1.5,
  "time_slot": "08:00-20:00"
}
```

---

## 🎯 Use Cases

* Smart Home Energy Optimization
* Demand Response Algorithms
* Load Forecasting Models
* Cost Minimization under Time-of-Use Tariffs
* AI-based Scheduling Systems

---

## 🛠️ Possible Extensions

* Add real-time electricity pricing
* Integrate renewable energy availability
* Add user priority levels
* Include historical energy consumption data
* Build optimization models using:

  * Linear Programming
  * Genetic Algorithms
  * Reinforcement Learning

---

## 📊 Target Audience

* Energy Management Researchers
* Smart Grid Developers
* Electrical Engineering Students
* Data Science & Optimization Enthusiasts

---

## 📜 License

This project is open-source and available for academic and research purposes.

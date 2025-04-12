# 🏭 Defect Classification using MES Data

A data analysis project to automate defect classification and detect root causes using MES logs from a battery manufacturing process (Electrolyte Filling - CEF).

---

## 🎯 Objective

Manual review of manufacturing defects is slow and inconsistent. This project:
- Categorizes defects using process parameters and shift/operator info
- Visualizes root causes by line/operator
- Enables early alerts to reduce defect rate and improve product quality

---

## 🗂 Dataset Overview

| Table            | Description                        | Key Fields                              |
|------------------|------------------------------------|------------------------------------------|
| `defect_log`     | Defect event log per cell          | `cell_id`, `defect_type`, `timestamp`   |
| `process_log`    | MES sensor data from CEF process   | `cell_id`, `vacuum_time`, `pressure`, `status_code` |
| `operator_shift` | Operator and line assignments      | `operator_id`, `line_no`, `shift_time`  |

---

## 🧪 Workflow Summary

1. Merge and clean MES + defect logs
2. Apply rule-based classification:
   - e.g., `if vacuum_time < 3s and pressure < 100kPa → Underfilling`
3. Visualize top root causes by line/operator/time
4. Output defect dashboard & summaries

---

## 📊 Sample Output

### 📌 Root Cause Dashboard (Spotfire/Power BI)

![dashboard](dashboard/dashboard_spotfire.png)

---

## 📈 Results & Impact

- Classified 90% of defects with clear root cause categories
- Reduced defect rate from 0.10% → 0.04%
- Saved approx. \$120K annually in quality control & rework
- Enabled real-time alert system for risky process conditions

---

## 🛠 Tools Used

- **Python**: `pandas`, `numpy`, `matplotlib`
- **SQL**: Data joins, CASE logic
- **Spotfire** / **Power BI**: Visualization
- **Git**: Version control
- **Jupyter Notebook**: Development & analysis

---

## 📁 Project Structure


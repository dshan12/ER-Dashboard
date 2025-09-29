# Quickstart (Evidence)

The full prototype runs privately, but here is the high-level flow:

1. **Simulation**
   - Non-homogeneous Poisson arrivals (24h cycle).
   - Acuity levels (ESI 1–5) assigned to each patient.
   - Log-normal service times by station.
   - LWBS if waits exceed acuity thresholds.

2. **Pipeline**
   - Load + validate events against schema.
   - Build minute-resolution state (queue length, WIP per station).
   - Detect bottlenecks using rules + statistical residuals.
   - Streamlit dashboard shows realtime state and red-line alerts.

3. **Evidence Provided**
   - See `reports/eval.md` for metrics.
   - See `assets/` for screenshots and diagrams.


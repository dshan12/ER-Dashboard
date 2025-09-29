# Technical Notes

## Design Choices
- **Simulation only**: all logs generated stochastically, no PHI.
- **Acuity-based priority**: patients queued with ESI 1–5 priority.
- **Finite resources**: beds are limited; patients wait or LWBS.
- **Transparent rules**: thresholds + imbalance checks before ML.
- **Realtime UI**: Streamlit dashboard with red-line alert overlays.

## Evaluation
- Alerts consistently fire *earlier* than manual spotting proxy (queue ≥ high threshold).
- Door-to-bed delays stratified by ESI levels.
- LWBS rates rise under simulated congestion.

## Limitations
- No staff shift model.
- Simplified patient pathways.
- Forecasting = baseline only (Holt-Winters, ARIMA).
- LWBS modeled via wait thresholds, not behavioral.

## Next Steps
- Pilot with anonymized real logs.
- Add staff/resource scheduling.
- Extend branching pathways (labs, consults).


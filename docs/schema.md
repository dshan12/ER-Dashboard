# Event Schema (Synthetic Only)

| column           | type    | description |
|------------------|---------|-------------|
| event_id         | string  | unique event identifier |
| timestamp        | string  | ISO8601 UTC timestamp |
| patient_id       | string  | pseudo ID (no PHI) |
| esi              | int     | acuity level (1–5, 1 = most urgent) |
| event_type       | enum    | admission · treatment · discharge · lwbs |
| station          | enum    | triage · beds · imaging · treatment · waiting |
| duration_minutes | float   | duration of event (where applicable) |
| hospital_id      | string  | fixed synthetic ID |
| unit_id          | string  | fixed synthetic ID |
| source           | string  | always `simulated` |
| note             | string  | optional details (e.g. LWBS reason) |


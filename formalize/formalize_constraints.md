| Constraint ID | Constraint | Formal Expression | Simple Meaning |
|---|---|---|---|
| C1 | The barrier must not open while a train is present. | `Train_Present → ¬Barrier_Open` | If a train is present, the barrier should not be open. |
| C2 | The barrier must close when a train is approaching. | `Train_Approaching → Barrier_Closed` | If a train is coming, the barrier should close. |
| C3 | Warning lights must turn ON when a train approaches. | `Train_Approaching → Warning_Light` | If a train is coming, the warning light should turn on. |
| C4 | The audible alarm must turn ON when a train approaches. | `Train_Approaching → Alarm` | If a train is coming, the alarm should turn on. |
| C5 | The barrier must stay closed while a train is present. | `Train_Present → Barrier_Closed` | While the train is at the crossing, the barrier must stay closed. |
| C6 | The barrier can open only after the train has cleared the crossing. | `Barrier_Open → Train_Cleared` | The barrier should open only when the train has completely passed. |
| C7 | The barrier must not open if the train sensor has failed. | `Sensor_Failure → ¬Barrier_Open` | If the sensor fails, the barrier should not open. |
| C8 | A barrier failure must cause a safety response. | `Barrier_Failure → Emergency` | If the barrier fails, the system should enter a safe/emergency state. |

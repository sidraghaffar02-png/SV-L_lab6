# Task 3 — Identify Constraint Violations

## Railway Level-Crossing Control System

A constraint violation happens when the system does something that goes against a defined safety rule.

### Violation 1 — C1

**Constraint:**  
`Train_Present → ¬Barrier_Open`

**Violation:**  
`Train_Present = TRUE`  
`Barrier_Open = TRUE`

**Explanation:**  
A train is present, but the barrier is open. This violates the rule that the barrier must not be open when a train is present.

---

### Violation 2 — C2

**Constraint:**  
`Train_Approaching → Barrier_Closed`

**Violation:**  
`Train_Approaching = TRUE`  
`Barrier_Closed = FALSE`

**Explanation:**  
A train is approaching, but the barrier did not close. The barrier should be closed when a train is coming.

---

### Violation 3 — C3

**Constraint:**  
`Train_Approaching → Warning_Light`

**Violation:**  
`Train_Approaching = TRUE`  
`Warning_Light = FALSE`

**Explanation:**  
A train is approaching, but the warning light is OFF. The warning light should turn ON.

---

### Violation 4 — C4

**Constraint:**  
`Train_Approaching → Alarm`

**Violation:**  
`Train_Approaching = TRUE`  
`Alarm = FALSE`

**Explanation:**  
A train is approaching, but the audible alarm is OFF. The alarm should be ON to warn people.

---

### Violation 5 — C5

**Constraint:**  
`Train_Present → Barrier_Closed`

**Violation:**  
`Train_Present = TRUE`  
`Barrier_Closed = FALSE`

**Explanation:**  
A train is passing through the crossing, but the barrier is not closed. The barrier must remain closed while the train is present.

---

### Violation 6 — C6

**Constraint:**  
`Barrier_Open → Train_Cleared`

**Violation:**  
`Barrier_Open = TRUE`  
`Train_Cleared = FALSE`

**Explanation:**  
The barrier opened before the train completely cleared the crossing. The barrier should only open after the train has passed.

---

### Violation 7 — C7

**Constraint:**  
`Sensor_Failure → ¬Barrier_Open`

**Violation:**  
`Sensor_Failure = TRUE`  
`Barrier_Open = TRUE`

**Explanation:**  
The sensor has failed, but the barrier opened. The barrier should remain closed when there is a sensor failure.

---

### Violation 8 — C8

**Constraint:**  
`Barrier_Failure → Emergency`

**Violation:**  
`Barrier_Failure = TRUE`  
`Emergency = FALSE`

**Explanation:**  
The barrier has failed, but the system did not activate the emergency response. A barrier failure should trigger a safety response.

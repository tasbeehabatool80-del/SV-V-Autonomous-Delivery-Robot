# State Transition Table

| Current State | Event / Condition | Next State |
|---|---|---|
| IDLE | Delivery Request Received | NAVIGATING |
| NAVIGATING | Obstacle Detected | AVOIDING_OBSTACLE |
| AVOIDING_OBSTACLE | Obstacle Avoided | NAVIGATING |
| NAVIGATING | Destination Reached | DELIVERING |
| DELIVERING | Delivery Successful | RETURNING |
| RETURNING | Warehouse Reached | IDLE |
| NAVIGATING | Critical Battery | RETURNING |

# Verification

## Check 1 — Invalid Transition

### Transition Checked
IDLE → DELIVERING

### Result
Invalid.

### Reason
The robot must first receive a delivery request and navigate to the destination before entering the DELIVERING state.

### Requirement Violated
R9.

---

## Check 2 — Missing Transition

### Transition Checked
AVOIDING_OBSTACLE → NAVIGATING

### Result
Required.

### Reason
Without this transition, the robot would remain stuck in AVOIDING_OBSTACLE and could not continue its delivery journey.

### Requirement Related
R4.

---

## Check 3 — Obstacle During Delivery

### Transition Checked
AVOIDING_OBSTACLE → DELIVERING

### Result
Invalid.

### Reason
The robot must first return to NAVIGATING and reach the destination before entering DELIVERING.

### Requirement Violated
R10.

# Delivery Robot Requirements

| Req. ID | Requirement |
|---|---|
| R1 | The system shall place the robot in the IDLE state when the robot is switched on. |
| R2 | The system shall transition the robot from IDLE to NAVIGATING when a delivery request is received. |
| R3 | The system shall transition the robot from NAVIGATING to AVOIDING_OBSTACLE when an obstacle is detected. |
| R4 | The system shall transition the robot from AVOIDING_OBSTACLE back to NAVIGATING when the obstacle has been avoided. |
| R5 | The system shall transition the robot from NAVIGATING to DELIVERING when the destination is reached. |
| R6 | The system shall transition the robot from DELIVERING to RETURNING when the package is successfully delivered. |
| R7 | The system shall transition the robot from RETURNING to IDLE when the warehouse is reached. |
| R8 | The system shall transition the robot from NAVIGATING to RETURNING when the battery reaches a critical level. |
| R9 | The system shall prevent the robot from transitioning directly from IDLE to DELIVERING. |
| R10 | The system shall prevent the robot from transitioning directly from AVOIDING_OBSTACLE to DELIVERING. |

# Delivery Robot State Model

## States

| State | Description |
|---|---|
| IDLE | Robot is waiting for a delivery request. |
| NAVIGATING | Robot is travelling toward the destination. |
| AVOIDING_OBSTACLE | Robot is avoiding a detected obstacle. |
| DELIVERING | Robot is delivering the package at the destination. |
| RETURNING | Robot is travelling back to the warehouse. |

## Events / Conditions

1. Delivery Request Received
2. Obstacle Detected
3. Obstacle Avoided
4. Destination Reached
5. Delivery Successful
6. Critical Battery
7. Warehouse Reached

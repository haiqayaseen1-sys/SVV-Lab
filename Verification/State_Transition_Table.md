# State Transition Table

## Task 4 — State Transition Table

| Current State | Event/Condition | Next State | Action |
|---|---|---|---|
| IDLE | Delivery Request Received | NAVIGATING | Start moving toward the destination. |
| NAVIGATING | Obstacle Detected | AVOIDING_OBSTACLE | Stop normal navigation and avoid the obstacle. |
| AVOIDING_OBSTACLE | Obstacle Avoided | NAVIGATING | Resume navigation toward the destination. |
| NAVIGATING | Destination Reached | DELIVERING | Start the delivery process. |
| DELIVERING | Delivery Successful | RETURNING | Begin returning to the warehouse. |
| NAVIGATING | Critical Battery | RETURNING | Stop the delivery journey and return to the warehouse. |
| RETURNING | Warehouse Reached | IDLE | Become idle and wait for another delivery request. |

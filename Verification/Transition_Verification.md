# Transition Verification

## Task 5 — Verification Activity

### Check 1 — Invalid Transition

**Question:** Can the robot move directly from IDLE to DELIVERING?

**Answer:** No.

**Reason:** The robot must first receive a delivery request and navigate to the destination. A direct transition from IDLE to DELIVERING would violate the behavioral restriction.

---

### Check 2 — Missing Transition

**Question:** What happens if the robot moves from NAVIGATING to AVOIDING_OBSTACLE but there is no transition back?

**Answer:** The robot cannot continue its delivery journey.

**Reason:** After successfully avoiding the obstacle, the robot must return to NAVIGATING so that it can continue toward the destination.

---

### Check 3 — Obstacle During Delivery

**Question:** Can the robot move from AVOIDING_OBSTACLE directly to DELIVERING?

**Answer:** No.

**Reason:** The robot must first return to NAVIGATING after the obstacle has been avoided. It can enter DELIVERING only after reaching the destination.

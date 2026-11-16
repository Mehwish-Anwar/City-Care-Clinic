# Validation Run A (Student A)


| ID | Item | Answer | Evidence | Where question came from |
| :--- | :--- | :--- | :--- | :--- |
| CL-001 | Does each requirement contain only one "shall" or "may" statement? | No | R-07 has three actions in one sentence (cancel, update schedule, notify). | Rule: Clear |
| CL-002 | Is every requirement free of undefined vague words (e.g., "quickly", "user-friendly", "securely", "normal", "policy")? | No | R-02 ("quickly"), R-08 ("user-friendly"), R-09 ("securely"), R-12 ("normal"), and R-13 ("policy") use vague words. | Rule: Clear |
| CL-003 | Does every speed or time requirement state a number with a unit? | No | R-02 has no response time number; R-12 gives no exact working hours. | Rule: Testable |
| CL-004 | Could a pass/fail test be written for every requirement? | No | R-02, R-08, R-09, and R-13 cannot be tested objectively without clear metrics. | Rule: Testable |
| CL-005 | Are all appointment duration rules free of contradictions? | No | R-04 fixes appointments at 15 minutes, which contradicts R-05 (10 to 30 minutes). | Rule: Free of contradictions |
| CL-006 | Does the document define what happens when a reminder fails to reach a patient? | No | R-06 mentions sending reminders, but gives no fallback if delivery fails. | Rule: Complete |
| CL-007 | Does the document specify how the system stops two users from booking the exact same time slot? | No | R-03 says "prevent double bookings" but gives no locking or conflict rule. | Risk: Double bookings |
| CL-008 | Does the document state how many minutes before an appointment a reminder is sent? | No | R-06 says "before appointments" without specifying hours or minutes. | Risk: Forgotten appointments |
| CL-009 | Does the document define a cutoff time before an appointment after which online cancellation is blocked? | No | R-07 allows cancellation "at any time," even 1 minute before the visit. | Risk: Late cancellations |
| CL-010 | Does the document specify how many concurrent users the system must support during Monday morning peak hours? | No | Missing requirement; the SRS has no load or capacity limit for busy hours. | Risk: Monday morning rush |
| CL-011 | Does the document state a backup plan if the online system goes offline during clinic hours? | No ? | R-12 covers working hours, but no offline mode or recovery plan is stated. | Risk: System downtime |
| CL-012 | Does the document state how a patient receives confirmation after booking an appointment? | No | R-01 allows booking online, but never mentions sending a booking confirmation. | User: Patient |
| CL-013 | Does the document state whether doctors can block off unavailable time slots on their schedule? | No | R-14 only lets doctors view their daily schedule, not block breaks or leave. | User: Doctor |
| CL-014 | Does the document specify how emergency walk-in patients are given priority over routine bookings? | No | R-10 mentions walk-ins, but gives no rule for urgent emergency overrides. | User: Receptionist |
| CL-015 | Does the document state how a clinic administrator adds new doctors to the system? | No | Missing requirement; Clinic administrator has zero requirements in the SRS. | User: Clinic administrator |
| CL-016 | Does the document specify which user roles may view a patient's medical record? | No | R-09 says "stored securely" without defining role-based access rules. | User: Data protection officer |
| CL-017 | Does the document specify accessibility features (such as large text or screen reader support) for elderly patients? | No ? | R-08 says "user-friendly for all age groups" with no accessibility details. | Risk: Elderly patients excluded |
| CL-018 | Does the document define the exact "clinic policy" rules for handling overdue payments? | No | R-13 refers to "clinic policy" without explaining what the system must do. | Rule: Complete |

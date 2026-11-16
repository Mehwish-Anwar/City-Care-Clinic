# Agreed Validation Findings — MediTrack SRS

After comparing Run A and Run B, we recommend that **CityCare Clinic NOT sign the contract** until the software company fixes the following problems in the SRS:

## 1. Direct Contradiction
- **R-04 vs. R-05 (Conflicting Appointment Lengths):** R-04 says every appointment must last **15 minutes**, while R-05 says doctors can set appointment lengths between **10 and 30 minutes**. Both cannot be true at the same time.

## 2. Vague and Untestable Requirements
- **R-02 (No Speed Target):** "Respond quickly" has no number or unit (e.g., *under 2 seconds*). This is especially risky during Monday morning peak hours.
- **R-08 (No Accessibility Standards):** "User-friendly for all age groups" cannot be tested and does not protect elderly patients (e.g., needs large fonts, simple navigation, or phone support).
- **R-09 (No Privacy or Access Rules):** "Stored securely" does not define encryption, login rules, or which staff roles (doctor vs. receptionist) can view private medical records.
- **R-12 (Undefined Hours):** "Normal working hours" lacks exact opening and closing times, days of the week, and required uptime percentage.
- **R-13 (Missing Payment Rules):** "As per clinic policy" is undefined. The SRS must state whether overdue payments block new bookings or only trigger a warning.

## 3. Incomplete & Ambiguous Requirements
- **R-03 (No Double-Booking Mechanism):** Simply stating "prevent double bookings" is not enough; the SRS must explain how two simultaneous requests for the same slot are handled.
- **R-06 (Incomplete Reminder Rules):** Does not state *when* reminders are sent (e.g., 24 hours and 2 hours before), *how* they are sent (SMS/email), or what happens if delivery fails.
- **R-07 (Compound Requirement & No Cutoff Time):** Combines three separate actions into one sentence and allows patients to cancel "at any time" with zero notice, which wastes doctor time.
- **R-10 (No Emergency Walk-In Priority):** Allows receptionists to book walk-ins, but gives no rule for handling urgent emergency walk-ins when slots are full.
- **R-11 (Unclear Limit Scope):** "Up to 3 active appointments" does not state whether this limit applies per doctor, per clinic, or across a specific time period.

## 4. Missing User & Operational Requirements
- **No Clinic Administrator Functions:** The Clinic Administrator is listed as a system user, but there are zero requirements for adding/removing doctors, setting clinic holidays, or managing user accounts.
- **No Doctor Schedule Controls:** R-14 only allows doctors to *view* their schedule; they cannot block off leave, breaks, or unavailable slots.
- **No Booking Confirmation:** R-01 allows patients to book online, but never specifies sending a booking confirmation or reference number.
- **No Peak-Load or Backup Plan:** The SRS ignores the clinic manager's worry about busy Monday mornings (concurrent user capacity) and lacks a backup workflow if the system goes offline.

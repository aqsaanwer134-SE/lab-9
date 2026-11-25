# Task 2 Individual Run – Student A (Part B, Alone)

**System:** MediTrack – Online Appointment System for CityCare Clinic

| Field | Value |
| --- | --- |
| Reviewer | Student A |
| Date | 2026-11-25 |
| Checklist | `checklist/v0.1.md` |
| Document reviewed | `srs/meditrack-srs.md` |
| Start time | 10:00 |
| End time | 10:28 |
| Duration | 28 minutes |
| Conditions | Individual run, no discussion with partner |

**Legend:** `?` in the last column = reviewer was unsure.

| ID | Item | Answer | Evidence (Requirement ID and reason) | Unsure |
| --- | --- | --- | --- | --- |
| C-01 | Does every response-time requirement state a numeric limit in a time unit? | No | R-02: "quickly" has no number or unit. | |
| C-02 | Does every requirement that uses a quality word state a measurable acceptance criterion? | No | R-02 "quickly", R-08 "user-friendly", R-09 "securely" have no measure. | |
| C-03 | Is the appointment length defined consistently in every requirement that mentions it? | No | R-04 fixes 15 minutes; R-05 allows 10 to 30 minutes. | |
| C-04 | Does each requirement describe exactly one behaviour? | No | R-07: cancellation, schedule update and receptionist notification in one requirement. | |
| C-05 | Does the document define the term "active appointment"? | No | R-11: "active" is used but never defined. | |
| C-06 | Is every external policy referred to by a requirement identified by name or included in the document? | No | R-13: "clinic policy" is not named or attached. | |
| C-07 | Does the document define what counts as a double booking? | No | R-03: states the goal only; no definition (same doctor, same patient, overlap?). | |
| C-08 | Does the document state what happens when two users try to book the same slot at the same time? | No | R-03: no rule for simultaneous attempts. | ? |
| C-09 | Does the document state how long before an appointment each reminder is sent? | No | R-06: "before appointments" gives no time. | |
| C-10 | Does the document name the channel used to send reminders? | No | R-06: no SMS, email, call or app channel stated. | |
| C-11 | Does the document say which roles may view a patient's medical record? | No | R-09: no roles or access rules. | |
| C-12 | Does the document require every access to a patient's record to be written to an audit log? | No | R-09: no audit or access logging. | |
| C-13 | Does the document provide a booking channel other than the website for patients who cannot use it? | No | R-01 is online only; R-10 covers walk-ins only, not phone booking. | ? |
| C-14 | Does the document state how emergency walk-in patients are given priority? | No | R-10: walk-ins are covered; emergencies and priority are not mentioned. | |
| C-15 | Does the document state the number of simultaneous users the system must support? | No | No requirement mentions load or concurrent users. | |
| C-16 | Does the document define "normal working hours" with specific days and times? | No | R-12: hours are not specified. | |
| C-17 | Does the document state that a cancelled slot becomes available for other bookings? | No | R-07: schedule is updated, but slot release for rebooking is not stated. | |
| C-18 | Does the document state how a doctor blocks time when unavailable? | No | R-14 and R-05 do not cover leave or blocked time. | |
| C-19 | Does the document contain at least one requirement for the clinic administrator role? | No | No requirement mentions the administrator. | |
| C-20 | Does the document state that receptionists can book appointments for walk-in patients? | Yes | R-10 states this directly. | |

## Summary

| Yes | No | N/A | Unsure (?) |
| --- | --- | --- | --- |
| 1 | 19 | 0 | 2 (C-08, C-13) |

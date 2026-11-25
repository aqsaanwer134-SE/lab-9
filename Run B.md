# Task 2 Individual Run – Student B (Part B, Alone)

**System:** MediTrack – Online Appointment System for CityCare Clinic

| Field | Value |
| --- | --- |
| Reviewer | Student B |
| Date | 2026-11-25 |
| Checklist | `checklist/v0.1.md` |
| Document reviewed | `srs/meditrack-srs.md` |
| Start time | 10:00 |
| End time | 10:31 |
| Duration | 31 minutes |
| Conditions | Individual run, no discussion with partner |

**Legend:** `?` in the last column = reviewer was unsure.

| ID | Item | Answer | Evidence (Requirement ID and reason) | Unsure |
| --- | --- | --- | --- | --- |
| C-01 | Does every response-time requirement state a numeric limit in a time unit? | No | R-02: "quickly" is not a number. | |
| C-02 | Does every requirement that uses a quality word state a measurable acceptance criterion? | No | R-08 "user-friendly" and R-09 "securely" have no measure (R-02 counted under C-01). | |
| C-03 | Is the appointment length defined consistently in every requirement that mentions it? | No | R-04 (fixed 15 min) contradicts R-05 (10 to 30 min). | |
| C-04 | Does each requirement describe exactly one behaviour? | No | R-07 contains three behaviours (cancel, update schedule, notify). | |
| C-05 | Does the document define the term "active appointment"? | No | R-11: no definition (future only? confirmed only?). | ? |
| C-06 | Is every external policy referred to by a requirement identified by name or included in the document? | No | R-13: "clinic policy" is not provided. | |
| C-07 | Does the document define what counts as a double booking? | Yes | R-03 addresses double bookings. | ? |
| C-08 | Does the document state what happens when two users try to book the same slot at the same time? | No | R-03: no rule on simultaneous requests. | |
| C-09 | Does the document state how long before an appointment each reminder is sent? | No | R-06: timing missing. | |
| C-10 | Does the document name the channel used to send reminders? | No | R-06: channel missing. | |
| C-11 | Does the document say which roles may view a patient's medical record? | No | R-09: no roles named. | |
| C-12 | Does the document require every access to a patient's record to be written to an audit log? | No | R-09: no logging requirement. | |
| C-13 | Does the document provide a booking channel other than the website for patients who cannot use it? | Yes | R-10: receptionists can book for patients who come to the clinic. | ? |
| C-14 | Does the document state how emergency walk-in patients are given priority? | No | R-10: no mention of emergency or priority. | |
| C-15 | Does the document state the number of simultaneous users the system must support? | No | Nothing on load in any requirement. | |
| C-16 | Does the document define "normal working hours" with specific days and times? | No | R-12: "normal working hours" is undefined. | |
| C-17 | Does the document state that a cancelled slot becomes available for other bookings? | Yes | R-07: updating the doctor's schedule implies the slot is freed. | ? |
| C-18 | Does the document state how a doctor blocks time when unavailable? | No | No requirement for leave or blocked time. | |
| C-19 | Does the document contain at least one requirement for the clinic administrator role? | No | Administrator is never mentioned. | |
| C-20 | Does the document state that receptionists can book appointments for walk-in patients? | Yes | R-10. | |

## Summary

| Yes | No | N/A | Unsure (?) |
| --- | --- | --- | --- |
| 4 | 16 | 0 | 4 (C-05, C-07, C-13, C-17) |

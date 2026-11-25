# Task 3 Joint Findings (Part B, Together)

**System:** MediTrack – Online Appointment System for CityCare Clinic

**Output:** Comparison of Run A and Run B, conflict resolution, final answers and the real problems in the SRS.

| Field | Value |
| --- | --- |
| Reviewers | Student A and Student B |
| Date | 2026-11-25 |
| Joint session | 20 minutes |
| Inputs | `runs/run-A.md`, `runs/run-B.md` |
| Checklist | `checklist/v0.1.md` (20 items) |

## 1. Comparison of the Two Runs

| Measure | Result |
| --- | --- |
| Items answered identically | 17 of 20 (85%) |
| Items answered differently | 3 of 20 (C-07, C-13, C-17) |
| Items marked "?" by A | C-08, C-13 |
| Items marked "?" by B | C-05, C-07, C-13, C-17 |
| Time taken | A: 28 minutes, B: 31 minutes |

All three disagreements were also marked "?" by at least one reviewer. This shows that the "?" mark correctly predicted the weak items.

## 2. Conflicts Between Run A and Run B

| Item | Student A | Student B | Cause of conflict | Agreed answer | Reasoning |
| --- | --- | --- | --- | --- | --- |
| C-07 | No | Yes | Item says "define", but B accepted a mere mention of "double bookings" in R-03. | **No** | R-03 states a goal but never says what a double booking is (same doctor and overlapping time? same patient in two places?). |
| C-13 | No | Yes | Item does not say whether in-person booking counts as "another channel". | **No** | R-10 only covers walk-ins who are already at the clinic. An elderly patient who telephones, which is the current process, is not covered. |
| C-17 | No | Yes | B treated "update the doctor's schedule" as meaning the slot is released. | **No** | R-07 does not say the slot becomes bookable by others. An implication is not a requirement. |

**Lesson:** All three conflicts come from item wording (Unambiguous test), not from reading mistakes. These items are rewritten in Section 6.

## 3. Final Agreed Answers

| ID | Final answer | Evidence |
| --- | --- | --- |
| C-01 | No | R-02 has no number or unit. |
| C-02 | No | R-02, R-08, R-09 use unmeasured quality words. |
| C-03 | No | R-04 and R-05 contradict each other. |
| C-04 | No | R-07 contains three behaviours. |
| C-05 | No | R-11 uses "active" without definition. |
| C-06 | No | R-13 refers to an unnamed "clinic policy". |
| C-07 | No | R-03 does not define double booking. |
| C-08 | No | R-03 has no rule for simultaneous requests. |
| C-09 | No | R-06 gives no reminder timing. |
| C-10 | No | R-06 gives no reminder channel. |
| C-11 | No | R-09 names no roles. |
| C-12 | No | R-09 has no audit-log requirement. |
| C-13 | No | R-01 is online only; R-10 covers walk-ins only. |
| C-14 | No | R-10 has no emergency or priority rule. |
| C-15 | No | No load requirement exists. |
| C-16 | No | R-12 does not define working hours. |
| C-17 | No | R-07 does not release the slot. |
| C-18 | No | No unavailability requirement exists. |
| C-19 | No | Administrator never appears. |
| C-20 | Yes | R-10. |

**Result: 19 defects found, 1 pass.** The high number of "No" answers is expected for a draft SRS with this many vague requirements.

## 4. Real Problems in the Document

Severity scale: **Critical** = directly breaks a clinic worry; **High** = likely to cause failure or dispute; **Medium** = causes confusion or rework.

| ID | Requirement(s) | Problem | Clinic worry | Checklist items | Severity | Recommended fix |
| --- | --- | --- | --- | --- | --- | --- |
| F-01 | R-03 | "Prevent double bookings" is not defined and gives no rule for two users booking the same slot at the same time. The manager's top concern is therefore not testable. | Double bookings | C-07, C-08 | Critical | Define double booking (same doctor, overlapping time). State that the second simultaneous request is rejected and the user is offered the next free slot. |
| F-02 | R-09 | "Stored securely" is vague. No roles, no access rules, no audit log, no encryption, no legal basis. | Medical privacy | C-02, C-11, C-12 | Critical | List roles allowed to view records, require encryption at rest and in transit, and log every access. |
| F-03 | R-04, R-05 | Direct contradiction: fixed 15 minutes versus a doctor-set 10 to 30 minutes. | Double bookings | C-03 | High | Keep R-05, and make 15 minutes the default length. Delete R-04 or merge it into R-05. |
| F-04 | R-02 | "Quickly" has no number or unit, so it cannot be tested. | Busy Mondays | C-01, C-02 | High | For example: "95% of booking requests shall complete within 3 seconds with 100 concurrent users." |
| F-05 | R-06 | Reminder timing, channel, number of reminders and patient reply are missing. | Forgotten appointments | C-09, C-10 | High | State timing (for example 24 hours and 2 hours before), channel (SMS or call for elderly patients) and whether the patient can confirm or cancel. |
| F-06 | R-12 | "Normal working hours" is undefined. No availability percentage, no peak-load requirement. | Busy Mondays | C-15, C-16 | High | Define days and hours, an availability target, and a Monday 08:00 to 12:00 load target. |
| F-07 | R-10 | Walk-ins are covered, emergencies are not. No priority rule, no rule for a fully booked doctor. | Emergency walk-ins | C-14 | High | Add an emergency-booking requirement that lets a receptionist insert a patient ahead of the queue and records the reason. |
| F-08 | R-01, R-08 | System is online only. "User-friendly for all age groups" is untestable. No phone or assisted booking for elderly patients. | Elderly patients | C-02, C-13 | High | Add assisted booking by telephone through a receptionist. Replace R-08 with measurable criteria (for example, "90% of test users aged 65+ complete a booking unaided in 5 minutes"). |
| F-09 | Whole document | Clinic administrator and data protection officer have no requirements. Two of five users are missing. | Medical privacy | C-12, C-19 | High | Add administrator requirements (manage doctors, schedules, users) and DPO requirements (audit report, data-access requests). |
| F-10 | R-07 | Three behaviours in one requirement. "At any time" has no cut-off, so late cancellations leave empty slots. Slot release is not stated. Patient receives no confirmation. | Forgotten appointments (cost) | C-04, C-17 | Medium | Split into separate requirements. Add a cancellation cut-off or late-cancellation rule. State that the slot is released and the patient receives confirmation. |
| F-11 | R-11 | "Active appointment" is undefined. It is unclear whether the limit also applies to bookings made by receptionists, or to a parent booking for family members. | Elderly patients | C-05 | Medium | Define "active" (for example, confirmed and not yet past). State who the limit applies to and any exceptions. |
| F-12 | R-13 | Refers to an unnamed "clinic policy". Payment handling appears nowhere else, so it is outside the appointment scope or incomplete. | None directly | C-06 | Medium | Attach the policy by name and version, or remove the requirement and treat payments in a separate document. |
| F-13 | Whole document | No requirement lets a doctor block time for leave or breaks. Bookings could be made when the doctor is absent. | Double bookings | C-18 | Medium | Add: "Doctors shall be able to mark time slots as unavailable, and those slots shall not be bookable." |

## 5. Traceability: Clinic Worry to Findings

| Clinic manager's worry | Covered by findings | Status in current SRS |
| --- | --- | --- |
| Double bookings must never happen | F-01, F-03, F-13 | Not adequately addressed |
| Patients forget appointments | F-05, F-10 | Weak |
| Medical information is private | F-02, F-09 | Not adequately addressed |
| Elderly and emergency walk-ins must not be left out | F-07, F-08, F-11 | Not adequately addressed |
| Monday mornings are very busy | F-04, F-06 | Not addressed |

## 6. Improvements for Checklist v0.2

| Item | Weakness found | Proposed change |
| --- | --- | --- |
| C-07 | "Define" was read as "mention". | "Does the document state the conditions (doctor and time overlap) under which two bookings count as a double booking?" |
| C-13 | "Other than the website" unclear for in-person booking. | "Does the document allow a patient to book by telephone through a receptionist?" |
| C-17 | "Becomes available" can be inferred. | "Does a requirement explicitly say that a cancelled slot can be booked by another patient?" |
| C-02 | Overlaps with C-01 for R-02. | Exclude response-time words from C-02. |
| C-05 | Single-term item is narrow. | Generalise: "Is every term that controls a business rule defined?" |
| New | Checklist contains almost no "Yes" answers on this SRS. | Add items that pass on good practice (for example, "Does every requirement have a unique ID?") to confirm the checklist can discriminate. |

## 7. Conclusion and Recommendation

The MediTrack SRS addresses none of the clinic manager's five worries to a testable standard. We recommend that CityCare Clinic **does not sign the contract** until the vendor resolves at least the Critical and High findings (F-01 to F-09) and re-issues the SRS for a second review with checklist v0.2.

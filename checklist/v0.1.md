# Task 1 Build the Validation Checklist (Part A)

**System:** MediTrack – Online Appointment System for CityCare Clinic

**Output:** Checklist v0.1 with 20 yes/no items, each tested against AOUT (Atomic, Observable, Unambiguous, Traceable).

| Field | Value |
| --- | --- |
| Version | 0.1 |
| Applies to | `srs/meditrack-srs.md` |
| Number of items | 20 |
| Answer values | Yes / No / N/A |

## 1. Rules Applied to Every Item

Every item passes the four **AOUT** tests:

| Letter | Test | Meaning |
| --- | --- | --- |
| A | Atomic | One question only (no "and"). |
| O | Observable | Answerable by reading the document. |
| U | Unambiguous | Two reviewers give the same answer. |
| T | Traceable | The last column records why the question exists. |

**Polarity rule:** "Yes" is always the good answer. "No" signals a defect and must be justified with a requirement ID.

## 2. Sources of the Items

### 2.1 Risk Register (CityCare Clinic)

| Risk ID | Risk | Clinic manager's worry |
| --- | --- | --- |
| RK-1 | Two patients booked into the same slot | Double bookings must never happen |
| RK-2 | Patients forget appointments, causing lost revenue | Patients forget appointments |
| RK-3 | Medical information disclosed to the wrong person | Medical information is private |
| RK-4 | Elderly patients cannot use the online system | Elderly patients must not be left out |
| RK-5 | Emergency walk-ins are treated like routine bookings | Emergency walk-ins must not be left out |
| RK-6 | System is slow or unavailable at peak time | Monday mornings are very busy |
| RK-7 | Cancelled slots stay empty and are wasted | Patients forget appointments, which costs money |

### 2.2 Document-Quality Rules

Clear, Testable, Consistent, Complete, Atomic.

### 2.3 User Coverage

| User | Items |
| --- | --- |
| Patient | C-09, C-10, C-13 |
| Doctor | C-18 |
| Receptionist | C-14, C-20 |
| Clinic administrator | C-19 |
| Data protection officer | C-11, C-12 |

## 3. Checklist

| ID | Item | Answer | Evidence | Where question came from |
| --- | --- | --- | --- | --- |
| C-01 | Does every response-time requirement state a numeric limit in a time unit? | | | Quality rule: Testable; RK-6 |
| C-02 | Does every requirement that uses a quality word (such as "quickly", "securely", "user-friendly") state a measurable acceptance criterion? | | | Quality rule: Clear / Testable |
| C-03 | Is the appointment length defined consistently in every requirement that mentions it? | | | Quality rule: Consistent; RK-1 |
| C-04 | Does each requirement describe exactly one behaviour? | | | Quality rule: Atomic |
| C-05 | Does the document define the term "active appointment"? | | | Quality rule: Clear |
| C-06 | Is every external policy referred to by a requirement identified by name or included in the document? | | | Quality rule: Complete |
| C-07 | Does the document define what counts as a double booking? | | | RK-1 |
| C-08 | Does the document state what happens when two users try to book the same slot at the same time? | | | RK-1 |
| C-09 | Does the document state how long before an appointment each reminder is sent? | | | RK-2; User: Patient |
| C-10 | Does the document name the channel used to send reminders? | | | RK-2; User: Patient |
| C-11 | Does the document say which roles may view a patient's medical record? | | | RK-3; User: Data protection officer |
| C-12 | Does the document require every access to a patient's record to be written to an audit log? | | | RK-3; User: Data protection officer |
| C-13 | Does the document provide a booking channel other than the website for patients who cannot use it? | | | RK-4; User: Patient (elderly) |
| C-14 | Does the document state how emergency walk-in patients are given priority? | | | RK-5; User: Receptionist |
| C-15 | Does the document state the number of simultaneous users the system must support? | | | RK-6 |
| C-16 | Does the document define "normal working hours" with specific days and times? | | | RK-6; Quality rule: Unambiguous |
| C-17 | Does the document state that a cancelled slot becomes available for other bookings? | | | RK-7 |
| C-18 | Does the document state how a doctor blocks time when unavailable? | | | User: Doctor |
| C-19 | Does the document contain at least one requirement for the clinic administrator role? | | | User: Clinic administrator |
| C-20 | Does the document state that receptionists can book appointments for walk-in patients? | | | User: Receptionist |

## 4. Instructions for Reviewers

1. Answer every item with **Yes**, **No** or **N/A**.
2. For every **No**, record the requirement ID and a one-line reason.
3. Mark any item you were unsure about with **?**.
4. Record your start time and end time.
5. Do not discuss answers with your partner during the individual run.

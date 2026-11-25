# lab-9



MediTrack is an online appointment system proposed for CityCare Clinic (12 doctors, 6 receptionists, about 400 patients per week). This lab builds a validation checklist, applies it to the vendor's SRS in two independent runs, and agrees on the real problems in the document.

## Structure

| Task | File | Content |
|---|---|---|
| Input | `srs/meditrack-srs.md` | The MediTrack SRS to be validated (R-01 to R-14). |
| **Task 1** | `checklist/v0.1.md` | Validation checklist with 20 items, 7 risks and coverage of all 5 users. |
| **Task 2** | `runs/run-A.md` | Student A's individual run (28 minutes). |
| **Task 2** | `runs/run-B.md` | Student B's individual run (31 minutes). |
| **Task 3** | `findings.md` | Conflicts between the runs, final answers and 13 findings. |

## Key Results

| Measure | Result |
|---|---|
| Checklist items | 20 (Yes is always the good answer) |
| Agreement between A and B | 17 of 20 (85%) |
| Conflicts resolved | 3 (C-07, C-13, C-17) |
| Defects found | 19 of 20 items answered No |
| Real problems | 13 (2 Critical, 7 High, 4 Medium) |
| Recommendation | Do not sign until Critical and High findings are fixed |

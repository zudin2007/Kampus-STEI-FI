# FASE 7: EXCEL TRACKING TEMPLATES
## Ready-to-Use Spreadsheet Formats

---

## TEMPLATE 1: TA_Topics_Submitted.xlsx

**Purpose:** Track semua topic submissions dari mahasiswa

```
SHEET: "Submissions"

COLUMNS:
A  | NIU          | Student ID (e.g., 2203001)
B  | Nama         | Full name
C  | Program      | Program of study (STEI-FI)
D  | Topik        | Submitted topic title
E  | Area         | Area (SI, Keamanan, Cloud, AI, Networking, Other)
F  | Deskripsi    | Brief description (100 words max)
G  | Alasan       | Reason for choosing topic
H  | Status       | Submitted / Pending / Received
I  | Tanggal Terima | Date received (auto: TODAY())
J  | Catatan      | Any notes (incomplete, format issue, etc)

SAMPLE DATA ROW:
| 2203001 | Andi Wijaya | STEI-FI | Mobile App Security Framework | Keamanan | Framework untuk... | Tertarik dgn... | Submitted | 20/6/26 | Format OK |

AUTO CALCULATIONS:
- Row total submitted: COUNT non-empty
- Pending count: COUNTIF(H:H, "Pending")
- On-time submission: COUNTIF(I:I, "<=20/6/26")

PIVOT TABLE (Optional):
- Count by Area (how many in each research area)
- Count by Program
- Submission timeliness
```

---

## TEMPLATE 2: TA_Topics_Decision.xlsx

**Purpose:** Track review results (Approved / Revision Needed / Rejected)

```
SHEET: "Review Results"

COLUMNS:
A  | NIU          | Student ID
B  | Nama         | Full name
C  | Topik        | Topic title
D  | Area         | Area
E  | Reviewer 1   | Name of reviewer
F  | Reviewer 2   | Name of reviewer
G  | Decision     | APPROVED / REVISION NEEDED / REJECTED
H  | Feedback 1   | Main feedback point
I  | Feedback 2   | Second feedback
J  | Feedback 3   | Third feedback (if any)
K  | Actionable   | What student needs to fix (if revision needed)
L  | Deadline     | Resubmission deadline (if revision)
M  | Email Sent   | Date feedback email sent
N  | Student Response | Received revision? Y/N/Pending
O  | Final Status | APPROVED (after revision) / REJECTED / APPROVED (original)

SAMPLE ROW:
| 2203001 | Andi | Mobile App Security | Keamanan | Dr. Budi | Dr. Siti | APPROVED | Good scope | Feasible 1sem | Original | - | - | 25/6 | - | APPROVED |

CONDITIONAL FORMATTING:
- APPROVED → Green fill
- REVISION NEEDED → Yellow fill
- REJECTED → Red fill

AUTO SUMMARY:
- Total approved: COUNTIF(G:G, "APPROVED")
- Total revision needed: COUNTIF(G:G, "REVISION NEEDED")
- Total rejected: COUNTIF(G:G, "REJECTED")
- Approval rate: [Approved count / Total] %

FILTERS:
- By Area (dropdown)
- By Decision (dropdown)
- By Student Status (dropdown)
```

---

## TEMPLATE 3: TA_Supervisor_Assignment.xlsx

**Purpose:** Assign pembimbing & track workload balance

```
SHEET: "Assignments"

COLUMNS:
A  | NIU          | Student ID
B  | Nama         | Student name
C  | Topik        | Assigned topic
D  | Area         | Research area
E  | Supervisor Utama | Primary supervisor name
F  | Supervisor Utama Email | Email for contact
G  | Supervisor Utama Phone | Phone for contact
H  | Co-Supervisor | Co-supervisor (if applicable)
I  | Co-Sup Email | Email
J  | Assignment Date | When assigned (auto: TODAY())
K  | Status       | ASSIGNED / CONFIRMED / PENDING CONFIRMATION
L  | Confirmation Date | When supervisor confirmed
M  | Notes        | Any special notes

SAMPLE ROW:
| 2203001 | Andi | Mobile App Security | Keamanan | Dr. Budi | budi@stei.ac.id | 081234567 | Dr. Siti | siti@stei.ac.id | 28/6 | CONFIRMED | 28/6 | - |

SHEET: "Supervisor Workload"

COLUMNS:
A  | Supervisor   | Supervisor name
B  | Existing    | How many students already (from previous year)
C  | New Assigned | New students assigned this year
D  | Total        | =B+C
E  | Max Allowed | 7 (company standard)
F  | Status      | OK / OVERLOAD
G  | Notes       | Can take more? Willing to overload?

SAMPLE ROW:
| Dr. Budi | 3 | 2 | 5 | 7 | OK | - |
| Dr. Siti | 5 | 3 | 8 | 7 | OVERLOAD | Agree to take 8 |

AUTO CHECKS:
- If Total > Max: Flag as "OVERLOAD" in red
- Total ALL assignments should not exceed [X students]
- Balance check: std dev of workload < 2 (fairly balanced)

PIVOT TABLE:
- Workload distribution (bar chart)
- Assignments per supervisor
```

---

## TEMPLATE 4: TA_Supervisor_Confirmations.xlsx

**Purpose:** Track supervisor confirmations & readiness

```
SHEET: "Confirmations"

COLUMNS:
A  | Supervisor   | Supervisor name
B  | Email Sent   | Date confirmation email sent
C  | Students Assigned | List of student names (comma separated)
D  | Count        | Number of students
E  | Confirmation | YES / NO / PENDING
F  | Confirmation Date | When they replied
G  | Any Issues?  | Conflict / Overload concern / Other
H  | Resolution   | What was done (reassign, negotiate, etc)
I  | Ready Status | READY / ON HOLD / NEEDS RESOLUTION
J  | Follow-up    | Date of follow-up (if pending)

SAMPLE ROW:
| Dr. Budi | 28/6 | Andi, Bobi, Citra | 3 | YES | 28/6 | None | - | READY | - |
| Dr. Siti | 28/6 | Dedi, Eka, Fani, Gina | 4 | PENDING | - | Not sure about Gina's topic | - | ON HOLD | 1/7 |

DEADLINE TRACKING:
- Confirmation deadline: [DATE + 2 DAYS]
- Any not confirmed by [DATE]? Flag for follow-up

AUTO SUMMARY:
- Confirmed: COUNTIF(E:E, "YES")
- Pending: COUNTIF(E:E, "PENDING")
- Declined: COUNTIF(E:E, "NO")
- Confirmation rate: [Confirmed / Total] %
- Status: ALL READY / SOME PENDING / ISSUES FOUND

IF ANY "NO":
→ ACTION REQUIRED - Escalate to Kaprodi for reassignment
```

---

## TEMPLATE 5: TA_First_Meeting_Checklist.xlsx

**Purpose:** Track first meetings between students & supervisors

```
SHEET: "First Meeting Tracking"

COLUMNS:
A  | NIU          | Student ID
B  | Nama         | Student name
C  | Supervisor   | Supervisor name
D  | Topic        | Topic
E  | Meeting Scheduled | Date scheduled (or "Not yet")
F  | Meeting Held | YES / NO / PENDING
G  | Meeting Date | Actual date held
H  | Duration (min) | Minutes spent
I  | Discussion Points | Briefly: design, methodology, resources, timeline
J  | Feedback Given | Summary of supervisor feedback
K  | Action Items | What student needs to do before next meeting
L  | Next Meeting | Date of next planned meeting
M  | Status       | ON TRACK / DELAYED / NEEDS FOLLOW-UP

SAMPLE ROW:
| 2203001 | Andi | Dr. Budi | Mobile App Security | 1 Jul | YES | 1/7 | 45 | Design, Literature | Good design, feasible scope | Start data collection, read 5 papers | 8/7 | ON TRACK |

AUTOMATED CHECKS:
- Meetings within 1 week of semester start? Flag if delayed
- All meetings held by [DATE]? COUNTIF(F:F, "YES") / Total
- On-time rate: [ON TRACK / DELAYED] count

ALERTS:
- If Meeting Scheduled = "Not yet" AND today >= [DATE] → FLAG "DELAYED"
- If NO meeting within 2 weeks → Escalate for intervention
```

---

## TEMPLATE 6: TA_Progress_Monitoring.xlsx

**Purpose:** Track overall progress during semester (Week-by-week)

```
SHEET: "Progress by Week"

COLUMNS:
A  | NIU          | Student ID
B  | Nama         | Student name
C  | Supervisor   | Supervisor name
D  | Topic        | Topic
E  | Wk1-2 Status | Literature review started? Y/N
F  | Wk3-4 Status | Data collection? Y/N
G  | Wk5-8 Status | Analysis started? Y/N
H  | Wk9-10 Status | Writing draft? Y/N
I  | Wk11-12 Status | Draft review 1 completed? Y/N
J  | Wk13-14 Status | Revision completed? Y/N
K  | Wk15 Status  | Final submission? Y/N
L  | Current Week | [AUTO: TODAY() - semester start week]
M  | Overall Progress | 0-100% estimate
N  | On Track?   | YES / DELAYED / AT RISK
O  | Issues      | Any blockers/concerns?
P  | Intervention | Action taken (if needed)

SAMPLE ROW:
| 2203001 | Andi | Dr. Budi | Mobile App Security | Y | Y | Y | N | - | - | - | 8 | 45% | DELAYED | Data access issues | Meeting to problem-solve |

CONDITIONAL FORMATTING:
- N/A → Gray (future week)
- Y → Green (completed)
- N → Red (not done, should be done)
- DELAYED → Yellow
- AT RISK → Red

HEAT MAP:
- Overall progress column colored by percentage (red <50%, yellow 50-75%, green 75%+)

SUMMARY STATISTICS:
- On time: [YES count / total]
- Delayed: [DELAYED count / total]
- At risk: [AT RISK count / total]
- Average progress: [AVG of %]
```

---

## TEMPLATE 7: TA_Plagiarism_Check.xlsx

**Purpose:** Track plagiarism check results & compliance

```
SHEET: "Plagiarism Results"

COLUMNS:
A  | NIU          | Student ID
B  | Nama         | Student name
C  | Topic        | Topic
D  | Submission Date | When submitted for plagiarism check
E  | Checker Used | Turnitin / iThenticate / Copyscape / Other
F  | Similarity %  | Plagiarism similarity percentage
G  | Status       | PASS (<20%) / FAIL (>20%) / PENDING
H  | Review by    | Who reviewed the report
I  | Review Date  | When reviewed
J  | Sources      | Top sources flagged (if >20%)
K  | Assessment   | Is plagiarism acceptable? (proper citations?) Y/N
L  | Action       | APPROVED / REQUEST REVISION / ESCALATE
M  | Student Response | Recheck date (if requested revision)
N  | Final Status | CLEARED / PENDING REVISION / ESCALATED

SAMPLE ROW:
| 2203001 | Andi | Mobile App Security | 15/12 | Turnitin | 18% | PASS | Dr. Budi | 15/12 | Mostly citations from books | Yes, proper citations | APPROVED | - | CLEARED |
| 2203002 | Bobi | Cloud Architecture | 15/12 | Turnitin | 35% | FAIL | Dr. Siti | 15/12 | Wikipedia 20%, ResearchPaper 10% | No, needs revision | REQUEST REVISION | 18/12 | PENDING |

THRESHOLD:
- <20% = PASS (automatic)
- 20-40% = NEEDS REVIEW
- >40% = LIKELY PLAGIARISM (escalate)

COMPLIANCE TRACKING:
- Total checked: COUNT non-empty in column E
- Passed (>20%): COUNTIF(G:G, "PASS")
- Failed or pending: COUNTIF(G:G, "FAIL") + COUNTIF(G:G, "PENDING")
- Compliance rate: [PASS / Total] %

IF NON-COMPLIANT:
→ Cannot defend unless cleared
→ Escalate to Kaprodi for final decision
```

---

## HOW TO USE THESE TEMPLATES

### Week 1 (20-26 Juni):
1. Create **TA_Topics_Submitted.xlsx**
2. Collect topic submissions → log in spreadsheet
3. Daily update of submission count

### Week 2 (23-25 Juni):
1. Create **TA_Topics_Decision.xlsx**
2. Record review results after dosen meeting
3. Generate summary for communication

### Week 2-3 (27-5 Juli):
1. Create **TA_Supervisor_Assignment.xlsx**
2. Assign supervisors & track workload balance
3. Create **TA_Supervisor_Confirmations.xlsx**
4. Track confirmations from dosen

### Semester Start (1 September+):
1. Create **TA_First_Meeting_Checklist.xlsx**
2. Update weekly as meetings happen
3. Create **TA_Progress_Monitoring.xlsx**
4. Update every 2 weeks during semester

### Before Submission:
1. Create **TA_Plagiarism_Check.xlsx**
2. Track plagiarism check results
3. Ensure all students passed before defense

---

## MASTER FOLDER STRUCTURE

```
TA_2026_2027/
├─ 01_SUBMISSIONS/
│  └─ TA_Topics_Submitted.xlsx [ACTIVE WEEK 1]
│
├─ 02_REVIEW/
│  └─ TA_Topics_Decision.xlsx [ACTIVE WEEK 2]
│
├─ 03_ASSIGNMENTS/
│  ├─ TA_Supervisor_Assignment.xlsx [ACTIVE WEEK 2-3]
│  └─ TA_Supervisor_Confirmations.xlsx [ACTIVE WEEK 3]
│
├─ 04_MONITORING/
│  ├─ TA_First_Meeting_Checklist.xlsx [ACTIVE SEM START]
│  └─ TA_Progress_Monitoring.xlsx [ACTIVE ONGOING]
│
├─ 05_FINAL/
│  └─ TA_Plagiarism_Check.xlsx [ACTIVE WEEK 15]
│
└─ BACKUPS/
   └─ [Archive of all above after completion]
```

---

**Versi:** 1.0 | **Status:** Ready to Use | **Untuk:** Phase 7 Implementation

# FASE 8: EXCEL TRACKING TEMPLATES
## Sistem Penilaian & Assessment TA 2026/2027

---

## TEMPLATE 1: Rubric_Master_[MK_CODE].xlsx

**Purpose:** Master rubric template untuk semua MK assessment

```
SHEET: "Rubric Template"

HEADER:
Course: [MK_CODE] [MK_NAME]
Instructor: [DOSEN_NAME]
Assessment: [Quiz 1 / Midterm / Final / Project / etc]
Date: [TGL ASSESSMENT]

CPMK ALIGNED:
Learning Outcomes Measured: [CPMK 1, 2, 3]

RUBRIC TABLE:
Columns:
A | Criteria (3-5 criteria)
B | Excellent (85-100 points)
C | Good (70-84 points)
D | Fair (60-69 points)
E | Poor (<60 points)
F | Student Score

SAMPLE ROWS:
| Completeness | All components present & detailed | Most components | Some missing | Major gaps | ___ |
| Accuracy | No errors | 1-2 minor | 3-4 errors | >4 errors | ___ |
| Clarity | Well-organized & clear | Generally clear | Somewhat unclear | Difficult | ___ |
| Originality | Fully original | Mostly original | Some copying | Extensive copying | ___ |

SCORING:
- Total points: Sum of all criteria (up to 100)
- Weight: [IF part of 30% tugas component = value out of 30]
- Notes: [Any special notes for this assessment]

INSTRUCTIONS FOR DOSEN:
☐ Create 1 rubric per assessment type (quiz, midterm, final, project)
☐ Keep 3-5 criteria (not too many)
☐ Make descriptions clear & specific
☐ Provide examples if helpful
☐ Save as: Rubric_[MK_CODE]_[Assessment_Type].xlsx

AUTO CALCULATION:
- Score for each student automatically sums criteria
- Ready to use for grade entry
```

---

## TEMPLATE 2: Grade_Entry_Form_[SEMESTER].xlsx

**Purpose:** Master grade entry tracking for semester

```
SHEET: "Grade Entry Log"

COLUMNS:
A  | Course Code | [MK_CODE]
B  | Course Name | [MK_NAME]
C  | Instructor  | [DOSEN_NAME]
D  | Total Students | [#]
E  | Grade Entry Start | [DATE]
F  | Grade Entry Deadline | [HARD DEADLINE DATE - NO EXTENSION]
G  | Status | SUBMITTED / PENDING / OVERDUE
H  | Submission Date | [When submitted to SIAKNG]
I  | Total Grades Submitted | [# of students]
J  | Verification | CHECKED / PENDING
K  | Issues Found | [Any errors found]
L  | Resolution | [How resolved]
M  | Notes | [Any special notes]

SAMPLE ROW:
| SI101 | Intro SI | Dr. Budi | 45 | 16-Jul | 5-Aug | PENDING | - | 0 | - | - | - | MK will start week 1 |
| SI102 | Programming | Dr. Siti | 50 | 16-Jul | 5-Aug | SUBMITTED | 4-Aug | 48 | CHECKED | 2 students absent | Marked as 0 | Missing: 2 students |

SUMMARY METRICS:
- Total MK: COUNT(A:A)
- Submitted: COUNTIF(G:G, "SUBMITTED")
- Pending: COUNTIF(G:G, "PENDING")
- Overdue: COUNTIF(G:G, "OVERDUE")
- Submission rate: [SUBMITTED / Total]%
- Verification rate: [CHECKED / Total]%

ALERTS:
- If status = "OVERDUE" → Escalate to Kaprodi IMMEDIATELY
- If verification = "PENDING" → Spot-check before posting to students
```

---

## TEMPLATE 3: Assessment_Schedule_[SEMESTER].xlsx

**Purpose:** Master assessment calendar for entire semester

```
SHEET: "Weekly Assessment Schedule"

COLUMNS:
A  | Week | 1-16
B  | Date | [START - END of week]
C  | Course Code | [MK_CODE]
D  | Course Name | [MK_NAME]
E  | Assessment Type | Quiz / Assignment / Midterm / Final / Project
F  | Assessment Title | [Specific name]
G  | Due Date | [When due]
H  | Responsible Dosen | [NAME]
I  | Submission Method | In-class / Online / Paper / SIAKNG
J  | Grading Deadline | [When grades must be entered]
K  | Weight | [% of final grade]
L  | Rubric Ready | YES / NO
M  | Materials Ready | YES / NO
N  | Notes | Any special notes

SAMPLE ROWS:
Week 1-2 | Jul 20-Aug 5 | SI101 | Intro SI | Assignment | Background Research | Jul 25 | Dr. Budi | Online/Email | Jul 26 | 5% | YES | YES | First week - light workload |
Week 8-9 | Sep 15-29 | SI101 | Intro SI | Midterm Exam | UTS | Sep 22 | Dr. Budi | In-class | Sep 23 | 35% | YES | YES | Schedule coordinated with other dosen |
Week 8-9 | Sep 15-29 | SI102 | Programming | Midterm Exam | UTS | Sep 23 | Dr. Siti | In-class | Sep 24 | 35% | YES | YES | No conflict with SI101 |

PIVOT TABLE:
- Assessments by week (histogram - shows if overload any week)
- Assessments by course (ensure reasonable spread)
- Grade entry deadline tracking

BALANCE CHECK:
- Week with most assessments: ___ (target: not >3 major assessments/week)
- No conflicting exams same time? Verify manually
- Grading deadlines feasible for dosen? (Should be within 3-5 days after assessment)

VERIFICATION:
☐ All midterms scheduled Week 8-9? YES
☐ All finals scheduled Week 15-16? YES
☐ No assessment on exam weeks (week 8, 15-16)? YES
☐ Grade entry deadlines clearly marked? YES
☐ No dosen overload (realistic grading timeline)? YES
```

---

## TEMPLATE 4: Dosen_Training_Attendance.xlsx

**Purpose:** Track training attendance & completion

```
SHEET: "Training Attendance"

COLUMNS:
A  | No | 1, 2, 3...
B  | Dosen Name | [NAME]
C  | Department | [DEPT]
D  | Training Session | Pagi (9am) / Siang (1pm)
E  | Attendance | HADIR / TIDAK / IZIN
F  | Sign-in Time | [TIME]
G  | Sign-out Time | [TIME]
H  | Duration | [AUTO: =G-F]
I  | Active Participation | YES / SOMEWHAT / NO
J  | Rubric Practice | YES / NO / PARTIAL
K  | SIAKNG Demo Participated | YES / NO
L  | Questions Asked | [Brief note]
M  | Certificate Given | YES / NO
N  | Post-Training Survey Score | [1-5 stars]
O  | Notes | [Any special notes]

SAMPLE ROW:
1 | Dr. Budi | SI | Pagi | HADIR | 09:00 | 11:00 | 2.0 hrs | YES | YES | YES | Yes, asked about rubric | YES | 5 | Good engagement, will implement |
2 | Dr. Siti | SI | Siang | HADIR | 13:00 | 15:00 | 2.0 hrs | YES | YES | YES | No questions | YES | 4 | Quiet but engaged |

SUMMARY:
- Total attended: COUNTIF(E:E, "HADIR")
- Absent: COUNTIF(E:E, "TIDAK")
- Excused: COUNTIF(E:E, "IZIN")
- Attendance rate: [HADIR / Total]%
- Avg participation: [AVG of participation score]
- Avg survey score: [AVG of survey]

FOLLOW-UP:
- Who didn't attend? [LIST] → Schedule alternative 1-on-1
- Who had low participation? [LIST] → Follow-up conversation
- Who asked questions? [LIST] → Provide additional resources

CERTIFICATES:
- Printed & signed for all attendees? YES
- Attached to personnel files? YES
```

---

## TEMPLATE 5: Grading_System_Readiness.xlsx

**Purpose:** Verify all components ready before semester

```
SHEET: "Readiness Checklist"

COLUMNS:
A  | Component | [What to check]
B  | Owner | [Who is responsible]
C  | Deadline | [By when]
D  | Status | NOT STARTED / IN PROGRESS / COMPLETED / ISSUE
E  | Details | [What is done / Issue description]
F  | Follow-up | [Next action needed]
G  | Completion Date | [When actually completed]

DOSEN READINESS:
1 | Training completed | WK1 | 20-Jul | COMPLETED | All 15 dosen trained (or alternative 1-on-1) | - | 20-Jul |
2 | RPS updated with assessment detail | Each dosen | 10-Aug | IN PROGRESS | 12/15 submitted | Remind remaining 3 | - |
3 | Rubrics created & ready | Each dosen | 10-Aug | IN PROGRESS | 10/15 submitted | Provide template to remaining | - |
4 | SIAKNG access verified | Admin | 5-Aug | COMPLETED | All dosen tested login | - | 5-Aug |
5 | Grade entry practice done | Each dosen | 20-Jul | COMPLETED | Practiced during training | - | 20-Jul |

ADMIN READINESS:
6 | SIAKNG system tested | IT | 5-Aug | COMPLETED | Full system test done, no issues | - | 5-Aug |
7 | Student rosters verified | Admin | 5-Aug | COMPLETED | All rosters checked & correct | - | 5-Aug |
8 | Grade entry deadlines set | Admin | 10-Aug | IN PROGRESS | Set in calendar, email ready | Send reminder emails | - |
9 | Plagiarism system ready | IT | 10-Aug | COMPLETED | Turnitin configured, test run done | - | 10-Aug |

STUDENT COMMUNICATION:
10 | Grading system explained to students | Dosen | 10-Aug | IN PROGRESS | Email sent | Post on portal | - |
11 | Assessment schedule communicated | Dosen | 10-Aug | IN PROGRESS | In syllabi | Confirm in week 1 class | - |

SUMMARY:
- Total items: 11
- Completed: [COUNT]
- In progress: [COUNT]
- Issues: [COUNT]
- Overall readiness: [COMPLETED / TOTAL]%

GO/NO-GO DECISION:
☐ Ready to start semester: YES / NO (if NO, identify blockers)
```

---

## HOW TO USE

### Week 1 (15-19 JULI):
1. Create Rubric_Master template
2. Distribute to dosen with examples
3. Ask dosen to prepare rubrics for their MK

### Week 2 (20-26 JULI):
1. Conduct training (use rubric templates)
2. Track attendance in Dosen_Training_Attendance.xlsx
3. Verify SIAKNG access in Grade_Entry_Form
4. Create Assessment_Schedule for semester

### Week 3 (27-31 JULI):
1. Finalize Assessment_Schedule (verify no conflicts)
2. Update Grading_System_Readiness (verify all ready)
3. Conduct spot-check verifications
4. Ready for semester!

---

**Versi:** 1.0 | **Status:** Ready to Use | **Untuk:** Phase 8 Implementation

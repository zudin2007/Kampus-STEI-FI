# FASE 10: TRACKING SPREADSHEET TEMPLATES
## Data Entry & Reporting for Monitoring System

**Purpose:** Centralized Excel-based tracking for all Fase 10 monitoring data  
**Applies to:** 1 Agustus - End of Semester (16 weeks)  
**Owner:** Academic Admin  
**Frequency:** Updated weekly (Mondays) + biweekly review + end-of-semester archive

---

## MASTER SPREADSHEET OVERVIEW

**File Name:** `Monitoring_Data_2026_2027_STEI_FI.xlsx`

**Contains 5 worksheets:**
1. **WEEKLY_SUMMARY** - High-level week-by-week snapshot
2. **DOSEN_ATTENDANCE** - Detailed dosen tracking
3. **ABK_WORKLOAD** - Admin & support staff workload
4. **INCIDENTS_LOG** - All incidents, red flags, escalations
5. **METRICS_DASHBOARD** - Summary charts & trends

---

## SHEET 1: WEEKLY_SUMMARY

**Purpose:** Bird's-eye view of each week's status  
**Update frequency:** Every Monday by 9:00 AM  
**Time to update:** 15 minutes

```
COLUMN HEADERS:
A: Week Number (1-16)
B: Date Range (e.g., "1-7 Agustus")
C: Dosen Attendance %
D: Classes Covered (Yes/No)
E: Critical Issues (Y/N & brief description)
F: Red Flags Escalated (Count)
G: ABK Status (GREEN / YELLOW / RED)
H: Overall Status (✓ GOOD / ⚠ CAUTION / ❌ CRITICAL)
I: Notes

SAMPLE DATA ROW:
| Week | Date Range | Dosen % | Classes | Issues | Flags | ABK | Overall | Notes |
|------|------------|---------|---------|--------|-------|-----|---------|-------|
| 1    | 1-3 Aug    | 98%     | Yes     | No     | 0     | GREEN | ✓ GOOD | Smooth start |
| 2    | 4-10 Aug   | 95%     | Yes     | 1      | 1     | YELLOW | ⚠ CAUTION | 1 dosen sick, covered |

FORMULAS:
- Dosen % = Average of daily attendance rate
- Classes = IF(all_classes_covered, "Yes", "No")
- Overall = IF(dosen%<95%, "❌ RED", IF(flags>2, "❌ RED", IF(abk_status="RED", "❌ RED", IF(dosen%<98%, "⚠ YELLOW", "✓ GOOD"))))

CONDITIONAL FORMATTING:
- Dosen % < 90%: Red background
- Dosen % 90-95%: Yellow background
- Dosen % > 95%: Green background
- "Yes" in Classes Covered: Green
- "No" in Classes Covered: Red
- Overall "✓ GOOD": Green border
- Overall "⚠ CAUTION": Yellow border
- Overall "❌ CRITICAL": Red, bold

TREND ANALYSIS:
Add at bottom:
├─ Average attendance rate (weeks 1-16): =AVERAGE(C:C)
├─ Weeks with issues: =COUNTIF(E:E, "Y")
├─ Total escalations: =SUM(F:F)
└─ Class coverage success: =COUNTIF(D:D, "Yes")/16*100 &"%"
```

---

## SHEET 2: DOSEN_ATTENDANCE

**Purpose:** Track each dosen's attendance daily  
**Update frequency:** Every Monday (backfill previous week)  
**Time to update:** 30 minutes

```
COLUMN HEADERS:
A: Dosen Name
B: Program/Department
C: Primary Courses
D: Week 1 Status
E: Week 1 Notes
F: Week 2 Status
G: Week 2 Notes
... (repeat for all 16 weeks)
U: Overall Attendance Rate (semester)
V: Issues/Flags

LEGEND FOR STATUS:
P = Present (teaches all scheduled classes)
L-C = Leave - Approved (conference, sabbatical, etc)
L-U = Leave - Unapproved (not authorized)
S = Sick leave (medical issue)
H = Holiday/Public holiday
? = Unable to verify

SAMPLE DATA:
| Dosen | Program | Courses | Week1 | W1 Notes | Week2 | W2 Notes | ... | Attendance% | Issues |
|-------|---------|---------|-------|----------|-------|----------|-----|-------------|--------|
| Dr. A | SI      | SE, BD  | P     |          | P     |          | ... | 100%        | None   |
| Dr. B | SI      | AI      | L-C   | Conf     | P     |          | ... | 92%         | 1 leave|
| Dr. C | SI      | BD      | S     | Flu      | S     | Still ill| ... | 88%         | Monitor|

NOTES FIELD (for context):
- "Conference" (approved absence)
- "Medical" (sick leave with note)
- "Family emergency"
- "Training" (professional development)
- "No notice" (RED FLAG)
- "Returning from leave"

FORMULAS:
- Overall Attendance % = (Weeks present / 16 weeks) * 100%
- Issues flag = IF(attendance<90%, "MONITOR", IF(no_shows>1, "ESCALATE", "NONE"))

CONDITIONAL FORMATTING:
- "P" = Green
- "L-C" = Blue (leave, approved)
- "S" = Yellow (sick)
- "?" = Gray (unknown)
- If any dosen <90% attendance: Highlight row in pink

SORTING OPTIONS:
- By department
- By attendance rate (ascending)
- By issues (flagged first)
```

---

## SHEET 3: ABK_WORKLOAD

**Purpose:** Track admin & support staff workload & capacity  
**Update frequency:** Biweekly (every 2 weeks on Monday)  
**Time to update:** 20 minutes

```
COLUMN HEADERS:
A: Date (biweekly review date)
B: Staff Name
C: Role (Admin, Lab Tech, Equipment, etc.)
D: Workload Level (NORMAL / HEAVY / CRITICAL)
E: Pending Tasks (count)
F: Average Processing Time (days)
G: Overtime Needed (Y/N)
H: Burnout Risk (NONE / LOW / MEDIUM / HIGH)
I: Issues
J: Actions Taken
K: Status

SAMPLE DATA:
| Date | Name | Role | Workload | Pending | Avg Time | OT | Burnout | Issues | Actions | Status |
|------|------|------|----------|---------|----------|----|---------+--------|---------|--------|
| 4Aug | Ani  | Admin| NORMAL   | 5       | 2 days   | N  | NONE    | None   | Monitor | ✓ OK   |
| 4Aug | Budi | Lab  | HEAVY    | 12      | 3 days   | Y  | MEDIUM  | 1 staff short | Hire temp | ⚠ WATCH |
| 4Aug | Citra| Tech | NORMAL   | 3       | 1 day    | N  | NONE    | None   | Continue | ✓ OK   |

WORKLOAD SCALE:
- NORMAL: Typical workload, tasks completed on time
- HEAVY: Increased workload, minor delays, manageable
- CRITICAL: Overloaded, significant delays, at risk of errors

BURNOUT RISK SCALE:
- NONE: Staff fine, good morale
- LOW: Minor stress, manageable
- MEDIUM: Visible stress, starting to complain, morale affected
- HIGH: Serious burnout risk, needs intervention

FORMULAS:
- Burnout Risk = IF(workload="CRITICAL", "HIGH", IF(workload="HEAVY", "MEDIUM", "NONE"))
- Status = IF(burnout="HIGH", "🔴 CRITICAL", IF(burnout="MEDIUM", "⚠ YELLOW", "✓ GREEN"))

ACTIONS COLUMN:
Possible entries:
- "Monitor" (check next review)
- "Hire temporary" (if short-staffed)
- "Redistribute work"
- "Extend deadline"
- "Process improvement"
- "Staff meeting to discuss"

TREND ANALYSIS:
Add summary rows at bottom:
├─ Average workload this period: NORMAL/HEAVY/CRITICAL
├─ Staff needing support: ___ people
├─ Burnout risk: ___ MEDIUM, ___ HIGH
├─ Hiring needed: Y/N [How many]
└─ Process improvements to implement: [LIST]
```

---

## SHEET 4: INCIDENTS_LOG

**Purpose:** Document all incidents, issues, escalations  
**Update frequency:** As issues occur (real-time)  
**Time to update:** 10 minutes per incident

```
COLUMN HEADERS:
A: Incident ID (e.g., INC-001)
B: Date/Time Occurred
C: Issue Category (RED FLAG 1-10 or OTHER)
D: Description (brief)
E: Severity (EMERGENCY / URGENT / HIGH / MEDIUM / LOW)
F: Who Reported
G: Escalated To (Kaprodi/WK1/Dekan/None)
H: Time Escalated
I: Actions Taken (by whom, when)
J: Resolution (brief description)
K: Status (OPEN / CLOSED)
L: Follow-up Needed (Y/N)

SAMPLE DATA:
| ID | Date/Time | Category | Description | Severity | Reported By | Escalated To | Time | Actions | Resolution | Status | FU |
|----|-----------|----------|-------------|----------|------------|--------------|------|---------|------------|--------|-----|
|INC-001|1Aug 14:00|FLAG 1|Dr.X no-show|URGENT|Academic Admin|Kaprodi|14:30|Substitute assigned, students notified|Covered by Dr.Y|CLOSED|N|
|INC-002|3Aug 10:00|FLAG 6|Dr.Z sick|HIGH|Kaprodi|None|N/A|Monitor, covered by backup|3 weeks, then back|CLOSED|Y-check morale|
|INC-003|6Aug 09:00|FLAG 8|Backlog in registrations|URGENT|Admin|Kaprodi|09:30|Hired temp staff, extended deadline|50% processed|OPEN|Y-check resolution|

ISSUE CATEGORIES:
- RED FLAG 1: Dosen multiple no-shows
- RED FLAG 2: Lab closure
- RED FLAG 3: SIAKNG down
- RED FLAG 4: Staff resignation
- RED FLAG 5: Safety incident
- RED FLAG 6: Frequent sick days
- RED FLAG 7: Teaching quality complaints
- RED FLAG 8: Processing backlog
- RED FLAG 9: Equipment broken
- RED FLAG 10: Staff leave requests
- OTHER: [Description]

SEVERITY SCALE:
- EMERGENCY: Immediate action required, safety/critical operations at risk
- URGENT: Action needed within hours/same day
- HIGH: Action needed within 1 week
- MEDIUM: Action needed within 2 weeks
- LOW: Routine issue, plan for next month

STATUS:
- OPEN: Issue ongoing, not yet fully resolved
- CLOSED: Issue resolved, no further action needed

FORMULAS:
- Time to escalation = (Time escalated - Time occurred)
- Resolution time = (Status change to CLOSED - Date occurred)
- Escalation rate = COUNTIF(E:E, "<>None") / Total incidents

TRENDS:
Add summary at bottom:
├─ Total incidents: ___
├─ Critical incidents: ___
├─ Escalated incidents: ___
├─ Average resolution time: ___ days
├─ Most common issue: ___________
└─ Patterns identified: [IF ANY]
```

---

## SHEET 5: METRICS_DASHBOARD

**Purpose:** Summary charts and KPI tracking  
**Update frequency:** Weekly (Monday)  
**Time to update:** Automatic (pulls from other sheets via formulas)

```
SECTION 1: KEY PERFORMANCE INDICATORS (KPIs)

Dosen Attendance Rate: ___%
  Target: 95%+
  Status: ✓ MET / ⚠ BELOW
  Trend: ↑ Improving / = Stable / ↓ Declining
  Week-by-week: [LINE CHART]

Class Coverage Rate: ___%
  Target: 100%
  Status: ✓ MET / ⚠ BELOW
  Classes at risk: ___
  Uncovered classes: [IF ANY]

Red Flags/Week: ___
  Average: ___ per week
  Target: <1 per week
  Status: ✓ MET / ⚠ ABOVE
  Trend: [BAR CHART by week]

ABK Workload: [STACKED BAR CHART]
  NORMAL: ___ staff
  HEAVY: ___ staff
  CRITICAL: ___ staff
  Burnout risk: ___ staff at MEDIUM/HIGH risk

Issue Resolution Time: ___ days
  Average: ___ days (from escalation to close)
  Target: <5 days
  Status: ✓ MET / ⚠ SLOW

SECTION 2: ATTENDANCE TREND CHART

[LINE CHART]
X-axis: Weeks 1-16
Y-axis: Attendance % (80-100%)
Lines:
├─ Overall attendance rate (blue)
├─ Target line at 95% (red dashed)
└─ Minimum acceptable at 90% (orange dashed)

Interpretation:
- Above red line = Excellent
- Between red & orange = Acceptable
- Below orange = Needs action

SECTION 3: RED FLAGS SUMMARY

By severity:
├─ EMERGENCY: ___ incidents
├─ URGENT: ___ incidents
├─ HIGH: ___ incidents
└─ MEDIUM+LOW: ___ incidents

By category:
├─ Dosen issues: ___ incidents
├─ Staff issues: ___ incidents
├─ System/Equipment: ___ incidents
└─ Other: ___ incidents

Escalation rate: __% (of all incidents escalated)

SECTION 4: SEMESTER PROGRESS

Weeks completed: ___ / 16
Semester status:
├─ Early (weeks 1-4): [Summary if in this phase]
├─ Mid-semester (weeks 5-10): [Key findings if in this phase]
└─ Late (weeks 11-16): [Key findings if in this phase]

Overall assessment: ✓ ON TRACK / ⚠ CAUTION / ❌ PROBLEMS

SECTION 5: ACTION ITEMS SUMMARY

Open issues requiring follow-up: ___ items
By owner:
├─ Academic Admin: ___ items
├─ Kaprodi: ___ items
├─ WK1: ___ items
└─ Other: ___ items

Items due this week: [LIST]
Items overdue: [LIST] ⚠️

SECTION 6: NOTES & OBSERVATIONS

Semester trends (from coordinator observation):
- What's working well: ___________________
- What's concerning: ___________________
- Recommendations for improvement: ___________

Coordinator's overall assessment:
"Overall, semester is [ON TRACK / SLIGHTLY CONCERNING / PROBLEMATIC]
because [REASONS]."

FORMULAS (auto-calculated):
All metrics pull from other sheets via formulas, so they update automatically
when underlying data changes. Example:
=AVERAGE(WEEKLY_SUMMARY!C:C) [for overall attendance %]
=COUNTIF(INCIDENTS_LOG!E:E, "EMERGENCY") [for critical incidents]
```

---

## DATA ENTRY WORKFLOW

**Every Monday at 9:00 AM:**

```
STEP 1: Update DOSEN_ATTENDANCE sheet (15 min)
        ├─ Add columns for this week
        ├─ Enter status for each dosen (P/L/S/?)
        └─ Add notes (if any absences)
        
STEP 2: Update WEEKLY_SUMMARY sheet (10 min)
        ├─ Calculate dosen attendance % this week
        ├─ Verify all classes covered (Y/N)
        ├─ Note any critical issues
        ├─ Count red flags escalated
        └─ Assess ABK status
        
STEP 3: Review INCIDENTS_LOG (5 min)
        ├─ Check for any open incidents from last week
        ├─ Update status if resolved
        ├─ Close resolved incidents
        └─ Note any new incidents discovered
        
STEP 4: METRICS_DASHBOARD auto-updates (automatic)
        ├─ Charts refresh automatically
        ├─ KPIs calculate automatically
        └─ Review for trends

STEP 5: Generate weekly email report (10 min)
        ├─ Use data from sheets to write Kaprodi email
        ├─ Export summary as PDF or screenshot
        ├─ Send by 9:00 AM Monday
        
TOTAL TIME: 40 minutes per week
```

---

## BIWEEKLY DEEPER ANALYSIS (Every 2 weeks on Monday)

```
ADDITIONAL TASK: Update ABK_WORKLOAD sheet

STEP 1: Survey ABK staff (15 min)
        ├─ Ask each person: Workload level (NORMAL/HEAVY/CRITICAL)
        ├─ Ask: How many pending tasks?
        ├─ Ask: Processing time (how fast are you working)
        ├─ Ask: Do you need overtime?
        └─ Ask: How's your stress level?
        
STEP 2: Enter data into ABK_WORKLOAD sheet (10 min)
        ├─ Fill in workload level
        ├─ Enter pending task count
        ├─ Calculate average processing time
        └─ Note any issues/concerns
        
STEP 3: Analyze trends (10 min)
        ├─ Compare to previous biweekly (is workload increasing?)
        ├─ Identify who's overloaded
        ├─ Identify who has capacity to help
        └─ Recommend actions (hiring, redistribution, etc.)
        
STEP 4: Plan interventions (5 min)
        ├─ For each staff member at HEAVY/CRITICAL:
        │  └─ Decide: Hire temporary? Redistribute? Extend deadline?
        └─ Assign responsible person to implement
        
TOTAL TIME: 40 minutes every 2 weeks

WHEN: Mondays of weeks 2, 4, 6, 8, 10, 12, 14, 16
```

---

## MID-SEMESTER REVIEW (Week 8 - Detailed Analysis)

```
ADDITIONAL TASK: Comprehensive analysis and reporting

STEP 1: Compile all data from weeks 1-8 (30 min)
        ├─ Average attendance rate (weeks 1-8)
        ├─ Classes covered consistently? 100%?
        ├─ Total incidents: ___ (by type)
        ├─ Escalations: ___ (all resolved?)
        ├─ ABK workload trend: improving? getting worse?
        └─ Any major patterns?

STEP 2: Create mid-semester report (45 min)
        ├─ Executive summary (1 page)
        ├─ Detailed findings (attendance, incidents, ABK)
        ├─ Trends & patterns (what's changing?)
        ├─ Recommendations for 2nd half
        └─ Any early wins to celebrate
        
STEP 3: Present to leadership (30 min)
        ├─ Brief Kaprodi + WK1
        ├─ Share findings
        ├─ Discuss recommendations
        ├─ Get approval for any major changes
        └─ Answer questions

STEP 4: Plan adjustments for weeks 9-16 (20 min)
        ├─ If attendance is low: What interventions?
        ├─ If incidents high: What's the root cause? Fix it?
        ├─ If ABK overloaded: Hire? Redistribute?
        ├─ If systems failing: What upgrades needed?
        └─ Implement starting week 9

TOTAL TIME: 2 hours (concentrated in week 8)

DELIVERABLE: Mid-semester report (use template from File 44, Section 7)
```

---

## END-OF-SEMESTER ARCHIVE (Week 16 - Final Summary)

```
FINAL TASK: Complete semester analysis and archive

STEP 1: Complete final data entry (20 min)
        ├─ Enter week 16 attendance data
        ├─ Close all open incidents
        ├─ Final ABK workload assessment
        └─ Note any end-of-semester issues

STEP 2: Calculate final metrics (15 min)
        ├─ Overall attendance rate (16 weeks): ___%
        ├─ Class coverage success rate: ___%
        ├─ Total incidents: ___ (by severity)
        ├─ Critical incidents resolved: ___%
        ├─ ABK staff retention: ___%
        └─ Overall semester assessment: ✓ SUCCESSFUL / ⚠ WITH ISSUES / ❌ PROBLEMATIC

STEP 3: Generate end-of-semester report (1 hour)
        ├─ Full semester analysis
        ├─ What went well
        ├─ What needs improvement
        ├─ Lessons learned
        ├─ Recommendations for next year
        └─ Historical data for comparison

STEP 4: Archive all data (20 min)
        ├─ Save final spreadsheet: Monitoring_Data_2026_2027_FINAL.xlsx
        ├─ Save reports as PDFs
        ├─ Backup to secure location
        ├─ Share final report with Dekan + Kaprodi + WK1
        └─ File in institutional records

STEP 5: Team debrief & lessons (30 min)
        ├─ Meet with monitoring team
        ├─ Discuss: What we learned this semester
        ├─ Discuss: What to do differently next year
        ├─ Thank team for their work
        └─ Plan improvements for next semester

TOTAL TIME: 2.5 hours (concentrated in week 16)

DELIVERABLE: End-of-semester report (use template from File 44, Section 7)
ARCHIVE: All data, reports, incident logs filed for future reference
```

---

## BACKUP & SECURITY

```
BACKUP SCHEDULE:

Weekly backup: Every Friday 5:00 PM
├─ Create copy: Monitoring_Data_2026_2027_BACKUP_[DATE].xlsx
├─ Save to: Cloud storage (Google Drive, OneDrive, etc.)
└─ Keep: At least 4 recent backups (rolling)

Biweekly manual check:
├─ Verify all data is current
├─ Verify no duplicates or inconsistencies
├─ Verify formulas calculating correctly
└─ Check for any corruption

End-of-semester archive:
├─ Save final version: Monitoring_Data_2026_2027_FINAL.xlsx
├─ Save to: Institutional archive + personal backup
├─ Format: Excel + PDF (for long-term readability)
└─ Share access: Kaprodi, WK1, Dekan (read-only)

FILE LOCATIONS:

Working copy: [Shared drive]/Academic_Monitoring/2026_2027/
Backups: [Shared drive]/Academic_Monitoring/2026_2027/Backups/
Archive: [Institutional records]/2026_2027_Reports/
Emergency backup: [Personal cloud storage]

ACCESS CONTROL:

Who can edit: Academic Admin (primary), Kaprodi (secondary)
Who can view: Kaprodi, WK1, relevant department heads
Who cannot access: Students, external parties
Password protection: [IF SENSITIVE DATA] - Share password via secure channel
```

---

## TROUBLESHOOTING COMMON ISSUES

```
PROBLEM: Attendance numbers don't match system records

SOLUTION:
1. Check SIAKNG logs (official attendance source)
2. Reconcile: Did dosen mark attendance in system?
3. If discrepancy: Contact dosen to verify
4. Update spreadsheet with official records
5. Note: "Cross-checked with SIAKNG [DATE]"

PROBLEM: Staff member data is inaccurate

SOLUTION:
1. Verify directly with staff member
2. Ask: "Is this how many tasks you have?"
3. Update if needed
4. Note discrepancy in incident log if significant

PROBLEM: Formula not calculating correctly

SOLUTION:
1. Check: Is formula referencing correct cells?
2. Check: Is data format correct (numbers not text)?
3. Fix formula: =SUM() not =SUM(text cells)
4. Test: Enter sample data to verify formula works

PROBLEM: Too much data, spreadsheet is slow

SOLUTION:
1. Archive old data (move weeks 1-8 to separate file)
2. Delete unnecessary columns
3. Reduce chart complexity
4. Save as XLSX not XLS

PROBLEM: Can't remember which sheet to update

SOLUTION:
1. Print checklist: "Monday tasks" and post it
2. Set calendar reminders
3. Create checklist in system (checkbox list)
4. Have backup person know workflow too
```

---

## SAMPLE DATA FOR TESTING

```
WEEK 1 - SAMPLE DATA:

Dosen Attendance:
- Dr. A: P (present)
- Dr. B: P (present)
- Dr. C: L-C (conference)
Overall: 2/3 = 67% (but this is partial week, not full picture)

Class Coverage:
- All 9 classes covered this week ✓

Incidents:
- None

ABK Status:
- Normal workload
- 2 pending registration forms
- Expected completion: by Wednesday

WEEK 2 - SAMPLE DATA:

Dosen Attendance:
- Dr. A: P (present)
- Dr. B: P (present)
- Dr. C: P (back from conference)
- Dr. D: S (sick - flu)
Overall: 3/4 = 75% (partial week) → But with full view = 93% overall

Class Coverage:
- Dr. D's classes covered by Dr. A (substitute assigned)
- 10 classes all covered this week ✓

Incidents:
- INC-001: Dr. D sick, covered by Dr. A
  Status: CLOSED
  Action: Monitored, Dr. D returned after 3 days

ABK Status:
- 2 staff normal workload
- 3 pending items
- Processing time: 2 days (on target)
- No issues

[Continue for weeks 3-16...]
```

---

## QUICK REFERENCE GUIDE

```
WHAT TO TRACK & WHEN:

DAILY (automatic from dosen):
→ Who taught which classes
→ Any cancellations or delays

WEEKLY (Monday 9 AM):
→ Overall attendance % for the week
→ Classes covered: Y/N
→ Any critical issues this week
→ Red flags escalated
→ ABK workload check-in

BIWEEKLY (Mondays of even weeks):
→ Detailed ABK workload assessment
→ Trend analysis (is anything getting worse?)
→ Midcourse corrections needed?

MID-SEMESTER (Week 8):
→ Comprehensive review
→ Attendance trends
→ Incident patterns
→ Recommendations for 2nd half

END-OF-SEMESTER (Week 16):
→ Final metrics
→ Overall assessment
→ Lessons learned
→ Archive all data
→ Prepare next year's plan

TOOLS:
→ Spreadsheet (Excel): Daily tracking
→ Email: Weekly reporting
→ Dashboard: Visual trends
→ Incident log: Documentation
→ Reports: Summary & analysis
```

---

**Versi:** 1.0 | **Untuk:** Fase 10 - Data Tracking & Reporting  
**Last Updated:** Juli 2026  
**Owner:** Academic Admin

---

## GETTING STARTED

**Week 1 checklist:**

1. ✓ Save template file: `Monitoring_Data_2026_2027.xlsx`
2. ✓ Create 5 worksheets (using templates above)
3. ✓ Setup formulas & conditional formatting
4. ✓ Test with sample data (use examples above)
5. ✓ Share with Kaprodi (view access only)
6. ✓ Create weekly reminder (every Monday 8:30 AM)
7. ✓ Backup location confirmed
8. ✓ Team trained on data entry

**Success metric:** By Week 2, you should have clean, accurate data for all monitoring indicators. If anything looks off, troubleshoot it early!

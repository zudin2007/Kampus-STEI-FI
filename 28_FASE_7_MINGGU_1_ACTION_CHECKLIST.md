# FASE 7 - MINGGU 1 ACTION CHECKLIST
## JUNI 20-26, 2026 - IDENTIFIKASI & TOPIC REVIEW

**Owner:** Kaprodi  
**Status:** READY TO EXECUTE  
**Dokumentasi:** 21_FASE_7_SKRIPSI_TUGAS_AKHIR.md + 26_FASE_7_EMAIL_TEMPLATES.md + 27_FASE_7_EXCEL_TEMPLATES.md

---

## ⚡ DAY 1 (TODAY - 20 JUNI) - MORNING

### Task 1: Prepare & Send Topic Submission Email
**Time:** 2 hours  
**Owner:** Kaprodi + Admin

```
PREPARATION:
☐ Open: 26_FASE_7_EMAIL_TEMPLATES.md
☐ Copy EMAIL 1: "Topic Submission Announcement"
☐ Customize:
   - Replace [INSERT DATE] dengan: 24 JUNI 2026 jam 12:00
   - Replace [KAPRODI_EMAIL] dengan: actual email Anda
   - Check area list (SI, Keamanan, Cloud, AI, Networking) → sesuai program Anda
   - Review content: semantically correct Bahasa Indonesia?
   
SEND:
☐ Email list: [obtain dari Admin → semua mahasiswa S7+]
☐ Send via: Gmail / Outlook / institutional email
☐ Subject line: COPY EXACTLY dari template
☐ Body: Paste dari template (after customization)
☐ Attachment: "TA_Guidelines.pdf" (jika ada)
☐ CC: Admin akademik (untuk record)
☐ BCC: Yourself

VERIFICATION:
☐ Email sent successfully? Check sent folder
☐ At least 1 test send ke Anda terlebih dahulu? YES
☐ Record: Email sent time & recipient count
   
TIME LOG: Start __:__ End __:__ Total: __ mins
```

---

## ⚡ DAY 1 (TODAY - 20 JUNI) - AFTERNOON

### Task 2: Create Excel Tracking Sheet
**Time:** 1.5 hours  
**Owner:** Admin

```
SETUP:
☐ Open Excel → New Workbook
☐ Save as: "TA_Topics_Submitted_2026.xlsx"
☐ Location: [KAMPUS_STEI_FI Folder]/TA_2026_2027/01_SUBMISSIONS/

SHEET SETUP:
☐ Use template from 27_FASE_7_EXCEL_TEMPLATES.md
☐ Copy columns: NIU | Nama | Program | Topik | Area | Deskripsi | Alasan | Status | Tanggal | Catatan
☐ Format header: Bold, blue background, white text
☐ Column widths: Auto-fit

DATA ENTRY:
☐ Enter all eligible students (S7+, GPA ≥ 2.0):
   ├─ Source: SIAKNG or student database
   ├─ Total count: ___ students
   └─ Format: Copy-paste from source (then clean up)

AUTO FORMULAS:
☐ Column I (Tanggal Terima): =TODAY() [for submitted entries]
☐ Status: Default = "Pending"
☐ Add summary row:
   ├─ Total Invited: =COUNTA(A:A)
   ├─ Submitted: =COUNTIF(H:H, "Submitted")
   ├─ Pending: =COUNTIF(H:H, "Pending")
   └─ On-time rate: =[Submitted before deadline]/[Total Invited]%

FORMATTING:
☐ Freeze header row (View → Freeze Panes)
☐ Add data validation to Status column (dropdown: Pending, Submitted, Incomplete)
☐ Add conditional formatting:
   - Status="Submitted" → Green background
   - Status="Incomplete" → Yellow background
   - Status="Pending" → Gray background

SAVE & BACKUP:
☐ Save file (Ctrl+S)
☐ Create backup copy: "TA_Topics_Submitted_2026_BACKUP_[DATE].xlsx"
☐ Share link with Kaprodi for view access

TIME LOG: Start __:__ End __:__ Total: __ mins
```

---

## ⚡ DAY 2 (21 JUNI) - MORNING

### Task 3: Confirm Email Sent & Monitor Submissions
**Time:** 30 minutes  
**Owner:** Admin

```
MORNING CHECK:
☐ Email confirmed sent to all students? YES
☐ Any bounce-back emails? Check inbox
   → If yes: Get correct emails & resend ASAP
☐ Any student questions received? 
   → Forward to Kaprodi with answer template
   
TRACK SUBMISSIONS:
☐ Create email filter in Gmail: [From student subject contains "TOPIK TA"]
   → Auto-label as "TA_SUBMISSIONS" for easy tracking
   
☐ Open Excel sheet: TA_Topics_Submitted_2026.xlsx
☐ Start monitoring: Mark each submission as "Submitted" + date received
☐ Screenshot count every 4 hours → send update to Kaprodi

DAILY EMAIL TO KAPRODI (end of day):
"
SUBMISSION UPDATE - Hari 1 (21 Juni 2026)

Total invited: 45 students
Submitted so far: 12 students (27%)
Pending: 33 students

Expected flow:
- Day 1-2: 30%
- Day 2-3: 60%
- Day 3-4: 85%
- By deadline: 95%+ (late submissions are OK if very close to deadline)

Any issues: None yet

Next: Monitor submissions & prepare for review meeting
"

TIME LOG: Start __:__ End __:__ Total: __ mins
```

---

## ⚡ DAY 3-5 (22-24 JUNI) - DAILY MONITORING

### Task 4: Track Submissions Daily
**Time:** 15 minutes per day  
**Owner:** Admin

```
DAILY ROUTINE (Each morning):
☐ Check Excel sheet: Count new submissions since yesterday
☐ Update "Status" column: Mark as "Submitted" if received
☐ Update "Tanggal Terima" column: Add date
☐ Note any issues in "Catatan" column
   Examples:
   - Topic format incorrect → "Need to reformat"
   - Missing area selection → "Ask for clarification"
   - Plagiarism detected (title copied) → "Discuss with student"
   
☐ Check daily submission rate:
   - Is it on pace for 95% by deadline?
   - Too slow? Send reminder email TODAY
   
REMINDER EMAIL (If submission < 80% by Day 3):
"
Subject: REMINDER - Topic TA Submission Deadline [24 JUNI JAM 12:00]

Yth Mahasiswa,

Ini adalah reminder untuk yang belum submit topik TA Anda.

DEADLINE: 24 JUNI 2026 JAM 12:00 (Hari Kamis, sebelum jam lunch)

Submit sekarang jika sudah siap. Jangan tunda-tunda!

Email: [KAPRODI_EMAIL]

Terima kasih,
Kaprodi
"

☐ Send reminder? [IF submission rate < target]
☐ Document: Time sent, recipient count

TIME LOG (total for day): ___ mins
```

---

## ⚡ DAY 6 (25 JUNI) - TOPIC REVIEW MEETING PREP

### Task 5: Prepare for Review Meeting
**Time:** 3-4 hours  
**Owner:** Kaprodi + Admin + Dosen Senior

```
MORNING: COMPILE SUBMISSIONS
☐ Close Excel: TA_Topics_Submitted_2026.xlsx
☐ Status: All submissions received (deadline passed)
☐ Total submitted: ___ students
☐ Any incomplete? Mark & plan follow-up
☐ Create summary:
   | Metric | Count |
   | Total Invited | ___ |
   | Submitted | ___ |
   | Submission Rate | ___% |
   | By Area: SI | ___ |
   | By Area: Keamanan | ___ |
   | By Area: Cloud | ___ |
   | Etc | ... |

COMPILE DOCUMENT FOR REVIEW MEETING:
☐ Create file: "TA_Topics_ForReview_[DATE].docx"
☐ Content:
   1. Summary statistics (above)
   2. List all topics submitted (100% of list):
      | # | Nama | Topik | Area | Feasible? | Unique? | Data Access? | Notes |
      
      [Copy from Excel, evaluate each by reviewers later in meeting]
      
   3. Any obvious issues to flag:
      - Duplicate topics (same as last year?)
      - Overly broad topics?
      - No data access?
      - Not aligned with program?
      
   4. Recommendation: Which topics to discuss/reject in meeting

SEND TO REVIEW TEAM:
☐ Recipients: Kaprodi + Senior Dosen 1 + Senior Dosen 2
☐ Time: Send TODAY afternoon (give them time to review)
☐ Message: "Attached adalah daftar 45 topik untuk direview besok. Please scan & prepare feedback"
☐ Meeting details: When/where/duration

ORGANIZE REVIEW MEETING:
☐ Schedule: [SET DATE - suggest 23-24 JUNI, 2 hours, morning]
☐ Location: Kaprodi's office or meeting room
☐ Attendees: Kaprodi + 2-3 senior dosen
☐ Materials:
   ☐ Print: TA_Topics_ForReview document (1 copy per person)
   ☐ Print: Feedback form (template below)
   ☐ Whiteboard/flipchart for tallying decisions
   
FEEDBACK FORM TEMPLATE:
"
TA TOPIC REVIEW FORM

Reviewer: [NAME]
Date: [DATE]
Topic #: [X]

Student Name: ____________
Topic Title: ____________
Area: ____________

EVALUATION:
☐ Feasible for 1 semester? YES / NEEDS CLARIFICATION / NO
☐ Unique (not duplicate)? YES / MAYBE / NO
☐ Has data access? YES / UNCLEAR / NO
☐ Aligned with program? YES / SOMEWHAT / NO
☐ Overall recommendation?
   ☐ APPROVED
   ☐ NEEDS MINOR REVISION
   ☐ NEEDS MAJOR REVISION
   ☐ REJECT (too broad / unclear / etc)

Comments: _______________
"

☐ Print feedback forms (X copies = reviewers)

PREPARE DECISION SHEET:
☐ Create Excel: "TA_Topics_Decision_2026.xlsx" [template from 27]
☐ Pre-fill: Student names, topics, area
☐ Leave decision columns empty (to fill during meeting)
☐ Will print & manually mark during meeting, then enter into Excel

TIME LOG: Start __:__ End __:__ Total: __ mins
```

---

## ⚡ DAY 6-7 (24-25 JUNI) - TOPIC REVIEW MEETING

### Task 6: Conduct Review Meeting
**Time:** 2-3 hours  
**Owner:** Kaprodi (chair) + Senior Dosen

```
MEETING SETUP:
☐ Time: [23-24 JUNI, MORNING, 2-3 hours]
☐ Location: [KAPRODI OFFICE / MEETING ROOM]
☐ Attendees present: Check everyone on-time (0 latecomers)
☐ Materials: Print copies, whiteboard, markers

MEETING STRUCTURE:
1. Opening (5 min):
   ☐ Kaprodi: "Welcome, agenda, timeline"
   ☐ Explain evaluation criteria (feasibility, uniqueness, data access, alignment)
   
2. Review Topics (120 min):
   ☐ Go through each topic (fast pace: ~3 min per topic)
   ☐ Reviewer 1: "Feasible?" 
   ☐ Reviewer 2: "Unique?"
   ☐ Reviewer 3: "Data & resources?"
   ☐ Kaprodi: Quick vote → APPROVED / REVISION / REJECT
   ☐ Record decision on paper form
   ☐ [Skip lengthy discussion - be efficient]
   
3. Closing (10 min):
   ☐ Tally results: How many approved? Revision? Reject?
   ☐ Next steps: Communicate to students (25 Juni)
   ☐ Thank reviewers

DURING MEETING:
☐ Kaprodi or scribe: Track decisions on "TA_Topics_Decision_2026.xlsx"
   - For each topic, mark: APPROVED / REVISION NEEDED / REJECTED
   - Tally at end
   
☐ For REVISION NEEDED topics: Quick note what needs to change
   Examples: "Scope too broad", "Clarify data access", "Combine with [Topic X]"
   
☐ For REJECTED topics: Note reason
   Examples: "Duplicate", "Not feasible", "Out of scope"

DECISIONS SUMMARY (end of meeting):
| Decision | Count | % |
| APPROVED | ___ | ___% |
| REVISION NEEDED | ___ | ___% |
| REJECTED | ___ | ___% |
| TOTAL | ___ | 100% |

TIME LOG: Start __:__ End __:__ Total: __ mins
```

---

## ⚡ DAY 8 (25 JUNI) - COMMUNICATE DECISIONS

### Task 7: Send Feedback to Students
**Time:** 2 hours  
**Owner:** Admin + Kaprodi

```
PREPARE:
☐ Finalize Excel: TA_Topics_Decision_2026.xlsx
☐ Sort by decision type (APPROVED, REVISION, REJECTED)
☐ Create email lists:
   ├─ List 1: Students with APPROVED topics
   ├─ List 2: Students with REVISION NEEDED
   └─ List 3: Students with REJECTED
   
☐ Prepare draft emails (use templates from 26_FASE_7_EMAIL_TEMPLATES.md):
   ├─ EMAIL 2: For APPROVED students
   ├─ EMAIL 3: For REVISION NEEDED students
   └─ [Custom email for REJECTED if needed]

SEND EMAILS:
☐ Email 2 - APPROVED students:
   ☐ Copy from template 26
   ☐ Customize: Recipient name, topic title, feedback (generic positive)
   ☐ Send individually (mail merge) or in batch
   ☐ CC: Kaprodi
   ☐ Record: Sent to ___ students, time ___

☐ Email 3 - REVISION NEEDED students:
   ☐ Copy from template 26
   ☐ Customize: Recipient name, topic title, specific feedback
   ☐ Revision deadline: 1 JULI 2026 JAM 12:00 [extend 6 days for revision]
   ☐ Send individually
   ☐ Record: Sent to ___ students

☐ Custom email - REJECTED students (if any):
   Subject: Topic Tidak Bisa Disetujui - Silakan Submit Ulang
   
   "
   Yth. [NAMA],
   
   Sayangnya, topik TA Anda tidak bisa disetujui dengan alasan:
   
   [REASON]: [SPECIFIC DETAIL]
   
   Ini bukan final. Anda bisa submit topik baru dengan deadline:
   [DATE]
   
   Konsultasikan dengan dosen untuk topik alternatif.
   
   Terima kasih,
   Kaprodi
   "
   ☐ Send to affected students
   ☐ Record: Sent to ___ students

DOCUMENTATION:
☐ Create summary file: "TA_Decision_Communication_Summary_[DATE].txt"
   Content:
   - APPROVED: X students notified
   - REVISION NEEDED: X students notified with deadline [DATE]
   - REJECTED: X students notified with next submission date [DATE]
   - All emails sent successfully? YES
   - Any bounces? [LIST]

TIME LOG: Start __:__ End __:__ Total: __ mins
```

---

## 📊 WEEK 1 SUMMARY & METRICS

### Success Criteria:

```
✅ Topic submissions collected: Target 95%+ of eligible students
✅ Review meeting conducted: All senior dosen participated
✅ Decisions made: 100% of submitted topics evaluated
✅ Communication sent: 100% of students notified of status
✅ Excel tracking active: Ready for Week 2

ACTUAL NUMBERS (Fill in):
- Total eligible students: ___
- Submitted: ___ (___%)
- Approved: ___ (___%)
- Revision needed: ___ (___%)
- Rejected: ___ (___%)
- Pending resubmission: ___

TIMELINE STATUS:
☐ Day 1 (20 Jun): Email sent ✓
☐ Days 2-4 (21-24 Jun): Submissions tracked ✓
☐ Day 5-6 (23-24 Jun): Review meeting conducted ✓
☐ Day 7 (25 Jun): Decisions communicated ✓

ISSUES ENCOUNTERED:
[List any problems & how resolved]

READY FOR WEEK 2? YES / NO
If NO, what needs to be fixed?
```

---

## 🚀 NEXT: WEEK 2 (27 JUNI - 5 JULI)

When ready, proceed to:
**28_FASE_7_MINGGU_2_ACTION_CHECKLIST.md** [To be created]

Week 2 focuses on:
- Process revision submissions (if any)
- Finalize topic approvals
- Create pembimbing assignments
- Confirm with dosen supervisors

---

**Versi:** 1.0 | **Status:** Ready to Execute | **Estimated Time:** 12 hours across 7 days | **Owner:** Kaprodi + Admin

# SOP KOORDINASI JADWAL PERKULIAHAN
## Tahun Akademik 2026/2027

**Versi:** 1.0  
**Efektif:** 8 Juli 2026  
**PIC:** Koordinator Jadwal + Admin Akademik  
**Supervisor:** Wakil Ketua I

---

## QUICK REFERENCE - 7 STEPS

| Step | Kegiatan | Timeline | Owner | Output |
|------|----------|----------|-------|--------|
| 1 | Dapatkan draft jadwal | 8 Juli | Akademik | Draft jadwal |
| 2 | Mapping ruang & cek conflict | 9-11 Juli | Koordinator | Issue log |
| 3 | Koreksi & optimasi | 15-19 Juli | Koordinator | Jadwal revised |
| 4 | Konsultasi stakeholder | 20-21 Juli | Kaprodi | Feedback |
| 5 | Finalisasi & approval | 22-26 Juli | WK1 | Jadwal final |
| 6 | Persiapan distribution | 27-28 Juli | Admin | Format siap |
| 7 | Sosialisasi & publikasi | 29-31 Juli | Admin | Jadwal tersebar |

---

## DETAIL PROSEDUR

### STEP 1: DAPATKAN DRAFT JADWAL (8 JULI)

**Aktivitas:**
1. Hubungi Kaprodi/Admin Akademik untuk draft jadwal
2. Request format Excel dengan kolom: Kode MK, Nama MK, SKS, Semester, Dosen, Hari, Jam Mulai, Jam Selesai, Ruang, Peserta
3. Verifikasi format & kelengkapan data
4. Backup file di multiple location

**Checklist:**
- [ ] Draft jadwal diterima
- [ ] Format jelas & lengkap
- [ ] Semua MK sudah ada
- [ ] Data dosen & ruang sudah tercantum

**Output:** File Excel draft jadwal TA 2026/2027

---

### STEP 2: MAPPING RUANG & CEK CONFLICT (9-11 JULI)

**Aktivitas A: Buat Daftar Ruang**
```
Format:
Nama Ruang | Gedung | Kapasitas | AC | Proyektor | Fasilitas Lain | Status
[RUANG 1]  | [GED]  | [X org]   | ☐  | ☐         | [LIST]        | Baik/Rusak
```

**Aktivitas B: Check Jadwal Conflict**
```
Gunakan form: 07_FORM_VERIFIKASI_JADWAL_RUANG.md

Cek:
1. Dosen yang sama mengajar 2+ kelas same time?
2. Ruang yang sama pakai 2+ kelas same time?
3. Mahasiswa overlap jadwal wajib?
4. Beban dosen balanced (12-16 jam/minggu)?
```

**Aktivitas C: Dokumentasikan Issue**
```
Gunakan file: Issue_Log.xlsx

Format:
No | Issue Type | Detail | Impact | Severity | Resolution
1  | Dosen-Conflict | [DOSEN] mengajar MK1 & MK2 jam sama | 2 kelas | Critical | Geser jam
2  | Ruang-Conflict | Ruang A pakai MK1 & MK2 jam sama | 2 kelas | Critical | Geser ruang
```

**Checklist:**
- [ ] Daftar ruang lengkap & akurat
- [ ] Semua conflict teridentifikasi
- [ ] Issue log terstruktur & jelas
- [ ] Prioritas resolution ditentukan

**Output:** Issue log dengan semua conflict & solusi

---

### STEP 3: KOREKSI & OPTIMASI (15-19 JULI)

**Aktivitas A: Resolusi Conflict Satu Per Satu**
```
Untuk setiap conflict, tentukan solusi:

Conflict: [DOSEN] mengajar MK1 (Senin 09:00) & MK2 (Senin 10:00)
Opsi 1: Geser MK2 ke Selasa 09:00 (jika ruang ada)
Opsi 2: Geser MK1 ke Senin 13:00 (jika mahasiswa OK)
Opsi 3: Cari dosen pengganti untuk MK2

Keputusan: [PILIH OPSI & ALASAN]
Approval: Kaprodi / WK1
```

**Aktivitas B: Optimasi Alokasi Ruang**
```
Analisis:
- Ruang besar (>100 org): Alokasi ke kelas besar
- Ruang sedang (50-100): Alokasi ke kelas sedang
- Ruang kecil (<50): Alokasi ke kelas kecil
- Utilisasi: Target 60-80% per ruang
```

**Aktivitas C: Validasi Beban Dosen**
```
Cek per dosen:
- Total jam/minggu: 12-16 (optimal)
- Max 18-20 (acceptable)
- >20 jam: HARUS request approval Dekan

Jika overload:
- [ ] Cari dosen tambahan
- [ ] Geser beberapa MK ke dosen lain
- [ ] Buat kelas parallel
```

**Checklist:**
- [ ] Semua conflict resolved
- [ ] Ruang optimal dialokasikan
- [ ] Beban dosen balanced
- [ ] Semua keputusan documented

**Output:** Jadwal revised & issue log updated

---

### STEP 4: KONSULTASI STAKEHOLDER (20-21 JULI)

**Aktivitas A: Share Draft ke Kaprodi & Dosen Senior**
```
Email:
- Attach: Jadwal revised (Excel)
- Isi: "Jadwal sudah kami revisi berdasarkan feedback. 
  Mohon review & feedback dalam 2 hari"
- Deadline: [TGL] jam 16:00
```

**Aktivitas B: Collect Feedback**
```
Terima feedback tentang:
- Dosen preference jadwal
- Practical constraints (travel, meeting, dll)
- Ruang feasibility

Log semua feedback di spreadsheet:
Dosen | Feedback | Feasible? | Action
[NAMA] | [FEEDBACK] | ☐ Ya ☐ Tidak | [ACTION]
```

**Aktivitas C: Update Jadwal Based on Feedback**
```
Prioritas update:
1. Feedback Kaprodi (100% harus accommodate)
2. Feedback dosen senior (99% accommodate)
3. Feedback dosen lain (consider, balance dengan efficiency)

Untuk setiap change:
- Catat alasan
- Verify tidak ada new conflict timbul
- Update issue log
```

**Checklist:**
- [ ] Draft shared ke semua stakeholder
- [ ] Deadline feedback jelas dikomunikasikan
- [ ] Semua feedback collected & logged
- [ ] Update done based on priority

**Output:** Jadwal updated based on stakeholder feedback

---

### STEP 5: FINALISASI & APPROVAL (22-26 JULI)

**Aktivitas A: Final Quality Check**
```
Gunakan checklist dari 07_FORM_VERIFIKASI_JADWAL_RUANG.md:

☑ Completeness: Semua MK ada, tidak ada gap?
☑ Conflict: 100% resolved?
☑ Efficiency: Ruang & dosen optimal?
☑ Feasibility: Semua stakeholder agree?

Jika ada issue: Fix atau dokumen reason mengapa tidak bisa fix
```

**Aktivitas B: Create Final Version**
```
1. Save as: JADWAL_TA_2026_2027_FINAL_[TGL].xlsx
2. Lock cells untuk prevent accidental change
3. Backup di multiple location:
   - Local drive
   - Google Drive / Cloud
   - Email ke WK1

Format:
- Print: A3 landscape (untuk poster)
- Digital: Excel & PDF
- Per-dosen: Filter jadwal hanya MK yang diajar
- Per-prodi: Jadwal semua MK per prodi
- Per-ruang: Jadwal ruang untuk facilities
```

**Aktivitas C: Approval Dari Leadership**
```
Submit ke Kaprodi:
- Email: "Jadwal final TA 2026/2027 - mohon approval"
- Attach: Excel final + checklist QA
- Deadline: [TGL]

Submit ke WK1:
- Email: "Jadwal final sudah approve Kaprodi - ready for publication"
- Attach: Excel final + approval email dari Kaprodi
- Request: Approval final dari WK1

Submit ke Dekan (jika policy):
- Formal approval dari Dekan jika perlu
```

**Checklist:**
- [ ] QA checklist 100% pass
- [ ] Jadwal dalam format multiple (Excel, PDF, per-dosen, etc)
- [ ] Backup tersimpan di multiple location
- [ ] Approval dari Kaprodi terdapat
- [ ] Approval dari WK1 terdapat

**Output:** Jadwal final approved & ready for distribution

---

### STEP 6: PERSIAPAN DISTRIBUTION (27-28 JULI)

**Aktivitas A: Siapkan Berbagai Format**
```
1. Excel master (full jadwal)
   - Filename: Jadwal_TA_2026_2027_FINAL.xlsx
   
2. PDF poster (A3 landscape)
   - Filename: Jadwal_Poster_A3.pdf
   - Design: Besar, warna, mudah dibaca
   
3. Per-dosen schedule
   - Filename: Jadwal_Dosen_[NAMA].pdf
   - Content: Hanya jadwal MK yang diajar
   
4. Per-prodi schedule
   - Filename: Jadwal_Prodi_[PRODI].pdf
   - Content: Semua MK untuk mahasiswa prodi
   
5. Per-ruang schedule
   - Filename: Jadwal_Ruang_[RUANG].pdf
   - Content: Jadwal ruang untuk facilities mgmt
```

**Aktivitas B: Prepare Materi Sosialisasi**
```
Siapkan:
- Email template untuk dosen
- Email template untuk mahasiswa
- WhatsApp template reminder
- Poster template untuk cetak
- FAQ buat pertanyaan umum
```

**Aktivitas C: Setup Distribution Channel**
```
Channel yang akan digunakan:
1. Email (untuk dosen & mahasiswa)
2. Portal akademik (upload jadwal)
3. WhatsApp group (reminder)
4. Papan pengumuman (poster)
5. Website (jika ada)

Verify:
- [ ] Email list dosen lengkap
- [ ] Email list mahasiswa lengkap
- [ ] Portal portal ready untuk upload
- [ ] WA group active
- [ ] Lokasi poster sudah ditentukan
```

**Checklist:**
- [ ] Semua format siap (Excel, PDF, per-dosen, per-prodi)
- [ ] Template notifikasi siap
- [ ] Distribution channel ready
- [ ] Operator sudah trained

**Output:** File & template siap untuk distribution

---

### STEP 7: SOSIALISASI & PUBLIKASI (29-31 JULI)

**Aktivitas A: Kirim Jadwal ke Dosen (29 JULI)**
```
Email:
- Template: 09_TEMPLATE_NOTIFIKASI_JADWAL.md (Bagian A)
- Attachment: Jadwal_Dosen_[NAMA].pdf + Jadwal_Lengkap.xlsx
- CC: Kaprodi, WK1
- Deadline: Confirm receipt dalam 24 jam

Print hard copy:
- [ ] Print jadwal setiap dosen
- [ ] Arrange di pigeonhole atau kantor masing-masing
- [ ] Tandai tanggal diterima
```

**Aktivitas B: Publish Jadwal untuk Mahasiswa (29-30 JULI)**
```
1. Upload ke Portal Akademik
   - [ ] Upload Excel & PDF ke student portal
   - [ ] Test akses dari browser
   - [ ] Verify semua mahasiswa bisa download

2. Email to Mahasiswa
   - Template: 09_TEMPLATE_NOTIFIKASI_JADWAL.md (Bagian B)
   - Subject: Jadwal Perkuliahan TA 2026/2027
   - Attachment: Jadwal_Lengkap.pdf + Guide.pdf
   - Send: Hari Rabu pukul 09:00

3. WhatsApp Group (29 Juli sore)
   - Template: 09_TEMPLATE_NOTIFIKASI_JADWAL.md (Bagian D-Format 1)
   - Keep it short & friendly
   - Share link portal jika ada

4. Print Poster
   - [ ] Design poster (A2 landscape)
   - [ ] Print 5-10 lembar
   - [ ] Pajang di:
      - Papan pengumuman utama
      - Setiap building/gedung
      - Kantor admin
      - Ruang kelas (jika muat)
   - [ ] Dokumentasi dengan foto
```

**Aktivitas C: Verifikasi Reception & Follow-up**
```
Day 1 (29 Juli):
- [ ] Email sent to dosen & mahasiswa
- [ ] Portal upload done
- [ ] Poster dipajang
- [ ] Collect early feedback

Day 2-3 (30-31 Juli):
- [ ] Monitor: Ada pertanyaan/issue?
- [ ] Collect acknowledge dari dosen (minimal 80%)
- [ ] Siapkan FAQ untuk pertanyaan umum
- [ ] Final reminder ke mahasiswa via WA

Tracking:
- Email read receipt: ___% (target >70%)
- Dosen acknowledge: ___/[TOTAL] (target >90%)
- Portal akses: ___/[TOTAL] (monitoring)
```

**Checklist:**
- [ ] Email sent to all dosen & mahasiswa
- [ ] Portal successfully published
- [ ] Poster dipajang di semua lokasi
- [ ] WhatsApp reminder sent
- [ ] FAQ prepared for support
- [ ] Early issues handled

**Output:** Jadwal sudah tersebar ke semua stakeholders

---

## TROUBLESHOOTING GUIDE

| Problem | Solusi |
|---------|--------|
| Email bounced ke beberapa dosen | Verify email address yang benar, kirim ulang |
| Portal tidak bisa upload file | Contact IT support, check file size & format |
| Dosen komplain ada conflict setelah publish | Acknowledge & set meeting untuk resolve, minimize schedule change |
| Mahasiswa tidak bisa akses portal | Reset password, verify browser/internet connection |
| Poster tidak bisa dicetak | Ubah format ke PDF, adjust resolution |
| Ada conflict yang ketinggalan | Update issue log, komunikasi via email k semua pihak, revisi minor jadwal |

---

## CONTACT EMERGENCY

| Issue | Contact | Action | Timeline |
|-------|---------|--------|----------|
| Technical portal | IT Support | Kontak immediately | <1 jam |
| Conflict major | WK1 | Escalate & meeting | <2 jam |
| Dosen feedback major change | Kaprodi | Discuss feasibility | <4 jam |
| Facilities issue | Facilities Mgr | Koordinasi maintenance | <6 jam |

---

## APPROVAL & SIGN-OFF

Prosedur ini telah disetujui:

| Role | Nama | Tanda Tangan | Tanggal |
|------|------|---|---|
| Koordinator Jadwal | | | |
| Kaprodi | | | |
| WK1 | | | |

---

**Berlaku:** 8 Juli 2026  
**Version:** 1.0  
**Untuk:** Phase 2 - Koordinasi Jadwal TA 2026/2027

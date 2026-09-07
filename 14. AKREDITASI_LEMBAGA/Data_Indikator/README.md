# 📊 Data_Indikator - KPI & Metrics Dashboard

Folder ini berisi semua data & indikator kinerja untuk memantau kesiapan akreditasi.

## 📂 ISI FOLDER

```
Data_Indikator/
├── Dashboard_Akreditasi.xlsx        [Master dashboard KPI]
├── Standar_1_Indikator.xlsx         [KPI Standar 1]
├── Standar_2_Indikator.xlsx         [KPI Standar 2]
├── ... (S3-7)
├── Data_Dosen_SDM.xlsx              [Data dosen & tenaga]
├── Data_Mahasiswa_Lulusan.xlsx      [Data mahasiswa & alumni]
├── Data_Keuangan.xlsx               [Laporan keuangan]
├── Data_Fasilitas.xlsx              [Inventaris sarana]
├── Data_Publikasi_Penelitian.xlsx   [Publication database]
├── Tren_3_Tahun.xlsx                [Historical trend analysis]
└── Gap_Analysis.xlsx                [Gap vs target]
```

## 📈 DASHBOARD AKREDITASI

### Master Dashboard (Excel)
File: **Dashboard_Akreditasi.xlsx**

**Konten:**
- Overview tab: 7 standar score, overall progress
- Target tab: Target setiap KPI per standar
- Current tab: Realisasi saat ini per KPI
- Gap tab: Gap analysis (target - realisasi)
- Trend tab: Tren 3 tahun ke belakang
- Action tab: Action plan untuk closing gaps

**Update Frequency:** Bulanan (minimal)

## 🎯 INDIKATOR KINERJA PER STANDAR

### File: Standar_[1-7]_Indikator.xlsx

Struktur setiap file:
| KPI | Target | 2022 | 2023 | 2024 | Gap | Owner | Status |
|-----|--------|------|------|------|-----|-------|--------|
| [KPI 1] | | | | | | | |
| [KPI 2] | | | | | | | |
| ... | | | | | | | |

**Setiap Standar Include:**
1. 5-10 KPI utama
2. Data 3 tahun terakhir (untuk trend)
3. Target yang realistis
4. Gap analysis & owner
5. Action plan untuk improvement

## 📊 DATABASE UTAMA

### 1. Data SDM (Dosen & Tenaga Kependidikan)
File: **Data_Dosen_SDM.xlsx**

Kolom:
- Nama | NIDN | Gelar (S2/S3) | Bidang Keahlian
- Publikasi/tahun | Penelitian | Pengabdian
- Kepuasan (1-5) | Status (Tetap/Kontrak)
- KPI Achievement

**Untuk Standar 3, Gunakan Data ini**

### 2. Data Mahasiswa & Lulusan
File: **Data_Mahasiswa_Lulusan.xlsx**

Tabs:
- **Admission**: Jumlah pendaftar, diterima, nilai masuk (3 tahun)
- **Retention**: Retention rate per angkatan
- **Graduation**: On-time vs delayed graduation
- **GPA**: Distribusi nilai rata-rata
- **Tracer**: Alumni employment status
- **Satisfaction**: Hasil survey kepuasan

**Untuk Standar 4, Gunakan Data ini**

### 3. Data Keuangan
File: **Data_Keuangan.xlsx**

Tabs:
- **Balance Sheet**: Aset, liabilitas, equity (3 tahun)
- **Income Statement**: Revenue & expense (3 tahun)
- **RKAT**: Budget vs realisasi tahunan
- **Source**: Diversitas sumber pembiayaan
- **Sustainability**: Analisis keberlanjutan

**Untuk Standar 6, Gunakan Data ini**

### 4. Data Fasilitas & Sarana
File: **Data_Fasilitas.xlsx**

Tabs:
- **Gedung**: Luas, kondisi, utilization rate
- **Ruang Kuliah**: Jumlah, kapasitas, equipment
- **Laboratorium**: Daftar lab, peralatan, maintenance
- **Perpustakaan**: Koleksi (buku, jurnal, e-resource)
- **IT**: Infrastructure, bandwidth, security
- **Maintenance**: Budget & track maintenance

**Untuk Standar 6, Gunakan Data ini**

### 5. Data Publikasi & Penelitian
File: **Data_Publikasi_Penelitian.xlsx**

Kolom:
- Tahun | Judul | Penulis | Jurnal/Konferensi
- Type (Internasional/Nasional) | Impact Factor
- Research Grant | Pengabdian

**Untuk Standar 7, Gunakan Data ini**

## 📈 TREN ANALYSIS

File: **Tren_3_Tahun.xlsx**

**Analisis Tren:**
- Ambil 20-30 KPI kritis
- Plot data 3 tahun terakhir
- Identifikasi trend: naik, turun, stabil
- Interpretasi: why?
- Proyeksi: ke arah mana?

**Visual:** Include charts untuk presentasi asesor

## 🚨 GAP ANALYSIS

File: **Gap_Analysis.xlsx**

Struktur:
| KPI | Target BAN-PT | Current | Gap | % Gap | Root Cause | Action | Timeline | Owner |
|-----|---|---|---|---|---|---|---|---|

**Identify:**
1. KPI yang belum capai target
2. Root cause analysis
3. Action plan spesifik
4. Timeline realistis untuk closure
5. Owner & resource needed

## 📋 DATA QUALITY CHECKLIST

Sebelum pakai data dalam SER/presentasi:

- [ ] Data verified & accurate (cross-check multiple sources)
- [ ] Data terkini (update terakhir: _____)
- [ ] Data complete (no missing values)
- [ ] Data consistent (tidak ada outliers aneh)
- [ ] Data traceable (ada source/dokumentasi)
- [ ] Data presented clearly (format baik)

## 🔄 DATA UPDATE CYCLE

| Frekuensi | Activity | Owner | Tools |
|-----------|----------|-------|-------|
| **Bulanan** | Update KPI current values | Each Unit | Excel |
| **Bulanan** | Update Gap Analysis | Koordinator | Excel |
| **Tri-Bulanan** | Generate trend report | Koordinator | Excel + Charts |
| **Semester** | Deep analysis 3-tahun trend | Tim per Standar | Detailed Report |
| **Tahunan** | Publish data untuk SER | Koordinator | Master Database |

## 📱 HOW TO USE

### STEP 1: Setup
1. Copy template files
2. Input data dari setiap unit
3. Verify & validate
4. Backup digital

### STEP 2: Monitoring
- Update Dashboard setiap bulan
- Check gap terhadap target
- Identify issue & escalate
- Adjust action plan jika perlu

### STEP 3: Presentation
- Generate chart dari Dashboard
- Include tren 3 tahun
- Highlight kekuatan & kelemahan
- Show action plan untuk improvement

### STEP 4: SER & Asesor
- Reference data dari folder ini
- Lampirkan tabel/chart dalam dokumen
- Siapkan backup data untuk verifikasi asesor

---

**Versi:** 1.0 | Dibuat: 7 September 2026

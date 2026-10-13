# Checklist Persiapan LMS — STEI Fithrah Insani

Arsip repo dari halaman *Checklist Persiapan LMS* (`Checklist_Persiapan_LMS_STEI_FI.html`). Status centang diambil dari penyimpanan bersama (Supabase, tabel `unit_checks`, kunci `stei_lms_persiapan`) dan disinkronkan berkala. Kode item (A1, B2, ...) bersifat tetap dan menjadi kunci sinkron. Item yang sedang dikerjakan tetap `[ ]` dan diberi akhiran ` — 🔄 Dikerjakan (unit, tanggal): catatan`; item selesai `[x]`.

## A. Penemuan & Keputusan (Fase 0)
*10 item · Okt–Des 2026*

- [x] **A1** Kirim pesan pertanyaan ke pengembang SISCA / staf TI (vendor, e-learning, ekspor/API, login tunggal, jumlah pengguna) — PIC: WK1 · ⏰ Minggu 3 Okt
- [x] **A2** Dapatkan identitas vendor/pengembang SISCA dan kontak teknisnya — PIC: WK1 + UPT TI · ⏰ Minggu 3 Okt
- [x] **A3** Audit fitur portal dosen dan portal mahasiswa: apakah sudah ada unggah materi, tugas, presensi, penilaian — PIC: UPT TI + WK1 · ⏰ Okt 2026
- [ ] **A4** Konfirmasi kemampuan SISCA: ekspor CSV, API, atau akses basis data, serta kemungkinan login tunggal — PIC: UPT TI · ⏰ Okt 2026
- [ ] **A5** Kumpulkan jumlah mahasiswa dan dosen aktif per program studi (ES dan PS) — PIC: Kaprodi + Admin Akademik · ⏰ Okt 2026
- [ ] **A6** Audit infrastruktur dan personel TI yang tersedia untuk mengelola LMS — PIC: WK2 + UPT TI · ⏰ Nov 2026
- [ ] **A7** Tetapkan rentang anggaran LMS (lisensi/hosting/pelatihan) dan minta penawaran bila perlu — PIC: WK2 · ⏰ Nov 2026
- [ ] **A8** Verifikasi ketentuan regulasi pembelajaran daring/blended pada Permendikbudristek No. 53/2023 — PIC: LPM · ⏰ Nov 2026
- [ ] **A9** Survei kebutuhan singkat kepada dosen dan mahasiswa — PIC: Kaprodi + LPM · ⏰ Nov 2026
- [ ] **A10** Keputusan pimpinan: platform dan model hosting (memakai modul SISCA, Moodle terkelola, atau Google Classroom untuk pilot) — PIC: Ketua + WK1 · ⏰ Des 2026

## B. Keamanan Akun & Kebijakan Data
*5 item · Okt–Des 2026*

- [ ] **B1** Ganti kata sandi akun admin SISCA dan ganti akun admin bersama dengan akun bernama per petugas — PIC: UPT TI · ⏰ Segera
- [ ] **B2** Wajibkan ganti kata sandi saat login pertama (SISCA atau LMS) bagi dosen dan mahasiswa — PIC: UPT TI · ⏰ Nov 2026
- [ ] **B3** Susun kebijakan pelindungan data pribadi untuk LMS (siapa boleh melihat apa, masa simpan data) — PIC: LPM + WK2 · ⏰ Nov 2026
- [ ] **B4** Tetapkan hak akses berbasis peran (mahasiswa, dosen, Kaprodi, WK1, LPM, admin) — PIC: WK1 + UPT TI · ⏰ Des 2026
- [ ] **B5** Rencana cadangan data (backup) dan pemulihan LMS — PIC: UPT TI · ⏰ Des 2026

## C. Persiapan Pilot (Semester Genap 2026/2027)
*8 item · Des 2026 – awal semester genap*

- [ ] **C1** Pilih 5–8 mata kuliah pilot dari kedua prodi (termasuk Kewirausahaan II, Pasar Modal, dan Scale Up UMKM) — PIC: Kaprodi + WK1 · ⏰ Des 2026
- [ ] **C2** Lengkapi RPS dan bahan ajar kelas pilot (Master Book dan modul) — PIC: Dosen pengampu · ⏰ Jan 2027
- [ ] **C3** Siapkan platform dan alamat (subdomain) di domain kampus — PIC: UPT TI · ⏰ Jan 2027
- [ ] **C4** Impor data mahasiswa, dosen, dan kelas dari SISCA — PIC: UPT TI + Admin Akademik · ⏰ Jan 2027
- [ ] **C5** Buat templat kelas dari RPS (16 pertemuan, CPMK, tugas, penilaian) — PIC: WK1 + Dosen pilot · ⏰ Jan 2027
- [ ] **C6** Pelatihan dosen pilot — PIC: WK1 + UPT TI · ⏰ Jan 2027
- [ ] **C7** Susun panduan singkat untuk mahasiswa — PIC: Prodi + UPT TI · ⏰ Jan 2027
- [ ] **C8** Uji coba internal: login, presensi, tugas, nilai, forum — PIC: UPT TI + Dosen pilot · ⏰ Jan 2027

## D. Pelaksanaan & Evaluasi Pilot
*5 item · Semester genap 2026/2027*

- [ ] **D1** Presensi dan penilaian kelas pilot berjalan di LMS — PIC: Dosen pilot · ⏰ Selama semester
- [ ] **D2** Pendampingan mingguan dosen pilot — PIC: WK1 + UPT TI · ⏰ Selama semester
- [ ] **D3** Survei kepuasan dan kemanfaatan LMS (dosen dan mahasiswa) — PIC: LPM · ⏰ Pertengahan semester
- [ ] **D4** Ekspor nilai akhir kelas pilot ke SISCA — PIC: Dosen pilot + Admin Akademik · ⏰ Akhir semester
- [ ] **D5** Evaluasi pilot dan rekomendasi perluasan — PIC: WK1 + LPM · ⏰ Akhir semester

## E. Perluasan & Tata Kelola
*5 item · TA 2027/2028*

- [ ] **E1** Terbitkan SOP LMS dalam kerangka SOP WK1 — PIC: WK1 + LPM · ⏰ Sebelum TA 2027/2028
- [ ] **E2** Rencana perluasan LMS ke seluruh mata kuliah — PIC: WK1 + Kaprodi · ⏰ Sebelum TA 2027/2028
- [ ] **E3** Integrasi terjadwal SISCA–LMS atau login tunggal — PIC: UPT TI · ⏰ TA 2027/2028
- [ ] **E4** Masukkan bukti pembelajaran dari LMS ke tracker akreditasi — PIC: LPM · ⏰ Berkala
- [ ] **E5** Tambahkan indikator LMS (adopsi, kepuasan) ke dashboard internal — PIC: WK1 · ⏰ TA 2027/2028

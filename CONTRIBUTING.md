# Panduan Kerja Sama di Repositori STEI FI

Repositori ini publik. Pemilik repositori (WK1) meninjau dan menggabungkan setiap perubahan. Anggota tim unit bekerja lewat **fork** atau cabang sendiri, lalu mengajukan **pull request (PR)**. Tidak ada push langsung ke `master` oleh kontributor.

## 1. Pengaturan awal (sekali saja)

1. Buka halaman repositori, tekan **Fork**.
2. Salin fork ke komputer:
   ```bash
   git clone https://github.com/<akun-anda>/Kampus-STEI-FI.git
   cd Kampus-STEI-FI
   git remote add upstream https://github.com/zudin2007/Kampus-STEI-FI.git
   ```

## 2. Setiap kali mulai bekerja

Selalu mulai dari versi terbaru, supaya tidak terjadi konflik.

- Cara mudah: di halaman fork, tekan **Sync fork → Update branch**, lalu `git pull`.
- Cara terminal:
  ```bash
  git fetch upstream
  git checkout master
  git merge --ff-only upstream/master
  git push origin master
  ```

Lalu buat cabang baru untuk satu topik pekerjaan, dengan nama `unit/topik-singkat`:

```bash
git checkout -b wk2/rekap-serapan-anggaran
```

## 3. Bekerja

- **Satu topik per PR.** PR kecil lebih cepat ditinjau dan digabung.
- Ubah hanya berkas yang berkaitan dengan unit Anda (lihat peta di bagian 6).
- Uji halaman HTML di komputer sebelum mengirim:
  ```bash
  cd "1. AKREDITASI & REGULASI/Akreditasi versi revisi/Persiapan tahun ajaran baru"
  python3 -m http.server 8000
  ```
  Buka `http://localhost:8000/<nama-halaman>.html`. Halaman meminta kata sandi staf.
- Pesan commit dalam Bahasa Indonesia, kalimat perintah singkat. Contoh: `Perbarui daftar tugas WK2 minggu ini`.

## 4. Mengirim perubahan

```bash
git add <berkas-yang-diubah>
git commit -m "Perbarui daftar tugas WK2 minggu ini"
git push -u origin wk2/rekap-serapan-anggaran
```

1. Di GitHub, tekan **Compare & pull request**, tujuan `zudin2007/Kampus-STEI-FI` cabang `master`.
2. Isi templat PR dan tunggu **Pemeriksaan Pull Request** selesai (hijau).
3. Pemilik repositori meninjau, meminta perbaikan bila perlu, lalu menggabungkan (squash).
4. Setelah digabung: hapus cabang, lalu lakukan sync fork lagi (bagian 2).

Bila terjadi konflik: sync fork, lalu `git rebase upstream/master` pada cabang Anda dan `git push --force-with-lease`.

## 5. Yang tidak boleh masuk repositori (publik)

Simpan di **Drive terbatas**, dan di repositori cukup tautannya.

- Data pribadi mahasiswa, dosen, atau pegawai (nama beserta nilai, tagihan, alamat, nomor identitas).
- Data keuangan rinci (rekap tagihan SPP, gaji, rekening).
- Kata sandi, kunci API, token, dan berkas `.env`.
- Dokumen internal yang belum dipublikasikan (LED, soal ujian, draf RPS OBE).
- Berkas besar (di atas 5 MB).

Jangan mengubah tanpa izin pemilik: hash kata sandi gerbang pada halaman HTML, berkas di `.github/workflows/`, dan konfigurasi basis data.

Pemeriksaan otomatis pada PR akan menolak berkas dengan nama atau isi yang mencurigakan, berkas terlalu besar, dan halaman HTML yang rusak.

## 6. Peta area kerja per unit

| Unit | Folder dokumen | Halaman Pusat Kerja | Checklist |
|---|---|---|---|
| WK1 | `WK1_BIDANG_AKADEMIK/` | `WK1_Pusat_Kerja_STEI_FI.html` | `Checklist_Persiapan_TA_Baru_WK1_STEI_FI.html` |
| WK2 | `7. WK2_BIDANG_KEUANGAN/` | `WK2_Pusat_Kerja_STEI_FI.html` | `Checklist_Persiapan_TA_Baru_WK2_STEI_FI.html` |
| WK3 | `8. WK3_BIDANG_SARANA_PRASARANA/` (isinya Kemahasiswaan, Alumni, Kerjasama) | `WK3_Pusat_Kerja_STEI_FI.html` | `Checklist_Persiapan_TA_Baru_WK3_STEI_FI.html` |
| Kaprodi | `9. KAPRODI_AKADEMIK/` | `Kaprodi_Pusat_Kerja_STEI_FI.html` | `Checklist_Persiapan_TA_Baru_Prodi_ESPS_STEI_FI.html` |
| LPM | `11. LPM_QUALITY_ASSURANCE/` | `LPM_Pusat_Kerja_STEI_FI.html` | `Checklist_Persiapan_TA_Baru_LPM_STEI_FI.html` |
| LPPM | `10. LPPM_PENELITIAN/` | `LPPM_Pusat_Kerja_STEI_FI.html` | `Checklist_Persiapan_TA_Baru_LPPM_STEI_FI.html` |
| Ketua | `2. KEPEMIMPINAN & MANAJEMEN/` | `Ketua_Pusat_Kerja_STEI_FI.html` | `Checklist_Persiapan_TA_Baru_Ketua_STEI_FI.html` |

Halaman HTML berada di `1. AKREDITASI & REGULASI/Akreditasi versi revisi/Persiapan tahun ajaran baru/`. Begitu PR digabung ke `master`, situs terbit otomatis di GitHub Pages.

## 7. Meminta atau melaporkan tugas

Gunakan **Issues → New issue → Tugas unit** agar pekerjaan tercatat: unit, uraian, tenggat, dan bukti selesai. Sebutkan nomor issue pada PR (misalnya `Terkait #12`).

## 8. Bantuan

Tanyakan lewat Issue atau langsung kepada WK1. Status pengisian checklist dijelaskan di halaman *Panduan Pengisian Checklist*.

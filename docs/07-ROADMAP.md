# 07 — Roadmap & Rencana Kerja

Model pengembangan media mengikuti alur **ADDIE** (Analysis, Design, Development, Implementation,
Evaluation), umum dipakai di penelitian pengembangan (R&D) pendidikan.
Tanggal di bawah adalah perkiraan; sesuaikan dengan jadwal kuliah.

| Fase | Minggu | Kegiatan | Keluaran | Status |
|---|---|---|---|---|
| **Analysis** | — | Wawancara siswa S02 (beban kognitif) | Laporan wawancara | ✅ selesai (6 Nov 2026) |
| | 1 | Wawancara tambahan 4–6 siswa + 1–2 guru; cek CP/ATP | Temuan diperbarui di `01-RISET` | ⬜ |
| **Design** | 1–2 | Finalisasi PRD, desain pembelajaran, konten | Dokumen `docs/` v1.0 | 🟡 draf |
| | 2 | Wireframe semua layar (Figma/kertas) | Wireframe | ⬜ |
| | 2–3 | Tulis bank soal ±60 soal + petunjuk | `src/content/soal/*.json` | ⬜ |
| **Development** | 3 | Siapkan proyek (Vite, TS, PWA, Capacitor), token gaya | Kerangka aplikasi jalan | ⬜ |
| | 3–4 | `engine/` (volume, penilaian, diagnosis, fading) + unit test | Logika teruji | ⬜ |
| | 4–5 | Lab 3D, jaring-jaring, kubus satuan | F-03, F-04, F-05 | ⬜ |
| | 5–6 | Modul 0–5 (tes awal → soal cerita) | F-01, F-02, F-06–F-11 | ⬜ |
| | 6–7 | Modul 6–7, volume sebagian, Jelaskan Kembali, Cek Ulang | F-14–F-16 | ⬜ |
| | 7 | Mode luring, simpan progres, build APK | F-12, F-13, APK | ⬜ |
| | 8 | Tantangan & mode presentasi (bila waktu cukup) | F-17, F-18 | ⬜ |
| **Implementation / Validasi** | 8–9 | Validasi ahli materi & ahli media; revisi | Lembar validasi | ⬜ |
| | 9 | Uji coba kelompok kecil (5–10 siswa) | Data SUS, Paas, catatan | ⬜ |
| **Evaluation** | 10 | Uji lapangan (1 kelas) pretest–posttest; revisi akhir | Laporan efektivitas | ⬜ |

## Milestone

- **M1 – Dokumen siap:** semua file `docs/` disetujui dosen pembimbing.
- **M2 – Prototipe klik:** wireframe dapat diklik, diuji ke 2–3 siswa.
- **M3 – MVP inti:** Lab 3D + Modul 1–4 berjalan di web.
- **M4 – MVP lengkap:** semua *Must have* di web + APK.
- **M5 – Tervalidasi:** lolos validasi ahli & uji kelompok kecil.

## Rencana Fase Lanjutan (setelah MVP)
1. Bangun ruang lain: prisma, limas, tabung, kerucut, bola.
2. Luas permukaan (terhubung dengan jaring-jaring).
3. Dasbor guru sederhana (ekspor hasil ke CSV).
4. Ukuran desimal dan konversi satuan lanjutan.

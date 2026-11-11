# 08 — Rencana Evaluasi & Pengujian

## 1. Pengujian Perangkat Lunak

### 1.1 Unit test (wajib untuk `src/engine/`)
| Fungsi | Kasus uji minimal |
|---|---|
| `volumeKubus(s)` | 6 → 216; 1 → 1; 10 → 1000 |
| `volumeBalok(p,l,t)` | 8,4,3 → 96; 20,6,4 → 480 |
| `volumeSebagian(V, a, b)` | 72000, 2, 3 → 48000 (tanpa galat desimal) |
| `konversi(nilai, dari, ke)` | 1000 cm³ → 1 dm³ → 1 liter |
| `diagnosis(soal, jawaban)` | 136 untuk balok 8×4×3 → `RUMUS_LUAS`; 18 untuk kubus 6 → `S_KALI_3`; 96 cm² → `SATUAN` |
| `fading(riwayat)` | 2 benar berturut → naik level; 2 salah → turun |

### 1.2 Uji fungsional (manual/Playwright)
- [ ] Alur Beranda → Tes Awal → modul sesuai skor.
- [ ] Slider mengubah bangun dan angka di rumus secara sinkron.
- [ ] Jaring-jaring membuka & menutup tanpa celah.
- [ ] Petunjuk bertingkat muncul berurutan.
- [ ] Progres tetap ada setelah aplikasi ditutup.
- [ ] Mode pesawat: semua modul tetap berjalan (web PWA & APK).
- [ ] Tampilan benar di 360 px, 768 px, 1920 px.

### 1.3 Uji perangkat
Minimal 3 HP Android berbeda (salah satunya RAM ≤ 3 GB) + 2 browser desktop.

## 2. Validasi Ahli

| Validator | Aspek | Instrumen |
|---|---|---|
| Ahli materi (dosen/guru matematika) | Kebenaran konsep, kesesuaian CP, kualitas soal, bahasa | Angket skala Likert 1–4/1–5 |
| Ahli media | Tampilan, navigasi, keterbacaan, prinsip CLT | Angket skala Likert |

Kriteria layak: rata-rata skor ≥ 3,25 dari 4 (atau ≥ 80%). Revisi sesuai saran sebelum uji siswa.

## 3. Uji Coba Siswa

### 3.1 Kelompok kecil (5–10 siswa, kemampuan beragam)
- **Think-aloud**: siswa mengerjakan sambil mengucapkan pikirannya; catat titik bingung.
- **SUS (System Usability Scale)** 10 butir → target ≥ 70.
- **Skala beban mental Paas (1–9)** setelah tiap modul.

### 3.2 Uji lapangan (1 kelas)
- Desain: *one group pretest–posttest* (atau dua kelompok bila memungkinkan: aplikasi vs LKS).
- Instrumen: tes 10 soal (setara pretest–posttest), mencakup substitusi, soal cerita, volume sebagian.
- Analisis: N-gain; uji t berpasangan (bila data normal) atau Wilcoxon.
- Ukur juga beban kognitif per jenis memakai kuesioner tiga dimensi (mis. instrumen Leppink dkk.,
  2013: intrinsic, extraneous, germane) yang diadaptasi ke bahasa Indonesia.

## 4. Pemetaan Tujuan ke Metrik

| Tujuan PRD | Metrik | Instrumen |
|---|---|---|
| G1 Extraneous load turun | Skor Paas / dimensi extraneous | Kuesioner beban kognitif |
| G2 Substitusi benar | % benar langkah substitusi | Log aplikasi + posttest |
| G3 Soal cerita | Skor soal cerita | Pretest–posttest |
| G4 Volume sebagian | % benar soal pecahan | Posttest |
| G5 Mudah dipakai | Skor SUS | Angket SUS |

## 5. Etika
- Izin sekolah, persetujuan orang tua, dan persetujuan siswa (seperti pada wawancara S02).
- Data siswa memakai kode (S01, S02, …), bukan nama.

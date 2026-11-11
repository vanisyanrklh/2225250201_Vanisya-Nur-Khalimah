# RuangKu — Aplikasi Belajar Volume Kubus & Balok (SMP)

Aplikasi pembelajaran matematika untuk siswa SMP yang berjalan di **web** dan **Android**,
dirancang berdasarkan **Cognitive Load Theory** dan hasil wawancara siswa.

**Pengembang:** Vanisya Nur Khalimah (2225250201) — S1 Pendidikan Matematika
**Status:** MVP v0.1 (11 November 2026) — semua fitur *Must have* dan sebagian besar *Should have* sudah dibuat

## Cara Menjalankan

Butuh **Node.js 20+** (sudah terpasang di `%LOCALAPPDATA%\Programs\node-v26.13.0-win-x64`).
Buka terminal **baru** (agar PATH terbaca), lalu di folder ini:

```bash
npm install        # sekali saja
npm run dev        # buka http://localhost:5173 di browser
```

Untuk mencoba di HP Android yang tersambung ke Wi-Fi yang sama, buka alamat
`http://<IP-laptop>:5173` yang tampil di terminal.

| Perintah | Fungsi |
|---|---|
| `npm run test` | menjalankan 95 unit test (rumus, diagnosis kesalahan, fading, bank soal) |
| `npm run build` | build produksi ke `dist/` (bisa di-upload ke GitHub Pages/Netlify) |
| `npm run android:sync` | build lalu salin ke proyek Android `android/` |
| `npm run android:open` | buka proyek di Android Studio → *Build > Build APK(s)* |

Membuat APK membutuhkan **Android Studio** (sudah termasuk JDK dan Android SDK).

## Fitur yang Sudah Ada

| Fitur PRD | Lokasi |
|---|---|
| F-01 Tes Awal diagnostik | Modul 0 |
| F-02 Unsur bangun ruang (sorot sisi/rusuk/titik sudut, ukuran) | Modul 1 |
| F-03 Lab 3D (slider ukuran, putar) | Lab 3D |
| F-04 Jaring-jaring animasi | Modul 1, Lab 3D |
| F-05 Kubus satuan lapis demi lapis | Modul 2, Lab 3D |
| F-06 Contoh soal bertahap | Modul 3 |
| F-07 Latihan berpemandu + fading 4 level | Modul 4–7 |
| F-08 Alat soal cerita (ketuk angka → kolom diketahui) | Modul 5 |
| F-09 Perkalian bertahap | Langkah "Hitung" |
| F-10 Petunjuk bertingkat (3 level) | Semua latihan |
| F-11 Umpan balik spesifik jenis kesalahan | Langkah "Simpulkan" |
| F-12 Luring (PWA + APK) | otomatis |
| F-13 Progres tersimpan di perangkat | otomatis |
| F-14 Volume sebagian (simulasi air) | Modul 6, Lab 3D |
| F-15 Jelaskan Kembali | Akhir Modul 7 |
| F-16 Cek Ulang | Setelah setiap soal |
| F-17 Tantangan "Tepat Penuh" | Tantangan |
| F-18 Mode presentasi | Lab 3D |

Belum dibuat: F-19 konversi satuan lanjutan (baru ada konversi ke liter), F-20 bangun gabungan,
F-21 lencana, F-22 narasi suara, dan mode 2D cadangan otomatis (sudah ada "Mode ringan" manual
di Pengaturan).

## Dokumen Perencanaan

| No | Dokumen | Isi |
|---|---|---|
| 01 | [Riset Wawancara](docs/01-RISET-WAWANCARA.md) | Ringkasan temuan wawancara S02 + implikasi desain |
| 02 | [PRD](docs/02-PRD.md) | Masalah, tujuan, persona, user stories, fitur & prioritas |
| 03 | [Desain Pembelajaran](docs/03-DESAIN-PEMBELAJARAN.md) | Tujuan pembelajaran, prinsip CLT, struktur modul |
| 04 | [Konten Materi](docs/04-KONTEN-MATERI.md) | Kaitan kurikulum, materi, bank soal, tes awal |
| 05 | [UI/UX](docs/05-UI-UX.md) | Prinsip tampilan, warna, wireframe, daftar periksa |
| 06 | [Arsitektur Teknis](docs/06-ARSITEKTUR-TEKNIS.md) | Teknologi, struktur folder, model data, build |
| 07 | [Roadmap](docs/07-ROADMAP.md) | Tahapan ADDIE, jadwal, milestone |
| 08 | [Evaluasi](docs/08-EVALUASI.md) | Unit test, validasi ahli, uji coba siswa, metrik |
| — | [CLAUDE.md](CLAUDE.md) | Aturan kerja untuk Claude/pengembang |

## Urutan Membaca
1 → 2 → 3 → 5 → 6, lalu 4, 7, 8 sesuai kebutuhan.

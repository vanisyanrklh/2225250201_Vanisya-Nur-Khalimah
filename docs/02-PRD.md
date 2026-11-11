# 02 — Product Requirements Document (PRD)

**Nama kerja aplikasi:** *RuangKu — Belajar Volume Kubus & Balok*
(nama dapat diganti)
**Versi dokumen:** 0.1 (draf) · 11 November 2026
**Pemilik produk:** Vanisya Nur Khalimah (S1 Pendidikan Matematika)
**Platform:** Web (browser) & Android

---

## 1. Latar Belakang

Wawancara beban kognitif dengan siswa kelas IX (S02) menunjukkan bahwa siswa sudah mengenal
rumus volume kubus dan balok, tetapi masih mengalami hambatan pada: (1) memasukkan ukuran ke
dalam rumus, (2) memahami soal cerita yang panjang, (3) volume sebagian (pecahan), dan
(4) ketelitian perkalian. Siswa adalah pembelajar visual yang terbantu oleh gambar, praktik
nyata, dan permainan, tetapi tidak menyukai tampilan yang ramai. Detail temuan:
[`01-RISET-WAWANCARA.md`](01-RISET-WAWANCARA.md).

## 2. Pernyataan Masalah

> Siswa SMP yang sudah hafal rumus volume kubus dan balok masih sering gagal menyelesaikan soal
> karena beban kognitif yang tidak perlu (soal panjang, penjelasan terlalu cepat, tidak ada
> visual) dan karena langkah menghubungkan ukuran di soal dengan rumus belum terlatih.

## 3. Tujuan Produk

| ID | Tujuan | Indikator keberhasilan (target MVP) |
|---|---|---|
| G1 | Mengurangi *extraneous load* saat belajar volume | Skor beban mental (skala Paas 1–9) turun ≥ 1 poin dibanding belajar dari LKS |
| G2 | Melatih langkah substitusi & perhitungan secara bertahap | ≥ 80% siswa uji benar pada langkah substitusi di posttest |
| G3 | Membangun skema penyelesaian soal cerita | Skor soal cerita posttest naik ≥ 20% dari pretest |
| G4 | Mengenalkan volume sebagian (pecahan) secara visual | ≥ 70% siswa menjawab benar soal volume 2/3, 1/2, 3/4 |
| G5 | Mudah dipakai | Skor SUS ≥ 70 |

## 4. Non-Tujuan (di luar cakupan MVP)

- Bangun ruang selain kubus dan balok (prisma, limas, tabung, dll.) → fase berikutnya.
- Akun, login, kelas daring, dasbor guru → fase berikutnya.
- Chat/forum, papan peringkat publik, iklan.
- Konten video panjang.

## 5. Pengguna

### Persona utama — "Nisa", siswa SMP kelas VIII–IX
- Sudah pernah belajar volume sejak SD, hafal rumus.
- Pembelajar visual, cepat "blank" saat membaca soal panjang.
- Sering tertinggal saat guru menjelaskan langkah substitusi.
- Memakai HP Android kelas menengah ke bawah, kuota terbatas.
- Suka praktik nyata dan permainan.

### Persona sekunder — Guru matematika
- Ingin media yang bisa dipakai di kelas (proyektor) atau diberikan sebagai latihan mandiri.
- (MVP) Hanya sebagai pengguna tampilan presentasi; belum ada fitur pemantauan.

## 6. User Stories

| ID | Sebagai… | Saya ingin… | Agar… | Temuan |
|---|---|---|---|---|
| US-01 | siswa | mengatur panjang, lebar, tinggi balok/ sisi kubus dengan slider dan melihat bentuknya berubah | saya bisa membayangkan ukuran | T-19, T-10 |
| US-02 | siswa | melihat bangun "dibuka" menjadi jaring-jaring | saya paham unsur bangun ruang | T-19, T-20 |
| US-03 | siswa | melihat volume sebagai tumpukan kubus satuan | saya paham *mengapa* rumusnya p × l × t | T-14, T-06 |
| US-04 | siswa | mempelajari unsur kubus/balok (sisi, rusuk, titik sudut, p, l, t) sebelum volume | saya tidak bingung saat memasukkan angka | T-20, T-06 |
| US-05 | siswa | mengikuti contoh soal langkah demi langkah dengan kecepatan saya sendiri dan mengulang langkah | saya tidak tertinggal | T-12 |
| US-06 | siswa | mengisi langkah "Diketahui → Ditanya → Rumus → Substitusi → Hitung" dengan bantuan | saya terbiasa dengan polanya | T-05, T-18 |
| US-07 | siswa | menyorot angka penting dalam soal cerita lalu menyeretnya ke kolom diketahui | soal panjang tidak membuat saya blank | T-09, T-07 |
| US-08 | siswa | menghitung perkalian bertahap dan mendapat umpan balik di setiap langkah | saya tahu di mana saya salah | T-08 |
| US-09 | siswa | meminta petunjuk bertingkat ketika buntu | saya bisa menyelesaikan sendiri | T-16 |
| US-10 | siswa | melihat simulasi air mengisi balok 1/2, 2/3, 3/4 | saya paham volume sebagian | T-03 |
| US-11 | siswa | menulis/memilih penjelasan dengan kata-kata sendiri setelah menjawab | pemahaman saya lebih kuat | T-17 |
| US-12 | siswa | membandingkan data yang saya pakai dengan data di soal (Cek Ulang) | saya yakin jawaban benar | T-15 |
| US-13 | siswa | memainkan tantangan singkat setelah materi | belajar lebih seru | T-14 |
| US-14 | siswa | memakai aplikasi tanpa internet setelah dibuka pertama kali | kuota saya hemat | Persona |
| US-15 | guru | menampilkan Lab 3D di proyektor | bisa dipakai saat mengajar | Persona |

## 7. Fitur & Prioritas (MoSCoW)

### Must have (MVP)
| ID | Fitur | Deskripsi singkat | User story |
|---|---|---|---|
| F-01 | **Tes Awal (diagnostik)** | 5 soal singkat untuk menentukan titik mulai; siswa yang sudah mahir bisa melewati materi dasar. | US-04 |
| F-02 | **Modul Unsur Bangun Ruang** | Mengenal sisi, rusuk, titik sudut, p, l, t pada kubus/balok; interaktif ketuk-label. | US-04 |
| F-03 | **Lab 3D** | Kubus/balok 3D, slider ukuran, putar, tampilkan label ukuran langsung pada rusuk. | US-01, US-15 |
| F-04 | **Jaring-jaring** | Animasi membuka/menutup bangun menjadi jaring-jaring. | US-02 |
| F-05 | **Kubus Satuan** | Mengisi bangun dengan kubus 1 cm³ lapis demi lapis → menurunkan rumus. | US-03 |
| F-06 | **Contoh Soal Bertahap (worked example)** | Langkah tampil satu per satu; tombol *Lanjut* / *Ulangi langkah*. | US-05 |
| F-07 | **Latihan Berpemandu (faded example)** | Langkah dilengkapi sebagian oleh aplikasi; bantuan berkurang seiring kemahiran. | US-06 |
| F-08 | **Alat Soal Cerita** | Sorot angka → seret ke kolom "Diketahui"; ilustrasi otomatis berlabel. | US-07 |
| F-09 | **Kalkulator Langkah** | Perkalian bertahap (p × l → hasil × t) dengan cek per langkah. | US-08 |
| F-10 | **Petunjuk Bertingkat** | 3 level: arahan umum → langkah spesifik → contoh serupa. | US-09 |
| F-11 | **Umpan Balik Spesifik** | Deteksi jenis kesalahan (salah substitusi, salah kali, salah satuan, pakai rumus luas). | US-08 |
| F-12 | **Mode Luring (offline)** | Semua konten tersedia tanpa internet (PWA + APK). | US-14 |
| F-13 | **Penyimpanan Progres Lokal** | Progres & skor disimpan di perangkat. | — |

### Should have
| ID | Fitur | User story |
|---|---|---|
| F-14 | **Volume Sebagian** — simulasi air mengisi 1/2, 2/3, 3/4 bangun | US-10 |
| F-15 | **Jelaskan Kembali** (self-explanation: pilih/susun kalimat penjelasan) | US-11 |
| F-16 | **Cek Ulang** — tabel perbandingan data dipakai vs data soal | US-12 |
| F-17 | **Tantangan** — mini-game (mis. "Isi kotak tepat penuh", "Tebak ukuran") | US-13 |
| F-18 | **Mode Presentasi** — tampilan besar untuk proyektor | US-15 |

### Could have
- F-19 Konversi satuan volume (cm³ ↔ dm³ ↔ liter ↔ m³).
- F-20 Soal campuran: volume gabungan kubus + balok.
- F-21 Lencana pencapaian sederhana (tanpa papan peringkat).
- F-22 Mode suara (narasi teks-ke-suara untuk langkah).

### Won't have (MVP)
- Login, server, dasbor guru, multiplayer, iklan.

## 8. Alur Pengguna Utama

```
Buka aplikasi
  └─► Beranda (3 pilihan besar: Belajar · Lab 3D · Tantangan)
        └─► Belajar
              ├─► Tes Awal (bisa dilewati)
              ├─► 1. Unsur Kubus & Balok
              ├─► 2. Dari Kubus Satuan ke Rumus
              ├─► 3. Contoh Soal Bertahap
              ├─► 4. Latihan Berpemandu  ──(benar 3x berturut)──► bantuan dikurangi
              ├─► 5. Soal Cerita
              ├─► 6. Volume Sebagian
              └─► 7. Latihan Akhir + Jelaskan Kembali
```

Detail rancangan pembelajaran: [`03-DESAIN-PEMBELAJARAN.md`](03-DESAIN-PEMBELAJARAN.md).

## 9. Kebutuhan Non-Fungsional

| ID | Kebutuhan | Target |
|---|---|---|
| NF-01 | Performa | Dibuka < 3 detik di Android RAM 3 GB; animasi 3D ≥ 30 fps |
| NF-02 | Ukuran | APK < 20 MB; muatan awal web < 2 MB |
| NF-03 | Luring | 100% konten MVP berjalan tanpa internet |
| NF-04 | Kompatibilitas | Android 8.0+; Chrome, Edge, Firefox, Safari versi terbaru |
| NF-05 | Aksesibilitas | Kontras teks ≥ 4.5:1, target sentuh ≥ 48 dp, ukuran huruf dapat diperbesar |
| NF-06 | Privasi | Tidak mengumpulkan data pribadi; semua data di perangkat (aman untuk anak) |
| NF-07 | Bahasa | Bahasa Indonesia baku yang sederhana, kalimat ≤ 15 kata |
| NF-08 | Responsif | Nyaman di layar 360 px (HP) hingga 1920 px (proyektor) |

## 10. Metrik (diukur saat uji coba)

- Ketuntasan modul (% siswa menyelesaikan 7 modul).
- Akurasi per langkah (diketahui, substitusi, perkalian, satuan).
- Jumlah petunjuk yang diminta per soal (indikator kesulitan).
- Skala beban mental Paas & skor SUS.

## 11. Risiko & Mitigasi

| Risiko | Dampak | Mitigasi |
|---|---|---|
| 3D berat di HP murah | Lag → beban extraneous naik | Mode 2D isometrik cadangan otomatis bila fps rendah |
| Gamifikasi mengalihkan fokus | Extraneous load naik | Game hanya setelah materi, tanpa animasi dekoratif |
| Responden riset hanya 1 | Fitur bias ke siswa berkemampuan baik | Tambah wawancara; uji coba dengan siswa beragam |
| Waktu pengembangan terbatas | MVP tidak selesai | Kerjakan sesuai prioritas Must → Should; lihat roadmap |

## 12. Kriteria Rilis MVP

- Semua fitur **Must have** berjalan di web & APK Android.
- Lolos uji ahli materi dan ahli media (validasi).
- Uji keterbacaan dengan minimal 5 siswa SMP.
- Tidak ada bug kritis pada daftar uji [`08-EVALUASI.md`](08-EVALUASI.md).

## 13. Dokumen Terkait

- [`03-DESAIN-PEMBELAJARAN.md`](03-DESAIN-PEMBELAJARAN.md) — prinsip CLT & alur modul
- [`04-KONTEN-MATERI.md`](04-KONTEN-MATERI.md) — isi materi & bank soal
- [`05-UI-UX.md`](05-UI-UX.md) — pedoman tampilan
- [`06-ARSITEKTUR-TEKNIS.md`](06-ARSITEKTUR-TEKNIS.md) — teknologi & struktur kode
- [`07-ROADMAP.md`](07-ROADMAP.md) — jadwal
- [`08-EVALUASI.md`](08-EVALUASI.md) — rencana uji & validasi

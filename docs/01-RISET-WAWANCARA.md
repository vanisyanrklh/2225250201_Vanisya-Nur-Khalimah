# 01 — Ringkasan Riset: Wawancara Beban Kognitif

> Sumber: `Pencatatan hasil wawancara.docx` (Dokumen/). Dokumen ini merangkum temuan dan
> menerjemahkannya menjadi **implikasi desain**. Semua keputusan di PRD harus bisa ditelusuri
> ke salah satu kode temuan di sini (T-xx).

## 1. Identitas Wawancara

| Keterangan | Isi |
|---|---|
| Kode siswa | S02 |
| Kelas | IX SMP |
| Tanggal | 6 November 2026 |
| Pewawancara | Vanisya Nur Khalimah |
| Materi | Volume Kubus dan Balok |
| Durasi | 38 menit, dengan persetujuan siswa |
| Artefak pemicu | Buku paket/LKS, Soal 1 (kubus s = 6 cm), Soal 2 (balok 8 × 4 × 3 cm) |
| Kerangka | Cognitive Load Theory (CLT): Intrinsic, Extraneous, Germane Load |

## 2. Temuan Utama per Dimensi

### A. Pengalaman awal (K01–K03)
| Kode | Temuan | Kutipan kunci |
|---|---|---|
| T-01 | Materi sudah dikenal sejak SD kelas 6, dikaitkan dengan konteks sehari-hari (kotak pensil, kotak hadiah). | "menghitung volume kotak pensil berbentuk balok" |
| T-02 | Guru memakai praktik/pembuktian, proyektor, latihan kelompok & individu. | — |
| T-03 | **Lancar pada volume utuh, ragu pada volume sebagian** (mis. 2/3 kubus, "diisi air sebanyak 2/3"). | "suka ragu kalo disuruh ngitung volume … yang tidak utuh" |

### B. Intrinsic Load (IL01–IL05)
| Kode | Temuan | Implikasi |
|---|---|---|
| T-04 | Siswa **sudah membedakan** rumus kubus (s³) dan balok (p × l × t). | Rumus dasar bukan titik sulit utama → jangan berlama-lama; sediakan tes awal untuk melewati. |
| T-05 | Strategi: fokus dulu pada **apa yang diketahui**. | Bangun scaffold "Diketahui → Ditanya → Rumus → Hitung". |
| T-06 | **Kesulitan memasukkan angka ke dalam rumus** (substitusi) bila belum paham konsep. | Langkah substitusi harus dipandu & divisualkan (angka "masuk" ke rumus dari gambar). |
| T-07 | Soal cerita *kadang* sulit karena harus memahami konsep di baliknya. | Latih penerjemahan soal cerita → model matematika secara bertahap. |
| T-08 | Sumber kesalahan: **kurang fokus pada perkalian**; mengecek ulang angka dengan soal. | Perkalian bertahap (p × l dulu, lalu × t), tombol cek per langkah. |

### C. Extraneous Load (EL01–EL05)
| Kode | Temuan | Implikasi |
|---|---|---|
| T-09 | **Soal panjang / kalimat sulit membuat "otak blank"**, harus dibaca berkali-kali. | Kalimat pendek, satu informasi per kalimat, fitur sorot (highlight) info penting. |
| T-10 | **Gambar membantu** ("langsung terbayang"); soal cerita tanpa gambar membingungkan. | Setiap soal cerita punya ilustrasi bangun berlabel. |
| T-11 | Gaya belajar visual; tampilan menarik menambah semangat. | Visual rapi & menarik, tetapi relevan dengan materi. |
| T-12 | **Guru menjelaskan terlalu cepat**, tertinggal pada bagian memasukkan angka ke rumus. | Belajar sesuai kecepatan sendiri (self-paced), tombol "ulangi langkah", contoh tambahan. |
| T-13 | Mudah membedakan panjang vs lebar dari besarnya ukuran. | Tidak perlu fitur khusus; cukup label pada gambar. |

### D. Germane Load (GL01–GL05)
| Kode | Temuan | Implikasi |
|---|---|---|
| T-14 | Paling terbantu oleh **praktik nyata** (membuat kubus dari kardus) dan **game**. | Manipulasi 3D interaktif + aktivitas tantangan ringan bertema materi. |
| T-15 | Memeriksa jawaban dengan mencocokkan ukuran yang ditulis dengan soal. | Fitur "Cek Ulang": tampilkan kembali data yang dipakai vs data di soal. |
| T-16 | Bila buntu, minta **penjelasan ulang** dari guru/teman. | Petunjuk bertingkat (hint 1 → 2 → 3) dan "jelaskan lagi dengan cara lain". |
| T-17 | **Menjelaskan ke teman membuatnya lebih paham** (efek self-explanation). | Prompt "Jelaskan dengan kata-katamu" setelah menyelesaikan soal. |
| T-18 | Transfer ke soal baru: cari yang diketahui dulu. | Konsisten memakai pola yang sama di semua soal (skema). |

### E. Rekomendasi desain dari siswa (DS01–DS03)
| Kode | Temuan | Implikasi |
|---|---|---|
| T-19 | Ingin **visualisasi bangun ruang yang ukurannya bisa diatur** dan **jaring-jaring**. | Fitur inti: Lab 3D (slider p, l, t / s) + animasi jaring-jaring. |
| T-20 | Perlu penjelasan bertahap tentang **ukuran (p, l, t), unsur-unsur, jaring-jaring**. | Modul pra-pelatihan (pretraining) unsur bangun ruang sebelum volume. |
| T-21 | **Tidak perlu** latar belakang ramai atau visual di luar materi. | Antarmuka minimalis; dekorasi dilarang di layar belajar. |

## 3. Sintesis: Masalah yang Harus Diselesaikan Aplikasi

1. **Substitusi ukuran ke rumus** adalah titik rawan (T-06, T-12) → paling sering tertinggal.
2. **Soal cerita panjang** membebani memori kerja (T-07, T-09) → beban *extraneous* tinggi.
3. **Volume sebagian / pecahan** (T-03) → belum terbentuk skema.
4. **Kesalahan hitung perkalian** karena kurang fokus (T-08).
5. Siswa visual yang butuh **manipulasi konkret** (T-10, T-14, T-19) namun **tanpa dekorasi berlebihan** (T-21).

## 4. Keterbatasan Riset & Saran Lanjutan

- Baru **1 responden (S02)** dengan kemampuan relatif baik → temuan belum bisa digeneralisasi.
  Disarankan menambah 4–6 siswa dengan kemampuan beragam (rendah, sedang, tinggi) dan
  1–2 guru matematika.
- Belum ada data kuantitatif. Rencana pengukuran ada di [`08-EVALUASI.md`](08-EVALUASI.md).
- Perlu dicek ulang kesesuaian dengan Capaian Pembelajaran Kurikulum Merdeka Fase D
  (lihat [`04-KONTEN-MATERI.md`](04-KONTEN-MATERI.md)).

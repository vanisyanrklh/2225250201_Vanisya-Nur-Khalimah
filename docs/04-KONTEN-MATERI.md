# 04 — Konten Materi & Bank Soal

## 1. Keterkaitan Kurikulum

- **Kurikulum Merdeka, Fase D (SMP kelas VII–IX), elemen Geometri**: siswa dapat menjelaskan
  cara menentukan luas permukaan dan volume bangun ruang serta menyelesaikan masalah terkait.
- Materi volume kubus dan balok sudah dikenalkan di SD (Fase C); di SMP berfungsi sebagai
  penguatan dan fondasi untuk prisma, limas, tabung, dll.
- ⚠️ **Tugas:** cocokkan kembali dengan dokumen CP/ATP resmi terbaru dan buku siswa yang dipakai
  sekolah mitra sebelum validasi ahli materi.

## 2. Ringkasan Materi

### 2.1 Unsur
| Unsur | Kubus | Balok |
|---|---|---|
| Sisi (bidang) | 6 persegi kongruen | 6 persegi panjang (3 pasang kongruen) |
| Rusuk | 12, sama panjang | 12 (4 panjang, 4 lebar, 4 tinggi) |
| Titik sudut | 8 | 8 |
| Ukuran | sisi (s) | panjang (p), lebar (l), tinggi (t) |
| Jaring-jaring | 11 bentuk berbeda | beberapa bentuk (tergantung ukuran) |

### 2.2 Rumus
- Volume kubus: **V = s × s × s = s³**
- Volume balok: **V = p × l × t**
- Volume sebagian: **V_bagian = pecahan × V_penuh** (mis. 2/3 × V)
- Satuan: mm³, cm³, dm³ (= liter), m³. 1 dm³ = 1.000 cm³ = 1 liter.

### 2.3 Makna konsep
Volume = banyaknya kubus satuan yang dapat mengisi bangun ruang.
Balok p × l × t = (banyak kubus di satu lapis alas: p × l) × (banyak lapis: t).

## 3. Bank Soal (contoh awal — perlu dikembangkan menjadi ±60 soal)

Format setiap soal disimpan sebagai data JSON (lihat [`06-ARSITEKTUR-TEKNIS.md`](06-ARSITEKTUR-TEKNIS.md)).

### Level 1 — Langsung (angka sudah diberikan)
1. Sebuah kubus memiliki panjang sisi 6 cm. **Berapa volumenya?** → 216 cm³ *(soal pemicu wawancara)*
2. Sebuah balok memiliki p = 8 cm, l = 4 cm, t = 3 cm. **Berapa volumenya?** → 96 cm³ *(soal pemicu wawancara)*
3. Kubus dengan sisi 10 cm. **Berapa volumenya?** → 1.000 cm³
4. Balok p = 12 cm, l = 5 cm, t = 2 cm. → 120 cm³

### Level 2 — Soal cerita pendek
5. Kotak pensil Rina berbentuk balok. Panjangnya 20 cm, lebarnya 6 cm, tingginya 4 cm.
   **Berapa volume kotak pensil itu?** → 480 cm³
6. Kotak hadiah berbentuk kubus. Panjang sisinya 15 cm.
   **Berapa volume kotak hadiah?** → 3.375 cm³

### Level 3 — Mencari unsur yang tidak diketahui
7. Volume balok 240 cm³. Panjang 10 cm dan lebar 6 cm. **Berapa tingginya?** → 4 cm
8. Volume kubus 125 cm³. **Berapa panjang sisinya?** → 5 cm

### Level 4 — Volume sebagian (T-03)
9. Akuarium berbentuk balok berukuran 60 cm × 30 cm × 40 cm. Akuarium diisi air 2/3 bagian.
   **Berapa volume air?** → 2/3 × 72.000 = 48.000 cm³ = 48 liter
10. Bak mandi berbentuk kubus dengan sisi 90 cm. Bak terisi 1/2 bagian.
    **Berapa liter air di bak?** → 1/2 × 729.000 = 364.500 cm³ = 364,5 liter

### Level 5 — Penalaran / tantangan
11. Berapa banyak kubus kecil bersisi 2 cm yang dapat mengisi kardus 10 × 8 × 6 cm? → 60 buah
12. Jika sisi kubus dijadikan 2 kali lipat, volumenya menjadi berapa kali lipat? → 8 kali

## 4. Soal Tes Awal (diagnostik)

| No | Mengukur | Soal |
|---|---|---|
| 1 | Unsur | Berapa banyak rusuk pada balok? |
| 2 | Konsep | Balok tersusun dari 3 lapis, tiap lapis 4 × 2 kubus satuan. Berapa kubus seluruhnya? |
| 3 | Rumus kubus | Kubus sisi 4 cm, volumenya? |
| 4 | Substitusi balok | p = 7, l = 3, t = 2. Volumenya? |
| 5 | Soal cerita | Kotak susu 6 cm × 4 cm × 10 cm. Volumenya? |

Aturan: benar ≥ 4 → mulai di Modul 5; benar 2–3 → Modul 3; benar ≤ 1 → Modul 1.

## 5. Daftar Tugas Konten

- [ ] Kembangkan bank soal menjadi ±60 soal (12 per level).
- [ ] Buat penjelasan "Jelaskan Kembali" (pilihan kalimat benar & pengecoh) untuk tiap level.
- [ ] Siapkan 3 petunjuk bertingkat untuk setiap soal.
- [ ] Siapkan daftar jawaban salah yang umum untuk diagnosis kesalahan.
- [ ] Validasi oleh ahli materi (dosen/guru matematika).

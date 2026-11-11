# 06 — Arsitektur Teknis

## 1. Keputusan Teknologi

Kebutuhan: satu kode untuk **web + Android**, bisa **luring**, ada **3D interaktif**, ringan di HP murah,
dan bisa dikerjakan oleh satu orang.

| Lapisan | Pilihan | Alasan |
|---|---|---|
| Bahasa | **TypeScript** | Mencegah banyak bug sejak awal; tetap JavaScript di browser |
| Kerangka UI | **React 18 + Vite** | Populer, banyak tutorial, build cepat |
| 3D | **Three.js** via **@react-three/fiber** + **@react-three/drei** | Kubus/balok, slider, jaring-jaring, kubus satuan |
| Gaya | **CSS global + variabel CSS** (`src/styles/tokens.css`, token dari `05-UI-UX.md`) | Sederhana, tanpa kerangka CSS besar |
| State | **Zustand** | Ringan untuk progres & pengaturan |
| Penyimpanan | **localStorage** via Zustand `persist` (kunci `ruangku:progres:v1`) | Luring, tanpa server |
| Luring web | **PWA** (`vite-plugin-pwa`) | Bisa di-"install" dari browser, jalan tanpa internet |
| Android | **Capacitor** | Membungkus build web yang sama menjadi APK/AAB |
| Pengujian | **Vitest** (engine + konsistensi bank soal); uji alur di browser dengan Playwright (opsional) | Logika soal teruji |
| Kualitas kode | `tsc --noEmit` (mode strict) | Konsisten |

**Alternatif yang dipertimbangkan:** Flutter (performa baik, tapi 3D lebih sulit dan web-nya lebih berat);
Unity (3D kuat, tapi APK besar dan berlebihan untuk kebutuhan ini). Pilihan React + Capacitor paling
seimbang untuk pengembang tunggal.

**Fallback performa:** bila fps < 25 selama 3 detik, tampilkan mode 2D isometrik (SVG) dengan
interaksi yang sama.

## 2. Arsitektur Tingkat Tinggi

```
┌──────────────────────── Aplikasi (React) ────────────────────────┐
│  Halaman (pages)   : Beranda, Modul 0–7, Lab 3D, Tantangan       │
│  Komponen (ui)     : Tombol, Slider, PapanAngka, Petunjuk, ...   │
│  Komponen 3D       : Balok3D, Kubus3D, JaringJaring, KubusSatuan │
│                      SimulasiAir                                  │
│  Mesin belajar     : penilaian langkah, diagnosis kesalahan,     │
│  (src/engine)        fading, pemilihan soal  ← logika murni, diuji│
│  Konten (src/content): soal & materi dalam JSON                  │
│  Penyimpanan       : progres lokal (localStorage/IndexedDB)       │
└──────────────────────────────────────────────────────────────────┘
          │ build web (dist/)
          ├──► PWA di hosting statis (GitHub Pages / Netlify / Vercel)
          └──► Capacitor ──► APK Android
```

Tidak ada server/backend di MVP. Tidak ada data pribadi yang dikirim ke mana pun.

## 3. Struktur Folder (rencana)

```
ruangku/
├─ CLAUDE.md
├─ README.md
├─ docs/                     ← dokumen perencanaan ini
├─ public/                   ← ikon, manifest PWA
├─ src/
│  ├─ main.tsx
│  ├─ App.tsx                ← routing
│  ├─ pages/                 ← Beranda, ModulUnsur, ModulKubusSatuan, ...
│  ├─ components/
│  │  ├─ ui/                 ← Tombol, Slider, PapanAngka, KartuPetunjuk
│  │  └─ three/              ← Balok3D, JaringJaring, KubusSatuan, SimulasiAir
│  ├─ engine/                ← logika murni (TANPA React)
│  │  ├─ volume.ts           ← hitung volume, volume sebagian, konversi satuan
│  │  ├─ penilaian.ts        ← cek jawaban per langkah
│  │  ├─ diagnosis.ts        ← jenis kesalahan → umpan balik
│  │  └─ fading.ts           ← aturan naik/turun level bantuan
│  ├─ content/
│  │  ├─ soal/*.json
│  │  └─ materi/*.json
│  ├─ store/                 ← zustand: progres, pengaturan
│  └─ styles/tokens.css      ← warna, ukuran huruf
├─ tests/                    ← unit & e2e
├─ android/                  ← dibuat otomatis oleh Capacitor
└─ package.json
```

## 4. Model Data

### Soal (`src/content/soal/*.json`)
```json
{
  "id": "balok-cerita-001",
  "modul": 5,
  "level": 2,
  "bangun": "balok",
  "jenis": "volume",
  "teks": [
    "Kotak pensil Rina berbentuk balok.",
    "Panjangnya 20 cm, lebarnya 6 cm, tingginya 4 cm.",
    "**Berapa volume kotak pensil itu?**"
  ],
  "ukuran": { "p": 20, "l": 6, "t": 4 },
  "pecahan": null,
  "satuan": "cm",
  "jawaban": { "nilai": 480, "satuan": "cm³" },
  "petunjuk": [
    "Ukuran apa saja yang diketahui?",
    "Ganti p, l, t pada rumus V = p × l × t.",
    "Contoh: balok 5 × 2 × 3 → 5 × 2 = 10, 10 × 3 = 30 cm³."
  ],
  "kesalahanUmum": [
    { "nilai": 368, "kode": "RUMUS_LUAS" },
    { "nilai": 30, "kode": "DIJUMLAH" }
  ]
}
```

### Progres (localStorage `ruangku:progres:v1`)
```json
{
  "versi": 1,
  "modulSelesai": [0, 1, 2],
  "levelBantuan": { "balok": 2, "kubus": 3 },
  "riwayat": [
    { "soalId": "balok-cerita-001", "benar": true, "petunjukDipakai": 1, "waktuDetik": 74 }
  ],
  "pengaturan": { "ukuranHuruf": "normal", "kurangiAnimasi": false, "suara": false }
}
```

## 5. Aturan Perhitungan

- Gunakan bilangan bulat untuk ukuran MVP; volume sebagian dihitung dengan pecahan
  (pembilang/penyebut) lalu dibandingkan secara eksak — **hindari galat floating point**
  (mis. `2/3 * 72000` dihitung sebagai `72000 * 2 / 3`).
- Satuan disimpan terpisah dari nilai; konversi lewat `engine/volume.ts`.

## 6. Build & Rilis

| Perintah | Fungsi |
|---|---|
| `npm run dev` | jalankan di browser lokal |
| `npm run test` | jalankan unit test |
| `npm run build` | build web ke `dist/` |
| `npx cap sync android` | salin build ke proyek Android |
| `npx cap open android` | buka di Android Studio → *Build APK* |

Rilis web: GitHub Pages/Netlify (gratis). Rilis Android: APK dibagikan langsung untuk uji coba;
Google Play (opsional) memerlukan akun pengembang dan kebijakan privasi untuk aplikasi anak
(*Designed for Families*).

## 7. Keamanan & Privasi
- Tanpa login, tanpa pelacakan pihak ketiga, tanpa iklan.
- Jika kelak menambah analitik untuk penelitian: data anonim, dengan izin sekolah & orang tua.

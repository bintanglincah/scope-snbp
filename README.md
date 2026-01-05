# 🔭 Scope 1.0 - Navigate Your Journey (Patch 8.4)

![Scope 1.0 Banner](logo.png) 
*(Opsional: Ganti logo.png dengan screenshot aplikasi jika ada)*

**Scope 1.0** adalah aplikasi web modern untuk memprediksi peluang kelolosan siswa SMA dalam seleksi SNBP (Seleksi Nasional Berdasarkan Prestasi) masuk Perguruan Tinggi Negeri (PTN) di Indonesia. 

Aplikasi ini menggunakan algoritma **Smart Adaptive Logic** untuk menghitung passing grade estimasi tahun 2026 berdasarkan tren data historis, keketatan rasio pendaftar, dan bobot prestasi siswa.

## ✨ Fitur Unggulan (Patch 8.4)

### 🧠 Core System
* **Smart Adaptive Logic:** Prediksi nilai tidak hanya berdasarkan angka mentah, tetapi memperhitungkan rasio keketatan (Pendaftar vs Daya Tampung) dan faktor "Hype" jurusan (Teknik/Medis).
* **Organic Ceiling Cap:** Pembatasan nilai maksimal yang realistis (randomized cap antara 94.70 - 96.00) agar prediksi tidak menyentuh angka yang tidak masuk akal (99.00).
* **Logic Split Calculation:** Pemisahan murni antara Nilai Akademik (Rapor) dan Bonus Prestasi (Sertifikat/Golden Ticket) untuk akurasi winrate.
* **JSON Database:** Database terpisah (`database.json`) yang ringan dan mudah dikelola, memuat ribuan data prodi PTN.

### 🎨 UI/UX (Midnight Eye-Care)
* **Glassmorphism Design:** Tampilan modern dengan panel kaca gelap (smoked glass) yang elegan.
* **Dark Mode Native:** Palet warna gradien *Deep Space* yang nyaman di mata untuk penggunaan lama.
* **Interactive Wizard:** Form input bertahap (Step-by-Step) dengan validasi nama dan nilai.
* **Personalized Greeting:** Sapaan interaktif di hasil akhir yang berubah sesuai persentase peluang siswa (Motivasi, Selamat, dll).

### 🔍 Smart Recommendation
* **3-Layer Priority:** Sistem rekomendasi cerdas yang memprioritaskan kampus berdasarkan kasta peluang:
    1.  **The Big 3** (UI, UGM, ITB)
    2.  **The Challengers** (UNDIP, ITS, UNAIR, UB, dll)
    3.  **Other PTNs**
* **Cluster Matching:** Hanya merekomendasikan jurusan yang sejenis/satu rumpun (Misal: Kedokteran hanya akan direkomendasikan Kedokteran di kampus lain).

## 🛠️ Teknologi yang Digunakan

* **HTML5** - Struktur semantik.
* **CSS3** - Styling, Flexbox, Grid, CSS Variables, & Animations.
* **Vanilla JavaScript (ES6+)** - Logika kalkulasi, DOM Manipulation, dan Fetch API.
* **JSON** - Penyimpanan data Passing Grade & Daya Tampung.

## 🚀 Cara Menjalankan (Local Development)

Karena aplikasi ini menggunakan `fetch API` untuk memanggil `database.json`, aplikasi ini **tidak bisa** dijalankan hanya dengan klik 2x file `index.html` (akan terkena blokir CORS policy browser).

Gunakan salah satu cara di bawah ini:

### Opsi 1: VS Code Live Server (Direkomendasikan)
1.  Install ekstensi **Live Server** di VS Code.
2.  Buka file `index.html`.
3.  Klik kanan -> **Open with Live Server**.

### Opsi 2: Python Simple Server
Jika kamu memiliki Python terinstall:
```bash
python -m http.server 8000
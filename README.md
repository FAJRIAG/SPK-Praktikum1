# Laporan Praktikum Sistem Pendukung Keputusan

**Dosen Pengajar:** Moh. Ali Fikri, M.Kom.  
**Program Studi:** Sistem Informasi  
**Institusi:** Politeknik Negeri Indramayu (POLINDRA)

---

## MODUL 1: Pengenalan Data dan Permasalahan Keputusan
### (Berbasis Web - Flask)

### A. Identitas Praktikum
*   **Mata Kuliah:** Sistem Pendukung Keputusan
*   **Bobot:** 3 SKS (1 SKS Teori, 2 SKS Praktikum)
*   **Pertemuan:** Praktikum 1
*   **Durasi:** 2 × 50 menit
*   **Platform:** Web (Flask – Python)
*   **Mode:** Individu

### B. Deskripsi Praktikum
Praktikum ini bertujuan untuk memberikan pemahaman awal mengenai peran data dan informasi dalam proses pengambilan keputusan. Fokus utama adalah membangun aplikasi web berbasis Flask yang mampu:
1.  Menerima data kriteria dan alternatif dalam format CSV.
2.  Menampilkan data dalam bentuk tabel yang informatif.
3.  Menyajikan ringkasan informasi seperti jumlah data dan kelengkapan data.

*Catatan: Pada tahap ini, fokus adalah transformasi data menjadi informasi dan perumusan masalah sebagai fondasi SPK, sebelum melangkah ke perhitungan metode (SMART, SAW, TOPSIS, AHP).*

### C. Capaian Pembelajaran
Setelah menyelesaikan praktikum ini, mahasiswa mampu:
*   Menjelaskan perbedaan data dan informasi dalam konteks SPK.
*   Merumuskan masalah keputusan (goal, alternatif, kriteria).
*   Menyiapkan dataset SPK dalam format CSV.
*   Mengembangkan aplikasi web sederhana menggunakan Flask.
*   Menyajikan data dalam bentuk tabel dan ringkasan informasi.

### D. Dasar Teori Singkat
Sistem Pendukung Keputusan (SPK) adalah sistem berbasis komputer yang membantu pengambil keputusan menghadapi masalah semi-terstruktur dan tidak terstruktur. Kualitas keputusan sangat ditentukan oleh kualitas data yang dikumpulkan dan diolah pada tahap awal ini.

### E. Studi Kasus
**Kasus:** Seleksi Penerima Beasiswa  
**Tujuan (Goal):** Menentukan mahasiswa yang paling layak menerima beasiswa.  
**Alternatif:** Mahasiswa A, Mahasiswa B, Mahasiswa C, Mahasiswa D, Mahasiswa E.  
**Kriteria:**
1.  IPK (Benefit)
2.  Penghasilan Orang Tua (Cost)
3.  Prestasi Akademik/Nonakademik (Benefit)
4.  Kehadiran (Benefit)
5.  Jumlah Tanggungan (Benefit)

### F. Struktur Proyek
```text
.
├── app.py              # Logika Utama Flask
├── requirements.txt    # Daftar Dependency
├── data/               # Folder Dataset CSV
│   ├── kriteria.csv
│   └── alternatif.csv
├── templates/          # Folder Template HTML
│   └── index.html
└── venv/               # Virtual Environment
```

### G. Penjelasan Kode Utama
1.  **Flask Initialization**: `app = Flask(__name__)` digunakan untuk memulai instance aplikasi web.
2.  **Pandas Integration**: Digunakan untuk membaca file CSV dan mengubahnya menjadi DataFrame yang mudah diolah.
3.  **Routing HTML**: `@app.route("/")` mengarahkan pengguna ke halaman utama yang menampilkan tabel data.
4.  **File Upload Logic**: Menggunakan `request.files` untuk menangani unggahan dataset baru dari user.
5.  **Data To HTML**: Fungsi `to_html(classes='table')` dari Pandas mempermudah konversi data menjadi tabel visual di browser.

---
*Dibuat untuk memenuhi Tugas Praktikum 1 - Sistem Pendukung Keputusan.*

# Proposal Tugas Akhir - Institut Teknologi Sepuluh Nopember (ITS)

> **Evaluasi Kinerja Algoritma Multi-Object Tracking (MOT) Berbasis YOLO11 untuk Analitik Perilaku Konsumen pada Lingkungan Ritel Komersial**

---

## 📌 Informasi Penelitian
- **Peneliti**: Danendra Galang Yugastama
- **Program Studi**: S1 Teknik Informatika / Teknologi Informasi / Rekayasa Sistem *(sesuaikan)*
- **Departemen**: Teknik Informatika / Teknologi Informasi *(sesuaikan)*
- **Fakultas**: FTEIC
- **Institusi**: Institut Teknologi Sepuluh Nopember (ITS), Surabaya

---

## 📖 Ringkasan Penelitian

Sistem analitik video ritel fisik (*brick-and-mortar*) berbasis visi komputer sering menghadapi kendala penurunan akurasi akibat fenomena oklusi visual dan kerumunan pengunjung yang padat. Oklusi berkepanjangan memicu terjadinya **fragmentasi identitas (*identity churn / switches*)**, di mana algoritma pelacak gagal mempertahankan identitas objek dan menetapkan ID baru secara keliru. Fenomena ini mendistorsi penghitungan metrik operasional bisnis, seperti durasi waktu singgah (*dwell time*) dan estimasi waktu antrean di kasir.

Penelitian ini mengadopsi paradigma **Tracking-by-Detection (TbD)** dengan mengunci model **YOLO11** sebagai variabel kontrol pada tahap deteksi, serta mengevaluasi empat algoritma pelacakan multi-objek kontemporer sebagai variabel independen:
1. **ByteTrack** (Asosiasi deteksi skor rendah & tinggi)
2. **BoT-SORT** (Kompensasi pergerakan kamera & filter Kalman teroptimasi)
3. **OC-SORT** (*Observation-Centric recovery* untuk mengatasi jeda oklusi)
4. **Deep OC-SORT** (Integrasi modul ekstraksi fitur kenampakan / Re-ID)

Tujuan utama penelitian ini adalah menguji secara empiris korelasi antara metrik evaluasi pelacakan akademik (**MOTA**, **IDF1**) dengan tingkat presisi metrik bisnis ritel di dunia nyata terhadap data acuan (*ground truth*) rekaman CCTV operasional toko.

---

## 📂 Struktur Repositori

```text
Proposal_Tugas_Akhir_ITS/
├── konten/
│   ├── 1-pendahuluan.tex        # Bab 1: Latar Belakang, Batasan, & Tujuan
│   ├── 2-tinjauan-pustaka.tex    # Bab 2: Landasan Teori, TbD, MOT, & Research Gap
│   ├── 3-metodologi.tex          # Bab 3: Diagram Alir, Dataset, Pipeline, & Metrik Evaluasi
│   ├── 4-lainnya.tex             # Bab Tambahan / Rencana Lanjutan
│   └── 5-jadwal-penelitian.tex   # Jadwal dan Rencana Kerja Penelitian
├── pustaka/
│   ├── pustaka.bib               # Basis data sitasi BibLaTeX / Biber
│   └── tanda-hubung.tex          # Aturan hyphenation bahasa Indonesia
├── gambar/                       # Diagram alir, arsitektur sistem, & aset visual
├── sampul/                       # Halaman judul dan format cover resmi ITS
├── main.tex                      # File master dokumen proposal LaTeX
├── .gitignore                    # Berkas filter file sementara (build artifacts)
└── README.md                     # Dokumentasi repositori
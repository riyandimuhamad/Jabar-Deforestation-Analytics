# 🌍 Sistem Pendukung Keputusan: Pemetaan Zona Rawan Bencana Hidrometeorologi di Jawa Barat

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Looker Studio](https://img.shields.io/badge/Looker_Studio-4285F4?style=for-the-badge&logo=google&logoColor=white)

## 📌 Deskripsi Proyek
Proyek ini merupakan implementasi *Business Intelligence* (BI) dan *Data Mining* untuk memetakan zona rawan bencana hidrometeorologi (banjir dan longsor) di Jawa Barat. Dengan mengeksploitasi korelasi antara data curah hujan, tingkat deforestasi (alih fungsi lahan), dan riwayat kejadian bencana, sistem ini mengelompokkan wilayah ke dalam tiga tingkat risiko: **Aman (Hijau)**, **Waspada (Kuning)**, dan **Bahaya (Merah)**.

Proyek ini dibangun sebagai *Minimum Viable Product* (MVP) untuk sistem *Early Warning System* (EWS) berbasis data.

## 🎯 Objektif & Key Insights
* **Clustering Otomatis:** Menggunakan algoritma **K-Means** untuk mengelompokkan wilayah berdasarkan tingkat risiko secara objektif, menghilangkan bias manual.
* **Intelligent Labeling:** Sistem secara matematis mendeteksi dan melabeli cluster "Bahaya" berdasarkan kalkulasi *risk score* tertinggi.
* **Case Study Highlight - Bandung Barat:** Melalui analisis dashboard, ditemukan anomali kerawanan longsor tingkat tinggi di kawasan Bandung Barat yang berkorelasi kuat dengan masifnya alih fungsi lahan di area dengan kemiringan lereng ekstrem, meskipun curah hujan tidak berada di puncaknya.

## 🏗️ Arsitektur & Workflow (MVP)
Saat ini, proyek berjalan dengan arsitektur berikut:
1. **Data Processing & ML (Python):** * Pre-processing data (Standardization/Min-Max Scaling).
   * Menjalankan K-Means Clustering (`k=3`).
   * *Export* hasil clustering yang sudah dilabeli ke dalam format `.csv` atau langsung ke Google Sheets.
2. **Data Visualization (Looker Studio):**
   * Mengambil data olahan untuk divisualisasikan menjadi *Interactive Dashboard*.
   * Menampilkan *Geo-mapping* persebaran zona rawan dan *Scatter Plot* korelasi hujan vs. deforestasi.

## 🚀 Future Roadmap (Pengembangan Lanjutan)
Proyek ini dirancang untuk di-scale menjadi EWS yang sepenuhnya otomatis dengan arsitektur masa depan:
- [ ] **n8n Automation Pipeline:** Pembuatan workflow otomatis untuk men-scrape data cuaca harian dari BMKG/OpenWeatherMap dan mengupdate database/Google Sheets secara *real-time* tanpa intervensi manual.
- [ ] **Agentic AI (Disaster Advisor):** Integrasi AI Agent yang memantau *database* secara proaktif. Jika terdeteksi anomali kritis (Curah Hujan Tinggi + Deforestasi Tinggi di satu titik), AI akan menggenerasi dan mengirimkan pesan peringatan dini (EWS) beserta narasi rekomendasi evakuasi ke WhatsApp pemangku kebijakan (seperti BPBD).

## 💻 Cara Menjalankan Script Python Lokal
1. Clone repositori ini:
   ```bash
   git clone (https://github.com/riyandimuhamad/Jabar-Deforestation-Analytics)

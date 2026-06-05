# JCBDAAH-004_Delta

# Final Project: Telco Customer Churn Analysis & Financial Optimization
### **Team DELTA**
* Yoseph Cristaday Limbong
* Akhdan Zacky Bahreisy
* Ikhtiari Zulmiati Arifin Pua Geno
---

## 📌 1. Project Overview
Repository ini berisi proyek akhir dari **Team DELTA** yang berfokus pada analisis **Telco Customer Churn**. Melalui pendekatan berbasis data (*data-driven approach*), proyek ini tidak hanya memetakan karakteristik pelanggan yang berhenti berlangganan (*churn*), melainkan juga mengkalkulasi dampak kerugian finansial riil secara historis serta merancang **Early Warning System (EWS)** dan strategi retensi taktis berbasis ROI untuk meminimalkan *revenue leakage* (kebocoran pendapatan) di masa mendatang.

---

## 🎯 2. Business & Project Objectives
### **Problem Statement**
* **Kebocoran Pendapatan Masif:** Perusahaan mendeteksi adanya kehilangan pendapatan bulanan (*Monthly Charges*) yang signifikan akibat tingginya tingkat *churn* pada kelompok pelanggan premium.
* **Strategi Pemasaran Tidak Efektif:** Program penawaran (*Offers*) yang ada saat ini berjalan kurang optimal dan berpotensi salah sasaran, terutama pada kluster pengguna layanan utama seperti *Fiber Optic*.

### **Goals & Analytical Approach**
1. **Financial Impact Mapping:** Menghitung total kebocoran pendapatan bulanan dan akumulasi kerugian historis riil berdasarkan variabel `MonthlyCharges` dan `TotalCharges`.
2. **Leakage Point Identification:** Mengidentifikasi infrastruktur jaringan dan fasilitas tambahan (*streaming services*, *security features*) yang paling rentan terhadap risiko *churn*.
3. **Offer Effectiveness Evaluation:** Mengevaluasi kinerja setiap program *Offer* (A-E) guna merestrukturisasi kebijakan pemasaran.
4. **Early Warning System (EWS):** Membangun penyaringan data untuk mengisolasi kelompok pelanggan aktif yang berada di zona bahaya (*Swing Voters*).
5. **Tactical Retention Guidance:** Menyusun rekomendasi alokasi anggaran biaya penyelamatan (*Customer Retention Cost* / CRC) dengan tingkat pengembalian investasi (ROI) yang terukur.

---

## 📊 3. Key Insights & Findings

### **1. Dampak Finansial & Karakteristik Churn**
* **Kebocoran Pendapatan Bulanan:** Kerugian akibat pelanggan *churn* menembus **USD 139,130.85 per bulan**.
* **Segmentasi Premium:** Pelanggan yang kabur memiliki rata-rata tagihan bulanan sebesar **USD 74.44**, jauh melampaui pelanggan aktif yang hanya **USD 61.27**. Ini membuktikan hilangnya segmen *high-spending*.
* **Akumulasi Kerugian Historis:** Akumulasi total kerugian riil dari pelanggan yang terlanjur *churn* menyentuh angka masif sebesar **USD 2,862,926.90**.

### **2. Titik Kebocoran Jaringan & Layanan**
* **Infrastruktur Utama:** Jaringan **Fiber Optic** menyumbang kontribusi mutlak sebesar **86.74%** (sekitar **USD 2.48 Juta**) dari total pendapatan yang hilang.
* **Fitur Tambahan:** Mayoritas pelanggan *churn* adalah pengguna aktif fitur hiburan seperti *Streaming Movies* (**70.01%**) dan *Streaming TV* (**69.81%**).

### **3. Efektivitas Program Pemasaran**
* **Kegagalan Terbesar:** **Offer E** mencatat tingkat kegagalan tertinggi dengan *churn rate* mencapai **52.9%**.
* **Keberhasilan Tertinggi:** **Offer A** menjadi program paling sukses dalam mengikat pelanggan dengan tingkat *churn* terendah, yaitu hanya **6.7%**.

### **4. Prioritas Utama Early Warning System (Swing Voters)**
Melalui proses integrasi fitur, kami memetakan kelompok pelanggan bernilai tinggi yang rentan bergeser dengan kriteria:
* **Status:** Masih Aktif
* **Segmen Value:** High/Mid-Value
* **Infrastruktur:** Fiber Optic
* **Satisfaction Score:** Tepat di angka **3** (skala 1-5, mengindikasikan posisi netral/mudah goyah).

> ⚠️ **Total Populasi Kritis:** **811 User** dengan nilai potensi kerugian jangka panjang (CLTV) sebesar **USD 3,764,805.00** (hampir USD 3.76 Juta).

---

## 🚀 4. Rekomendasi Taktis (Panduan Operasional)

### **1. Eksekusi Program Retensi Berbasis Skenario**
Tim *Customer Retention* disarankan membidik **Skenario Moderat (Target Sukses 30%)** sebagai KPI awal. Dengan menyelamatkan **243 pelanggan** dari 811 *user* kritis tersebut, perusahaan secara langsung memotong potensi kerugian jangka panjang sebesar **USD 1,129,441.50** (Lebih dari USD 1.1 Juta).

### **2. Alokasi Anggaran Taktis di Bawah CRC Ceiling**
* **Batas Maksimal Anggaran (CRC Ceiling):** Maksimal **USD 415 per user** (Total pagu kluster: USD 336,565.00).
* **Rekomendasi Alokasi (USD 200 per user):**
  * **Voucher Kompensasi & Audit Jaringan (USD 150/user):** Pengiriman teknisi proaktif untuk jalur *Fiber Optic* + potongan tagihan USD 15 selama 10 bulan.
  * **Subsidi Free Akses Fitur Keamanan (USD 50/user):** Gratis layanan *Tech Support* atau *Online Security* selama 1 tahun (fitur ini terbukti meningkatkan loyalitas).
* **Finansial Buffer:** Menyisakan cadangan aman sebesar **USD 215 per user** untuk menjaga efisiensi anggaran (*High ROI*).

### **3. Restrukturisasi Kebijakan Produk**
* **Hentikan Offer E** dan lakukan audit fundamental terhadap skema penawarannya yang memicu *churn*.
* **Replikasi Struktur Offer A** untuk diimplementasikan pada perluasan segmentasi pasar lainnya.

---

## 🛠️ 5. Struktur Notebook & Workflow Analisis
Notebook ini disusun secara modular berdasarkan standar industri untuk mempermudah proses penilaian oleh mentor:
* **`Section 0. Import Library`**: Memuat seluruh *environment dependencies* (Pandas, NumPy, Matplotlib, Seaborn).
* **`Section 1. Business Understanding`**: Penentuan matriks bisnis, objektif operasional, dan indikator keuangan.
* **`Section 2. Data Understanding`**: Eksplorasi format dataset, dimensi data (7.043 baris), tipe data, dan pemeriksaan awal *missing values*.
* **`Section 3. Data Cleaning`**: Penangan data kosong, standardisasi inkonsistensi teks, dan eliminasi data duplikat.
* **`Section 4. Feature Generation`**: Pembentukan fitur-fitur turunan krusial (pengelompokan *Tenure Group*, penentuan indikator *Customer Status*, dan ekstraksi logika *Total Services*).
* **`Section 5. Data Analysis`**: Visualisasi distribusi, *cross-tabulation*, korelasi variabel terhadap *Satisfaction Score*, dan penemuan titik bocor keuangan.

---

## 📈 6. Business Impact
Implementasi dari hasil analisis data dan rekomendasi taktis Team DELTA ini diproyeksikan akan memberikan dampak langsung terhadap kesehatan finansial perusahaan sebagai berikut:

* **Penyelamatan Pendapatan (Revenue Recovery):** Melalui penargetan terfokus pada 811 pelanggan kritis (*Swing Voters*) menggunakan Skenario Moderat (Target Sukses 30%), perusahaan berpotensi mengamankan nilai umur pelanggan (*Customer Lifetime Value* / CLTV) sebesar **USD 1,129,441.50** yang sebelumnya terancam hilang.
* **Efisiensi Anggaran Retensi (CRC Optimization):** Dengan menetapkan biaya alokasi penyelamatan sebesar **USD 200 per user** (di bawah batas maksimal *CRC Ceiling* sebesar USD 415), perusahaan berhasil menghemat anggaran operasional kluster sebesar **USD 174,365.00** (*cost saving*) sekaligus menciptakan dana cadangan yang aman (*financial buffer*).
* **Mitigasi Kerugian Sistemik (Systemic Loss Mitigation):** Penghentian program **Offer E** (yang memiliki kegagalan/churn rate hingga 52.9%) dan replikasi pola **Offer A** (churn rate hanya 6.7%) akan menghentikan tren pembengkakan kerugian historis (*Total Charges*) yang secara akumulatif telah merugikan perusahaan sebesar **USD 2,862,926.90**.
* **Peningkatan Indeks Kepuasan & Retensi Jangka Panjang:** Intervensi proaktif berupa audit jaringan *Fiber Optic* serta pembagian fitur keamanan gratis tepat sasaran diproyeksikan mampu mendongkrak rata-rata *Satisfaction Score* kelompok kritis dari nilai netral (3) ke arah zona aman (4-5), mengunci loyalitas segmen *high-spending* untuk siklus bisnis berikutnya.

---
✨ *Project ini disusun dengan komitmen penuh untuk memberikan dampak bisnis nyata bagi pertumbuhan berkelanjutan perusahaan.* **Team DELTA - 2026**

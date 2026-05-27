# Dokumen Spesifikasi Desain (Desain.md)
**Nama Sistem**: Margin.alia - School-Notebook Design System
**Versi**: V. Alpha (Spring 26)
**Deskripsi**: Sistem desain bertema buku catatan sekolah dengan estetika kertas bergaris (*ruled cream paper*), tinta biru dongker (*ink-navy writing*), dan garis tepi merah (*red margin*). Dirancang untuk antarmuka yang ramah, organik, dan berfokus pada produktivitas akademis.

---

## 1. Sistem Warna (Color Palette)
Desain ini menggunakan warna-warna alat tulis klasik untuk menciptakan nuansa organik dan analog.

**Warna Dasar & Teks (Base & Text)**
* **Paper**: Latar belakang utama (krem/kuning pucat) yang menyerupai kertas buku tulis.
* **Ink**: Biru dongker gelap (Navy), digunakan untuk warna teks utama, garis *border*, dan *outline* elemen.

**Warna Aksen & Indikator (Accent & Stationery)**
* **Red**: Merah terang, digunakan untuk garis margin vertikal di sisi kiri halaman, tombol aksi utama (*Primary Button*), dan elemen peringatan/penting (seperti nilai "A+").
* **Blue**: Biru medium, digunakan untuk tombol aksi sekunder dan indikator progres.
* **Marker**: Kuning terang, digunakan untuk elemen *sticky notes*, *highlight* teks, dan label penanda.
* **Mint, Eraser (Pink), Graphite (Abu-abu)**: Warna-warna pastel pendukung untuk label status, *tags* (misal: *Done*, *Past due*), dan *badge* kategori.

---

## 2. Tipografi (Typography)
Sistem ini menggunakan tiga jenis *font* ("Three Voices") untuk memisahkan konteks antara elemen antarmuka, konten tekstual, dan elemen organik/tulisan tangan.

* **Caveat (Display)**
    * *Gaya*: Menyerupai tulisan tangan (*handwritten*).
    * *Penggunaan*: *Headlines*, elemen dekoratif, tanda tangan, dan teks di dalam *sticky notes*.
* **Fraunces (Schoolbook)**
    * *Gaya*: Serif klasik.
    * *Penggunaan*: Teks paragraf utama (*Body*), judul konten, dan salinan editorial. Memberikan kesan akademis dan mudah dibaca.
* **Inter (Interface)**
    * *Gaya*: Sans-serif modern dan bersih.
    * *Penggunaan*: Label antarmuka, tombol, *captions*, input form, dan data metrik (seperti persentase progres).

---

## 3. Komponen Antarmuka (UI Components)

**Bentuk dan Karakteristik Visual**
* **Border & Outline**: Komponen utama seperti *card*, *input field*, dan tombol memiliki *border* solid berwarna **Ink** (biru dongker) dengan ketebalan medium, memberikan kesan seolah-olah digambar dengan pena.
* **Shadows**: Elemen melayang seperti *sticky notes* memiliki bayangan (*drop shadow*) halus namun tegas untuk memisahkan dari latar belakang bergaris.

**Tombol (Buttons)**
* **Primary (Save/Action)**: Latar belakang **Red**, teks putih (Inter).
* **Secondary (Done/Shared)**: Latar belakang warna pastel (Mint/Blue) dengan *outline* **Ink** dan teks **Ink**.
* **Ghost/Outlined (Reset/Hint)**: Latar belakang transparan (putih/krem) dengan *outline* **Ink**.

**Sticky Notes & Label**
* Menggunakan kotak berwarna **Marker** (kuning) yang diputar sedikit (*tilted*) agar terlihat tidak kaku, sering kali dilengkapi dengan grafis selotip putih semi-transparan di bagian atasnya. Teks di dalamnya menggunakan *font* **Caveat**.

---

## 4. Visualisasi Data & Indikator
* **Progress Bar**: Menggunakan garis sederhana bergaya kapsul dengan warna isi sesuai status (misalnya merah untuk *low progress*, hijau/kuning untuk status lainnya), dibingkai dengan *outline* **Ink**.

---

## 5. Layout & Struktur (Page Anatomy)
* **Background Pattern**: Seluruh halaman dirender di atas latar belakang dengan garis-garis horizontal tipis berwarna abu-abu/biru pudar (menyerupai *ruled paper*).
* **The Red Margin**: Terdapat satu garis vertikal berwarna merah tebal di sisi kiri layar yang memanjang dari atas ke bawah, merepresentasikan batas margin buku tulis. Konten antarmuka umumnya diletakkan di sebelah kanan garis margin ini, sementara elemen dekoratif atau *bullet point* bisa berada di sebelah kiri margin.
* **Cards (Course/Plan)**: Konten dikelompokkan dalam kotak-kotak bersudut sedikit membulat, dengan latar belakang putih solid untuk menutup garis-garis *background* di belakangnya, memastikan keterbacaan teks (Fraunces/Inter) tetap optimal.

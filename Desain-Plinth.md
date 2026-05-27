# Dokumen Spesifikasi Desain (Desain.md)
**Nama Sistem**: Plinth
**Versi**: V1.0
**Tema**: Light, Tactile, Outlined (Neo-Brutalism Minimalis)
**Deskripsi**: Sebuah bahasa desain yang bersih dan minimalis, dibangun di sekitar primitif *stacked offset* (bayangan padat yang bertumpuk). Fokus utama sistem ini adalah memberikan sensasi taktil (*tactile*) melalui mekanisme interaksi "tekan" (*press*) yang memuaskan pada setiap elemen antarmuka.

---

## 1. Sistem Warna (Color Palette)
Menggunakan palet warna terang yang sangat dibatasi, dengan kontras garis luar (*outline*) yang tegas.

**Warna Dasar & Permukaan (Base & Surface)**
* **Canvas**: `#FFFFFF` (Putih murni) - Digunakan sebagai latar belakang utama halaman (*workspace*).
* **Paper**: `#FAF7F2` (Putih tulang/krem sangat pucat) - Digunakan untuk latar belakang *card* sekunder atau area form.

**Garis & Teks (Borders & Text)**
* **Ink**: `#111111` (Hitam pekat) - Warna paling krusial. Digunakan untuk semua teks, ikon, dan *border* garis luar setebal `2px` pada semua komponen.

**Aksen (Accent)**
* **Coral**: `#FD9B9B` (Merah muda/Salmon terang) - Warna aksen utama untuk tombol aksi (*Primary Button*), *checkbox* aktif, dan *highlight*.
* **Soft**: `#FFE2DB` (Merah muda sangat pucat) - Digunakan untuk status *hover*, latar belakang komponen pasif, atau panel sekunder.

---

## 2. Tipografi (Typography)
Sistem ini hanya menggunakan dua keluarga *font* untuk menjaga kebersihan visual.

* **Display (Teks Utama/Judul)**: `Space Grotesk`
    * *Penggunaan*: Judul halaman, *header* panel, dan elemen tipografi yang membutuhkan penekanan (*display moments*).
* **Body (Teks UI/Paragraf)**: `Inter`
    * *Penggunaan*: Teks paragraf, label form, isi tombol, dan data tabular.

---

## 3. Komponen Antarmuka & Mekanik Taktil (UI & The "Press" Mechanic)
Ini adalah inti dari desain Plinth. Setiap permukaan interaktif bertumpu pada dasar *Ink* (hitam) dan bereaksi terhadap sentuhan.

**Geometri Dasar**
* **Border/Outline**: Semua *card*, tombol, form input, dan *checkbox* WAJIB memiliki *border* solid berwarna *Ink* (`#111111`) dengan ketebalan presisi `2px`.
* **Radius**: Semua sudut komponen melengkung dengan radius `12px` (tidak ada sudut tajam).

**Mekanisme Interaksi "Press States"**
Setiap elemen yang bisa di-klik (tombol, *card* interaktif, *tab*) menggunakan sistem bayangan padat (*solid drop-shadow* berwarna *Ink*) yang mensimulasikan ruang tiga dimensi:
1. **REST (Diam)**: Komponen memiliki bayangan padat dengan jarak (*offset*) `4px` ke arah bawah-kanan.
2. **HOVER (Disorot)**: Saat kursor berada di atas komponen, komponen seolah terangkat naik. Jarak bayangan bertambah menjadi `6px`.
3. **PRESS (Ditekan)**: Saat di-klik, komponen langsung turun menempel ke dasar. Jarak bayangan menjadi `0px` (*snaps to 0*).

---

## 4. Elemen Spesifik (Forms & Checklists)
* **Input Fields**: Latar belakang putih (*Canvas*) dengan *border* `2px Ink`. Saat fokus, bisa ditambahkan *offset shadow* ringan atau *border* yang lebih tegas.
* **Checkbox**: Kotak kecil dengan radius yang disesuaikan. Saat aktif (dicentang), latar belakang berubah menjadi *Coral* dengan ikon centang hitam (*Ink*), tetap mempertahankan *border* `2px` dan mekanisme *Press* yang sama.
* **Tabs**: Berbagi garis batas (*outlined base*) yang sama. Tab yang aktif biasanya memiliki latar belakang *Ink* dengan teks *Canvas* (putih), sedangkan tab tidak aktif memiliki latar belakang transparan/putih.

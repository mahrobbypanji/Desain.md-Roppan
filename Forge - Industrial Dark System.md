# Dokumen Spesifikasi Desain (Desain.md)
**Nama Sistem**: Forge - Industrial Dark System
**Versi**: V01
**Deskripsi**: Sebuah sistem desain *industrial-grade dark* yang dirancang untuk permukaan teknis yang padat (*dense technical surfaces*), seperti *dashboard* operasional, konsol, dan portal *developer*.

---

## 1. Sistem Warna (Color Palette)
Desain ini menggunakan skema warna gelap dengan tingkat kontras yang tinggi pada bagian aksen untuk memandu interaksi pengguna.

**Aksen & Interaksi (Accent)**
* **Ember (Primary Accent)**: `#F65A1A` 
    * *Penggunaan*: Tombol utama (Active/Hover), indikator grafik, *toggle switches* aktif, notifikasi, dan *border highlight*.

**Permukaan & Latar Belakang (Surfaces)**
* **Graphite/Surface**: `#131315`
    * *Penggunaan*: Warna latar belakang utama aplikasi dan *base canvas*.
* **Ink / Darker Surfaces**: Variasi gelap dari *Graphite* untuk membedakan lapisan panel atau *card*.

**Garis & Pembatas (Borders)**
* **Filament**: Border dengan ketebalan `1px`.
    * *Penggunaan*: Memisahkan antar komponen, garis *grid*, dan *outline* pada panel *card*. Warna border menggunakan abu-abu gelap dengan opasitas rendah agar tidak mendominasi.

---

## 2. Tipografi (Typography)
Menggunakan kombinasi tiga jenis *font* untuk membedakan hierarki informasi antara *display*, teks reguler, dan data teknis.

* **Display & Headings**: `Space Grotesk`
    * *Weight*: 700 (Bold)
    * *Penggunaan*: Judul halaman, angka metrik utama berukuran besar, dan label *call-to-action* tebal.
* **Body & UI Text**: `Inter`
    * *Weight*: 400 (Regular) / 500 (Medium)
    * *Penggunaan*: Paragraf deskripsi, label *button* sekunder, navigasi, dan teks *interface* umum.
* **Technical & Data**: `JetBrains Mono`
    * *Ukuran Standar*: `12px`
    * *Penggunaan*: Angka metrik spesifik, kode, *log*, ID komponen, dan data numerik pada tabel atau grafik.

---

## 3. Komponen Antarmuka (UI Components)

**Bentuk dan Sudut (Radius)**
* **Radius Standar**: `4px`
    * Semua elemen seperti tombol, *card*, *input field*, dan *progress bar* memiliki sudut yang sedikit membulat (hampir kotak tajam) untuk mempertahankan kesan *industrial* dan *technical*.

**Tombol (Buttons)**
* **Primary Button**: Latar belakang `#F65A1A`, teks putih/hitam (tergantung kontras), radius `4px`.
* **Secondary/Ghost Button**: Latar belakang transparan atau *dark gray*, teks putih/abu-abu, menggunakan *border* `1px` berwarna abu-abu terang atau `#F65A1A` jika sedang *hover*.

**Kontrol Form (Form Controls)**
* **Toggle Switch**: Saat aktif (ON) menggunakan warna `#F65A1A`, saat non-aktif (OFF) menggunakan warna latar belakang abu-abu gelap.
* **Checkbox**: Kotak berukuran kecil (radius 2-4px), saat dicentang (*checked*) latar belakang berubah menjadi `#F65A1A` dengan ikon centang (*tick*) berwarna kontras (putih/gelap).
* **Input Field**: Latar belakang *input* menggunakan warna *surface* yang lebih terang dari latar belakang utama, dengan *border* `1px` *Filament*.

---

## 4. Visualisasi Data (Data Visualization)
* **Grafik Batang (Bar Charts)**: Menggunakan balok-balok vertikal berwarna abu-abu redup untuk data historis/pasif, dan satu balok berwarna `#F65A1A` terang untuk menyorot data saat ini (*current/active data*).
* **Metrik Angka**: Angka utama menggunakan *font* yang sangat besar, didampingi dengan teks kecil di sebelahnya (misal: persentase kenaikan/penurunan berwarna hijau atau abu-abu) untuk memberikan konteks.

---

## 5. Ikonografi (Iconography)
* **Library Utama**: `Tabler Icons` (Versi 1.6)
* **Gaya**: *Outlined* (garis luar), garis tipis, bersih, dan konsisten.
* **Penggunaan**: Ikon indikator status, menu navigasi, dan ikon aksi di dalam tombol.

---

## 6. Layout & Struktur
* **Grid System**: Menggunakan sistem *hairline grids* yang terlihat samar untuk memisahkan setiap blok informasi.
* **Card-based UI**: Data dan metrik dikelompokkan dalam kotak-kotak (*panels*) terpisah dengan *border* `1px` untuk menyusun informasi padat agar tetap rapi dan terstruktur.

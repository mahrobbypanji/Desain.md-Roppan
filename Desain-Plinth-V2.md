---
version: 1.0
name: Plinth
description: A quiet, light system with a satisfying press. Built around a stacked offset primitive for tactile neo-brutalism.
theme: light
colors:
  canvas: "#FFFFFF"
  paper: "#FAF7F2"
  ink: "#111111"
  coral: "#FD9B9B"
  soft: "#FFE2DB"
  text-muted: "#555555"
typography:
  display:
    fontFamily: "'Space Grotesk', sans-serif"
    fontSize: "2.5rem"
    fontWeight: 700
    letterSpacing: "-0.02em"
    lineHeight: 1.1
  body:
    fontFamily: "'Inter', sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    letterSpacing: "0"
    lineHeight: 1.5
  label:
    fontFamily: "'Inter', sans-serif"
    fontSize: "0.875rem"
    fontWeight: 500
    letterSpacing: "0.01em"
    lineHeight: 1.4
rounded:
  base: "12px"
  checkbox: "6px"
spacing:
  sm: "8px"
  md: "16px"
  lg: "24px"
  xl: "32px"
border:
  width: "2px"
  color: "{colors.ink}"
  style: "solid"
elevation:
  rest: "4px 4px 0px {colors.ink}"
  hover: "6px 6px 0px {colors.ink}"
  press: "0px 0px 0px {colors.ink}"
motion:
  duration: "100ms"
  ease: "ease-out"
components:
  card:
    backgroundColor: "{colors.canvas}"
    border: "2px solid {colors.ink}"
    rounded: "{rounded.base}"
    padding: "24px"
    shadow: "{elevation.rest}"
  button-primary:
    backgroundColor: "{colors.coral}"
    textColor: "{colors.ink}"
    border: "2px solid {colors.ink}"
    rounded: "{rounded.base}"
    padding: "12px 24px"
    shadow: "{elevation.rest}"
    typography: "{typography.label}"
  button-secondary:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    border: "2px solid {colors.ink}"
    rounded: "{rounded.base}"
    padding: "12px 24px"
    shadow: "{elevation.rest}"
  input:
    backgroundColor: "{colors.canvas}"
    border: "2px solid {colors.ink}"
    rounded: "{rounded.base}"
    padding: "12px 16px"
---

# Dokumen Spesifikasi Desain (Desain.md)
**Nama Sistem**: Plinth
**Versi**: V1.0
**Tema**: Light, Tactile, Outlined (Neo-Brutalism Minimalis)
**Deskripsi**: Sebuah bahasa desain yang bersih dan minimalis, dibangun di sekitar primitif *stacked offset* (bayangan padat yang bertumpuk). Fokus utama sistem ini adalah memberikan sensasi taktil (*tactile*) melalui mekanisme interaksi "tekan" (*press*).

## 1. Sistem Warna (Color Palette)
* **Canvas (`#FFFFFF`)**: Warna dasar latar belakang (*workspace*).
* **Paper (`#FAF7F2`)**: Latar komponen interaktif sekunder (form abu-abu hangat).
* **Ink (`#111111`)**: Warna paling krusial untuk struktur; digunakan untuk teks, *border*, dan elemen *shadow* padat (*offset shadow*).
* **Coral (`#FD9B9B`)**: Aksen eksklusif untuk tindakan primer dan *checkbox* yang tercentang.

## 2. Tipografi (Typography)
* **Space Grotesk**: Digunakan pada *heading* panel untuk memberikan sentuhan kontemporer.
* **Inter**: Tipografi paragraf, UI kontrol, dan komponen tab.

## 3. Komponen Antarmuka & Mekanik Taktil (The "Press" Mechanic)
Seluruh identitas Plinth dibentuk oleh kombinasi batas tepi dan bayangan padat, bukan gradasi warna.
* **Struktur Wajib**: Seluruh komponen panel, tombol, form, dan *checkbox* WAJIB memiliki `border` 2px solid berwarna `ink` (`#111111`) dan sudut membulat (*border-radius*) `12px` (atau `6px` untuk elemen kecil).
* **Press States (Interaksi)**:
  * **REST (Diam)**: Komponen memiliki bayangan padat `box-shadow` dengan *offset* bawah-kanan sebesar `4px`.
  * **HOVER (Disorot)**: *Offset* bayangan bertambah memanjang ke `6px`, menyimulasikan elemen yang terangkat (*lifts to 6px*). Modifikasi posisi komponen (`translate`) sejauh `-2px` ke kiri dan atas.
  * **PRESS (Ditekan)**: *Offset* bayangan menjadi `0px`, menyimulasikan elemen yang tertekan sempurna dan merapat ke lantai halaman (*snaps to 0*). Modifikasi posisi komponen kembali sejauh `+6px` ke kanan dan bawah untuk menutupi jejak *shadow*.

## 4. Aturan Desain (Do's and Don'ts)
* **DO**: Terapkan mekanisme *press states* (Rest -> Hover -> Press) secara konsisten pada *semua* permukaan yang interaktif (termasuk label Tab dan item list).
* **DON'T**: Jangan pernah menggunakan bayangan *blur*. Seluruh nilai *blur-radius* pada *box-shadow* harus bernilai `0px`.

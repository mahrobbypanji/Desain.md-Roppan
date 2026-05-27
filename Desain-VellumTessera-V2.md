---
version: 1.0 (Alpha)
name: Vellum Tessera
description: A warm light product system blending hand-pressed tessellated cream surfaces with a single teal-to-iris-to-blue gradient glow.
theme: light
colors:
  vellum: "#F5F2EB"
  ivory: "#FDFAF5"
  ink: "#1C1C28"
  sage: "#B5C7B8"
  gradient-teal: "#55B97C"
  gradient-iris: "#7B5AF4"
  gradient-glow: "#2F7CF8"
  on-vellum: "#2D2D3A"
  on-ivory: "#2D2D3A"
  on-ink: "#FFFFFF"
typography:
  display:
    fontFamily: "'Fraunces', serif"
    fontSize: "3.5rem"
    fontWeight: 500
    letterSpacing: "-0.02em"
    lineHeight: 1.1
  headline:
    fontFamily: "'Fraunces', serif"
    fontSize: "2rem"
    fontWeight: 500
    letterSpacing: "-0.01em"
    lineHeight: 1.2
  body-ui:
    fontFamily: "'Inter', sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    letterSpacing: "0"
    lineHeight: 1.5
  label-caps:
    fontFamily: "'Inter', sans-serif"
    fontSize: "0.75rem"
    fontWeight: 600
    letterSpacing: "0.1em"
    lineHeight: 1.2
    textTransform: "uppercase"
rounded:
  sm: "8px"
  md: "12px"
  lg: "18px"
  xl: "24px"
  xxl: "32px"
  pill: "999px"
spacing:
  sm: "12px"
  md: "24px"
  lg: "40px"
  xl: "64px"
elevation:
  soft-ambient: "0 8px 24px rgba(181, 199, 184, 0.15), 0 2px 8px rgba(181, 199, 184, 0.05)"
  glow-hover: "0 12px 32px rgba(123, 90, 244, 0.25)"
components:
  button-primary:
    background: "linear-gradient(135deg, {colors.gradient-teal}, {colors.gradient-iris}, {colors.gradient-glow})"
    textColor: "#FFFFFF"
    rounded: "{rounded.pill}"
    padding: "12px 24px"
    border: "none"
    typography: "{typography.body-ui}"
  card-ivory:
    backgroundColor: "{colors.ivory}"
    rounded: "{rounded.xxl}"
    padding: "32px"
    shadow: "{elevation.soft-ambient}"
    border: "1px solid rgba(255,255,255,0.5)"
  dark-hero-panel:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.on-ink}"
    rounded: "{rounded.xxl}"
    padding: "48px"
---

# Dokumen Spesifikasi Desain (Desain.md)
**Nama Sistem**: Vellum Tessera
**Versi**: V1.0 (Alpha)
**Deskripsi**: Sebuah sistem desain produk bernuansa cahaya hangat (*warm light*) yang menggabungkan warna dasar krem (*cream*) dengan elemen geometris yang tenang. Desain ini mengedepankan estetika *editorial* dengan antarmuka yang terasa organik, elegan, dan lembut.

## 1. Sistem Warna (Color Palette)
Sistem ini menghindari warna putih murni dan memilih warna berbasis krem (*earthy*).
* **Vellum (`#F5F2EB`)**: Latar belakang utama *website*. Memberikan kesan hangat.
* **Ivory (`#FDFAF5`)**: Warna untuk permukaan komponen (seperti *Card*), memberikan peninggian visual secara natural di atas kanvas Vellum.
* **Ink (`#1C1C28`)**: Warna untuk tipografi utama dan blok *card* khusus mode gelap untuk menciptakan kontras tinggi.
* **Signature Gradient**: Paduan dari *Teal*, *Iris*, dan *Glow*. Digunakan eksklusif untuk aksi utama (tombol primer) dan elemen ornamen bermotif geometris.

## 2. Tipografi (Typography)
* **Fraunces**: Digunakan untuk elemen *Display* dan *Headline* untuk mempertahankan estetika majalah editorial klasik.
* **Inter**: Digunakan untuk *Body* dan UI demi keterbacaan tingkat tinggi pada data dan deskripsi fungsional.

## 3. Komponen Antarmuka (UI Components)
* **Radii & Bentuk**: Elemen menggunakan sudut melengkung yang ekstrim (*Generously rounded*). *Card* standar menggunakan `32px`, sedangkan elemen interaktif (tombol, *chip*) menggunakan `999px` (*pill-shaped*).
* **Depth & Elevation**: Sistem tidak menggunakan *border* gelap untuk memisahkan struktur. Pemisahan dilakukan menggunakan `soft-ambient` *shadow* yang memanfaatkan warna dasar `sage` dengan opasitas rendah.
* **Motif Tessera**: Komponen pendukung bisa menggunakan motif bentuk heksagonal sebagai ornamen geometris yang tenang (*quiet geometry*).

## 4. Aturan Desain (Do's and Don'ts)
* **DO**: Berikan jarak (*whitespace*) ekstra longgar antar komponen (minimal `40px` atau `64px`) untuk mendukung kesan *calm product surfaces*.
* **DON'T**: Jangan pernah menggunakan *drop shadow* berwarna hitam pekat. Selalu gunakan bayangan dengan rona warna hangat (*sage/ivory*).

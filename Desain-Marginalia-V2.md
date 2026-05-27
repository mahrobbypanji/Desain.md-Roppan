---
version: alpha
name: Margin.alia
description: A school-notebook design system featuring ruled cream paper, ink-navy writing, and a single red margin. Built for friendly, organic, and academic productivity interfaces.
theme: light
colors:
  background: "#F9F6EE"
  surface: "#FFFFFF"
  ink: "#1E293B"
  ink-light: "#475569"
  margin-red: "#EF4444"
  action-blue: "#3B82F6"
  marker-yellow: "#FDE047"
  mint: "#A7F3D0"
  eraser-pink: "#FECDD3"
  graphite: "#94A3B8"
  focus: "rgba(30, 41, 59, 0.15)"
typography:
  display:
    fontFamily: "'Caveat', cursive, sans-serif"
    fontSize: "3rem"
    fontWeight: 700
    letterSpacing: "0.02em"
    lineHeight: 1.2
  headline-lg:
    fontFamily: "'Fraunces', serif"
    fontSize: "2rem"
    fontWeight: 600
    letterSpacing: "-0.01em"
    lineHeight: 1.25
  title-md:
    fontFamily: "'Fraunces', serif"
    fontSize: "1.25rem"
    fontWeight: 600
    letterSpacing: "0"
    lineHeight: 1.3
  body-md:
    fontFamily: "'Fraunces', serif"
    fontSize: "1rem"
    fontWeight: 400
    letterSpacing: "0"
    lineHeight: 1.6
  label-sm:
    fontFamily: "'Inter', sans-serif"
    fontSize: "0.875rem"
    fontWeight: 500
    letterSpacing: "0.02em"
    lineHeight: 1.4
rounded:
  sm: "4px"
  md: "8px"
  lg: "12px"
  full: "9999px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "16px"
  lg: "24px"
  xl: "32px"
  xxl: "48px"
border:
  width: "2px"
  style: "solid"
  color: "{colors.ink}"
elevation:
  sticky-note: "4px 6px 12px rgba(0, 0, 0, 0.12), 1px 2px 4px rgba(0, 0, 0, 0.08)"
  card: "none"
components:
  button-primary:
    backgroundColor: "{colors.margin-red}"
    textColor: "#FFFFFF"
    typography: "{typography.label-sm}"
    rounded: "{rounded.md}"
    border: "2px solid {colors.ink}"
    padding: "8px 16px"
  button-secondary:
    backgroundColor: "{colors.mint}"
    textColor: "{colors.ink}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.md}"
    border: "2px solid {colors.ink}"
    padding: "8px 16px"
  card:
    backgroundColor: "{colors.surface}"
    border: "2px solid {colors.ink}"
    rounded: "{rounded.lg}"
    padding: "24px"
  sticky-note:
    backgroundColor: "{colors.marker-yellow}"
    textColor: "{colors.ink}"
    typography: "{typography.display}"
    border: "none"
    shadow: "{elevation.sticky-note}"
    padding: "16px"
---

# Dokumen Spesifikasi Desain (Desain.md)
**Nama Sistem**: Margin.alia - School-Notebook Design System
**Versi**: V. Alpha (Spring 26)
**Deskripsi**: Sistem desain bertema buku catatan sekolah dengan estetika kertas bergaris (*ruled cream paper*), tinta biru dongker (*ink-navy writing*), dan garis tepi merah (*red margin*). Dirancang untuk antarmuka yang ramah, organik, dan berfokus pada produktivitas akademis.

## 1. Sistem Warna (Color Palette)
Desain ini menggunakan warna-warna alat tulis klasik untuk menciptakan nuansa organik dan analog. 

* **background (`#F9F6EE`)**: Warna utama halaman (*cream paper*).
* **surface (`#FFFFFF`)**: Latar belakang komponen *card* agar teks tetap terbaca tanpa terganggu pola garis halaman.
* **ink (`#1E293B`)**: Warna utama untuk tipografi dasar dan *border* semua elemen interaktif.
* **margin-red (`#EF4444`)**: Digunakan secara eksklusif untuk garis margin kiri dan aksi primer/destruktif.
* **marker-yellow (`#FDE047`)**: Latar belakang penekanan, *highlight*, dan komponen *sticky note*.

## 2. Tipografi (Typography)
Sistem ini menggunakan *Three Voices* untuk membedakan fungsi elemen UI:
* **Caveat**: Digunakan untuk elemen yang bersifat tidak formal, seperti catatan tambahan, *sticky notes*, dan penanda. Memberikan kesan *handwritten*.
* **Fraunces**: *Font* serif yang digunakan untuk *headline* dan *body copy*. Memberikan nuansa buku teks sekolah klasik yang serius namun mudah dibaca.
* **Inter**: Digunakan secara khusus untuk komponen UI teknis seperti tombol, *input form*, dan label metadata.

## 3. Komponen Antarmuka (UI Components)
* **Borders**: Seluruh komponen struktural (Card, Button, Input) wajib memiliki *border* solid `2px` berwarna `ink` (`#1E293B`) untuk memberikan kesan "digambar dengan pena".
* **Buttons**:
  * *Primary*: Menggunakan warna `margin-red` dengan teks putih.
  * *Secondary*: Menggunakan warna pastel (`mint` atau `action-blue`) dengan teks dan *border* `ink`.
* **Sticky Notes**: Komponen melayang (*floating*) yang menggunakan *background* `marker-yellow`, memiliki bayangan (`elevation.sticky-note`), rotasi acak antara -2 derajat hingga 2 derajat, dan diisi dengan tipografi `Caveat`.

## 4. Struktur Layout
* **Red Margin**: Layar harus memiliki garis vertikal setebal `2px` berwarna `margin-red` yang membentang dari *header* ke *footer* pada sisi kiri halaman (sekitar 10% - 15% dari lebar *viewport*). 
* **Ruled Paper Background**: *Background* utama dirender menggunakan *repeating-linear-gradient* CSS untuk membentuk garis horizontal tipis berwarna abu-abu/biru pudar setiap `32px` vertikal.

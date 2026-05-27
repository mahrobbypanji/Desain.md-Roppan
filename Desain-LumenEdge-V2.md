---
version: 1.0
name: Lumen Edge
description: A sub-chromatic dark system built on bottom-lit radial surfaces, hairline rims, and a single luminous horizon line that signals focus, depth, and intent.
theme: dark
colors:
  void: "#050507"
  graphite: "#0F1014"
  slate: "#18191E"
  hairline: "#2A2C35"
  muted: "#7A7F94"
  lumen: "#FFFFFF"
  lumen-soft: "rgba(255, 255, 255, 0.7)"
  horizon: "linear-gradient(90deg, rgba(255,255,255,0.2) 0%, rgba(255,255,255,1) 50%, rgba(255,255,255,0.2) 100%)"
typography:
  display:
    fontFamily: "'Space Grotesk', sans-serif"
    fontSize: "2.5rem"
    fontWeight: 700
    letterSpacing: "-0.02em"
    lineHeight: 1.1
  body-ui:
    fontFamily: "'Inter', sans-serif"
    fontSize: "0.875rem"
    fontWeight: 400
    letterSpacing: "0"
    lineHeight: 1.5
  mono:
    fontFamily: "'JetBrains Mono', monospace"
    fontSize: "0.75rem"
    fontWeight: 500
    letterSpacing: "0"
    lineHeight: 1.4
rounded:
  inner: "7px"
  outer: "14px"
spacing:
  sm: "8px"
  md: "16px"
  lg: "24px"
  xl: "48px"
motion:
  ease-signature: "cubic-bezier(0.15, 0.83, 0.66, 1)"
  duration: "1.00s"
components:
  panel:
    backgroundColor: "{colors.graphite}"
    borderTop: "1px solid {colors.hairline}"
    rounded: "{rounded.outer}"
    padding: "24px"
    shadow: "inset 0px -24px 48px -12px rgba(255,255,255,0.02)"
  button-engage:
    backgroundColor: "{colors.slate}"
    textColor: "{colors.lumen}"
    rounded: "{rounded.inner}"
    borderTop: "1px solid {colors.hairline}"
    borderBottom: "1px solid {colors.lumen}"
    padding: "8px 16px"
    typography: "{typography.body-ui}"
---

# Dokumen Spesifikasi Desain (Desain.md)
**Nama Sistem**: Lumen Edge
**Versi**: V 1.0
**Deskripsi**: Sebuah sistem desain gelap sub-kromatik (*sub-chromatic dark system*) yang mengusung tema *sleek minimalist future*. Desain ini mengeliminasi *noise* warna dan menggantinya dengan manipulasi cahaya.

## 1. Sistem Warna (Color Palette - Luminance Only)
Sistem membuang seluruh rona warna kontras dan murni bermain di rentang luminasi.
* **Void (`#050507`)**: Latar kanvas paling dalam.
* **Graphite & Slate (`#0F1014`, `#18191E`)**: Digunakan untuk permukaan panel (*engineered glass*).
* **Lumen (`#FFFFFF`)**: Cahaya utama sistem. Digunakan untuk teks primer, status interaktif aktif, dan pendaran.

## 2. Tipografi (Typography)
* **Space Grotesk**: Memberikan kesan *futuristic* dan teknis untuk judul dan data metrik besar.
* **Inter**: Keterbacaan optimal untuk deskripsi UI dan antarmuka *default*.
* **JetBrains Mono**: Format wajib untuk seluruh indikator persentase, kode metrik, dan parameter sistem.

## 3. Empat Sinyal Visual Utama (The Signals)
Desain ini menukar estetika warna (*color fills*) dengan konfigurasi cahaya:
1. **Radial Surfaces**: Ilusi pencahayaan dari bawah (*bottom-lit*) menggunakan *inset shadow* yang sangat redup (`rgba(255,255,255,0.02)`) di dalam komponen panel.
2. **Hairline Rims**: *Border* atas setebal `1px` berwarna `hairline` (`#2A2C35`) pada seluruh *card* untuk membentuk refleksi ujung material *glass*.
3. **Horizon Line**: Garis `border-bottom` bercahaya `lumen` (putih) yang menggunakan efek gradasi (*fading* di kiri dan kanan) sebagai indikator mutlak status aktif/*hover* sebuah elemen.
4. **Lumen Focus**: Cincin *focus state* (saat interaksi *keyboard*) direpresentasikan dengan pendar cahaya (*cool-white outer ring*), bukan garis biru standar.

## 4. Animasi & Transisi (Motion & Ease)
Seluruh transisi (baik interaksi tombol maupun pemuatan halaman) WAJIB menggunakan:
* **Fungsi Easing**: `cubic-bezier(0.15, 0.83, 0.66, 1)`
* **Durasi**: Relatif lambat (`1.00s` hingga `1.2s`) untuk mensimulasikan aktivasi mesin atau kaca rekayasa di masa depan.

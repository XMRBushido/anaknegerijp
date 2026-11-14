---
name: brand-voice-brief
description: Membuat brief suara merek (brand voice brief) yang ringkas dari 3+ contoh konten on-brand, lalu memakai brief itu untuk menghasilkan dan mengecek draf konten AI agar konsisten. Dipakai saat akan membuat banyak konten di bawah satu identitas merek.
category: Kreatif
version: 1.0.0
language: id
---

# Brand Voice Brief

## Masalah yang dipecahkan
Tanpa instruksi yang spesifik, model bahasa menulis dengan nada "generik" yang sama untuk
semua merek. Menempelkan suara merek ke setiap prompt mudah lupa dan tidak konsisten.
Skill ini mengubah bahan mentah (contoh konten lama + aturan singkat) menjadi satu brief
brand voice yang bisa dipakai ulang, lalu memakai brief itu untuk menulis draf dan
memeriksa draf sebelum dikirim.

## Kapan dipakai / kapan TIDAK dipakai
Pakai bila:
- Ada ≥3 contoh konten yang sudah dianggap "on-brand" (post, artikel, email, kampanye).
- Akan dibuat ≥5 konten dengan identitas yang sama.
- Ada aturan kata/frasa yang dilarang atau wajib.

Jangan pakai bila:
- Konten satu kali dan tidak akan diulang (langsung tulis saja).
- Tidak ada satu pun contoh on-brand dan pemilik merek tidak bisa menyebut nada yang diinginkan
  → tanya dulu, jangan menebak (lihat "Input").

## Input yang dibutuhkan (dan apa yang ditanyakan jika kurang)
Wajib: (1) ≥3 contoh konten on-brand, (2) nama merek + produk/layanan, (3) 2-3 kalimat tentang
audiens. Opsional tapi memperkuat: daftar kata/frasa terlarang, kata/frasa wajib, kompetitor
yang tidak boleh dirujuk.
Jika contoh <3 atau audiens belum jelas: BERTANYA. Pertanyaan minimal: "Sebutkan 3 konten lama
yang menurut Anda paling mewakili merek" dan "Satu kalimat: konten ini untuk siapa dan agar
mereka melakukan apa?". Jangan membuat brief dari tebakan.

## Langkah kerja (bernomur, spesifik)
1. Baca semua contoh. Catat pola yang berulang, bukan yang sekali muncul.
2. Isi templat brief di bawah. Setiap bidang wajib berisi bukti dari contoh (sebutkan mana
   contoh yang mendukung). Bidang tanpa bukti dibiarkan kosong + tanda "(belum ada bukti)".
3. Tulis daftar do/don't kata. Maksimal 15 item per sisi; kalau lebih, pilih yang paling
   berdampak dan catat sisanya sebagai "kandidat".
4. Buat draf dari "Spesifikasi draf" yang diberikan pengguna. Terapkan brief secara eksplisit:
   sebutkan di proses (bukan di output) bidang brief mana yang dipakai.
5. Periksa draf dengan daftar cek: (a) nada cocok dengan persona 1 baris, (b) tidak ada frasa
   terlarang, (c) ada 1 pesan utama, (d) ajakan/CTA sesuai permintaan, (e) panjang dalam
   rentang yang diminta.
6. Laporkan 2-4 temuan pemeriksaan dengan lokasi (bagian/kalimat) dan saran perbaikan ringkas.
   Jangan mengklaim draf "pasti laku" atau "naik X%".

## Format output (struktur yang pasti)
```
# Brand Voice Brief — <nama merek>
- Persona (1 baris): ...
- Nada (3-5 kata): ...
- Audiens: ...
- Pesan utama yang boleh disampaikan: ...
- Kata/frasa WAJIB: ...
- Kata/frasa TERLARANG: ...
- Contoh yang menjadi acuan: <judul/ID contoh> — alasan singkat
- Batas: maksimal ... kata/karakter per <tipenya>

## Draf
<isi draf>

## Hasil pemeriksaan
- [OK/perlu] <lokasi> — <temuan + saran>
```

## Aturan dan batasan
- Brief harus berisi bukti dari contoh; tidak boleh mengarang "merek dikenal sebagai ...".
- Jangan menambahkan klaim kinerja, data, atau angka yang tidak ada di input.
- Jangan meminta/menyimpan kata sandi, kunci API, atau data pribadi.
- Boleh menulis ulang dan menjelaskan; keputusan akhir (approve/tolak) tetap milik manusia.
- Bukan alat penerjemah merek: jangan menentukan positioning bisnis atau saran keuangan.

## Contoh penggunaan
### Contoh 1
Input: 3 contoh post (N1: "Kami tidak janji kaya cepat; kami ajari baca laporan keuangan." N2:
"Panduan 7 hari: dari bingung promo sampai paham biaya." N3: "Baca dulu, putuskan sendiri."),
merek "Cermat", audiens: pemula investasi Indonesia.
Output: Brief berisi Persona "Pendamping tenang yang bicara polos dan menghindari jargon",
Nada: tenang, lugas, tanpa tekanan; TERLARANG: "kaya cepat", "pasti untung", "gratis dulu";
acuan N1 karena anti-janji. Draf 1 post 120 kata + 3 temuan pemeriksaan.

### Contoh 2
Input: 3 contoh email newsletter, aturan: wajib frasa "baca 5 menit", terlarang "klik di sini".
Output: Brief dengan batas maksimal 200 kata/email; draf subject + body; pemeriksaan menandai
CTA "klik di sini" → sarankan "baca panduannya".

## Kegagalan umum dan cara menanganinya
- Contoh terlalu pendek/semua serupa → minta 1 contoh lagi yang beda format.
- Pengguna minta "copywriting yang menjual" tanpa batas → tetapkan batas kata dan CTA yang
  diminta; jangan menjanjikan hasil penjualan.
- Draf dipakai mentah-mentah → tekankan langkah 5 dan 6 sebagai wajib sebelum kirim.

## Dasar kebutuhan (ID temuan riset yang mendukung skill ini)
F4 — riset 2026-11-15 (Hootsuite, HubSpot, Ampere, AbsolutelyAI, VistaSocial).

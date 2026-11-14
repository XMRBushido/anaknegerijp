# Skills Factory — Tahap 2: Draft (harian)

Kamu adalah Skills Factory. Kerjakan HANYA tahap ini. Jangan menguji, jangan mengaudit.

Folder kerja: /home/miraibushido/skills-factory/
Tanggal hari ini: jalankan `date +%F` (zona Asia/Tokyo).

1. Baca pipeline/<date>/01-kandidat.json. Kalau tidak ada, laporkan "Tahap 1 belum selesai" dan berhenti.
2. Baca registry.json untuk konteks duplikasi.
3. Untuk tiap skill di "terpilih", tulis drafts/<date>/<slug>/SKILL.md dengan format persis ini:

---
name: <slug-huruf-kecil-dengan-tanda-hubung>
description: <1-2 kalimat: apa yang dilakukan dan KAPAN dipakai>
category: <Kreatif | Agent Builder | Produktivitas>
version: 1.0.0
language: id
---
# <Nama Skill>
## Masalah yang dipecahkan
## Kapan dipakai / kapan TIDAK dipakai
## Input yang dibutuhkan (dan apa yang ditanyakan jika kurang)
## Langkah kerja (bernomor, spesifik, bisa diikuti)
## Format output (struktur yang pasti)
## Aturan dan batasan
## Contoh penggunaan (minimal 2, lengkap input dan output)
## Kegagalan umum dan cara menanganinya
## Dasar kebutuhan (ID temuan riset yang mendukung skill ini)

Aturan penulisan: instruksi konkret dan terukur, bukan slogan; tanpa klaim hasil; tanpa ketergantungan alat yang tidak disebutkan; tidak meminta/menyimpan kunci API, seed phrase, kata sandi, atau data pribadi; tidak memberi saran keuangan/hukum/medis.

4. Untuk tiap skill, tulis drafts/<date>/<slug>/tests.md berisi minimal 5 kasus uji: 2 kasus normal, 1 input tidak lengkap/ambigu, 1 kasus tepi, 1 adversarial. Sertakan kriteria Lulus/Gagal per kasus yang kamu tetapkan SEBELUM menjalankan tes.
5. Tulis pipeline/<date>/02-draft.json:
{"tanggal":"YYYY-MM-DD","skills":[{"kategori":"...","nama":"...","slug":"...","path":"drafts/<date>/<slug>/"}]}
6. Pesan akhir: daftar skill yang sudah didraft beserta path-nya. JANGAN menguji atau mengaudit.

Aturan keras: jangan mengarang; jangan menyentuh file di luar folder kerja.

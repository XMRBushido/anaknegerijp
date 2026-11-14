# Skor Kandidat — 2026-11-15, run 06:00 (cron SF-1 `1e4a04f0b97e`)

Audit trail Tahap 1 untuk eksekusi terjadwal pagi. Run uji 00:xx tercatat di `01-kandidat-scoring.md` (run itu menghasilkan `01-kandidat.json` yang kini dicadangkan sebagai `01-kandidat.prev-0104.json`; isinya mengarah ke skill yang **sudah terdaftar** di registry sebagai SK-0003..SK-0006).

Cek duplikasi dilakukan terhadap **ke-6 entri registry.json** (SK-0001 s/d SK-0006) plus draft tanpa ID yang masih ada di `drafts/2026-11-15/` (`brand-voice-brief`, `agent-regression-eval`, `pkm-intake-triage`) sebagai tetangga terdekat.

Skala 1–5 per dimensi: F = Frekuensi kebutuhan, S = Rasa sakit, K = Kelayakan dibuat sebagai skill, U = Kemudahan diuji, N = Nilai jual. Total maksimal 25.

## Kreatif
| Rank | Nama | Slug | F | S | K | U | N | Total | Status |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Repurpose Asset Extraction | repurpose-asset-extraction | 5 | 4 | 4 | 4 | 4 | **21** | TERPILIH |
| 2 | Cross-Platform Format Spec Sheet | cross-platform-format-spec | 3 | 3 | 4 | 4 | 3 | 17 | Cadangan 1 |
| 3 | AI Visual Tool Fit Check | ai-visual-tool-fit-check | 3 | 4 | 3 | 3 | 4 | 17 | Cadangan 2 |
| 4 | Creative Review Loop | creative-review-loop | 3 | 3 | 4 | 3 | 3 | 16 | — |
| 5 | Campaign Idea Matrix | campaign-idea-matrix | 3 | 2 | 4 | 3 | 2 | 14 | — |

Dasar: R-2026-11-15-18 (utama), R-2026-11-15-14 (kandidat 3). Kandidat 2 memakai bahan R-18 yang sama (batas karakter per platform, perbedaan nada LinkedIn vs Instagram) dengan output paling sederiah; kandidat 4–5 bukti paling tipis.
Duplikasi: lolos dari SK-0005/SK-0001 (brand-voice-lock) dan draft `brand-voice-brief` — inputnya materi lama yang sudah jadi, bukan draf yang akan dinilai; outputnya lembar ekstraksi + rencana adaptasi per platform, bukan kunci suara/penilaian draf.

## Agent Builder
| Rank | Nama | Slug | F | S | K | U | N | Total | Status |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Agent Context Prune | agent-context-prune | 5 | 5 | 4 | 4 | 5 | **23** | TERPILIH |
| 2 | HITL Approval Gates | hitl-approval-gates | 5 | 4 | 4 | 4 | 5 | 22 | Cadangan 1 |
| 3 | Tool Call Reliability | tool-call-reliability | 5 | 5 | 4 | 4 | 4 | 22 | Cadangan 2 |
| 4 | Agent Cost & Observability Guardrail | agent-cost-observability-guardrail | 5 | 4 | 4 | 4 | 4 | 21 | — |
| 5 | Authorization Drift Guard | authorization-drift-guard | 4 | 4 | 3 | 3 | 4 | 18 | — (dasar riset 1 sumber) |

Dasar: R-2026-11-15-15 (6 sumber, terbit 2–11 Nov 2026) untuk peringkat 1; R-2026-11-15-11 (6 sumber) peringkat 2; R-2026-11-15-12 (6 sumber) peringkat 3; R-2026-11-15-10 (5 sumber) peringkat 4; R-2026-11-15-17 (1 sumber) peringkat 5 — diturunkan karena aturan "1 sumber = lemah".
Duplikasi: lolos dari SK-0006/SK-0002 (agent-eval-gate = gerbang pengukuran sebelum rilis) dan draft `agent-regression-eval` (perbandingan versi lama vs baru). Ketiga fungsi itu mengukur kinerja agent; yang diusulkan di sini mengatur **isi konteks dan memori saat agent berjalan** (apa yang masuk, kedaluwarsa, reset, konflik), sehingga trigger dan output berbeda.

## Produktivitas
| Rank | Nama | Slug | F | S | K | U | N | Total | Status |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Action Item Carry-Forward | action-item-carry-forward | 5 | 4 | 4 | 4 | 4 | 21 | DITOLAK (duplikat SK-0003) |
| 2 | Note Retrieval Rescue | note-retrieval-rescue | 4 | 4 | 4 | 4 | 4 | **20** | TERPILIH |
| 3 | Stale Note Review | stale-note-review | 4 | 3 | 4 | 3 | 3 | 17 | Cadangan 1 |
| 4 | Doc to Brief | doc-to-brief | 3 | 3 | 4 | 4 | 3 | 17 | Cadangan 2 |
| 5 | Meeting Prep Brief | meeting-prep-brief | 3 | 3 | 3 | 3 | 2 | 14 | DITOLAK (dekat SK-0003/SK-0004) |

**Penolakan peringkat 1:** `action-item-carry-forward` skornya tertinggi, tetapi output intinya (tugas | owner | tenggat | status) identik dengan tabel action item di SK-0003 `meeting-decisions-log`; perbedaannya hanya penambahan carry-forward/aging. Aturan Tahap 3: "anggap duplikat jika kamu ragu". Kandidat ini ditolak, bukan dipilih. R-2026-11-15-20 tetap dicatat sebagai riset dan bisa dipakai bila cakupannya diperjelas oleh manusia (misalnya register lintas-rapat yang berdiri sendiri tanpa ringkasan rapat).
Dasar peringkat 2: R-2026-11-15-19 (6 thread PKM independen).
Duplikasi peringkat 2: lolos dari SK-0004 `decision-ledger-audit` (menentukan status keputusan lintas-berkas dengan kutipan) dan draft `pkm-intake-triage` (triage saat menangkap). Yang diusulkan mengubah catatan yang **sudah tersimpan** agar bisa diambil kembali lewat pertanyaan — different function, output, and criterion.

## Kandidat ditolak / tidak dipakai
- `action-item-carry-forward` — duplikat SK-0003 (output action item table identik); lihat catatan di tabel.
- `meeting-prep-brief` — trigger dan output beririsan dengan SK-0003 dan SK-0004.
- `authorization-drift-guard` — skor 18, dan dasarnya hanya 1 sumber (R-17); tidak memenuhi ambang "2 sumber independen".
- `Agent Memory Hygiene` / `Context Drift Guard` (nama dari run 00:xx) — diserapkan ke `agent-context-prune` karena fungsinya sama; nama baru dipakai agar tidak menimpa draft lama.
- Kandidat generik "ringkasan dokumen", "template prompt", dan "marketplace skill" — tidak punya bukti spesifik atau sudah tercakup skill Hermes terpasang.

## Catatan operasi
- Registry berisi 6 entri, semuanya bertanggal 2026-11-15 (hasil run 00:xx); tidak ada entri dari tanggal lain.
- Run 00:xx menulis `01-kandidat.json` yang mengarah ke skill yang kini sudah ada di registry; bila SF-2 membaca berkas lama itu, akan terjadi pendaftaran ulang. Berkas lama dicadangkan ke `01-kandidat.prev-0104.json` dan `01-kandidat.json` diganti dengan kandidat baru yang lolos duplikasi.
- Tiga terpilih berbeda fungsi satu sama lain dan tidak menimpa slug mana pun di registry maupun drafts/.

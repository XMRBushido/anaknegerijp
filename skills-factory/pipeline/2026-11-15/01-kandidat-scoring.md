# Skor Kandidat — 2026-11-15 (audit trail Tahap 1)

Cek duplikasi: `registry.json` berisi **0 entri**, jadi tidak ada duplikat formal terhadap skill terdahulu; semua kandidat lolos cek duplikasi. Tiga terpilih juga berbeda fungsi satu sama lain.

Skala 1–5 per dimensi: F = Frekuensi kebutuhan, S = Rasa sakit, K = Kelayakan dibuat sebagai skill, U = Kemudahan diuji, N = Nilai jual. Total maksimal 25.

## Kreatif
| Rank | Nama | Slug | F | S | K | U | N | Total | Status |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Brand Voice Lock | brand-voice-lock | 4 | 4 | 5 | 5 | 4 | **22** | TERPILIH |
| 2 | AI Visual Tool Fit Check | ai-visual-tool-fit-check | 4 | 4 | 3 | 3 | 4 | 18 | Cadangan 1 |
| 3 | Content Repurpose Matrix | content-repurpose-matrix | 3 | 3 | 4 | 4 | 3 | 17 | Cadangan 2 |
| 4 | Creative Review Loop | creative-review-loop | 3 | 3 | 4 | 3 | 3 | 16 | — |
| 5 | Campaign Idea Matrix | campaign-idea-matrix | 3 | 2 | 4 | 3 | 2 | 14 | — |

Dasar: R-2026-11-15-01 (01), R-2026-11-15-14 (14). Kandidat 2–5 buktinya lebih tipis atau outputnya lebih sulit diuji secara objektif.

## Agent Builder
| Rank | Nama | Slug | F | S | K | U | N | Total | Status |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Agent Eval Gate | agent-eval-gate | 5 | 4 | 5 | 5 | 5 | **24** | TERPILIH |
| 2 | HITL Approval Gates | hitl-approval-gates | 5 | 4 | 4 | 4 | 5 | 22 | Cadangan 1 |
| 3 | Tool Call Reliability | tool-call-reliability | 5 | 5 | 4 | 4 | 4 | 22 | Cadangan 2 |
| 4 | Context Drift Guard | context-drift-guard | 4 | 5 | 3 | 3 | 4 | 19 | — |
| 5 | Agent Memory Hygiene | agent-memory-hygiene | 4 | 4 | 4 | 3 | 4 | 19 | — |

Dasar: 02, 11, 12, 09/04/06. Cadangan dipesan berdasarkan jumlah sumber: HITL (6 sumber) di atas Tool Call (5 sumber).

## Produktivitas
| Rank | Nama | Slug | F | S | K | U | N | Total | Status |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Decision Ledger Audit | decision-ledger-audit | 4 | 5 | 4 | 4 | 5 | **22** | TERPILIH |
| 2 | Meeting Decisions Log | meeting-decisions-log | 4 | 4 | 5 | 5 | 4 | 22 | Cadangan 1 |
| 3 | Knowledge Intake Triage | knowledge-intake-triage | 4 | 3 | 4 | 4 | 3 | 18 | Cadangan 2 |
| 4 | Action Item Tracker | action-item-tracker | 4 | 3 | 4 | 4 | 3 | 18 | — |
| 5 | Doc to Brief | doc-to-brief | 3 | 3 | 4 | 4 | 3 | 17 | — |

Dasar: 13, 03, 08. Seri 22–22 antara peringkat 1 dan 2 diputus untuk **Decision Ledger Audit**: buktinya primer (5 thread komunitas di 3 subreddit) dibanding sekunder/vendor, dan pembedanya paling tajam (mengaudit catatan yang sudah ada untuk menemukan keputusan yang masih berlaku, bukan membuat ringkasan baru dari rapat).

## Kandidat ditolak / tidak dipakai
- "Evaluasi agent versi platform X" — variasi kecil dari Agent Eval Gate; ditolak.
- "Brand voice generator" tanpa penilaian/audit — hanya separuh dari Brand Voice Lock; ditolak.
- "Meeting summary polos" tanpa keputusan/owner — lebih lemah dari Meeting Decisions Log dan Decision Ledger Audit; ditolak.
- "Marketplace/kurator skill" — hanya 1 sumber (R-07, opini); ditolak.
- "Prompt Injection Defense Checklist" — bukti kuat (2 paper) tapi sebagai skill mandiri lebih menyerupai panduan statis; tidak masuk 5 besar kategori Agent Builder.

## Catatan operasi
`drafts/2026-11-15/` sudah berisi draft dari sesi eksperimen sebelumnya (brand-voice-lock, brand-voice-brief, pkm-intake-triage, agent-regression-eval, agent-eval-gate, meeting-decisions-log), tetapi `registry.json` masih kosong dan `pipeline/2026-11-15/01-kandidat.json` belum ada. Tahap 2 akan menulis draft dari `01-kandidat.json` ini.

# Skills Factory — Hasil 2026-11-15 (DRAFT, menunggu persetujuan)

Ini bukan bagian dari situs. Ini hasil pabrik skill harian yang **belum dipublikasikan**.
Publikasi ke halaman Skills menunggu persetujuan XMRBUSHIDO.

## Isi

| Jalur | Isi |
|---|---|
| `SPEC.md` | Spesifikasi pabrik (peran, alur 7 tahap, aturan keras, batas biaya) |
| `PIPELINE.md` | Arsitektur pipeline berantai 4 job cron + berkas keadaan |
| `stage1-riset.md` … `stage4-audit.md` | Prompt tiap tahap |
| `registry.json` | Catatan semua skill yang diproses (skema v1, append-only) |
| `research/2026-11-15.md` | Bukti riset: 19 temuan ber-tautan sumber |
| `drafts/2026-11-15/<slug>/` | SKILL.md, tests.md, test-raw.md, audit.md per skill |
| `pipeline/2026-11-15/` | Berkas keadaan antar-tahap (kandidat → draft → uji) |
| `reports/` | Laporan harian (format laporan SF) |

## Skill yang lulus (laporan SF-4)

Batch resmi (run terjadwal 06:00–06:24):
- **SK-0007 Repurpose Asset Extraction** — Kreatif · 20/20
- **SK-0008 Agent Context Prune** — Agent Builder · 20/20
- **SK-0009 Note Retrieval Rescue** — Produktivitas · 20/20

Batch manual (validasi pipeline, 00:51–03:57):
- **SK-0004 Decision Ledger Audit** — Produktivitas · 20/20
- **SK-0005 Brand Voice Lock** — Kreatif · 20/20
- **SK-0006 Agent Eval Gate** — Agent Builder · 20/20

Riwayat batch lama (job `c665b971c239`, sudah di-pause): SK-0001, SK-0002, SK-0003.

## Yang belum dibereskan (perlu keputusan)

1. **Entri ganda di registry** — SK-0001 vs SK-0005 (`brand-voice-lock`), SK-0002 vs SK-0006 (`agent-eval-gate`). Aturan append-only dipegang, entri lama tidak diubah.
2. **Draft limbah** — `brand-voice-brief/`, `agent-regression-eval/`, `pkm-intake-triage/`, `meeting-decisions-log/`.
3. **Inkonsistensi `03-uji.json`** dengan registry untuk SK-0007/SK-0009 (putaran revisi & jumlah lulus).
4. **Durasi** — SF-4 ±2 jam 12 mnt; SF-3 ±30 mnt. Perlu diperketat bila mau 3 skill/hari yang hemat.

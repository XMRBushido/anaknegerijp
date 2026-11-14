# Skills Factory — Pipeline Berantai

Pabrik skill harian dipecah menjadi 4 tahap cron agar tiap tahap ringan dan bisa dipantau. Semua tahap zona waktu **Asia/Tokyo**, folder kerja `/home/miraibushido/skills-factory/`.

| Job | ID | Jadwal | Tahap | Deliver |
|---|---|---|---|---|
| SF-1 Riset & Kandidat | `1e4a04f0b97e` | `0 6 * * *` | riset + 5 kandidat/kategori + cek duplikasi + pilih 3 | local |
| SF-2 Draft | `657047c0f027` | `8 6 * * *` | tulis SKILL.md + tests.md per skill | local |
| SF-3 Uji | `6be9d5e97c9e` | `16 6 * * *` | 5 kasus uji per skill (sub-agent konteks bersih) | local |
| SF-4 Audit & Lapor | `bd485fc70ba6` | `24 6 * * *` | audit 10 butir + registry + laporan | telegram NOTIF |

Job lama `c665b971c239` ("Skills Factory Harian" versi tunggal) sudah **paused** — digantikan pipeline ini.

## Berkas keadaan (state)
`pipeline/<YYYY-MM-DD>/`
- `01-kandidat.json` — keluaran SF-1, masukan SF-2
- `02-draft.json` — keluaran SF-2, masukan SF-3
- `03-uji.json` — keluaran SF-3, masukan SF-4

Tiap tahap WAJIB berhenti dan melapor kalau berkas masukan belum ada (jangan menebak).

## Aturan
- Skill hanya masuk `drafts/`; publikasi ke situs menunggu persetujuan XMRBUSHIDO.
- `registry.json` skema versi 1; entri lama tidak pernah diubah/dihapus.
- Riset maks 15 pencarian/hari; revisi maks 2 putaran per skill.
- Detail lengkap per tahap ada di `stage1-riset.md`, `stage2-draft.md`, `stage3-uji.md`, `stage4-audit.md`.
- `SPEC.md` = spesifikasi pabrik (referensi); `SPEC.md` versi tunggal lama sudah tidak dipakai jadwal.

# anaknegerijp

Website &amp; halaman legal **Anaknegeri JP** (@XMRClaw).

- Live: https://xmrbushido.github.io/anaknegerijp/
- Deploy: push ke `main` → GitHub Pages build otomatis dari root.

## Struktur

| File | Isi |
|---|---|
| `index.html` | Beranda |
| `skills.html` | Katalog Skills AI Agent (jual skill siap pasang) |
| `terms.html` | Terms of Service |
| `privacy.html` | Privacy Policy |
| `404.html` | Halaman error |
| `styles.css` | Design system (token + komponen) |
| `favicon.svg`, `og-image.png` | Aset ikon & preview sosial |
| `robots.txt`, `sitemap.xml` | SEO |
| `tiktok*.txt` | **File verifikasi TikTok — JANGAN DIHAPUS/DIPINDAH** |

## Catatan

Semua tautan internal memakai path relatif, sehingga aman di subfolder
`/anaknegerijp/` maupun di domain root. Jangan kembalikan ke path absolut
seperti `/terms.html` — itu menunjuk ke root `github.io` dan menghasilkan 404.

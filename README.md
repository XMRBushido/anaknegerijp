# anaknegerijp

Website & halaman legal **Anaknegeri JP** (@XMRLABS).

- Live: https://xmrbushido.github.io/anaknegerijp/
- Deploy: push ke `main` → GitHub Pages build otomatis dari root.

## Struktur

| Path | Isi |
|---|---|
| `index.html` | Beranda |
| `skills.html` | Katalog Skills AI Agent (jual skill siap pasang) |
| `layanan.html` | Layanan bisnis & paket manajemen media sosial |
| `security-audit.html` | Layanan security audit workstation AI agent |
| `terms.html` | Terms of Service |
| `privacy.html` | Privacy Policy |
| `404.html` | Halaman error |
| `styles.css` | Design system (token + komponen) |
| `favicon.svg`, `favicon-32.png`, `app-icon.png`, `apple-touch-icon.png` | Ikon situs |
| `og-image.png`, `og-image.svg` | Preview sosial |
| `robots.txt`, `sitemap.xml` | SEO |
| `posters/` | Arsip poster konten sosial — tidak dipakai oleh build situs |
| `tiktok*.txt` | **File verifikasi TikTok — JANGAN DIHAPUS/DIPINDAH** |

## Pratinjau lokal

```bash
python3 -m http.server 8000
# buka http://localhost:8000/
```

## Catatan tautan

- Halaman biasa memakai path relatif, sehingga aman di subfolder
  `/anaknegerijp/` maupun di domain root. Jangan ubah menjadi path absolut
  seperti `/terms.html` — itu menunjuk ke root `github.io` dan menghasilkan 404.
- `404.html` adalah pengecualian: GitHub Pages dapat menyajikannya pada kedalaman
  URL apa pun, jadi path relatif bisa salah resolve. File itu sengaja memakai
  path absolut `/anaknegerijp/...`.

# CANDRA 385 — Personal Photo Log

Website portofolio multi-halaman dengan gaya jurnal visual pribadi. Beranda, rakitan, cerita, dan moodboard masing-masing punya halaman sendiri. Tidak memakai framework atau build step; semua foto berada di folder aset.

## Struktur

- `index.html` — halaman utama.
- `builds.html` — galeri rakitan, filter suasana, dan pembesar foto.
- `about.html` — cerita personal.
- `moodboard.html` — papan stiker interaktif.
- `css/site.css` — sistem visual, tema gelap, dan layout responsif.
- `js/theme.js` — tema terang/gelap.
- `js/navigation.js` — menu seluler.
- `js/gallery.js` — galeri dan filter foto.
- `js/moodboard.js` — moodboard dan penyimpanan pilihan.
- `js/sharing.js` — bagikan URL atau salin tautan.
- `js/scroll.js` — navigasi atas dan animasi masuk.
- `assets/images/` — foto potret, PC, dan stiker.

## Jalankan lokal

Ekstrak ZIP, buka terminal di folder `candra-385-portfolio`, kemudian jalankan:

```powershell
py -m http.server 8000
```

Buka `http://localhost:8000`.

## Deploy ke Cloudflare Pages

Perlu Node.js/npm dan akun Cloudflare. Jalankan dari folder hasil ekstrak:

```powershell
npx wrangler login
npx wrangler pages project create
npx wrangler pages deploy . --project-name=candra-385
```

Untuk domain sendiri, setelah deploy buka Workers & Pages → pilih proyek → Custom domains → Set up a domain.

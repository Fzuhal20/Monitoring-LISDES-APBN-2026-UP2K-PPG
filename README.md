# LISDES Monitoring System — APBN TA 2026 · UP2K Papua Pegunungan

Integrated Physical Progress Monitoring & Reporting Dashboard.

Aplikasi satu file (`index.html`) — tanpa build, tanpa server. Data dibaca langsung dari Google Spreadsheet yang dipublikasikan sebagai CSV.

## Deploy ke GitHub Pages

1. Buat repository baru di GitHub (mis. `lisdes-monitoring`).
2. Upload semua file di folder ini (`index.html`, `README.md`, `.nojekyll`) ke branch `main`.
3. Buka **Settings → Pages** → Source: **Deploy from a branch** → Branch: `main` / folder `/ (root)` → **Save**.
4. Tunggu ±1 menit. Dashboard tersedia di `https://<username>.github.io/lisdes-monitoring/`.

## Sumber data

- Default: Google Spreadsheet (File → Share → Publish to web → CSV).
- URL dapat diganti dari menu **13 — Settings** tanpa mengubah kode (tersimpan di browser).
- Opsional: worksheet **Kurva S** (kolom: Tanggal, Rencana Kumulatif %, Realisasi Kumulatif %) — publikasikan sebagai CSV dan tempel URL-nya di Settings.

## Kolom yang direkomendasikan untuk ditambahkan

- `PIC` — penanggung jawab lapangan
- `Target SLO` / `Realisasi SLO`
- `Last Update` (DD/MM/YYYY)
- `Rencana Progres (%)` atau worksheet Kurva S
- `Latitude` / `Longitude` (untuk peta)

## Keamanan

Tidak ada API key atau kredensial di frontend. Spreadsheet dibaca dari link publikasi CSV publik. Untuk data privat, gunakan backend/proxy dengan environment variable lalu arahkan URL di Settings ke endpoint tersebut.

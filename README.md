# Papan Progres Produksi — Apa Jadinya

Halaman statis papan progres seri Shorts "Apa Jadinya", diterbitkan lewat
GitHub Pages dari branch `gh-pages` repo ini:

https://demile02.github.io/progres/

## Arsitektur

- Halaman: statis, berkas di repo ini (sumber lokal:
  `~/workspace/progres/deploy-connector/`). Diterbitkan lewat connector
  GitHub (MCP resmi) sebagai snapshot berkas teks.
- Data: halaman mengambil `progress.json` dan `history.json` dari bucket
  publik Supabase Storage `progres` (project wasatify), diperbarui pusher
  lokal `~/workspace/progres/push-supabase.py` di VM asisten dengan siklus
  3 detik dari berkas `progress.json` episode yang sedang diproduksi.
- Ikon: berkas PNG ikon yang sama disajikan dari bucket Supabase tersebut
  (snapshot connector hanya membawa berkas teks/UTF-8, bukan biner).

Papan sebelumnya tinggal di VPS UpCloud (progres.213-163-193-255.sslip.io)
yang berhenti beroperasi 2 November 2026; arsitektur ini menggantikannya
tanpa bergantung pada VPS.

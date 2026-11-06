# Dashboard Kegiatan Harian Pemeliharaan Sarana

Dashboard Kegiatan Harian Pemeliharaan Sarana — logbook, pengingat, dan pekerjaan belum selesai real-time untuk staff pemelihara sarana rumah sakit.

Repo ini berisi dashboard **Monitoring Pompa & Tandon** untuk Instalasi Pemelihara Sarana (IPS), Rumah Sakit Adi Husada Kapasari.

## Cara membuka dashboard

- Buka file `index.html` langsung di browser, atau
- Aktifkan GitHub Pages untuk repo ini (Settings → Pages → Branch `main`, folder `/ (root)`), lalu buka alamat GitHub Pages repo ini.

## Lokasi yang dimonitor

| Lokasi | Yang dipantau |
| --- | --- |
| Joglo | Status Pompa, Level Tandon, Suhu Pompa, RSSI, IP Address |
| Kantin | Status Pompa, Level Tandon, Suhu Pompa, MCB, RSSI, IP Address |
| Lantai 6 | Level Tandon, RSSI, IP Address |

## Sumber data

Data diambil langsung (real-time) dari 3 Google Sheets dalam format CSV — satu sheet per lokasi (Joglo, Kantin, Lantai 6). Dashboard selalu menampilkan baris data terbaru dari masing-masing sheet.

## Fitur

- **Logbook / tabel real-time** — status pompa, level tandon, suhu, MCB, RSSI, dan IP address per lokasi, dengan badge warna (MENYALA/MATI, RENDAH/NORMAL/PENUH, MCB NORMAL/TRIP).
- **Auto-refresh 10 detik** — data diperbarui otomatis tanpa perlu me-refresh halaman; sel yang berubah akan berkedip sebentar.
- **Peringatan data berhenti 30 menit** — jika data dari sheet sudah tidak masuk selama 30 menit atau lebih, kartu lokasi diberi bingkai merah dan teks berkedip "DATA BERHENTI (X menit)".
- **Dark mode** — tombol 🌙/☀️ di pojok kanan atas; pilihan tersimpan di browser (localStorage).
- **Responsif** — tampil rapi di HP maupun di komputer.

## Cara mengganti logo RS

Logo Rumah Sakit ditampilkan di header kiri atas.

1. Siapkan file logo RS (format PNG, disarankan latar transparan atau putih).
2. Simpan sebagai `assets/logo-rs.png` di dalam repo ini (sejajar dengan `index.html` ada folder `assets`).
3. Logo akan langsung tampil menggantikan placeholder "LOGO RS".

Selama file `assets/logo-rs.png` belum ada, header menampilkan placeholder "LOGO RS" — dashboard tetap berfungsi normal.

## Dibuat oleh

Instalasi Pemelihara Sarana (IPS) — Rumah Sakit Adi Husada Kapasari.

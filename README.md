# Pengelolaan Stok Barang Toko Sembako Berbasis Web

Aplikasi sederhana untuk membantu toko sembako mencatat dan memantau persediaan barang. Aplikasi dibuat dengan React, TypeScript, Vite, dan penyimpanan browser (`localStorage`) agar dapat dipublikasikan sebagai website statis melalui GitHub Pages.

## Fitur utama

- Dashboard ringkasan jumlah barang, total stok, stok menipis, dan stok habis.
- Data barang dan kategori.
- Data pemasok untuk pencatatan penerimaan barang.
- Pencatatan barang masuk.
- Pencatatan barang keluar non-penjualan dengan alasan: rusak, kedaluwarsa, hilang, pemakaian internal, atau lainnya.
- Stok opname dan penyesuaian jumlah stok fisik.
- Riwayat pergerakan stok.
- Laporan posisi stok dan stok minimum.

## Menjalankan di komputer

Pastikan Node.js versi 20 atau lebih baru sudah terpasang.

```bash
npm install
npm run dev
```

Untuk membuat hasil build website statis:

```bash
npm run build
```

Hasil build berada di folder `dist/`.

## Penyimpanan data

Pada GitHub Pages, data disimpan di `localStorage` browser. Data hanya tersedia pada browser dan perangkat tempat data dimasukkan. Data tidak otomatis tersinkronisasi antarperangkat atau antar pengguna. Hapus data browser dapat menghilangkan data aplikasi, jadi lakukan ekspor/backup secara berkala jika fitur backup tersedia.

Aplikasi ini merupakan prototipe statis. Login demo dilakukan di sisi browser dan bukan sistem keamanan untuk data sensitif atau penggunaan multi-pengguna produksi.

## Akun demo

- Administrator: username `admin`, password `admin123`
- Petugas: username `kasir`, password `kasir123`

## Publikasi GitHub Pages

Workflow GitHub Actions di `.github/workflows/deploy.yml` akan memasang dependensi, menjalankan `npm run build`, lalu menerbitkan folder `dist/` ke GitHub Pages saat ada push ke branch `main` atau `master`.

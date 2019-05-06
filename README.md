# Proses Redirect 

Dari [burhanudinyahya.github.io](https://burhanudinyahya.github.io) ke [burhanudinyahya.id](https://www.burhanudinyahya.id)

## Pertama

Gunakan _plugins_ _jekyll-redirect-from_ artinya repo ini harus menggunakan jekyll.
Untung Github sekarang (06-05-2019) sudah mendukung jekyll secara bawaan, entah sejak kapan github menyediakan fitur ini.

Selanjutnya buat halaman `index.html` dan `_config.yml`

isi `index.html`
```
---
redirect_to: "https://www.burhanudinyahya.id"
---
```

isi `config.yml`
```
theme: jekyll-theme-minimal
gems:
  - jekyll-redirect-from
```
  
Langkah ini dapat men-_solving_ hanya sejauh halaman home, sedangkan halaman artikel masih ke 404 bawaan github pages.

## Kedua

Buat `robots.txt` agar blog ini tidak terindex di google

isi `robots.txt`
```
User-agent: *
Disallow: /
```

Langkah ini hanya de-index halaman home dari google, sedangkan halaman artikel masih ada.

## Ketiga

Akhirnya bisa redirect semua halaman, ke domain baru dengan `CNAME`

isi `CNAME`
```
burhanudinyahya.id
```

Langkah ini men-_solve_ semuanya, jadi 2 langkah sebelumnya sudah tak berlaku lagi.

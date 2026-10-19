# portfolio-media

Berkas gambar & video publik untuk website portofolio **Rangshar**
(<https://www.rangshar.my.id>). Disajikan lewat GitHub Pages:

```
https://xrgsss.github.io/portfolio-media/
```

Repo ini **hanya berisi media**, bukan kode website.

## Dari mana isinya

Dihasilkan dari repo [portofolio-rangshar](https://github.com/xrgsss/portofolio-rangshar)
dengan:

```bash
npm run optimize:media -- --out media-siap-unggah
```

Video dikecilkan (H.264, crf 28, lebar maks 1280 px) dan gambar diubah ke WebP.
Totalnya turun dari ~380 MB menjadi ~40 MB.

Susunan folder mengikuti pathname aslinya, misalnya:

```
images/optimized/portofolio/3d/0213.mp4
images/optimized/logo/Visual Studio Code.webp
```

## Jangan diubah manual

Kalau media di website diperbarui, jangan menyunting berkas di sini satu per
satu. Jalankan ulang langkah *optimize* dari repo utama, dorong isi foldernya ke
repo ini, lalu arahkan `data/*.json` dengan:

```bash
npm run repoint:media -- --host https://xrgsss.github.io/portfolio-media
```

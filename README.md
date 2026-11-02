# Rimba Pet — Demo Android

Starter demo toko hewan pribadi. Aplikasi ini memakai HTML/CSS/JavaScript, Capacitor, dan GitHub Actions.

## Fitur demo
- Katalog kategori hewan, pencarian, keranjang.
- Checkout simulasi (Transfer/COD/QRIS tidak memproses uang sungguhan).
- Riwayat pesanan dan perubahan status.
- Dashboard admin: omzet pesanan berstatus Selesai, jumlah pesanan, stok, tambah/edit/hapus produk.
- Edit akun dan profil toko.
- Penyimpanan lokal di perangkat melalui localStorage.

## Jalur paling mudah: buat APK dari GitHub
1. Buat repository baru di GitHub bernama `rimba-pet-demo`.
2. Upload seluruh isi folder proyek ini (termasuk folder `.github`).
3. Buka tab **Actions** pada repository.
4. Pilih workflow **Build Rimba Pet Demo APK**, lalu tekan **Run workflow**. Workflow juga berjalan otomatis saat ada push ke branch `main`.
5. Setelah selesai, buka hasil run dan cari bagian **Artifacts**.
6. Download `Rimba-Pet-Demo-APK`, ekstrak ZIP, lalu pindahkan `app-debug.apk` ke HP Android.
7. Buka APK dan izinkan instalasi dari sumber tersebut bila Android meminta izin.

## Build lokal dengan komputer
Persyaratan: Node.js 22+, Android Studio, Android SDK, dan Java yang dikelola Android Studio.
```bash
npm install
npx cap add android
npx cap sync android
npx cap open android
```
Di Android Studio pilih Build > Build Bundle(s) / APK(s) > Build APK(s).
APK debug biasanya berada di `android/app/build/outputs/apk/debug/app-debug.apk`.

## Uji melalui browser
Buka `www/index.html` di browser untuk melihat UI lokal. Untuk fitur PWA/install dari browser, deploy folder `www` ke hosting HTTPS seperti GitHub Pages.

## Catatan penting
- Ini prototipe satu toko/satu pemilik, bukan marketplace multi-penjual.
- Data disimpan di browser/perangkat. Hapus data aplikasi/browser dapat menghapus data demo.
- Tidak ada login aman, backend, sinkronisasi antarperangkat, pengiriman, atau pembayaran asli.
- Jangan gunakan untuk menerima pembayaran sungguhan. Integrasi produksi perlu backend, autentikasi, database, payment gateway resmi, validasi webhook, kebijakan privasi, serta keamanan.
- Listing hewan di sini data contoh. Pastikan perdagangan hewan sesuai hukum, kesehatan, kesejahteraan, dan dokumen yang berlaku.

# Alin Fit Tracker — Android APK via GitHub Actions

Repository starter untuk membungkus prototype HTML Alin Fit Tracker menjadi aplikasi Android menggunakan Capacitor. APK debug dibangun otomatis oleh GitHub Actions; build ini belum ditandatangani untuk rilis Play Store.

## Cara pakai

1. Buat repository baru di GitHub, misalnya `alin-fit-tracker`.
2. Ekstrak ZIP ini, lalu unggah seluruh isi folder ke root repository (pastikan folder `.github/workflows` ikut terunggah).
3. Buka tab **Actions** di repository dan aktifkan Actions jika diminta.
4. Pilih workflow **Build Alin Fit Tracker APK**, tekan **Run workflow**. Workflow juga berjalan saat ada push ke branch `main` atau `master`.
5. Tunggu sampai job hijau selesai. Buka hasil run, bagian **Artifacts**, lalu unduh `alin-fit-tracker-debug-apk`.
6. Ekstrak ZIP artifact dari GitHub dan instal `app-debug.apk` di perangkat Android. Android mungkin meminta izin memasang aplikasi dari sumber ini.

## Yang sudah disiapkan

- `www/index.html`: prototype HTML saat ini.
- `capacitor.config.json`: identitas aplikasi Android.
- `.github/workflows/build-apk.yml`: workflow untuk menghasilkan APK debug.

## Catatan penting

- Workflow membuat proyek Android saat build, jadi folder `android/` tidak perlu disertakan di awal.
- Data prototype disimpan di penyimpanan lokal WebView pada perangkat. Data browser versi web tidak otomatis pindah ke APK.
- Build ini menghasilkan **debug APK** untuk uji coba, bukan APK release yang ditandatangani untuk distribusi publik.
- Fitur yang bergantung pada koneksi eksternal atau integrasi wearable belum otomatis tersedia. Uji semua alur di perangkat sebelum dipakai untuk data penting.

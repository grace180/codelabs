# testing_app

A new Flutter project.

Execution Instructions

Untuk menjalankan semua tes pengujian pada project ini, pastikan anda berada di root folder projct flutter yang tepat dan jalankan perintah flutter test test/models/favorites_test.dart untuk menjalankan unit test, dan untuk menjalankan widget test jalankan perintah flutter test test/home_test.dart atau flutter run test/home_test.dart  untuk menjalankan widget test dengan menggunakan device atau emulator.

Unit Test
    berfungsi untuk menambahkan item ke daftar favorit
    Menghapus item dari daftar favorit
    Memastikan notifyListeners() berfungsi dengan memicu pembaruan UI

Widget Test
     Memastikan ListView muncul di layar Favorites dan Home
     Menekan tombol ikon favorit menambahkan dan menghapus item
     Memunculkan Snackbar setelah aksi dilakukan

Integration Test
    Menjalankan aplikasi secara utuh
    Menambahkan 3 item ke favorit
    Navigasi ke halaman Favorites
    Menghapus item favorit
    Menangkap metrik kinerja

Hasil dari pengujian diatas adalah semua kondisi berhasil terpenuhi (All tests passed)

Tantangan yang dihadapi dan cara mengatasinya
    Saat mencoba menjalankan integration test di chrome, terdapat beberapa tantangan yang ada seperti berikut ini:
    1. gagal menjalankan integration test saat menjalankan perintah flutter test integration_test/app_test.dart namun perintah tersebut menghasilkan error Web devices are not supported for integration tests yet. jadi saya mencoba menjalankan perintah flutter drive --driver=test_driver/integration_test.dart --target=integration_test/app_test.dart -d chrome da berhasil dijalankan.
    2. Ketika menjalankan perintah flutter drive, muncul pesan error Unable to start a WebDriver session for web testing. Make sure you have the correct WebDriver server (e.g. chromedriver) running at 4444. solusi yang saya lakukan yaitu mengunduh chromedriver yang sesuai dengan versi chrome yang terpasang kemudian menjalankan perintah chromedriver.exe --port=4444. flutter drive berhasil terhubung ke chromedriver dan pengujian dapat berjalan di browser Chrome.

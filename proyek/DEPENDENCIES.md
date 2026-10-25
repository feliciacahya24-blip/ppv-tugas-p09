# DEPENDENCIES

## Pustaka UI
- Nama dan versi: Bootstrap 5.3.3 (versi dikunci, tidak memakai latest)
- Sumber: CDN jsDelivr (https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/)
- Berkas yang dimuat: bootstrap.min.css dan bootstrap.bundle.min.js
- Alasan memilih: komponennya lengkap, dokumentasinya jelas, dan temanya bisa diubah lewat variabel CSS sehingga warna coklat dan krem TaskSplit tetap dipertahankan.

## Ukuran transfer (diukur di tab Network, Chrome)
| Berkas | Ukuran transfer |
|---|---|
| bootstrap.min.css | 34.0 kB |
| bootstrap.bundle.min.js | 25.2 kB |

## Komponen yang dipakai
| Komponen | Dipakai untuk | JavaScript pustaka |
|---|---|---|
| Nav pills | Menu tiga tampilan (Anggota, Bagi Tugas, Hasil) | Tidak (perpindahan tampilan oleh script.js) |
| Card | Kotak isi setiap tampilan | Tidak |
| Spinner | Indikator "Membagi tugas..." | Tidak |
| Toast | Notifikasi saat anggota atau tugas ditambah atau dihapus | Ya, lewat ui-pustaka.js |

## Pengaturan
- Semua panggilan JavaScript Bootstrap hanya ada di ui-pustaka.js (fungsi tampilkanToast).
- style.css dimuat setelah Bootstrap dan mengubah tema lewat variabel CSS (--bs-card-*, --bs-nav-*, --bs-toast-*).

## Jawaban 4 pertanyaan sebelum memasang pustaka
### 1. Kebutuhan
- Masalah yang diselesaikan: Pada aplikasi TaskSplit dibutuhkan tombol untuk menu, kotak isi, petunjuk adanya loading, hingga notifikasi dengan tampilan yang teratur tanpa menulis semuanya dari nol.
- Bisa dengan CSS biasa? Ada beberapa saja yang mampu memungkinkan, contohnya menu dan bagian kotak isi di Tugas 4 yang awalnya dibuat dengan CSS biasa. Dan yang paling terbantu adalah toast, karena posisi, animasi muncul, dan hilang otomatisnya sudah disediakan.
- Komponen yang benar-benar dipakai: Ada 4 komponen, yaitu nav pills, card, spinner, dan juga toast.

### 2. Biaya
- Tambahan ukuran: bootstrap.min.css 34.0 kB dan bootstrap.bundle.min.js 25.2 kB, total sekitar 59 kB (telah dillihat pengukurannya pada tab Network).
- Apakah hanya bisa diimpor sebagian? Lewat CDN seluruh berkasnya ikut dimuat. Mengimpor sebagian butuh Sass dan npm, yang belum saya pakai.
- Waktu belajar: Waktu yang dikeluarkan untuk belajar dan memahami penugasan adalah sekitar 30 menit, kemudian pengerjaannya dilakukan selama 2 hari.

### 3. Pemeliharaan
- Rilis terakhir: Bootstrap 5.3.3 dirilis tahun 2024, dan untuk versi yang lebih barunya sudah rilis (5.3.8, Januari 2026). Namun, saya sengaja mengunci 5.3.3 agar nantinya pada bagian tampilan tetap aman dan tidak berubah tanpa disadari.
- •	Kelengkapan Dokumentasi? Sudah tersedia di getbootstrap.com/docs/5.3 untuk versi yang saya pakai.
- Apabila pustaka berhenti dikembangkan: semua panggilan JavaScript Bootstrap saya kumpulkan di ui-pustaka.js, jadi kalau perlu diganti cukup mengubah satu berkas tersebut.

### 4. Pemasangan
- Versi terkunci: dipasang lewat CDN jsDelivr dengan nomor versi pasti (5.3.3), bukan CDN tanpa versi atau @latest. Saya tidak memakai npm.
- Dicatat di: DEPENDENCIES.md (tidak ada package.json karena tidak memakai npm).
- CSS sendiri: ditulis di style.css yang dimuat setelah Bootstrap, sehingga terpisah dari berkas pustaka dan temanya diatur lewat variabel CSS.
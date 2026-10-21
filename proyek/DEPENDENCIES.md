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
(Tempel 4 pertanyaan dari deck P09 beserta jawabanmu di sini.)
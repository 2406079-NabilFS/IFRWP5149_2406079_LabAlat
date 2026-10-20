Mahasiswa mengajukan KRS dengan memilih mata kuliah. Setiap pengajuan menjalankan validasi KRS yang memeriksa kelengkapan, prasyarat mata kuliah, dan benturan jadwal. Jika validasi berhasil, sistem menyimpan pengajuan berstatus menunggu persetujuan dosen wali. Pada konfirmasi penyimpanan, mahasiswa dapat memilih mengunduh bukti pengajuan. Dosen wali menyetujui atau menolak KRS dan memberikan catatan keputusan.

ID      |Kebutuhan tugas
SIA-R01 |Mahasiswa dapat melihat jadwal kuliah
SIA-R02 |Admin akademik dapat mengelola jadwal kuliah
SIA-R03 |Mahasiswa dapat mengajukan KRS
SIA-R04 |Sistem memvalidasi KRS sebagai bagian pengajuan
SIA-R05 |Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan
SIA-R06 |Dosen wali dapat memproses persetujuan atau penolakan KRS

Kode dimulai dari R03 agar kebutuhan jadwal SIA-R01 dan SIA-R02 dari Pertemuan 2 tetap mempunyai identitas berbeda.
Batas dan asumsi:
• Pengguna telah terautentikasi.
• Data mata kuliah, prasyarat, dan jadwal tersedia.
• Validasi gagal menyebabkan pengajuan belum berhasil tersimpan.
• Unduh bukti tidak menjadi syarat keberhasilan pengajuan.
• KRS tersimpan belum berarti disetujui.
• Pembayaran, pengisian nilai, dan implementasi basis data berada di luar tugas.

ID      |Nama Fungsi                |Aktor terkait  |Sumber Kebutuhan
UC-01   |Lihat Jadwal Kuliah        |Mahasiswa      |SIA-R01
UC-02   |Kelola Jadwal Kuliah       |Admin Akademik |SIA-R02
UC-03   |Ajukan KRS                 |Mahasiswa      |SIA-R03
UC-04   |Validasi KRS               |Sistem         |SIA-R04
UC-05   |Unduh Bukti Pengajuan KRS  |Mahasiswa      |SIA-R05
UC-06   |Proses Keputusan KRS       |Dosen Wali     |SIA-R06

SIA-UC03 «include» SIA-UC04
Alasan: pemeriksaan kelengkapan, prasyarat mata kuliah, dan benturan jadwal menjadi bagian validasi pengajuan.

SIA-UC05 «extend» SIA-UC03
Extension point: Bukti pengajuan tersedia.
Kondisi: [mahasiswa memilih mengunduh bukti].
Alasan: pengajuan tetap berhasil tanpa pengunduhan bukti.
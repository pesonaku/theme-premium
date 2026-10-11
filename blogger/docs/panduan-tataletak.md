# 📖 Panduan Penggunaan & Konfigurasi Tata Letak (Blogger.com)

Tema **Pesona Green Residence** dirancang agar dapat digunakan langsung oleh publik dan dikonfigurasi tanpa harus mengubah kode XML secara manual.

---

## 🚀 1. Cara Memasang Tema di Blogger

1. Masuk ke dashboard [Blogger.com](https://www.blogger.com).
2. Pilih blog Anda, lalu klik menu **Tema (Theme)** di navigasi sebelah kiri.
3. Klik tombol titik tiga (⋮) di sebelah tombol "Sesuaikan" / "Customize".
4. Pilih **Pulihkan (Restore)**.
5. Unggah file `blogger/template.xml` dari repositori ini.
6. Tunggu hingga proses upload selesai, dan buka blog Anda untuk melihat hasilnya.

---

## 🎨 2. Mengubah Warna Tema (Light Green Customizer)

1. Masuk ke menu **Tema** -> klik **Sesuaikan (Customize)**.
2. Pilih tab **Lanjutan (Advanced)**.
3. Anda akan melihat palet warna variabel:
   - **Warna Utama (Emerald)**: `#10b981`
   - **Warna Utama Gelap**: `#059669`
   - **Warna Latar Lembut**: `#ecfdf5`
   - **Warna Aksen Promo**: `#f59e0b`
4. Pilih warna sesuai keinginan Anda, lalu klik ikon **Simpan** di pojok kanan bawah.

---

## 🛠️ 3. Konfigurasi Konten Lewat Menu Tata Letak (Layout)

Buka menu **Tata Letak (Layout)** di dashboard Blogger. Anda dapat mengedit setiap widget dengan mengklik ikon pensil (Edit):

| Bagian (Section) | Nama Widget | Apa yang Dapat Diubah? |
| :--- | :--- | :--- |
| **Header Logo** | `Header1` | Nama blog atau unggah logo gambar perumahan |
| **Hero Slider** | `HTML101` | Link gambar banner promo, teks diskon, link CTA |
| **Keunggulan** | `HTML102` | 5 poin keunggulan (Cicilan, DP, Type luas, Double dinding, dll) |
| **Listing Rumah** | `HTML103` | Menambah/mengubah tipe rumah subsidi & komersil, foto, dan spek modal |
| **Galeri Kawasan**| `HTML104` | Link foto kegiatan akad masal, fasilitas, taman |
| **Profil Marketing**| `HTML105` | Foto marketing, nama, nomor WhatsApp sales |
| **FAQ** | `HTML106` | Daftar pertanyaan & jawaban seputar syarat KPR |
| **Testimoni** | `HTML107` | Ulasan konsumen, nama pembeli, rating bintang |
| **Lokasi & Peta** | `HTML108` | Alamat kantor pemasaran & link iframe Google Maps |
| **Postingan Blog** | `Blog1` | Jumlah artikel yang ditampilkan otomatis dari artikel Anda |

---

## 📱 4. Mengganti Nomor WhatsApp Marketing

Untuk mengganti nomor WhatsApp default (`6281234567890`) ke nomor Anda:
- Edit widget **HTML105** (Profil Tim Marketing) di Tata Letak.
- Ganti nomor telepon pada tautan `https://wa.me/6281234567890` dengan nomor WhatsApp Anda (diawali kode negara `62` tanpa tanda `+` atau `0`).

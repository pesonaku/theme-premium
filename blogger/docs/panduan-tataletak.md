# 📖 Panduan Tata Letak (Easy Layout Edition)

Tata letak tema **Pesona Green Residence (v3.0)** kini telah disederhanakan secara maksimal. **Pengguna TIDAK PERLU lagi mengklik "Tambahkan Gadget" yang membingungkan.**

Semua bagian halaman sudah tersedia dan tersusun rapi dari atas ke bawah. Pengguna cukup mengklik tombol **Edit (ikon pensil)** pada widget yang ingin diubah.

---

## 🗂️ Susunan Menu Tata Letak di Dashboard Blogger

Saat Anda membuka menu **Tata Letak (Layout)** di Blogger, Anda akan melihat blok-blok widget yang sudah dinamai dengan nomor urut:

```
[1] Header Logo Perumahan
    └─ Logo & Nama Perumahan (Klik Edit)

[2] Hero Banner & Promo Utama
    └─ Promo Hero Banner (Klik Edit)

[3] 5 Poin Keunggulan
    └─ Daftar 5 Keunggulan (Klik Edit)

[4] Daftar Listing Tipe Rumah
    └─ Daftar Tipe Rumah (Klik Edit)

[5] Tabel Simulasi Harga & Cicilan
    └─ Tabel Simulasi Cicilan (Klik Edit)

[6] Galeri Foto & Aktivitas
    └─ Foto Galeri Kawasan (Klik Edit)

[7] Profil Marketing Resmi
    └─ Profil Sales Advisor (Klik Edit)

[8] Tanya Jawab (FAQ)
    └─ Daftar FAQ Accordion (Klik Edit)

[9] Testimoni Konsumen
    └─ Daftar Ulasan & Rating (Klik Edit)

[10] Lokasi & Google Maps
    └─ Alamat & Peta (Klik Edit)

[11] Postingan Blog
    └─ Postingan Blog Bawaan (Otomatis dari menu Postingan)

[12] Info Brand Footer
    └─ Tentang Perumahan di Footer (Klik Edit)

[13] Floating Chat & Nomor WhatsApp
    └─ Pengaturan Chat & Nomor WA (Klik Edit)
```

---

## ✏️ Cara Mengubah Konten di Tata Letak (Layout)

1. Buka dashboard **Blogger.com** -> klik menu **Tata Letak (Layout)**.
2. Cari bagian yang ingin Anda ubah (misalnya: `[7] Profil Marketing Resmi` atau `[10] Lokasi & Google Maps`).
3. Klik tombol **Edit** (ikon pensil).
4. Masukkan atau ubah isi teks / HTML di kolom **Konten (Content)**.
5. Klik **Simpan (Save)** di jendela popup widget, lalu klik tombol **Simpan** (ikon disket di pojok kanan bawah Blogger).

> 💡 **Cara Kerja Sistem Konten:**
> - **Jika Kolom Konten Diisi**: Website akan menampilkan konten baru yang Anda tulis.
> - **Jika Kolom Konten Kosong**: Template secara otomatis menampilkan tampilan default bawaan tema yang rapi, modern, dan profesional.
> - **Mereset ke Semula**: Jika ingin mengembalikan tampilan awal bawaan tema, cukup kosongkan kembali kolom **Konten** lalu klik **Simpan**.

---

## 💡 Contoh Kustomisasi Cepat

### 1. Mengubah Kontak Marketing & WhatsApp (`[7]` & `[13]`)
- Buka widget **[7] Profil Marketing Resmi** atau **[13] Floating Chat & Nomor WhatsApp**.
- Masukkan link WhatsApp Anda dengan format:
  ```html
  https://api.whatsapp.com/send?phone=6281234567890&text=Halo%20Marketing
  ```
  *(Ganti `6281234567890` dengan nomor WhatsApp Anda diawali kode negara 62)*

### 2. Mengubah Lokasi Google Maps (`[10]`)
- Buka Google Maps di browser -> Cari lokasi perumahan / kantor Anda.
- Klik tombol **Bagikan (Share)** -> Pilih tab **Sematkan peta (Embed a map)** -> Salin kode HTML iframe.
- Buka widget **[10] Lokasi & Google Maps** di Blogger -> Tempelkan (paste) kode iframe ke kolom **Konten** -> Simpan.

### 4. Fitur Pop-up Detail Unit & Galeri
- Setiap kartu rumah di bagian `[4] Listing Tipe Rumah` kini dilengkapi tombol **🔍 Detail Unit**. Saat diklik, akan muncul jendela pop-up interaktif (SweetAlert2) yang menampilkan denah, rincian spesifikasi teknis, harga, cicilan, dan tombol chat WhatsApp pemesanan langsung.

---

## 🛡️ Jaminan Tampilan (Zero Blank Page)
Template menggunakan arsitektur **Dual-Fallback System**:
- Begitu tema di-upload ke Blogger, **semua data dummy (Hero, 5 Keunggulan, 4 Tipe Rumah, Tabel KPR, Galeri, Profil Marketing, FAQ, Testimoni, Maps, dan WhatsApp) langsung muncul 100% lengkap dan aktif**.
- Pengguna tidak perlu khawatir halaman kosong atau rusak jika belum sempat mengedit widget di menu Tata Letak.



# 📖 Panduan Penggunaan & Konfigurasi Tata Letak (Blogger.com)
## Versi Modular & High Conversion (Inspirasi: PesonaKahuripan.org)

Tema **Pesona Green Residence v2.0** mengadopsi sistem arsitektur widget modular yang fleksibel. Setiap bagian halaman dapat ditambah, diedit, atau dihapus langsung melalui menu **Tata Letak (Layout)** di dashboard Blogger.com.

---

## 🚀 1. Cara Memasang Tema di Blogger

1. Masuk ke dashboard [Blogger.com](https://www.blogger.com).
2. Pilih blog Anda, lalu klik menu **Tema (Theme)**.
3. Klik tanda panah/titik tiga (⋮) di sebelah tombol "Sesuaikan" / "Customize".
4. Pilih **Pulihkan (Restore)**.
5. Unggah file `blogger/template.xml` dari repositori ini.
6. Tunggu hingga proses upload selesai ("Tema dipulihkan").

---

## 🎨 2. Mengubah Warna Tema (Light Green Customizer)

1. Buka menu **Tema** -> klik **Sesuaikan (Customize)**.
2. Pilih tab **Lanjutan (Advanced)**.
3. Anda dapat langsung mengganti:
   - **Warna Utama (Emerald)**: `#10b981` (Warna tombol, link aktif, border fokus)
   - **Warna Utama Gelap**: `#059669` (Gradien tombol & hover)
   - **Warna Latar Lembut**: `#ecfdf5` (Badge pill, background seksi)
   - **Warna Aksen Promo**: `#f59e0b` (Bintang review & aksen badge)
4. Klik tombol **Simpan** (ikon disket) di pojok kanan bawah.

---

## 🎛️ 3. Pengaturan Bagian Halaman Lewat Menu Tata Letak (Layout)

Buka menu **Tata Letak (Layout)** di Blogger. Berikut daftar bagian dan cara mengisinya:

### 3.1 Header & Navigasi
- **Header & Logo (`Header1`)**: Masukkan nama perumahan atau unggah gambar logo transparan.
- **Navigasi Menu (`LinkList1`)**: Tambahkan item menu dengan target anchor:
  - `#keunggulan` (Keunggulan)
  - `#type-rumah` (Tipe Rumah)
  - `#harga` (Simulasi Harga)
  - `#galeri` (Galeri)
  - `#faq` (Tanya Jawab)
  - `#lokasi` (Lokasi)
  - `#kontak` (Kontak)

### 3.2 Hero Banner Cover (`cover-section`)
- Menggunakan widget **Image** (`Image11`).
  - **Judul**: Tagline utama banner (contoh: *Wujudkan Rumah Impian Anda*).
  - **Keterangan / Caption**: Deskripsi singkat promo perumahan.
  - **Gambar**: Unggah foto perumahan resolusi tinggi (1600x900px).
  - **Tautan / Link**: Masukkan link tujuan atau gunakan format ganda `Label Tombol|#link` (contoh: `Pilih Tipe Rumah|#type-rumah`).

### 3.3 Keunggulan / About (`about-section`)
- Terdiri dari widget **Image** modular (`Image21` s/d `Image25`):
  - Anda dapat **menambah widget Image baru** kapan saja dengan klik *Tambahkan Gadget -> Gambar*.
  - **Judul**: Poin keunggulan (contoh: *Cicilan Ringan*, *DP Hanya 1%*, *Double Dinding*).
  - **Keterangan**: Deskripsi penjelasan keunggulan.
  - **Gambar**: Icon / foto penunjang keunggulan.

### 3.4 Tipe Rumah / Service (`service-section`)
- Terdiri dari widget **Image** modular (`Image31`, `Image32`, `Image33`, dst):
  - **Judul**: Tipe rumah (contoh: *Type 30/60 Subsidi*, *Type 36/60 Komersil*).
  - **Keterangan**: Spesifikasi ringkas (kamar, luas tanah, fasilitas).
  - **Gambar**: Foto tampak depan rumah / denah layout.
  - **Tautan / Link**: Link WhatsApp pemesanan atau halaman artikel detail.

### 3.5 Simulasi Angsuran & Harga Promo (`offer-section`)
- Widget **HTML** (`HTML51`):
  - Berisi tabel perbandingan angsuran tenor 10, 15, 20 tahun untuk rumah subsidi dan komersil.
  - Anda dapat mengedit besaran nominal cicilan langsung pada widget ini.

### 3.6 Galeri Kawasan & Fasilitas (`gallery-section`)
- Widget **HTML** (`HTML90`):
  - Foto dokumentasi akad kredit, taman bermain, dan pos keamanan.
  - Terintegrasi dengan **FancyBox 5.0**: Setiap foto yang memiliki atribut `data-fancybox="gallery"` akan otomatis terbuka dalam format popup lightbox berkualitas tinggi saat diklik.

### 3.7 Tanya Jawab / FAQ Accordion (`faq-section`)
- Terdiri dari widget **Text** modular (`Text71` s/d `Text74`):
  - **Judul**: Pertanyaan (contoh: *Apakah angsuran KPR bersifat Flat?*).
  - **Isi Teks**: Jawaban lengkap.
  - Efek show/hide accordion bekerja otomatis tanpa perlu coding.

### 3.8 Kepuasan Konsumen / Review (`review-section`)
- Terdiri dari widget **Image** modular (`Image41`, `Image42`, `Image43`):
  - **Judul**: Nama konsumen (contoh: *Pak Hendra Pratama*).
  - **Keterangan**: Ulasan/testimoni konsumen.
  - **Gambar**: Foto profil konsumen.

### 3.9 Floating Chat & Lead Capture WhatsApp (`widget-section`)
- Widget **Image** (`Image91`):
  - **Judul**: Nama Marketing Online (contoh: *Siti - Sales Advisor*).
  - **Keterangan**: Kalimat sapaan bubble (contoh: *Halo, butuh simulasi angsuran atau info survei lokasi?*).
  - **Gambar**: Foto profil marketing.
  - **Fitur SweetAlert2**: Ketika pengunjung mengisi pertanyaan dan menekan tombol kirim, modal dialog interaktif akan meminta Nama & Nomor WhatsApp, lalu otomatis meneruskannya ke WhatsApp marketing dan mencatatnya ke Google Sheets (jika diaktifkan).

---

## 📲 4. Mengganti Nomor WhatsApp & Google Sheets Webhook

Buka widget **HTML1 (Script & Webhook Config)** di paling atas atau cari di menu Tata Letak:
```javascript
const $googleSheetScriptUrl = "URL_GOOGLE_APPS_SCRIPT_ANDA"; // Biarkan kosong jika tidak digunakan
const $marketingWhatsApp = "6281234567890"; // Ganti dengan nomor WhatsApp Anda
```
*(Gunakan format angka internasional diawali 62 tanpa spasi atau tanda plus).*

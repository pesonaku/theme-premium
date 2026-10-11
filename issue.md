# ≡ƒôï Architectural Plan & Implementation Roadmap: Theme Premium Landing Page Perumahan

Dokumen ini merupakan panduan spesifikasi dan instruksi tingkat tinggi (*High-Level Specification & Implementation Guide*) yang dirancang untuk diimplementasikan oleh **Programmer** atau **AI Model (Budget/Fast Model)** secara terstruktur dan bertahap.

---

## ≡ƒôî 1. Ringkasan Proyek & Tujuan

- **Nama Proyek**: Theme Premium Landing Page Properti / Perumahan
- **Target Deliverable Utama**: Template XML Blogger.com (`template.xml`) yang responsif, modern, berkecepatan tinggi (*fast loading*), ramah SEO (*SEO Friendly*), dan siap pakai (*public ready*).
- **Ekosistem Pendukung**: 
  - **Next.js**: Digunakan sebagai prototipe interaktif / versi headless web app landing page modern.
  - **Laravel**: Digunakan sebagai modul backend/API (opsional/ekstensi) untuk integrasi webhook lead capture (formulir booking / kontak WhatsApp) dan manajemen data properti.
- **Palette Warna Utama**: **Light Green & Fresh Emerald** (Nuansa asri, hijau perumahan, sejuk, profesional).
  - Primary: `#10B981` (Emerald) / `#059669`
  - Secondary/Light: `#ECFDF5` / `#D1FAE5`
  - Dark/Text: `#0F172A` / `#334155`
  - Accent: `#F59E0B` (Gold/Warm untuk badge promo)
- **Repository**: [https://github.com/pesonaku/theme-premium.git](https://github.com/pesonaku/theme-premium.git)

---

## ≡ƒÅù∩╕Å 2. Arsitektur Repositori

Struktur folder repository disarankan sebagai berikut:

```plaintext
theme-premium/
Γö£ΓöÇΓöÇ blogger/
Γöé   Γö£ΓöÇΓöÇ template.xml             # File tema XML utama siap import ke Blogger
Γöé   Γö£ΓöÇΓöÇ assets/
Γöé   Γöé   Γö£ΓöÇΓöÇ css/                 # File styling modular (sebelum dimerge ke XML)
Γöé   Γöé   ΓööΓöÇΓöÇ js/                  # Script interaktif (slider, modal, accordion)
Γöé   ΓööΓöÇΓöÇ docs/
Γöé       ΓööΓöÇΓöÇ panduan-tataletak.md # Panduan konfigurasi menu Tata Letak bagi user
Γö£ΓöÇΓöÇ frontend-nextjs/             # (Opsional) Versi React / Next.js Landing Page
Γö£ΓöÇΓöÇ backend-laravel/             # (Opsional) API Lead webhook & CRM lead intake
Γö£ΓöÇΓöÇ issue.md                     # File perencanaan ini
Γö£ΓöÇΓöÇ README.md                    # Dokumentasi penggunaan tema untuk publik
ΓööΓöÇΓöÇ note.txt                     # Catatan pengembangan
```

---

## ≡ƒÄ¿ 3. Spesifikasi Fitur & Struktur Section

Setiap section wajib dapat dikonfigurasi melalui menu **Tata Letak (Layout)** Blogger tanpa perlu mengedit kode HTML secara manual.

### 3.1 Header & Navigasi
- **Komponen**:
  - Logo Perumahan (mendukung format gambar atau teks nama perumahan).
  - Navigasi link dengan *smooth scroll* (Keunggulan, Type Rumah, FAQ, Lokasi, Kontak).
  - Hamburger menu drawer interaktif pada layar mobile/tablet.
  - Quick CTA button ("Hubungi Kami" / ikon WhatsApp / foto profile).
- **Blogger Widget**: `<b:section id='header-section'>` dengan widget `Header` dan `LinkList`.

### 3.2 Hero Banner & Slider Otomatis
- **Komponen**:
  - Auto-play carousel gambar perumahan resolusi tinggi dengan transisi halus.
  - Tagline promo dinamis (misal: "Promo Akhir Tahun: DP 0%, Free Biaya KPR").
  - Tombol CTA utama (Direct WhatsApp / Download Brosur).
  - Indikator slider & kontrol navigasi (prev/next).
- **Blogger Widget**: `<b:section id='hero-slider'>` dengan widget `HTML/JavaScript` atau kumpulan `Image`.

### 3.3 Judul, Deskripsi & Value Proposition
- **Komponen**:
  - Heading utama yang memikat, deskripsi konsep perumahan (asri, strategis, aman).
  - CTA Sekunder dan statistik ringkas (misal: "95% Terjual", "100+ Keluarga Bahagia").
- **Blogger Widget**: `<b:section id='intro-cta'>` widget `Text` atau `HTML/JavaScript`.

### 3.4 Keunggulan & USP (Unique Selling Proposition)
- **Komponen**:
  - Grid card interaktif dengan icon modern dan micro-hover animation.
  - Item bawaan:
    1. Cicilan Ringan (Mulai Rp 1 Jutaan/bulan)
    2. DP Hanya 1% (Bebas biaya awal yang memberatkan)
    3. Type Luas (Tata ruang maksimal dan sirkulasi udara baik)
    4. Double Dinding (Privasi dan kekokohan terjamin)
    5. Lingkungan Ramai & Strategis (Dekat tol, stasiun, pasar, dan sekolah)
- **Blogger Widget**: `<b:section id='features-section'>`.

### 3.5 Card Listing Type Rumah (Subsidi & Komersil)
- **Komponen**:
  - Tab filter kategori: **Semua | Rumah Subsidi | Rumah Komersil**.
  - Card Item:
    - Foto utama tipe rumah + badge status ("Subsidi" / "Komersil" / "Ready Stock").
    - Judul tipe (misal: "Type 30/60", "Type 45/72").
    - Harga mulai dari & estimasi angsuran.
    - Ikon spesifikasi: Kamar Tidur (jumlah), Kamar Mandi, Carport, Ruang Tamu, Luas Tanah/Bangunan.
    - Tombol "Lihat Detail" yang membuka **Modal/Popup Detail**:
      - Galeri foto tampak depan, denah (layout plan), dan interior.
      - Spesifikasi teknis (pondasi, dinding, genteng, listrik, air).
      - Tombol langsung: "Chat Sales via WhatsApp".
- **Blogger Widget**: `<b:section id='property-listings'>`.

### 3.6 Galeri Perumahan & Aktivitas
- **Komponen**:
  - Grid / Masonry galeri foto perumahan.
  - Dokumentasi fasilitas umum (taman bermain, masjid, pos keamanan) dan aktivitas perumahan (akad massal, serah terima kunci, event warga).
  - Lightbox interaktif (klik gambar untuk memperbesar).
- **Blogger Widget**: `<b:section id='gallery-section'>`.

### 3.7 Profil Tim Marketing
- **Komponen**:
  - Foto profesional marketing, nama, dan jabatan/spesialisasi.
  - Deskripsi sambutan ramah ("Siap mendampingi survei lokasi dan proses KPR hingga serah terima kunci").
  - Tombol CTA WhatsApp langsung dengan pesan otomatis (pre-filled message: *"Halo, saya tertarik dengan info perumahan #link website#"*).
- **Blogger Widget**: `<b:section id='marketing-section'>`.

### 3.8 FAQ (Frequently Asked Questions)
- **Komponen**:
  - Desain Accordion (Show/Hide) yang interaktif dan responsif.
  - Pertanyaan umum:
    - Persyaratan pengajuan KPR Subsidi & Komersil
    - Besaran booking fee & apakah uang kembali jika KPR ditolak
    - Estimasi serah terima bangunan
    - Legalitas sertifikat (SHM/HGB)
- **Blogger Widget**: `<b:section id='faq-section'>`.

### 3.9 Kepuasan Pelanggan & Testimoni
- **Komponen**:
  - Slider/Card review pembeli rumah.
  - Avatar foto pembeli, nama, tipe rumah yang dibeli, rating bintang (5 stars), dan ulasan autentik.
- **Blogger Widget**: `<b:section id='testimonials-section'>`.

### 3.10 Lokasi, Peta & Alamat Kantor
- **Komponen**:
  - Embed Google Maps responsif.
  - Alamat lengkap kantor pemasaran & lokasi proyek.
  - Tombol "Buka di Google Maps".
- **Blogger Widget**: `<b:section id='location-section'>`.

### 3.11 Artikel & Berita Properti
- **Komponen**:
  - Loop postingan artikel bawaan Blogger (`<b:widget type='Blog' id='Blog1'>`).
  - Menampilkan tips KPR, info kawasan, dan update progress pembangunan.
  - Thumbnail gambar, tanggal terbit, dan ringkasan kutipan artikel.
- **SEO Benefit**: Membantu indexing Google dan content marketing organik.

### 3.12 Footer & Sosial Media
- **Komponen**:
  - Profil singkat developer/perumahan.
  - Quick links navigasi.
  - Tautan akun sosial media (Instagram, Facebook, TikTok, YouTube).
  - Copyright info & legal disclaimer.
- **Blogger Widget**: `<b:section id='footer-section'>`.

---

## ΓÜÖ∩╕Å 4. Spesifikasi Teknis Blogger XML & Tata Letak

### 4.1 Desain Berbasis Widget & Bebas Sentuh Kode
Setiap bagian menggunakan standar Blogger XML v2/v3:
```xml
<b:section id='nama-section' class='nama-section' maxwidgets='5' showaddelement='yes'>
  <b:widget id='HTML1' locked='false' title='Konfigurasi Section' type='HTML'>
    <!-- Default Data & Template Rendering -->
  </b:widget>
</b:section>
```
Dengan parameter `showaddelement='yes'`, pengguna awam dapat menambah, menghapus, atau mengatur urutan widget langsung melalui dashboard Blogger (**Tata Letak** / **Layout**).

### 4.2 Pengaturan Warna Tema via Theme Designer (`<b:skin>`)
Sertakan variabel Blogger `<Variable>` di dalam `<b:skin>` agar user dapat mengubah warna utama (Light Green) ke warna lain sesuka hati langsung dari menu sesuaikan Blogger:
```xml
<Variable name="primaryColor" description="Warna Utama" type="color" default="#10b981" value="#10b981"/>
<Variable name="primaryDark" description="Warna Sekunder" type="color" default="#059669" value="#059669"/>
<Variable name="primaryBg" description="Warna Background Lembut" type="color" default="#f0fdf4" value="#f0fdf4"/>
```

### 4.3 SEO & Schema Markup
- **Semantic HTML5**: Memakai tag semantik (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`).
- **OpenGraph & Twitter Card**: Dinamis sesuai judul artikel atau judul perumahan saat dibagikan ke WhatsApp dan media sosial.
- **Schema.org Structured Data**:
  - `RealEstateAgent` untuk data kantor pemasaran.
  - `SingleFamilyResidence` untuk listing tipe rumah.
  - `FAQPage` untuk bagian FAQ agar tampil sebagai rich snippet di Google.
- **Core Web Vitals**: Gambar menggunakan `loading="lazy"`, font Google di-load asinkron (`preconnect`), dan kode JavaScript dibuat ringan (*vanilla JS*, tanpa jQuery berat).

---

## ≡ƒÜÇ 5. Tahapan Implementasi (Action Items untuk Developer / AI)

### Fase 1: Perancangan Kerangka XML Dasar
- [ ] Buat file `blogger/template.xml` dengan struktur dasar XML Blogger yang valid.
- [ ] Definisikan variabel CSS di `<b:skin>` (palette Light Green) dan reset CSS modern.
- [ ] Terapkan meta tag SEO, viewport responsive, dan Schema.org JSON-LD.

### Fase 2: Implementasi Komponen UI & Tata Letak
- [ ] Buat section Header & Navigasi (smooth scroll & mobile hamburger menu).
- [ ] Buat Hero Banner Slider dengan auto-slide JavaScript vanilla.
- [ ] Buat Section Keunggulan (5 poin keunggulan).
- [ ] Buat Listing Tipe Rumah beserta Modal Popup Detail & Galeri.
- [ ] Buat Galeri Perumahan (Lightbox), FAQ (Accordion), dan Profil Marketing (WhatsApp CTA).
- [ ] Konfigurasi Blog Widget (`<b:widget type='Blog'>`) untuk seksi Artikel.
- [ ] Buat Footer & Integrasi Social Media.

### Fase 3: Integrasi Menu Tata Letak (Blogger Layout UI)
- [ ] Pastikan seluruh section menggunakan `<b:section showaddelement='yes'>`.
- [ ] Berikan data demo bawaan (*dummy default data*) sehingga saat pertama kali di-upload, landing page langsung tampil indah dan rapi.
- [ ] Buat dokumentasi panduan user di `README.md` tentang cara mengisi data via Tata Letak.

### Fase 4: Ekosistem Next.js & Laravel (Opsional / Prototyping)
- [ ] `frontend-nextjs`: Siapkan komponen React sepadan untuk opsi deployment mandiri (Vercel/SSR).
- [ ] `backend-laravel`: Endpoint REST API untuk menangkap form kontak calon pembeli & meneruskan notifikasi otomatis ke WhatsApp marketing.

---

## ≡ƒÄ» 6. Kriteria Keberhasilan (Acceptance Criteria)

1. **Kompatibilitas**: Berhasil di-upload ke Blogger melalui menu *Tema -> Pulihkan (Restore)* tanpa error parsing XML.
2. **Fleksibilitas**: User dapat mengganti nomor WhatsApp, foto, tipe rumah, dan teks keunggulan cukup dari menu **Tata Letak**.
3. **Responsif**: Tampil sempurna di Mobile (360px - 480px), Tablet (768px), dan Desktop (1024px+).
4. **Performa**: Skor PageSpeed Insights mobile > 85, desktop > 95.
5. **Konversi**: Tombol CTA WhatsApp dan telepon mudah diakses di layar manapun (*Sticky WhatsApp button*).


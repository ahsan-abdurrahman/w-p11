# Scope: Landing Page ATH-THOOHIRIIN

Landing page profil pondok pesantren ATH-THOOHIRIIN, ponpes pencetak penghafal Al-Qur'an dengan kepribadian Islam dan jiwa wirausaha. Target pengunjung: orang tua / calon santri yang ingin mendaftarkan anaknya. Tujuan: meyakinkan orang tua untuk mendaftarkan anak.

**Build approach:** Skateboard (MVP dulu, versi paling tipis yang sudah bisa dipakai, lalu berkembang).
**Workflow:** Prototype (langsung build, tanpa verifikasi tambahan). Level paling ringan. Cocok untuk landing page profil yang cepat tampil. Fitur berisiko tinggi tetap bisa dinaikkan levelnya.

_Ini rekomendasi supaya build tetap teratur, bukan keharusan. Kalau kamu sudah tahu cara build fitur tertentu, pakai /develop dan lewati /architect. Kamu yang memutuskan kapan sebuah fitur `done`._

## At a glance

| # | Feature | Phase | Status |
|---|---------|-------|--------|
| 1 | Stack & tooling | Foundation | done |
| 2 | Design system & UI foundation | Foundation | planned |
| 3 | Hero section | Slice 1 | planned |
| 4 | Visi & misi | Slice 1 | planned |
| 5 | Program unggulan | Slice 1 | planned |
| 6 | Fasilitas | Slice 1 | planned |
| 7 | Kontak & CTA pendaftaran | Slice 1 | planned |
| 8 | Footer & media sosial | Slice 1 | planned |

## Foundations

### 1. Stack & tooling
Tentukan stack dan siapkan proyek yang bisa jalan, supaya semua slice berikutnya punya fondasi nyata.
**Done when:** stack tercatat di spec, proyek boot lokal, dan build lolos.
**Spec:** [0001](../specs/0001-stack-and-tooling.md)
- [x] Decide the stack (spec): `/architect stack & tooling`
- [x] Build it: /develop stack & tooling

### 2. Design system & UI foundation · needs a decision
Bahasa visual, layout, dan komponen dasar supaya halaman terasa kohesif dan profesional. Warna hijau dan kuning sudah ditentukan.
**Done when:** `design.md` mencakup tipografi/warna/spacing/komponen, dan komponen dasar handle focus dan keyboard.
- [ ] Design it (spec): `/architect design system & UI foundation`

## Slice 1: Landing page profil

### 3. Hero section · needs a decision
Bagian pertama yang dilihat pengunjung: nama ponpes, tagline kuat, dan CTA utama (Daftar Sekarang / Hubungi Kami).
**Done when:** hero menampilkan nama ponpes, tagline, dan CTA yang jelas; responsif di mobile dan desktop.
- [ ] Design it (spec): `/architect hero section`

### 4. Visi & misi · needs a decision
Menjelaskan tujuan ponpes dan nilai-nilai yang diusung, termasuk kepribadian Islam dan jiwa wirausaha.
**Done when:** visi dan misi ditampilkan dengan jelas, mudah dibaca, dan meyakinkan.
- [ ] Design it (spec): `/architect visi & misi`

### 5. Program unggulan · needs a decision
Menampilkan program-program unggulan ponpes (misal: tahfidz 30 juz, pendidikan karakter, pelatihan wirausaha).
**Done when:** program unggulan ditampilkan dengan deskripsi singkat dan jelas.
- [ ] Design it (spec): `/architect program unggulan`

### 6. Fasilitas · needs a decision
Menampilkan fasilitas ponpes (asrama, masjid, ruang belajar, dll) dengan placeholder gambar.
**Done when:** fasilitas ditampilkan dengan gambar placeholder dan deskripsi singkat.
- [ ] Design it (spec): `/architect fasilitas`

### 7. Kontak & CTA pendaftaran · needs a decision
Menampilkan kontak pendaftaran (WhatsApp, telepon, alamat) dan CTA yang jelas untuk mendaftar.
**Done when:** kontak lengkap ditampilkan, tombol WhatsApp bisa diklik, dan alamat jelas.
- [ ] Design it (spec): `/architect kontak & CTA pendaftaran`

### 8. Footer & media sosial · needs a decision
Footer dengan info singkat, link media sosial (Instagram, Facebook), dan copyright.
**Done when:** footer menampilkan info singkat, link media sosial, dan copyright.
- [ ] Design it (spec): `/architect footer & media sosial`

## Deferred
Di luar scope build ini, disimpan supaya plan tetap jujur.
- **Testimoni orang tua / santri**: bukti sosial dari orang tua atau santri · needs a decision
- **Galeri foto kegiatan**: dokumentasi kegiatan ponpes · needs a decision
- **Blog / artikel**: konten tentang ponpes dan tahfidz · needs a decision
- **Form pendaftaran online**: form pendaftaran langsung di website · needs a decision
- **SEO & analytics**: metadata, sitemap, structured data, tracking · needs a decision

## Legend

**Kotak keputusan.** Setiap fitur punya tepat satu, sub-task yang labelnya berakhir `(spec)`. Setiap kotak lain adalah kotak eksekusi dan `/architect` tidak pernah mencentangnya.

**Lifecycle fitur:** scope update saat fitur bergerak; setiap baris adalah apa yang ditampilkan dan siapa yang mengaturnya:

| State | Set by | Fitur menampilkan |
|---|---|---|
| `planned` · needs a decision | `/scope` | satu kotak: `Design it (spec): /architect <feature>` |
| `in-progress` (designed) | **`/architect` saat spec capture** | `Design it` tercentang; spec terhubung; `Build it: /develop <feature>` + **2 to 5 milestones**; kotak penutup sesuai tier; follow-up yang muncul didaftarkan |
| `in-progress` (building) | `/develop` | sub-kotak milestone dicentang satu per satu; code pointer terisi |
| `in-progress` (verified) | `/check verify` | `Build it` + milestones tercentang; `Verify it` tercentang |
| `done` | **kamu, saat kamu putuskan** (skill mana pun mengaturnya saat kamu bilang); `/sync` reconcile | kotak yang kamu jalankan tercentang, yang dilewati ditandai skipped; stage terakhir tier adalah titik saran untuk menyebutnya done; `/sync` capture konvensi |

- **Next step** = kotak pertama yang belum tercentang (selalu command atau milestone terpantau).
- **needs a decision** = jalankan `/architect` dulu; kalau tidak langsung ke `/develop` (atau `/audit` untuk standards & tooling). Tag hilang setelah spec ter-capture.
- **Atomic build tasks live in the spec's `## Build plan`, not here**: scope hanya membawa milestone rollup.
- **Status** `planned` → `in-progress` → `done`, plus `existing` (pre-workflow) dan `dropped` (de-scoped, disimpan untuk sejarah).
- **Approach tag** di samping heading (e.g. `· Facade`) meng-override project default untuk fitur itu; no tag = inherit.
- **Workflow tier tag** di samping heading (e.g. `· GA`, `· Prototype`) mengatur rigor fitur itu di atas atau di bawah project default; no tag inherit default. Dia menentukan kotak check dan saran next tiap skill.
- **Workflow** (header line) adalah project default, apa yang jalan setelah `/develop`: **Prototype** = nothing (percaya develop's own build time self check); **Alpha** = `/check verify`; **Beta** = `/check verify` then `/test`; **GA** = adds fresh model `/check review` then `/document`. Fitur yang di-build atas spec `Assumed` yang tidak diratifikasi tetap flagged, tapi tidak pernah memblokir `done`.
- **Pointer line** (`spec <n> · code in <path>`): spec link ditambah oleh `/architect`, code path oleh `/develop`.

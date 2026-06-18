# 📁 PTP Project Folder Structure

Dokumentasi standar struktur folder yang digunakan dalam project produksi.
Dibuat sebagai referensi bersama — baik untuk anggota tim baru maupun sebagai pengingat saat dibutuhkan.

---

## Daftar Isi

- [Tentang Repo Ini](#tentang-repo-ini)
- [Struktur Folder Umum](#struktur-folder-umum)
- [Struktur Folder Project Blender / 3D](#struktur-folder-project-blender--3d)
- [Konvensi Penamaan](#konvensi-penamaan)
- [Catatan](#catatan)

---

## Tentang Repo Ini

Repo ini **tidak berisi kode**, melainkan berisi panduan dan dokumentasi.

Tujuannya:
- Menyeragamkan cara mengorganisir file di setiap project
- Mempermudah kolaborasi dan handover antar anggota tim
- Menjadi referensi cepat yang bisa diakses kapan saja

---

## Struktur Folder Umum

Template dasar yang berlaku untuk semua jenis project:

```
📁 [YYYYMMDD]_[nama_project]/
├── 📁 00_tools/          # Referensi visual, moodboard, brief dari klien
├── 📁 01_pre_production/         # Aset mentah: model, tekstur, audio, footage
├── 📁 02_production/           # Dokumen: proposal, contract, catatan meeting
├── 📁 03_post_production/           # Output final yang dikirim ke klien
├── 📁 04_cgru/           # Work in progress — file kerja aktif
└── 📁 05_backup/          # Arsip — versi lama atau file yang sudah tidak aktif
```

> **Catatan penamaan folder project:** gunakan format `YYYYMMDD` di awal
> untuk memudahkan pengurutan otomatis berdasarkan tanggal mulai.
> Contoh: `20240315_iklan_produk_A`

---

## Struktur Folder Project Blender / 3D

Perluasan dari template umum, khusus untuk project berbasis Blender:

```
📁 [YYYYMMDD]_[nama_project]/
├── 📁 00_tools/
│   ├── 📁 00_csv/
│   └── 📁 01_preset_script/
│   │   ├── 📁 zeroxe-conf  # config untuk Zeroxe
│   │   │   ├── 📁 builder  # builder untuk Zeroxe
│
├── 📁 01_pre_production/
│   ├── 📁 00_script/
│   ├── 📁 01_animatic/
│   ├── 📁 02_audio/
│   ├── 📁 03_storyboard/
│   └── 📁 04_RND/        

├── 📁 02_production/
│   ├── 📁 01_asset/
│   │   ├── 📁 00_library_asset/    # Berisi file .blend yang bisa di reuse untuk tim asset
│   │   ├── 📁 01_char/             # Berisi file .blend character
│   │   │   └── 📁 c-[nama_character]/  
│   │   ├── 📁 02_prop/             # Berisi file .blend prop
│   │   │   └── 📁 p-[nama_prop]/
│   │   ├── 📁 03_set/              # Berisi file .blend set
│   │   │   └── 📁 s-[nama_set]/
│   │   ├── 📁 04_vehicle/          # Berisi file .blend vehicle
│   │   │   └── 📁 v-[nama_vehicle]/
│   │   └── 📁 05_matte/            # Berisi file image untuk lighting dan background
│   │   │   ├── 📁 mattepainting
│   │   │   └── 📁 skydome
│   ├── 📁 02_layout/ #/var/mnt/I/20260222_melangkah_dari_timur/02_production/02_layout/ep000/ep000_sq01/
│   │   ├── 📁 ep101/
│   │   │   ├── 📁 ep101_sq01
│   │   │   │   ├── 📁 ep101_sq01_sh0010
│   │   │   │   │   │   └── 📁 progress
│   │   │   └── 📁 ep..._sq..sh....
│   │   └── 📁 ep.../       
│   ├── 📁 03_blocking/
│   │   ├── 📁 ep101/
│   │   │   ├── 📁 ep101_sq01
│   │   │   │   ├── 📁 ep101_sq01_sh0010
│   │   │   │   │   │   └── 📁 progress
│   │   │   └── 📁 ep..._sq..
│   │   │   │   ├── 📁 ep..._sq.._sh....
│   │   │   │   │   │   └── 📁 progress
│   │   └── 📁 ep.../
│   └── 📁 04_animation/         
│   │   ├── 📁 ep101/         
│   │   └── 📁 ep.../
│
├── 📁 03_post_production/ 
│   ├── 📁 01_lighting/
│   │   ├── 📁 00_preset_lighting/
│   │   ├── 📁 ep101/         
│   │   └── 📁 ep.../
│   ├── 📁 02_compositing/
│   │   ├── 📁 00_preset_comp/
│   │   ├── 📁 ep101/         
│   │   └── 📁 ep.../
│   ├── 📁 03_vfx/
│   │   ├── 📁 00_library_vfx/
│   │   ├── 📁 ep101/
│   │   └── 📁 ep.../
│   └── 📁 04_editing/
│   │   ├── 📁 00_sound_library/
│   │   │   ├── 📁 amb/              # Berisi file audio ambient sound
│   │   │   ├── 📁 music/            # Berisi file audio music
│   │   │   ├── 📁 sfx/              # Berisi file audio sfx
│   │   │   └── 📁 vo/               # Berisi file audio untuk VO
│   │   ├── 📁 01_title/
│   │   ├── 📁 02_credit_title/
│   │   ├── 📁 03_subtitle/
│   │   ├── 📁 04_projects/
│   │   │   ├── 📁 ep101/
│   │   │   └── 📁 ep.../
│   │   └── 📁 05_exports/
│
└── 📁 04_cgru/
```

---

## Konvensi Penamaan

### Format Umum

```
[tipe]_[deskripsi]_[versi].[ekstensi]
```

Contoh:
- `chr_bajak_laut_kapten_v001.blend` — karakter
- `prp_peti_harta_v002.blend` — prop
- `env_pelabuhan_malam_v001.blend` — environment
- `sc_010_layout_v003.blend` — scene

### Prefix yang Digunakan

| Prefix | Kategori               |
|--------|------------------------|
| `c-`   | Character              |
| `p-`   | Prop                   |
| `s-`   | Environment            |
| `v-`   | Vehicle                |
| `lay`  | Layout                 |
| `blk`  | Blocking               |
| `anm`  | Animation              |
| `lgt`  | Lighting               |
| `comp` | Compositing            |
| `LIT`  | Mastershot Lighting    |
| `COMP` | Mastershot Compositing |

### Versi

- Gunakan versioning dengan 3 digit `v001`, `v002`, dst.

---

## Catatan

Dokumentasi ini bersifat **living document** — akan diperbarui seiring kebutuhan produksi berkembang.

Untuk pertanyaan atau usulan perubahan, silakan buka [Issue](../../issues) di repo ini.

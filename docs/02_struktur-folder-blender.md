# 🎬 Struktur Folder Project Blender / 3D

[← Kembali ke README](../README.md)

Perluasan dari template umum, khusus untuk project berbasis Blender.

---

## Daftar Isi

- [Struktur Lengkap](#struktur-lengkap)
- [Detail Folder Shot](#detail-folder-shot)
- [Detail Folder Asset](#detail-folder-asset)
- [Catatan Penting](#catatan-penting)

---

## Struktur Lengkap

```
📁 [YYYYMMDD]_[nama_project]/
├── 📁 00_tools/
│   ├── 📁 00_csv/
│   └── 📁 01_preset_script/
│       ├── 📁 zeroxe-conf      # config untuk Zeroxe
│       │   └── 📁 builder      # builder untuk Zeroxe
│
├── 📁 01_pre_production/
│   ├── 📁 00_script/
│   ├── 📁 01_animatic/
│   ├── 📁 02_audio/
│   ├── 📁 03_storyboard/
│   └── 📁 04_RND/
│
├── 📁 02_production/
│   ├── 📁 01_asset/
│   │   ├── 📁 00_library_asset/        # Berisi file .blend yang bisa di reuse untuk tim asset
│   │   ├── 📁 01_char/                 # Berisi file .blend character
│   │   │   └── 📁 c-[nama_character]/
│   │   ├── 📁 02_prop/                 # Berisi file .blend prop
│   │   │   └── 📁 p-[nama_prop]/
│   │   ├── 📁 03_set/                  # Berisi file .blend set
│   │   │   └── 📁 s-[nama_set]/
│   │   ├── 📁 04_vehicle/              # Berisi file .blend vehicle
│   │   │   └── 📁 v-[nama_vehicle]/
│   │   └── 📁 05_matte/                # Berisi file image untuk lighting dan background
│   │       ├── 📁 mattepainting
│   │       └── 📁 skydome
│   ├── 📁 02_layout/
│   │   ├── 📁 ep101/
│   │   └── 📁 ep.../
│   ├── 📁 03_blocking/
│   │   ├── 📁 ep101/
│   │   └── 📁 ep.../
│   └── 📁 04_animation/
│       ├── 📁 ep101/
│       └── 📁 ep.../
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
│       ├── 📁 00_sound_library/
│       │   ├── 📁 amb/             # Berisi file audio ambient sound
│       │   ├── 📁 music/           # Berisi file audio music
│       │   ├── 📁 sfx/             # Berisi file audio sfx
│       │   └── 📁 vo/              # Berisi file audio untuk VO
│       ├── 📁 01_title/
│       ├── 📁 02_credit_title/
│       ├── 📁 03_subtitle/
│       ├── 📁 04_projects/
│       │   ├── 📁 ep101/
│       │   └── 📁 ep.../
│       └── 📁 05_exports/
│
└── 📁 04_cgru/
```

---

## Detail Folder Shot

Berlaku untuk folder: `02_layout`, `03_blocking`, `04_animation`, `01_lighting`, `02_compositing`.

```
📁 ep101/
└── 📁 ep101_sq01/
    └── 📁 ep101_sq01_sh0010/
        ├── 📁 progress/
        │   ├── jgt_ep101_sq01_sh0010_lay_v001.blend
        │   ├── jgt_ep101_sq01_sh0010_lay_v002.blend
        │   └── jgt_ep101_sq01_sh0010_lay_v003.blend   # Progress file shot
        └── jgt_ep101_sq01_sh0010_lay.blend            # Main file shot
```

> Untuk type shot lain, ganti bagian `_lay_` menjadi `_blk_`, `_anm_`, `_lgt_`, atau `_comp_`.

---

## Detail Folder Asset

```
📁 01_asset/
├── 📁 01_char/
│   └── 📁 c-dara/
│       ├── 📁 progress/
│       │   ├── c-dara_v001.blend
│       │   └── c-dara_v002.blend       # Progress file Asset
│       └── c-dara.blend                # Main file Asset
├── 📁 02_prop/
│   └── 📁 p-obor/
│       ├── p-obor_v001.blend
│       └── p-obor_v002.blend           # Progress file Asset
│   p-obor.blend                        # Main file Asset
├── 📁 03_set/
│   └── 📁 s-rumah_kakek/
│       ├── s-rumah_kakek_v001.blend
│       └── s-rumah_kakek_v002.blend    # Progress file Asset
│   s-rumah_kakek.blend                 # Main file Asset
├── 📁 04_vehicle/
│   └── 📁 v-mobil_taxi/
│       ├── v-mobil_taxi_v001.blend
│       └── v-mobil_taxi_v002.blend     # Progress file Asset
│   v-mobil_taxi.blend                  # Main file Asset
└── 📁 05_matte/
    ├── 📁 mattepainting
    └── 📁 skydome
```

---

## Catatan Penting

> ⚠️ **Main file harus selalu steril dan bersih.**
>
> File main (yang ada langsung di dalam folder, bukan di dalam `progress/`) adalah file yang akan di-*link* oleh divisi lain (asset maupun file animasi). Jaga agar file ini tidak memiliki data sisa, error, atau perubahan yang belum siap — agar tidak mengganggu alur pipeline divisi lain.

---

## Lihat Juga

- [📂 Struktur Folder Umum](01_struktur-folder-umum.md)
- [🏷️ Konvensi Penamaan](03_konvensi-penamaan.md)

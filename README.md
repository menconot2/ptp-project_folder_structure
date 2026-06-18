<img width="630" height="512" alt="image" src="https://github.com/user-attachments/assets/b764e8da-c6ea-46ea-97d8-0f6a3edbfc79" /># 📁 PTP Project Folder Structure

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
├── 📁 00_tools/                # Berisi utility untuk keperluan tools dan lain lain
├── 📁 01_pre_production/       # Berisi konsep, animatic, storyboard, reff, dlll
├── 📁 02_production/           # Berisi file shot dan asset
├── 📁 03_post_production/      # Berisi file lighting, comp dan vfx
├── 📁 04_cgru/                 # Berisi program afanasy untuk renderfarm
└── 📁 05_backup/               # Arsip — versi lama atau file yang sudah tidak aktif
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
│   ├── 📁 02_layout/
│   │   ├── 📁 ep101/
│   │   └── 📁 ep.../       
│   ├── 📁 03_blocking/
│   │   ├── 📁 ep101/
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

## Detail isi dari struktur folder shot dan asset

### Struktur dalam folder untuk shot dan penamaan filenya

Contoh struktur dan penamaan file blender pada folder shot berlaku untuk layout, blocking, animation, lighting dan compoisiting (jika menggunakan blender):

```
│   │   ├── 📁 ep101/
│   │   │   ├── 📁 ep101_sq01
│   │   │   │   ├── 📁 ep101_sq01_sh0010
│   │   │   │   │   │   └── 📁 progress
│   │   │   │   │   │   │ jgt_ep101_sq01_sh0010_lay_v001.blend
│   │   │   │   │   │   │ jgt_ep101_sq01_sh0010_lay_v002.blend 
│   │   │   │   │   │   │ jgt_ep101_sq01_sh0010_lay_v003.blend   # Progress file shot
│   │   │   │   │   │ jgt_ep101_sq01_sh0010_lay.blend            # Main file shot
│   │   │   └── 📁 ep..._sq..
│   │   │   │   ├── 📁 ep..._sq.._sh....
│   │   │   │   │   │   └── 📁 progress
```
untuk type shot lain tinggal mengganti bagian "_`lay`_" menjadi "`blk`, `anm`, `lgt` dan `comp`"

### Struktur dalam folder untuk Asset dan penamaan filenya

Contoh struktur dan penamaan file blender pada folder Asset:

```
│   │   ├── 📁 01_char/
│   │   │   └── 📁 c-dara/
│   │   │   │   └── 📁progress
│   │   │   │   │ c-dara_v001.blend
│   │   │   │   │ c-dara_v002.blend            # Progress file Asset
│   │   │   │ c-dara.blend                     # Main file Asset
│   │   ├── 📁 02_prop/
│   │   │   └── 📁 p-obor/
│   │   │   │   │ p-obor_v001.blend
│   │   │   │   │ p-obor_v002.blend            # Progress file Asset
│   │   │   │ p-obor.blend                     # Main file Asset
│   │   ├── 📁 03_set/
│   │   │   └── 📁 s-rumah_kakek/
│   │   │   │   │ s-rumah_kakek_v001.blend
│   │   │   │   │ s-rumah_kakek_v002.blend     # Progress file Asset
│   │   │   │ s-rumah_kakek.blend              # Main file Asset
│   │   ├── 📁 04_vehicle/
│   │   │   └── 📁 v-mobil_taxi/
│   │   │   │   │ v-mobil_taxi_v001.blend
│   │   │   │   │ v-mobil_taxi_v002.blend      # Progress file Asset
│   │   │   │ v-mobil_taxi.blend               # Main file Asset
│   │   └── 📁 05_matte/
│   │   │   ├── 📁 mattepainting
│   │   │   └── 📁 skydome
```
### Catatan

Fungsi pada main file blender yang ada pada folder adalah yang nantinya akan di link (asset maupun file anim), diharapkan file main selalu steril dan bersih
agar tidak terjadi error yang di inginkan atau mengganggu alur pipeline divisi lain
    
---

## Konvensi Penamaan

### Format nama Asset

```
[kode_type_asset]_[nama_asset].[ekstensi]          # Untuk asset main
[kode_type_asset]_[nama_asset]_[versi].[ekstensi]  # Untuk asset progress
```

Contoh:
- `c-bajak_laut_kapten_v001.blend` — karakter
- `p-peti_harta_v002.blend` — prop
- `s-pelabuhan_malam_v001.blend` — set

### Format nama Shot

```
[judul_project]_[ep]_[sq]_[sh]_[kode_type_shot].[ekstensi]            # Untuk shot main
[judul_project]_[ep]_[sq]_[sh]_[kode_type_shot]_[versi].[ekstensi]    # Untuk shot progress
```
Contoh:
- `jgt_ep101_sq01_sh0010_lay_v003.blend` — layout
- `rmb_ep105_sq04_sh0210_blk_v003.blend` — blocking

### Kode yang Digunakan

|--------------------------------|
| Kode  | Type Asset             |
|-------|------------------------|
| `c-`  | Character              |
| `p-`  | Prop                   |
| `s-`  | Environment            |
| `v-`  | Vehicle                |
|--------------------------------|

|----------------------------------|
| Kode    | Type Shot              |
|---------|------------------------|
| `lay`   | Layout                 |
| `blk`   | Blocking               |
| `anm`   | Animation              |
| `lgt`   | Lighting               |
| `comp`  | Compositing            |
| `LIT`   | Mastershot Lighting    |
| `COMP`  | Mastershot Compositing |
|----------------------------------|

### Versi

- Untuk episode dimulai dari 100 `ep101`, `ep102`, dst
  jika ada season dua maka akan menjadi `ep201`, `ep301`, dst
- Gunakan kelipatan 10 untuk shot `sh0010`, `sh0020`, `sh0030`, dst
  untuk memberi space extra diantara dua shot `sh0015`, `sh0016`, dst
- Gunakan versioning dengan 3 digit `v001`, `v002`, dst.


---

## Catatan

Dokumentasi ini bersifat **living document** — akan diperbarui seiring kebutuhan produksi berkembang.

Untuk pertanyaan atau usulan perubahan, silakan buka [Issue](../../issues) di repo ini.

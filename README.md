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
├── 📁 _ref/          # Referensi visual, moodboard, brief dari klien
├── 📁 asset/         # Aset mentah: model, tekstur, audio, footage
├── 📁 doc/           # Dokumen: proposal, contract, catatan meeting
├── 📁 out/           # Output final yang dikirim ke klien
├── 📁 wip/           # Work in progress — file kerja aktif
└── 📁 arch/          # Arsip — versi lama atau file yang sudah tidak aktif
```

> **Catatan penamaan folder project:** gunakan format `YYYYMMDD` di awal
> untuk memudahkan pengurutan otomatis berdasarkan tanggal mulai.
> Contoh: `20240315_iklan_produk_A`

---

## Struktur Folder Project Blender / 3D

Perluasan dari template umum, khusus untuk project berbasis Blender:

```
📁 [YYYYMMDD]_[nama_project]/
├── 📁 _ref/
│   ├── 📁 moodboard/
│   └── 📁 brief/
│
├── 📁 asset/
│   ├── 📁 3d/
│   │   ├── 📁 model/       # File .blend model individual (linked library)
│   │   ├── 📁 rig/         # File .blend karakter/objek yang sudah di-rig
│   │   ├── 📁 material/    # File .blend material/shader library
│   │   └── 📁 hdri/        # File HDRI untuk lighting
│   ├── 📁 texture/
│   │   ├── 📁 raw/         # Tekstur original dari sumber eksternal
│   │   └── 📁 pack/        # Tekstur yang sudah diproses/dipaket
│   ├── 📁 audio/
│   └── 📁 footage/         # Video referensi atau footage untuk VFX
│
├── 📁 scene/               # File .blend scene utama (menggunakan linked library)
│   ├── 📁 layout/
│   ├── 📁 anim/
│   └── 📁 render/          # File .blend setup render final
│
├── 📁 render/              # Output render mentah (EXR, PNG sequences)
│   ├── 📁 beauty/
│   └── 📁 pass/            # Render passes (shadow, AO, dll.)
│
├── 📁 comp/                # File compositing (Blender, Nuke, After Effects, dll.)
│
├── 📁 out/                 # Output final — file yang dikirim ke klien
│
├── 📁 doc/
│
└── 📁 arch/
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

| Prefix | Kategori       |
|--------|----------------|
| `chr_` | Character      |
| `prp_` | Prop           |
| `env_` | Environment    |
| `veh_` | Vehicle        |
| `sc_`  | Scene          |
| `mat_` | Material       |
| `rig_` | Rig            |

### Versi

- Gunakan format `v001`, `v002`, dst.
- Jangan hapus versi lama — pindahkan ke folder `arch/`

---

## Catatan

Dokumentasi ini bersifat **living document** — akan diperbarui seiring kebutuhan produksi berkembang.

Untuk pertanyaan atau usulan perubahan, silakan buka [Issue](../../issues) di repo ini.

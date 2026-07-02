# 🏷️ Konvensi Penamaan

[← Kembali ke README](../README.md)

Aturan penamaan file yang digunakan di seluruh project produksi.

---

## Daftar Isi

- [Format Nama Asset](#format-nama-asset)
- [Format Nama Shot](#format-nama-shot)
- [Kode yang Digunakan](#kode-yang-digunakan)
- [Aturan Versi dan Episode](#aturan-versi-dan-episode)

---

## Format Nama Asset

```
[kode_type_asset]-[nama_asset].[ekstensi]              # Untuk asset main
[kode_type_asset]-[nama_asset]_[v + versi].[ekstensi]  # Untuk asset progress
```

Contoh:
- `c-bajak_laut_kapten.blend` — karakter main
- `c-bajak_laut_kapten_v001.blend` — karakter progress
- `p-peti_harta_v002.blend` — prop progress
- `s-pelabuhan_malam.blend` — set main

---

## Format Nama Shot

```
[judul_project]_[ep]_[sq]_[sh]_[kode_type_shot].[ekstensi]              # Untuk shot main
[judul_project]_[ep]_[sq]_[sh]_[kode_type_shot]_[v + versi].[ekstensi]  # Untuk shot progress
```

Contoh:
- `jgt_ep101_sq01_sh0010_lay.blend` — layout main
- `jgt_ep101_sq01_sh0010_lay_v003.blend` — layout progress
- `rmb_ep105_sq04_sh0210_blk_v003.blend` — blocking progress

---

## Kode yang Digunakan

### Kode Type Asset

| Kode | Type Asset  |
|------|-------------|
| `c-` | Character   |
| `p-` | Prop        |
| `s-` | Set / Environment |
| `v-` | Vehicle     |

### Kode Type Shot

| Kode   | Type Shot              |
|--------|------------------------|
| `lay`  | Layout                 |
| `blk`  | Blocking               |
| `anm`  | Animation              |
| `lgt`  | Lighting               |
| `comp` | Compositing            |
| `LIT`  | Mastershot Lighting    |
| `COMP` | Mastershot Compositing |

---

## Aturan Versi dan Episode

**Episode:**
- Dimulai dari `ep101`, `ep102`, dst.
- Jika ada season dua: `ep201`, `ep202`, dst.

**Shot:**
- Gunakan kelipatan 10: `sh0010`, `sh0020`, `sh0030`, dst.
- Kelipatan 10 memberi ruang untuk shot sisipan: `sh0015`, `sh0016`, dst.

**Versi:**
- Gunakan 3 digit: `v001`, `v002`, dst.
- File progress disimpan di dalam folder `progress/` — jangan dihapus.

---

## Lihat Juga

- [📂 Struktur Folder Umum](01_struktur-folder-umum.md)
- [🎬 Struktur Folder Blender / 3D](02_struktur-folder-blender.md)

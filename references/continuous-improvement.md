# Perbaikan Berkelanjutan Skill

Gunakan modul ini untuk menjaga skill `verify-technical-claims` terus meningkat lintas sesi. Tujuannya adalah menuju ketelitian yang makin tinggi, bukan mengklaim kesempurnaan absolut.

## Prinsip

- Anggap skill sebagai sistem hidup yang harus diperbarui ketika ada bukti, koreksi, contoh kasus, atau kebutuhan metodologis baru.
- Perlakukan "sempurna" sebagai target asimtotik: didekati melalui validasi berulang, bukan status final yang diklaim sekali.
- Jangan menambahkan aturan baru berdasarkan intuisi saja; dasarkan pada kegagalan nyata, kebutuhan user, sumber ilmiah, standar, atau praktik formal yang dapat dipertanggungjawabkan.
- Hindari memperbesar skill tanpa alasan. Tambahkan modul hanya bila mengurangi risiko, biaya, atau ambiguitas pada penggunaan nyata.

## Kapan Harus Diperbarui

Perbarui skill bila salah satu kondisi terjadi:

- User secara eksplisit meminta skill diperbarui, disempurnakan, atau diperbaiki.
- Ada celah metodologis baru, misalnya domain fisika, AI, matematika, atau pasar yang belum tertangani.
- Hasil penggunaan skill menunjukkan lompatan inferensi, istilah ambigu, atau format jawaban kurang membantu.
- Ada sumber ilmiah/standar baru yang mengubah cara klaim seharusnya dinilai.
- Ada pola klaim berulang yang layak dibuatkan modul, template, checklist, atau referensi khusus.

Jika user tidak meminta perubahan file, cukup laporkan rekomendasi pembaruan dan jangan mengubah skill diam-diam.

## Cara Memperbarui

1. Identifikasi kekurangan spesifik.
   - Apa yang gagal?
   - Pada bagian mana: sumber, premis, notasi, inferensi, domain, fisika, keputusan pra-empiris, atau format jawaban?

2. Tentukan bentuk pembaruan minimal.
   - Ubah `SKILL.md` bila instruksi inti atau trigger perlu diperbaiki.
   - Tambah/ubah file `references/` bila butuh modul khusus.
   - Tambah `scripts/` hanya bila proses perlu otomatisasi deterministik.

3. Jaga pemisahan konteks.
   - Instruksi inti tetap ringkas di `SKILL.md`.
   - Detail domain pindahkan ke `references/`.
   - Jangan menduplikasi penjelasan panjang di banyak tempat.

4. Validasi.
   - Jalankan validator skill setelah perubahan.
   - Jika ada skrip baru, jalankan contoh minimal.
   - Bila pembaruan kompleks, uji dengan satu prompt realistis.

5. Laporkan perubahan.
   - Sebutkan file yang diubah.
   - Sebutkan kemampuan baru.
   - Sebutkan batasan yang masih tersisa.

## Skala Kematangan

Gunakan skala ini saat menilai apakah skill sudah cukup baik:

- `Draft`: instruksi dasar ada, belum diuji pada kasus nyata.
- `Valid awal`: struktur valid dan bisa dipakai untuk kasus sederhana.
- `Layak pakai`: sudah mencakup workflow utama, batasan, dan validasi dasar.
- `Kuat`: sudah diuji pada beberapa domain dan punya modul pendukung.
- `Sangat kuat`: sudah punya contoh uji nyata, modul domain, dan koreksi dari kegagalan sebelumnya.

Jangan gunakan label `sempurna` kecuali user memakainya sebagai aspirasi; tetap jelaskan bahwa kesempurnaan praktis memerlukan penggunaan dan pembaruan berulang.

## Template Catatan Pembaruan

```text
Pemicu:
<permintaan user, kegagalan, atau celah baru>

Masalah:
<apa yang belum ditangani skill>

Perubahan:
<file dan instruksi baru>

Validasi:
<validator, uji contoh, atau alasan belum diuji>

Batasan tersisa:
<hal yang masih perlu diperbaiki>
```

## Aturan Lintas Sesi

Karena skill berada di folder default Codex, perubahan file skill akan tersedia untuk sesi berikutnya ketika skill terdeteksi atau dipanggil. Namun penggunaan lintas sesi tetap bergantung pada apakah skill ini dipicu oleh prompt user atau disebut eksplisit.

# Protokol Meta-Validasi

Gunakan modul ini untuk menguji kualitas hasil skill `verify-technical-claims` dan menemukan celah yang perlu diperbaiki. Modul ini ada karena penguji kebenaran tidak boleh menjadi satu-satunya hakim atas kebenaran dirinya sendiri.

## Prinsip

- Bedakan `terbukti di dalam sistem` dari `benar dalam model/sumber eksternal`.
- Perlakukan hasil skill sebagai hipotesis evaluatif yang harus bisa dikritik.
- Gunakan pembanding luar: paper, textbook, standar, data, reviewer, proof assistant, solver, atau contoh yang jawabannya sudah diketahui.
- Cari cara mematahkan keputusan skill, bukan hanya cara mendukungnya.
- Catat kegagalan sebagai bahan pembaruan skill.

## Rujukan Jangkar

- Gödel incompleteness: `https://plato.stanford.edu/entries/goedel-incompleteness/`
- Popper/falsifiability: `https://plato.stanford.edu/entries/popper/`
- Metamorphic testing untuk oracle problem: `https://pmc.ncbi.nlm.nih.gov/articles/PMC7252536/`
- NIST formal methods verification and validation: `https://www.nist.gov/publications/cost-effective-use-formal-methods-verification-and-validation-foundations`

## Kapan Wajib Dipakai

Jalankan meta-validasi bila:

- keputusan skill akan menentukan biaya besar, eksperimen mahal, atau implementasi panjang;
- klaim bersifat teori baru, rumus fisika baru, arsitektur AI baru, atau klaim pasar besar;
- skill memberi keputusan kuat seperti `Benar`, `Hentikan`, atau `Lanjut ke simulasi`;
- user mempertanyakan apakah skill itu sendiri sudah cukup benar;
- ada konflik sumber atau premis empiris yang belum kuat.

## Empat Lapisan Uji

### 1. Known-Answer Tests

Uji skill dengan kasus yang jawabannya sudah mapan.

Contoh:

- rumus dengan dimensi salah harus ditolak;
- klaim yang melanggar konservasi energi tanpa mekanisme harus ditandai;
- derivasi `E = mc^2` harus dikenali sebagai derivasi bersyarat dari relativitas, bukan bukti empiris final;
- argumen modus ponens valid harus dikenali valid bila premis benar.

Jika skill gagal pada kasus mapan, perbarui instruksi atau referensi.

### 2. Adversarial Tests

Buat kasus jebakan untuk menemukan kelemahan.

Jenis jebakan:

- premis empiris palsu tetapi inferensi valid;
- istilah berubah makna di tengah argumen;
- domain terlalu luas;
- rumus memakai konstanta benar tetapi hubungan salah;
- klaim "lebih baik" tanpa baseline;
- teori yang unfalsifiable.

Skill harus menolak atau mempersempit klaim tersebut.

### 3. Metamorphic Tests

Gunakan ketika jawaban benar sulit diketahui langsung. Ubah input dengan cara yang seharusnya tidak mengubah inti keputusan, lalu bandingkan hasil.

Relasi metamorfik yang berguna:

- Mengganti nama variabel tidak boleh mengubah validitas argumen.
- Menambahkan premis yang tidak relevan tidak boleh membuat klaim menjadi lebih benar.
- Mempersempit domain boleh menguatkan klaim; memperluas domain harus meningkatkan kehati-hatian.
- Menghapus sumber primer harus menurunkan kekuatan keputusan.
- Mengubah satuan fisika tidak boleh mengubah isi rumus bila konversinya benar.

Jika keputusan berubah tanpa alasan logis, ada celah.

### 4. External Oracle

Bandingkan hasil dengan hakim eksternal.

Gunakan sesuai kebutuhan:

- paper riset atau textbook untuk klaim ilmiah;
- standar resmi untuk satuan, protokol, atau definisi;
- proof assistant seperti Lean/Coq/Isabelle untuk pembuktian matematis formal bila tersedia;
- SMT solver seperti Z3 untuk konsistensi logika terbatas bila cocok;
- eksperimen mini atau data pendahuluan untuk premis empiris.

Jangan menganggap satu oracle sempurna. Bila oracle berbeda, laporkan konflik dan tingkat kepercayaannya.

## Skor Kepercayaan Hasil

Berikan label internal:

- `A`: lolos sumber primer, known-answer/adversarial test, dan tidak ada konflik penting.
- `B`: argumen kuat, tetapi salah satu lapisan uji belum lengkap.
- `C`: hanya valid bersyarat; premis empiris atau domain masih lemah.
- `D`: banyak asumsi belum teruji atau sumber tidak cukup.
- `F`: gagal logika, gagal sumber, atau kontradiktif.

Label ini bukan kebenaran absolut; ini ukuran kematangan evaluasi.

## Template Meta-Validasi

```text
Keputusan awal skill:
<status dan keputusan pra-empiris>

Known-answer/adversarial check:
<hasil>

Metamorphic check:
<perubahan input dan apakah keputusan stabil>

External oracle:
<paper/standar/prover/data dan hasil perbandingan>

Skor kepercayaan:
<A/B/C/D/F>

Celah skill:
<apa yang perlu diperbaiki>

Rekomendasi pembaruan:
<ubah SKILL.md, tambah referensi, tambah script, atau cukup catat batasan>
```

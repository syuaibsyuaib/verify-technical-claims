# Kerangka Logika Formal untuk Klaim Teknis

Gunakan referensi ini ketika klaim perlu dibuktikan atau dibantah secara eksplisit.

## 1. Normalisasi Klaim

Ubah klaim natural language menjadi bentuk:

- Objek: sistem, metode, teknologi, pasar, atau fenomena yang dibahas.
- Predikat: sifat yang diklaim, misalnya lebih cepat, aman, feasible, optimal, murah, akurat.
- Kondisi: batas lingkungan, asumsi, skala, data, perangkat, pasar, atau periode waktu.
- Pembanding: baseline yang dipakai bila klaim bersifat komparatif.
- Domain/model: himpunan objek yang dibicarakan dan interpretasi predikat/relasi.

Contoh:

```text
Klaim natural: "Metode X lebih efisien untuk inference LLM."
Bentuk uji: Untuk workload W pada hardware H dan metrik M, metode X menghasilkan M yang lebih baik daripada baseline B.
```

## 2. Jenis Premis

Pisahkan premis ke dalam kelas berikut:

- Premis empiris: didukung paper, benchmark, observasi, laporan pasar, atau dokumentasi.
- Premis definisional: berasal dari definisi istilah atau standar.
- Premis kausal: menyatakan hubungan sebab akibat.
- Premis kondisional: hanya berlaku dalam kondisi tertentu.
- Asumsi kerja: belum terbukti, tetapi diperlukan agar argumen bisa diuji.
- Aksioma/postulat: pernyataan primitif yang dipilih sebagai dasar sistem formal; jangan perlakukan sebagai fakta empiris kecuali didukung sumber/observasi.

Tandai setiap premis dengan status:

- `terdukung kuat`
- `terdukung terbatas`
- `diperdebatkan`
- `tidak terverifikasi`
- `bertentangan dengan sumber`

## 3. Bentuk Inferensi yang Umum

Gunakan bentuk argumen yang sederhana dan eksplisit.

Catatan metode:

- Gunakan tabel kebenaran untuk logika proposisional dengan jumlah atom terbatas.
- Gunakan pembuktian deduktif atau model/interpretasi untuk logika first-order, klaim berkuantor, relasi temporal, atau domain yang eksplisit.
- Gunakan evaluasi bukti empiris untuk premis tentang dunia nyata; validitas logis tidak otomatis membuktikan premis empiris benar.

### Modus Ponens

```text
P1. Jika A maka B.
P2. A benar.
C. Maka B.
```

Validitas: valid bila P1 dan P2 benar.

### Modus Tollens

```text
P1. Jika A maka B.
P2. B salah.
C. Maka A salah.
```

Validitas: valid bila P1 dan P2 benar.

### Silogisme Hipotetis

```text
P1. Jika A maka B.
P2. Jika B maka C.
C. Maka jika A maka C.
```

Validitas: valid, tetapi kekuatan empiris tergantung dukungan untuk P1 dan P2.

### Argumen Komparatif

```text
P1. Dalam kondisi K, metrik M untuk X lebih baik daripada Y.
P2. M adalah metrik relevan untuk tujuan T.
P3. Kondisi user termasuk K.
C. Untuk tujuan T pada kondisi user, X lebih baik daripada Y.
```

Risiko: P3 sering menjadi titik lemah karena kondisi nyata tidak sama dengan benchmark.

### Argumen Probabilistik

```text
P1. Bukti E meningkatkan probabilitas H.
P2. Tidak ada bukti kuat yang menurunkan H secara signifikan.
C. H lebih plausibel daripada alternatif yang tersedia.
```

Catatan: ini mendukung plausibilitas, bukan bukti deduktif absolut.

## 4. Pemeriksaan Kekeliruan

Cari masalah berikut sebelum memberi kesimpulan:

- Equivocation: istilah berubah makna di tengah argumen.
- Hasty generalization: hasil pada sampel kecil digeneralisasi terlalu luas.
- False equivalence: dua sistem dianggap setara padahal kondisi berbeda.
- Correlation-causation error: korelasi dipakai sebagai bukti sebab akibat.
- Benchmark mismatch: metrik, data, hardware, atau skala tidak sesuai klaim.
- Vendor bias: bukti berasal dari pihak yang punya kepentingan langsung.
- Missing baseline: klaim "lebih baik" tanpa pembanding yang jelas.

## 5. Mapping Kesimpulan

Gunakan mapping berikut:

- `Benar`: premis penting terdukung kuat dan inferensi valid untuk ruang lingkup klaim.
- `Sebagian benar`: ada bagian yang terdukung, tetapi ruang lingkup klaim terlalu luas.
- `Plausibel tetapi belum terbukti`: argumen masuk akal, tetapi bukti empiris belum cukup.
- `Tidak didukung`: tidak ada bukti relevan yang cukup, atau premis kunci tidak terverifikasi.
- `Salah/bertentangan`: klaim berlawanan dengan bukti kuat atau inferensinya kontradiktif.

## 6. Template Internal

```text
Klaim K:
Domain/model:
Subklaim:
S1.
S2.

Sumber:
R1.
R2.

Premis:
P1. [empiris, status, sumber]
P2. [definisional/aksioma/asumsi]
P3. [kondisional]

Inferensi:
I1. Dari P1 dan P2, ...
I2. Dari I1 dan P3, ...

Uji:
- Apakah premis faktual benar?
- Apakah kesimpulan mengikuti premis?
- Apakah ruang lingkup kesimpulan lebih luas dari bukti?

Keputusan:
Status:
Alasan:
Batasan:
```

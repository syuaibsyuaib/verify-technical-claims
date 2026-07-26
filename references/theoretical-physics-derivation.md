# Modul Derivasi Rumus Fisika Teoretis

Gunakan modul ini ketika user ingin membuat, menurunkan, atau menyaring kandidat rumus fisika sebelum simulasi atau eksperimen mahal. Tujuannya adalah menghasilkan kandidat rumus yang konsisten secara logika dan fisika, bukan mengklaim hukum alam baru tanpa uji empiris.

## Batas Kemampuan

Modul ini dapat membantu:

- merumuskan postulat fisika dan asumsi operasional;
- menentukan variabel, observabel, dan domain berlaku;
- menurunkan konsekuensi matematis dari postulat;
- memeriksa dimensi/satuan;
- memeriksa simetri, invariansi, dan hukum konservasi;
- membandingkan dengan teori mapan;
- menentukan apakah konsep layak lanjut ke simulasi.

Modul ini tidak boleh mengklaim:

- hukum fisika baru terbukti benar hanya dari logika;
- parameter numerik nyata benar tanpa pengukuran;
- prediksi empiris sudah benar sebelum diuji;
- rumus berlaku universal bila domainnya belum dibuktikan.

## Rujukan Jangkar

Gunakan rujukan primer/otoritatif ketika menilai klaim fisika:

- Einstein 1905, mass-energy equivalence (terjemahan resmi, The Einstein Papers Project, Princeton University Press): `https://einsteinpapers.press.princeton.edu/vol2-trans/186`
- Stanford Encyclopedia of Philosophy, mass-energy equivalence: `https://plato.stanford.edu/entries/equivME/`
- NIST SI units: `https://www.nist.gov/pml/owm/metric-si/si-units`
- Stanford Encyclopedia of Philosophy, symmetry and symmetry breaking: `https://plato.stanford.edu/entries/symmetry-breaking/`

Jika domainnya relativitas, kuantum, termodinamika, elektromagnetisme, fluida, atau kosmologi, cari juga paper, textbook, standar, atau review primer yang khusus untuk domain itu sebelum membuat keputusan.

## Alur Derivasi

1. Definisikan fenomena.
   - Apa yang ingin dijelaskan?
   - Apa observabel yang bisa diukur?
   - Apa domainnya: klasik, relativistik, kuantum, termal, kontinu, diskret, mikroskopik, makroskopik?

2. Tentukan variabel dan satuan.
   - Tulis semua variabel dengan satuan SI atau satuan natural yang dinyatakan eksplisit.
   - Bedakan konstanta universal, parameter sistem, dan variabel bebas.
   - Jangan lanjut bila besaran kiri dan kanan rumus tidak berdimensi sama.

3. Nyatakan postulat/asumsi.
   - Pisahkan postulat fisika mapan dari asumsi baru.
   - Tandai asumsi yang hanya bersifat model atau aproksimasi.
   - Jangan menyembunyikan asumsi dalam simbol.

4. Terapkan batas fisika.
   - Konservasi energi, momentum, momentum sudut, muatan, probabilitas, atau besaran relevan lainnya.
   - Simetri translasi, rotasi, Lorentz, gauge, paritas, skala, atau simetri lain bila relevan.
   - Catatan: hubungan simetri dan konservasi harus dipakai hati-hati; teorema Noether berlaku dalam kerangka aksi/Lagrangian dengan syarat matematis tertentu.

5. Turunkan kandidat rumus.
   - Gunakan aljabar, kalkulus, persamaan diferensial, variasi aksi, atau analisis dimensi sesuai domain.
   - Tulis langkah derivasi secara eksplisit.
   - Beri label mana yang deduksi, aproksimasi, atau input empiris.

6. Uji batas kasus.
   - Apakah rumus kembali ke teori mapan pada limit yang sesuai?
   - Contoh limit: kecepatan rendah, medan lemah, energi rendah, ukuran besar, temperatur nol/tinggi, waktu pendek/panjang.
   - Jika gagal pada limit mapan, konsep harus direvisi atau domainnya dipersempit.

7. Buat prediksi minimal.
   - Tentukan satu prediksi yang membedakan rumus ini dari teori lama.
   - Pilih uji murah yang paling mungkin mematahkan asumsi kunci.
   - Jangan menyarankan simulasi besar sebelum ada prediksi dan kriteria gagal.

## Checklist Wajib

Sebelum memberi keputusan, jawab:

- Apakah semua variabel punya makna fisik?
- Apakah dimensi kiri dan kanan sama?
- Apakah domain berlaku eksplisit?
- Apakah rumus menghormati hukum konservasi yang relevan?
- Apakah simetri yang diklaim benar-benar berlaku pada sistem?
- Apakah rumus punya batas klasik atau batas teori mapan?
- Apakah ada parameter bebas yang hanya dipasang agar hasil cocok?
- Apakah ada prediksi falsifiable?
- Apa uji paling murah sebelum simulasi besar?

## Red Flags

Hentikan atau minta revisi bila:

- satuan/dimensi tidak cocok;
- kesimpulan muncul dari definisi melingkar;
- rumus memakai konstanta tanpa alasan fisik;
- klaim melanggar konservasi tanpa mekanisme kompensasi;
- rumus berlaku universal tetapi dibangun dari domain sempit;
- tidak ada observabel yang bisa diuji;
- hasil bergantung pada frame acuan tanpa aturan transformasi;
- prediksi tidak berbeda dari teori lama.

## Template Output

```text
Fenomena:
Domain:
Observabel:

Legenda:
<simbol dan satuan>

Postulat/Asumsi:
A1. [mapan/baru/aproksimasi]
A2. [mapan/baru/aproksimasi]

Kandidat Rumus:
<rumus>

Derivasi Ringkas:
D1.
D2.
D3.

Uji Dimensi:
Kiri:
Kanan:
Status:

Uji Fisika:
Simetri/Invariansi:
Konservasi:
Batas Kasus:

Keputusan Pra-Empiris:
<Lanjut ke simulasi | Revisi dulu | Butuh data pendahuluan | Hentikan>

Prediksi dan Uji Murah:
<prediksi, cara uji, kriteria gagal>
```

## Pola Einstein sebagai Contoh Metode

Gunakan ini sebagai pola kerja, bukan sebagai template yang selalu menghasilkan hukum besar:

```text
P1. Tetapkan postulat fisika yang kuat.
P2. Pilih situasi ideal yang sederhana.
P3. Bandingkan deskripsi dari kerangka/model yang relevan.
P4. Paksa konsistensi energi, momentum, atau invarian.
P5. Turunkan konsekuensi matematis.
P6. Ajukan prediksi yang bisa diuji.
```

Pada derivasi massa-energi, pola pentingnya bukan sekadar simbol `E = mc^2`, tetapi disiplin: postulat relativitas, model emisi radiasi, transformasi antar kerangka, dan konsekuensi terukur. Setelah derivasi, eksperimen tetap diperlukan untuk mengonfirmasi dunia nyata.

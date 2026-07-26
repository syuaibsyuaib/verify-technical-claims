# Gerbang Uji Pra-Empiris

Gunakan referensi ini ketika user ingin membuktikan atau menyaring konsep sebelum simulasi, eksperimen, atau implementasi yang memakan biaya, waktu, dan energi.

## Tujuan

Logika formal dapat mengurangi risiko sebelum uji empiris dengan cara:

- membuktikan bahwa kesimpulan mengikuti asumsi tertentu;
- menemukan kontradiksi internal;
- menunjukkan asumsi tersembunyi yang wajib benar;
- membatasi domain tempat klaim mungkin berlaku;
- menolak konsep yang gagal secara logis sebelum diuji mahal;
- merancang uji minimal yang paling informatif bila bukti formal belum cukup.

Logika formal tidak dapat sendirian membuktikan:

- performa runtime nyata;
- akurasi empiris;
- stabilitas hardware;
- efisiensi energi aktual;
- adopsi pasar;
- efek kausal dunia nyata;
- hasil benchmark yang belum dijalankan.

## Keputusan Pra-Empiris

Gunakan salah satu keputusan berikut:

- `Lanjut ke simulasi`: tidak ada kontradiksi, premis kunci masuk akal/terdukung, dan simulasi punya tujuan yang jelas.
- `Revisi dulu`: struktur logika bisa diselamatkan, tetapi ada definisi, domain, asumsi, atau inferensi yang masih lemah.
- `Butuh data pendahuluan`: logika bersyarat valid, tetapi premis empiris utama belum punya dukungan cukup.
- `Hentikan`: konsep mengandung kontradiksi, melanggar batas teoretis yang kuat, atau kesimpulan tidak mengikuti premis.

## Checklist Penyaringan

Periksa hal berikut sebelum menyarankan simulasi:

1. Apakah klaim utama bisa ditulis sebagai proposisi atau formula yang jelas?
2. Apakah domain dan batas kondisi sudah eksplisit?
3. Apakah semua predikat/relasi didefinisikan?
4. Apakah ada premis yang bertentangan dengan sumber ilmiah atau batas matematis?
5. Apakah kesimpulan mengikuti premis tanpa lompatan tersembunyi?
6. Apakah konsep bisa gagal walau argumennya valid karena premis empiris belum terbukti?
7. Apakah ada uji murah yang bisa mematahkan premis paling berisiko?

## Bentuk Pembuktian yang Berguna

### Bukti Kondisional

```text
Jika P1, P2, dan P3 benar, maka C mengikuti.
P1 dan P2 terdukung; P3 belum teruji.
Keputusan: butuh data pendahuluan untuk P3 sebelum simulasi besar.
```

### Bukti Kontradiksi

```text
Asumsikan konsep K benar.
Dari K dan batas B, diperoleh C.
Namun C bertentangan dengan P yang terdukung kuat.
Maka K tidak dapat diterima dalam bentuk saat ini.
```

### Bukti Kelayakan Minimal

```text
Konsep K hanya layak diuji jika syarat S1, S2, dan S3 terpenuhi.
S1 terdukung, S2 lemah, S3 tidak diketahui.
Keputusan: revisi dulu atau lakukan uji murah untuk S2/S3.
```

## Output yang Diharapkan

Selalu berikan:

- status kebenaran konsep;
- keputusan pra-empiris;
- premis terkuat;
- premis paling rapuh;
- kontradiksi atau lompatan inferensi bila ada;
- uji minimal berikutnya yang paling murah dan paling informatif.

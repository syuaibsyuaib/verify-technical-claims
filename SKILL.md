---
name: verify-technical-claims
description: Verify technical claims and concepts by checking facts against research papers, standards, official documentation, reputable web sources, and market publications before deciding. Use when the user asks to "cek kebenaran konsep ini", validate a technical idea, prove or disprove a technical claim, compare a concept with scientific evidence, assess market-backed feasibility, derive or screen a candidate physics formula before simulation, or request formal-logic reasoning for a technical claim.
---

# Verify Technical Claims

## Tujuan

Gunakan skill ini sebagai gerbang uji pra-empiris untuk memeriksa klaim teknis sebelum simulasi atau implementasi yang mahal: kumpulkan bukti dari sumber tepercaya, ubah klaim menjadi premis dan kesimpulan, uji validitas logikanya, lalu jawab dalam bahasa Indonesia dengan status kebenaran yang proporsional terhadap bukti.

## Prinsip Utama

- Jangan membuat keputusan sebelum memeriksa fakta dan referensi yang relevan.
- Gunakan sumber primer terlebih dahulu: paper riset, standar, dokumentasi resmi, spesifikasi teknis, laporan regulator, atau data vendor resmi.
- Untuk klaim pasar, gunakan market publications yang kredibel: laporan analis, filing perusahaan, laporan industri, data adopsi, benchmark, atau publikasi vendor dengan catatan bias.
- Pisahkan tiga hal: kebenaran empiris premis, validitas inferensi, dan kekuatan kesimpulan.
- Perlakukan aksioma sebagai postulat/asumsi primitif dalam sistem formal, bukan otomatis sebagai "kebenaran mutlak" di dunia empiris.
- Tentukan domain, predikat, relasi, kondisi, dan model semantik sebelum menilai klaim yang memakai kuantor atau struktur first-order.
- Jangan menyebut konsep "terbukti benar" bila bukti hanya menunjukkan "didukung", "plausibel", atau "belum cukup bukti".
- Gunakan pembuktian formal untuk menyaring konsep sebelum eksperimen: temukan kontradiksi, asumsi tersembunyi, syarat minimal, dan konsekuensi logis yang wajib benar bila konsep ingin berhasil.
- Jangan mengklaim performa empiris, efisiensi runtime, stabilitas hardware, atau dampak pasar sebagai terbukti hanya dari logika formal.
- Untuk kandidat rumus fisika, wajib periksa dimensi/satuan, simetri/invariansi, hukum konservasi, batas kasus, dan prediksi teruji sebelum menyarankan simulasi.
- Perlakukan skill ini sebagai sistem yang harus terus diperbaiki menuju ketelitian yang lebih tinggi; gunakan `references/continuous-improvement.md` ketika ada koreksi, celah, contoh baru, atau kebutuhan metodologis baru.
- Jangan biarkan skill menjadi hakim tunggal atas dirinya sendiri; gunakan `references/meta-validation-protocol.md` untuk menguji hasil skill dengan kasus pembanding, sumber eksternal, falsifikasi, dan pemeriksaan lintas-metode.
- Bila web tersedia dan klaim bergantung pada informasi mutakhir, lakukan pencarian web. Berikan tautan sumber yang dipakai.

## Alur Kerja

1. Klarifikasi klaim.
   - Nyatakan klaim utama dalam satu kalimat.
   - Pecah klaim menjadi subklaim teknis yang bisa diuji.
   - Tandai istilah yang ambigu dan buat asumsi eksplisit bila perlu.

2. Kumpulkan referensi.
   - Cari paper riset, standar, dokumentasi resmi, atau publikasi pasar yang langsung relevan.
   - Prioritaskan sumber primer dan terbaru bila topiknya berubah cepat.
   - Catat keterbatasan sumber: simulasi, sampel kecil, konflik kepentingan, benchmark tidak sebanding, atau publikasi vendor.

3. Bentuk model logika.
   - Tulis premis faktual yang didukung sumber.
   - Tulis premis definisional, aksioma/postulat, atau asumsi operasional.
   - Nyatakan domain pembicaraan dan batas berlakunya setiap predikat.
   - Gunakan notasi matematika yang konsisten dan sertakan legenda simbol bila rumus tidak trivial.
   - Tulis kesimpulan yang ingin dibuktikan.
   - Gunakan kerangka di `references/formal-logic-framework.md` bila klaim membutuhkan struktur formal.
   - Gunakan panduan di `references/symbol-notation-guidelines.md` bila perlu memilih simbol, operator, kuantor, relasi, atau kode LaTeX.
   - Gunakan `references/theoretical-physics-derivation.md` bila user ingin menciptakan, menurunkan, atau menyaring kandidat rumus fisika.

4. Uji validitas.
   - Periksa apakah kesimpulan mengikuti premis.
   - Gunakan tabel kebenaran hanya untuk klaim logika proposisional yang atom-atomnya terbatas.
   - Untuk klaim berkuantor, temporal, probabilistik, atau empiris, gunakan pembuktian deduktif, model/interpretasi, atau evaluasi bukti yang sesuai.
   - Identifikasi lompatan inferensi, hidden assumptions, generalisasi berlebihan, atau kontradiksi.
   - Bedakan "argumen valid jika premis benar" dari "premis terbukti benar oleh bukti".
   - Gunakan `references/pre-empirical-gate.md` untuk memutuskan apakah konsep layak lanjut ke simulasi.

5. Beri keputusan.
   - Gunakan status: `Benar`, `Sebagian benar`, `Plausibel tetapi belum terbukti`, `Tidak didukung`, atau `Salah/bertentangan`.
   - Tambahkan keputusan pra-empiris: `Lanjut ke simulasi`, `Revisi dulu`, `Butuh data pendahuluan`, atau `Hentikan`.
   - Sertakan ringkasan bukti dan kelemahan.
   - Jika bukti kurang, sebutkan data atau eksperimen yang diperlukan untuk memutuskan.
   - Untuk konsep berisiko tinggi, baru, atau bernilai mahal, jalankan protokol meta-validasi sebelum menyatakan keputusan final.
   - Jika penggunaan skill mengungkap kekurangan baru, catat rekomendasi pembaruan; bila user meminta pembaruan skill, perbarui file skill dan validasi ulang.

## Format Jawaban

Gunakan struktur ini kecuali user meminta format lain:

```markdown
**Kesimpulan**
Status: <Benar | Sebagian benar | Plausibel tetapi belum terbukti | Tidak didukung | Salah/bertentangan>
Keputusan Pra-Empiris: <Lanjut ke simulasi | Revisi dulu | Butuh data pendahuluan | Hentikan>
<1-3 kalimat ringkasan keputusan.>

**Bukti Utama**
- <Sumber dan temuan singkat>
- <Sumber dan temuan singkat>

**Logika Formal Ringkas**
Klaim: <klaim utama>
Domain/Model: <domain, predikat, relasi, kondisi berlaku>
Legenda Simbol: <simbol penting dan artinya, bila diperlukan>
Premis:
P1. <premis yang didukung sumber>
P2. <premis definisional/aksioma/asumsi>
Inferensi:
<aturan atau bentuk argumen>
Kesimpulan:
C. <kesimpulan dan apakah mengikuti secara valid>

**Batasan**
- <ketidakpastian, asumsi, atau bukti yang kurang>

**Langkah Hemat Biaya Berikutnya**
- <uji minimal, bukti tambahan, atau revisi konsep sebelum simulasi besar>
```

Untuk kandidat rumus fisika, tambahkan bagian ringkas:

```markdown
**Uji Rumus Fisika**
Kandidat Rumus: <rumus>
Cek Dimensi: <lulus/gagal dan satuan>
Simetri/Invariansi: <prinsip yang dipakai>
Konservasi: <energi, momentum, muatan, atau lainnya>
Batas Kasus: <limit klasik/kecepatan rendah/skala kecil/dll>
Prediksi Teruji: <apa yang bisa diuji secara murah>
```

## Aturan Sitasi

- Sertakan tautan sumber untuk setiap keputusan faktual penting.
- Jangan mengutip panjang dari satu sumber. Parafrase dan ringkas.
- Bila sumber saling bertentangan, tampilkan konflik itu dan jelaskan sumber mana yang lebih kuat.
- Bila hanya menemukan sumber sekunder, katakan bahwa kesimpulan masih perlu diverifikasi dengan sumber primer.

## Perbaikan Berkelanjutan

- Gunakan `references/continuous-improvement.md` saat user meminta skill ini disempurnakan, saat ada kritik terhadap hasil, atau saat muncul jenis klaim baru yang belum tertangani.
- Gunakan `references/meta-validation-protocol.md` saat perlu menemukan celah skill, menguji hasil penting, atau menghindari siklus "penguji menguji dirinya sendiri".
- Jangan mengklaim skill ini sempurna secara absolut. Nyatakan tingkat kematangan berdasarkan validasi, cakupan domain, dan hasil penggunaan nyata.
- Setelah mengubah skill, selalu jalankan validator skill bila tersedia.

## Gaya

- Jawab dalam bahasa Indonesia.
- Gunakan bahasa tegas tetapi tidak berlebihan.
- Hindari klaim absolut untuk domain empiris kecuali bukti sangat kuat.
- Jelaskan logika secukupnya agar user dapat memeriksa alur pembuktian.

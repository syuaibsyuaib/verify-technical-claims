# Panduan Notasi Simbolik

Gunakan referensi ini ketika klaim teknis perlu diterjemahkan ke simbol matematika atau LaTeX. Tujuannya bukan memperbanyak simbol, tetapi mengurangi ambiguitas.

## Prinsip

- Pilih simbol yang umum dalam domain terkait bila ada konvensi yang jelas.
- Jangan memakai satu simbol untuk dua makna berbeda dalam argumen yang sama.
- Jangan memakai dua simbol berbeda untuk makna yang sama kecuali ada alasan eksplisit.
- Sertakan legenda simbol untuk rumus non-trivial.
- Gunakan kata biasa bila simbol membuat argumen lebih kabur.
- Bila mengandalkan buku/daftar simbol eksternal, gunakan sebagai rujukan notasi, bukan sebagai bukti kebenaran konsep.

## Kategori Simbol yang Sering Dipakai

- Kuantor: `\forall` untuk semua, `\exists` untuk ada.
- Penghubung logika: `\neg`, `\wedge`, `\vee`, `\rightarrow`, `\leftrightarrow`.
- Relasi: `=`, `\neq`, `<`, `>`, `\le`, `\ge`, `\subseteq`, `\in`.
- Set/domain: `\mathcal{D}`, `\mathcal{N}`, `\mathbb{R}`, `\mathbb{N}`.
- Fungsi/pemetaan: `f: A \to B`, `g(x)`, `h_t`.
- Probabilitas/statistik: `P(A)`, `P(A \mid B)`, `\mathbb{E}[X]`, `\operatorname{Var}(X)`.
- Optimisasi: `\arg\min`, `\arg\max`, `\min`, `\max`.
- Kompleksitas/pertumbuhan: `O(n)`, `\Theta(n)`, `\Omega(n)`.

## Template Legenda

```text
Legenda:
\mathcal{D}: domain objek yang diuji
x, y: elemen dalam domain
P(x): predikat bahwa x memenuhi properti P
R(x, y): relasi antara x dan y
t: indeks waktu atau kondisi temporal
```

## Pemeriksaan Notasi

Sebelum memberi jawaban final, periksa:

- Apakah domain setiap variabel jelas?
- Apakah semua predikat dan relasi didefinisikan?
- Apakah kuantor terlalu luas?
- Apakah implikasi `A \rightarrow B` hanya menyatakan hubungan logis, bukan otomatis hubungan sebab-akibat empiris?
- Apakah simbol probabilistik dipakai saat klaim sebenarnya deduktif, atau sebaliknya?
- Apakah LaTeX cukup sederhana untuk dibaca user?

## Contoh Ringkas

```text
Klaim: Semua sistem yang memenuhi properti S akan stabil.
Domain:
\mathcal{D}: himpunan sistem yang sedang dianalisis
Predikat:
S(x): x memenuhi properti S
T(x): x stabil dalam kondisi uji T
Formalisasi:
\forall x \in \mathcal{D}, S(x) \rightarrow T(x)
Catatan:
Kesimpulan ini hanya berlaku untuk domain \mathcal{D} dan definisi stabilitas T.
```

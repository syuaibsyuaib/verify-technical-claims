# Task: Audit & Perbaikan Skill `verify-technical-claims`

## Status: Selesai (siklus pertama)

## Riwayat Pekerjaan

### 1. Audit awal
- Memeriksa struktur folder, isi SKILL.md, dan 6 file references/.
- Hasil: struktur konsisten, semua cross-reference file valid, tidak ada broken reference.
- Ditemukan 4 hal minor untuk ditindaklanjuti.

### 2. Tindak lanjut 4 temuan minor
- **Tautan fourmilab.ch** — dikonfirmasi bukan sumber resmi (situs pribadi). Diganti dengan
  sumber resmi Princeton Einstein Papers Project.
- **Referensi "validator skill"** — dikonfirmasi bukan gap; merujuk ke tool eksternal resmi
  (`scripts/quick_validate.py` dari repo openai/skills, atau eval framework skill-creator).
- **Frasa "folder default Codex"** — dikonfirmasi akurat (skill ini memang mengikuti skema
  resmi Codex lewat agents/openai.yaml), sekaligus cross-compatible dengan Claude.
- **agents/openai.yaml** — diverifikasi ke dokumentasi resmi openai/skills: struktur field
  dan sintaks `$skill-name` pada default_prompt sudah 100% benar, tidak ada perubahan.
- Ditemukan 1 temuan baru: tautan NIST SI units memakai path lama yang sudah direstrukturisasi.

### 3. Perbaikan yang sudah diterapkan (file diubah)
- `references/theoretical-physics-derivation.md`:
  - Baris rujukan Einstein 1905 → diganti ke `einsteinpapers.press.princeton.edu/vol2-trans/186`
  - Baris rujukan NIST SI units → diganti ke path kanonik `nist.gov/pml/owm/metric-si/si-units`
- `evals/evals.json` (baru dibuat): 12 skenario uji mengikuti skema skill-creator
  (`skill_name`, `evals[].id/prompt/expected_output/expectations`), mencakup:
  - Known-answer tests (4): dimensi rumus fisika, modus ponens, framing E=mc^2, konservasi energi
  - Adversarial tests (4): premis palsu+inferensi valid, equivocation, missing baseline, unfalsifiable
  - Metamorphic tests (3): ganti nama variabel, premis irelevan, hapus sumber primer
  - Format compliance (1): struktur jawaban wajib + koreksi klaim EMA/lag
  - Validasi: JSON disusun & diverifikasi valid (parse + cek field wajib) sebelum ditulis ke lokasi final.

## Belum dikerjakan / opsional ke depan
- Menjalankan evals.json ini secara nyata lewat skill-creator eval loop / quick_validate.py
  (perlu konfirmasi user dulu sebelum eksekusi).
- Cek 3 tautan SEP lain yang belum diverifikasi eksplisit sebelumnya sudah dicek di sesi ini
  (Popper, equivME, symmetry-breaking) — semua valid, tidak perlu tindakan lagi.

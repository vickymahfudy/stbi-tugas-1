# STBI Tugas 1: Vector Space & Probabilistic Retrieval Models

Membandingkan performa model ranked retrieval pada dataset berita Indonesia: TF, TF-IDF, Word2Vec (TF-IDF weighted), dan Query-Likelihood Language Model dengan tiga varian smoothing (tanpa smoothing, Laplace, linear interpolation).

## Isi Repo

- `Tugas_1.ipynb` — notebook utama, berisi seluruh implementasi model dan analisis.
- `Tugas_1.md` — brief/soal tugas.
- `News.csv` — dataset berita (kolom `content` dipakai sebagai korpus).
- `hasil_retrieval.csv` — hasil top-10 retrieval per model per query, termasuk proksi relevansi otomatis dan kolom `relevan_manual` untuk penilaian manual.
- `hasil_timing.csv` — waktu komputasi tiap model per query.

## Model yang Diimplementasikan

1. **Vector Space Model**
   - TF (Cosine Similarity)
   - TF-IDF (Cosine Similarity)
   - Word2Vec (dilatih dari korpus, di-weight dengan TF-IDF)
2. **Query-Likelihood Language Model**
   - Tanpa smoothing
   - Add-one (Laplace) smoothing
   - Linear interpolation (Jelinek-Mercer)

## Status

- Task 1–3 (data prep, model, testing 5 query x 6 model, timing, perbandingan top-10): selesai.
- Task 4 (enhancement dengan stemming): belum selesai — proses stemming Sastrawi pada seluruh vocabulary korpus (14k+ dokumen) berjalan lambat, sedang dicari pendekatan yang lebih efisien.
- Word2Vec pretrained (sesuai brief): belum diterapkan, saat ini masih dilatih from-scratch dari korpus.
- Laporan tertulis: belum dibuat.

## Cara Menjalankan

```bash
pip install -r requirements.txt  # atau lihat import di cell pertama notebook
jupyter nbconvert --to notebook --execute --inplace Tugas_1.ipynb
```

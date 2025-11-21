# Vision Transformer Comparison: Swin vs DeiT on CIFAR-10

Repository ini berisi implementasi dan perbandingan performa dua arsitektur **Vision Transformer (ViT)** modern, yaitu **Swin Transformer** dan **DeiT (Data-efficient Image Transformer)**, pada dataset klasifikasi citra **CIFAR-10**.

Proyek ini dikerjakan sebagai pemenuhan Tugas Mata Kuliah Deep Learning Semester Ganjil 2025/2026.

## Deskripsi Tugas
Tujuan dari eksperimen ini adalah membandingkan efektivitas arsitektur Transformer hierarkis (Swin) melawan arsitektur Transformer ringan berbasis distilasi (DeiT) dalam aspek:
1. **Akurasi Klasifikasi** (Accuracy & F1-Score).
2. **Efisiensi Komputasi** (Jumlah Parameter & Ukuran Model).
3. **Kecepatan Inferensi** (Latency & Throughput).

## Model yang Digunakan
Eksperimen dilakukan menggunakan strategi **Transfer Learning (Fine-tuning)** dari pre-trained weights ImageNet-1k menggunakan library `timm`.

| Model | Arsitektur Code (`timm`) | Deskripsi Singkat |
| :--- | :--- | :--- |
| **Swin Transformer (Tiny)** | `swin_tiny_patch4_window7_224` | Hierarchical Vision Transformer dengan Shifted Windows. |
| **DeiT (Tiny)** | `deit_tiny_patch16_224` | Vision Transformer ringan dengan strategi Knowledge Distillation. |

## Struktur Repository
├── ViT_Comparison.ipynb # Source code utama (Jupyter Notebook)
├── README.md # Dokumentasi proyek
├── requirements.txt # Daftar library yang dibutuhkan

## Cara Menjalankan Code

### Opsi 1: Google Colab (Direkomendasikan)
1. Buka file `.ipynb` di repository ini.
2. Klik tombol "Open in Colab" (jika ada) atau download file dan upload manual ke [Google Colab](https://colab.research.google.com/).
3. Pastikan Runtime diatur ke **GPU** (Runtime > Change runtime type > T4 GPU).
4. Jalankan semua cell secara berurutan. Dataset CIFAR-10 akan diunduh secara otomatis.

### Opsi 2: Lokal (Jupyter Notebook)
1. Clone repository ini:
   ```bash
   git clone https://github.com/KennAustin/VisionTransformer.git
   cd ViT_Comparison
   pip install -r requirements.txt
   jupyter notebook
   ```

   
   


# Notebook Pengujian Inferensi LLM

Repositori ini berisi Jupyter Notebook yang dirancang untuk menguji inferensi dari Model Bahasa Besar (LLM) menggunakan platform Watsonx.ai dari IBM. Berikut adalah gambaran isi notebook dan bagaimana ia selaras dengan tujuan pembelajaran dalam bekerja dengan LLM.

## Fitur Utama Notebook

### 1. **Memahami Fitur Utama LLM**
   - Notebook ini menunjukkan penggunaan model LLM (contoh: "google/flan-ul2") untuk menghasilkan keluaran teks berbasis konteks.
   - Menunjukkan bagaimana LLM memproses prompt dan menghasilkan respons berdasarkan input tertentu.

### 2. **Dasar-dasar _Prompt Engineering_**
   - Notebook menyediakan kontrol terperinci atas input prompt dan parameter model, termasuk:
     - Metode decoding (misalnya, greedy decoding).
     - Batas token (`max_new_tokens` dan `min_new_tokens`).
     - Urutan penghentian untuk mengontrol akhir respons.
     - Penalti pengulangan untuk mengatur keragaman output.
   - Elemen-elemen ini memungkinkan pengguna untuk menyempurnakan prompt dan mengoptimalkan performa model.

### 3. **Menggunakan Prompt Lab dengan watsonx.ai**
   - Meskipun notebook ini tidak secara langsung menggunakan Watson Prompt Lab, strukturnya memungkinkan eksperimen dengan prompt dan parameter untuk pengujian inferensi pada watsonx.ai.
   - Pengguna dapat mengeksplorasi berbagai konfigurasi untuk memahami efek dari teknik _prompt engineering_ pada keluaran LLM.

### 4. **Menguji Inferensi Model LLM**
   - Fungsi `generate` dalam notebook mengirimkan prompt input ke model LLM yang telah dideploy menggunakan API Watson Machine Learning.
   - Fungsi ini mengambil dan menampilkan teks yang dihasilkan, memungkinkan pengujian inferensi model di skenario nyata.

## Struktur Notebook

1. **Autentikasi**: 
   - Menggunakan IBM Cloud IAM untuk mengautentikasi permintaan API dengan meminta pengguna memasukkan API key mereka.

2. **Definisi Fungsi Inferensi**:
   - Mengimplementasikan metode `generate` untuk berinteraksi dengan API Watson Machine Learning.

3. **Pengaturan Prompt dan Parameter**:
   - Mendefinisikan model, parameter, dan prompt contoh untuk pengujian inferensi LLM.

4. **Menjalankan Inferensi**:
   - Memanggil fungsi `generate` untuk mendapatkan dan menampilkan hasil dari model.

## Prasyarat

- Akses ke API Watson Machine Learning dari IBM.
- Model LLM yang telah dideploy (contoh: "google/flan-ul2") di platform watsonx.ai.
- Dependensi Python: `requests`, `ibm-cloud-sdk-core`.

## Cara Menggunakan

1. Klon repositori ini.
   ```bash
   git clone <repository-url>
   ```

2. Instal pustaka Python yang diperlukan.
   ```bash
   pip install requests ibm-cloud-sdk-core
   ```

3. Buka notebook di Jupyter atau JupyterLab.
   ```bash
   jupyter notebook TestLLM_Fawwaz.ipynb
   ```

4. Ikuti langkah-langkah dalam notebook:
   - Masukkan API key IBM Cloud Anda saat diminta.
   - Definisikan `project_id` dan parameter lainnya.
   - Jalankan inferensi dan tinjau output yang dihasilkan.

## Tujuan Pembelajaran

Notebook ini membantu pengguna untuk:

- Memahami fungsi LLM.
- Mencoba teknik _prompt engineering_.
- Menguji dan memvalidasi inferensi LLM dalam skenario praktis.
- Menggunakan platform Watsonx.ai secara efektif.

---

**Kontributor**: 
- Dibuat oleh [Nama atau Tim Anda].

**Lisensi**: Lisensi MIT

# 📚 Evaluasi Otomatis Tafsir QS 9:60 | Automatic Evaluation of Qur'anic Exegesis (QS 9:60)

Proyek ini menyediakan pipeline **evaluasi otomatis untuk respons AI terhadap QS 9:60** menggunakan tiga tafsir klasik: *al-Ṭabarī*, *Ibn Kathīr*, dan *al-Qurṭubī*. Evaluasi dilakukan berdasarkan rubrik 3 dimensi: **Validitas Tafsir**, **Struktur Bil Ma’tsūr**, dan **Halusinasi Tafsir**.

This project provides an **automated evaluation pipeline for AI-generated interpretations of QS 9:60**, grounded in three classical exegeses: *al-Ṭabarī*, *Ibn Kathīr*, and *al-Qurṭubī*. Evaluation is based on three dimensions: **Tafsir Validity**, **Bil Ma’tsūr Structure**, and **Hallucination Detection**.

---

## 🔍 Fitur Utama | Key Features

- ✅ Evaluasi berbasis kutipan literal dari tafsir klasik (`.txt`)
- 🧠 Prompt evaluasi dengan chain-of-thought dan few-shot rubric
- 📐 Skoring otomatis (0–10) per dimensi rubrik
- 📊 Output ke file Excel berisi skor dan komentar per tafsir

- ✅ Based on literal references from classical tafsir (`.txt`)
- 🧠 Chain-of-thought prompts with few-shot rubric evaluation
- 📐 Automatic scoring (0–10) per dimension
- 📊 Output as Excel file with detailed scores & comments

---

## 📁 Struktur Folder | Folder Structure

tafsir-eval-public/ ├── chaining/ # AI-generated responses │ └── DeepSeek_V2.xlsx ├── references/ # Classical sources & rubric │ ├── ibnu_katsir.txt │ ├── qurtubi.txt │ ├── thabari.txt │ └── rubrik_mini.txt ├── outputs/ # Evaluation results (Excel) │ └── DeepSeek_Evaluated_WithAuto.xlsx ├── responses/ # (Optional) Store manual responses └── tafsir_eval_pipeline.ipynb # Main notebook (Colab-ready)


---

## 🚀 Cara Menjalankan | How to Run (Google Colab)

1. Jalankan notebook `tafsir_eval_pipeline.ipynb` di Google Colab.
2. Pastikan semua file referensi ada di `/references/`.
3. Masukkan file respons AI (`DeepSeek_V2.xlsx`) ke `/chaining/`.
4. Sistem akan memproses dan menyimpan hasil ke `/outputs/`.

1. Run `tafsir_eval_pipeline.ipynb` on Google Colab.
2. Ensure reference files are in `/references/`.
3. Place AI responses (`DeepSeek_V2.xlsx`) in `/chaining/`.
4. The system will evaluate and save outputs to `/outputs/`.

---

## 📏 Rubrik Penilaian | Evaluation Rubric (Simplified)

**[A] Validitas Tafsir**  
Apakah klaim didukung kutipan literal dan tokoh yang sahih?  
*Are claims supported by literal citations and valid figures?*

**[B] Struktur Bil Ma’tsūr**  
Apakah pola penafsiran klasik diikuti (ayat → riwayat → mufassir)?  
*Does it follow the classical pattern: verse → narration → mufassir?*

**[C] Halusinasi Tafsir**  
Apakah ada tokoh, riwayat, atau kutipan yang tidak ditemukan di sumber klasik?  
*Are there any hallucinated figures, narrations, or fake citations?*

---

## 📊 Contoh Output | Example Output (Excel)

| Index | Validitas | Bil Ma’tsūr | Halusinasi |
|-------|-----------|-------------|------------|
|   0   |     6     |      5      |     4      |

Tiap dimensi disertai komentar naratif otomatis berdasarkan isi dokumen tafsir.  
Each dimension includes a narrative comment extracted from classical references.

---

## 📜 Lisensi | License

Proyek ini dilisensikan di bawah [MIT License](LICENSE).  
This project is licensed under the [MIT License](LICENSE).

---

## 🙋‍♂️ Penulis | Author

Dikembangkan oleh **Soleh Hasan Wahid** untuk mendukung riset evaluasi AI terhadap tafsir klasik.  
Developed by **Soleh Hasan Wahid** to support AI evaluation research on classical Qur'anic exegesis.

---

## 📎 Tautan Penting | Useful Links

- [📄 Rubrik Evaluasi](references/rubrik_mini.txt)
- [🧪 Data AI](chaining/DeepSeek_V2.xlsx)
- [📊 Hasil Evaluasi](outputs/DeepSeek_Evaluated_WithAuto.xlsx)

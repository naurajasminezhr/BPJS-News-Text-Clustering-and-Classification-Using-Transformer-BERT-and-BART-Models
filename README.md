# BPJS-News-Text-Clustering-and-Classification-Using-Transformer-BERT-and-BART-Models


## **Project Description**
This project aims to analyze news text using transformer-based approaches. The main processes in this project include:
1. **Zero-Shot Classification** using the **BART** model to determine the initial categories of news text.
2. **Embedding and Clustering** using the **BERT Base Uncased** model without fine-tuning.
3. **Fine-Tuning the BERT Model**, followed by embedding and clustering.
4. Experiments are conducted on various dataset columns:
   - *News title* column.
   - *News text* column (unprocessed).
   - *Cleaned/preprocessed news text* column.
  
## Team Members:
- Naura Jasmine Azzahra - 5026211005
- Ramadhanul Husna A. M. - 5026211059
- Fikri Septa Setiawan - 5026211109

## **Directory Structure**
The structure of the project's directory is as follows:

```
TRANSFORMER-FIX/
├── Bert Base Uncased Only_Kolom Text_Berita/
│   ├── Cosine Similarity Clustering - Model Transformers tanpa fine tuning.ipynb
│   ├── data_with_clusters.xlsx
│   ├── Embedding and PCA Clustering - Model Transformers no Finetuning.ipynb
│   └── text_berita_embeddings.pkl
├── Bert Base Uncased Only_Kolom Text_Berita_Clean/
│   ├── data_with_clusters_clean.xlsx
│   ├── Note.txt
│   ├── Teks Clean_Transformers_tanpa_fine_tuning.ipynb
│   └── text_berita_clean_embeddings.pkl
├── Bert Base Uncased Only_Pakai Kolom Judul/
│   ├── data_with_clusters_jdul.xlsx
│   ├── judul_clean_embeddings.pkl
│   └── Kolom Judul_Transformers.ipynb
├── Bert Base Uncased with Fine Tuning/
│   ├── Pakai Kolom Text_Berita/
│   │   ├── Clustering and Embedding_with fine tuned model.ipynb
│   │   ├── data_with_clusters.xlsx
│   │   ├── text_berita_embeddings.pkl
│   │   └── Transformers_Fine Tuning_teks berita.ipynb
│   ├── Pakai Kolom Text_Berita_Clean/
│   │   ├── Clustering-Embedding_Teks Clean_with fine tuned model.ipynb
│   │   ├── data_with_clusters_clean_fine_tuning_model.xlsx
│   │   ├── text_berita_clean_embeddings_fine_tuning_model.pkl
│   │   └── Transformers-Teks Clean_Fine Tuning.ipynb
│   └── Note.txt
├── data_ready_with_kategori.xlsx
├── Klasifikasi_Kategori_NEWS_BPJS_BART.ipynb
└── README.md
```

---

## **Process Steps**

### 1. **Zero-Shot Classification with BART**
- The initial dataset is classified into specific categories using the `facebook/bart-large-mnli` zero-shot classification model.
- This process is applied to the news text column to generate an initial category column.

### 2. **Embedding and Clustering Using BERT Base Uncased**
- The `bert-base-uncased` model is used to generate embeddings from news text.
- Embeddings are computed for three types of columns:
  - *News title* column.
  - *News text* column (unprocessed).
  - *Cleaned/preprocessed news text* column.
- The embeddings are then used for clustering using the KMeans algorithm.
- Cluster visualization is performed using PCA or t-SNE.

### 3. **Fine-Tuning the BERT Model**
- The BERT model is fine-tuned using a dataset with predefined categories.
- After fine-tuning, embeddings are recalculated, and clustering is performed to compare results with the non-fine-tuned model.

---

## **Results and Analysis**
### 1. **Cluster Visualization**
The clustering results are visualized as scatter plots after dimensionality reduction using PCA or t-SNE. An example visualization can be seen below:

Cluster Visualization

- Each color represents a single cluster.
- The data distribution shows how documents are grouped based on content similarity.

### 2. **Comparison of Clustering Results**
The clustering results are compared between the non-fine-tuned model and the fine-tuned model, as well as across different dataset columns.

---

## **Main Files**
Below are the main files along with their descriptions:

| File/Folder                                   | Description                                                                                  |
|-----------------------------------------------|---------------------------------------------------------------------------------------------|
| `Klasifikasi_Kategori_NEWS_BPJS_BART.ipynb`   | Notebook for zero-shot classification using the BART model.                                 |
| `data_ready_with_kategori.xlsx`               | Initial dataset with category columns from zero-shot classification results.                |
| `text_berita_embeddings.pkl`                  | Pickle file containing embeddings from the *news text* column.                              |
| `data_with_clusters.xlsx`                     | Clustering results from embeddings of the *news text* column.                               |
| `text_berita_clean_embeddings.pkl`            | Pickle file containing embeddings from the cleaned/preprocessed *news text* column.         |
| `data_with_clusters_clean.xlsx`               | Clustering results from embeddings of the cleaned/preprocessed *news text* column.          |
| `judul_clean_embeddings.pkl`                  | Pickle file containing embeddings from the *news title* column.                             |
| `data_with_clusters_jdul.xlsx`                | Clustering results from embeddings of the *news title* column.                              |

---

## **How to Run the Project**

1. Ensure all dependencies are installed:
   ```bash
   pip install transformers sklearn pandas matplotlib torch openpyxl
   ```

2. Run notebooks based on your requirements:
   - For zero-shot classification: `Klasifikasi_Kategori_NEWS_BPJS_BART.ipynb`.
   - For embedding and clustering without fine-tuning: 
     - `Embedding and PCA Clustering - Model Transformers no Finetuning.ipynb`.
     - `Teks Clean_Transformers_tanpa_fine_tuning.ipynb`.
     - `Kolom Judul_Transformers.ipynb`.
   - For fine-tuning: Notebooks inside the folder `Bert Base Uncased with Fine Tuning`.

3. Analyze clustering results through generated Excel files (`data_with_clusters.xlsx`, etc.).

---

## **Conclusion**
This project demonstrates how transformer models like BERT and BART can be effectively used for classification, embedding, and clustering of text data. By comparing results from various approaches (fine-tuned vs non-fine-tuned), this project provides insights into how text representation impacts clustering performance.

--- 

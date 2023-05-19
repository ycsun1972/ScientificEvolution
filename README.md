# ScientificEvolution

This is our research code for paper: Unraveling Scientific Evolutionary Paths: An Embedding-based Topic Analysis

We initially investigated mainstream and emerging embedding methods, including word2vec, doc2vec, BERT, and SciBERT, and compared their superiority in capturing semantics and extracting topics via several benchmarks, with TF-IDF and LDA as baselines.
The optimal word-level and document-level embedding methods were selected for topic extraction and scientific evolutionary path identification.

## Released Items
- Labeled WoS and MedLine datasets
- Codes for document clustering tasks
- Object detection dataset
- Word lists for data pre-processing
- Codes for scientific evolutionary path identification

## Preliminary Rreparations

### Install toolkits
```
gensim
sklearn
transformers
```

### Download Pretrained Models
- [bert_base_uncased](https://huggingface.co/bert-base-uncased)
- [biobert_base_cased](https://github.com/dmis-lab/biobert)
- [scibert_scivocab_uncased](https://github.com/allenai/scibert/)


## Embedding Methods Benchmark

### Labeled WoS and MedLine datasets
Datasets used for benchmarking embedding methods are stored in [datasets](datasets). The two datasets were extracted from the Web of Science and MedLine databases, separately. Each contains 50000 documents which are divided into ten categories. The corpora are stored in [50000_WoS.txt](datasets/50000_WoS.zip) and [50000_MedLine.txt](datasets/50000_MedLine.zip). And their labels are stored in [50000_WoS_label.txt](datasets/50000_WoS_Label.txt) and [50000_MedLine_Label.txt](datasets/50000_MedLine_Label.txt).

### Codes for document clustering tasks
Codes used for evaluating the performance of candidate methods are provided in  [embedding_and_baseline](embedding_and_baseline). Six files are contained, including codes for using [doc2vec](embedding_and_baseline/1_doc2vec.ipynb), [word2vec](embedding_and_baseline/2_word2vec_unweighted.ipynb), [BERT](embedding_and_baseline/6_bert.ipynb), [SciBERT](embedding_and_baseline/6_bert.ipynb), [BioBERT](embedding_and_baseline/6_bert.ipynb), [tf-idf](embedding_and_baseline/4_tf-idf.ipynb), and [LDA](embedding_and_baseline/5_lda.ipynb), to vectorize document and cluster documents.


##	Scientific Evolution Analysis
### Object detection dataset

The dataset is used to demonstrate the feasibility and effectiveness of the methodology in unraveling scientific evolutionary paths. It was collected from the Web of Science database, containing 56,529 peer-reviewed documents in the field of object detection, published between 2011 and 2020.

### Codes for scientific evolutionary path identification

There are two files in [evolution_analysis](evolution analysis):
- [topic_similarity_calculation_over_period](evolution_analysis/topic_similarity_calculation_over_period.ipynb), which is used for calculating the semantic similarity topics over periods.
- [term_extraction_for_topic_designation](evolution_analysis/term_extraction_for_topic_designation.ipynb), which is used for constructing terms’ semantic and co-occurrence networks, calculating the degree centrality of each term, and selecting the most representative terms for topic designation.

##	Citation
To be updated

##	Acknowledgments
To be updated

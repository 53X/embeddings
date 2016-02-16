# embeddings
This repository contains code accompanying publication of the paper: 
> Y. Choi, Y. Chiu, D. Sontag. [Learning Low-Dimensional Representations of Medical Concepts](http://cs.nyu.edu/~dsontag/papers/ChoiChiuSontag_AMIA_CRI16.pdf). To appear in Proceedings of the AMIA Summit on Clinical Research Informatics (CRI), 2016.

In the base directory there are two files containing the two best 300-dimensional embeddings learned in the paper:
* `claims_codes_hs_300.txt.gz`: Embeddings of ICD-9 diagnosis and procedure codes, NDC medication codes, and LOINC laboratory codes, learned on a large claims dataset from 2005 to 2013 for roughly 4 million people.
* `stanford_cuis_svd_300.txt.gz`: Embeddings of [UMLS](https://www.nlm.nih.gov/research/umls/) concept unique identifiers (CUIs), learned from 20 million clinical notes spanning 19 years of data from Stanford Hospital and Clinics, using a  [data set](http://datadryad.org/resource/doi:10.5061/dryad.jp917) released in a [paper](http://www.nature.com/articles/sdata201432) by Finlayson, LePendu & Shah.

In the `eval` directory there are three files of interest:
* [`eval/Embedding_Evaluation.ipynb`](https://github.com/clinicalml/embeddings/blob/master/eval/Embedding_Evaluation.ipynb), an iPython notebook which reproduces the main results of the paper. If you come up with your own embeddings, you can use this benchmark to quantitatively compare them to our embeddings.
* `eval/visualize_claims_embeddings.py` a Python program you can run which will allow you to look at nearest neighbors for the `claims_codes_hs_300.txt` embeddings (after decompressing the file using `gunzip`).
* `eval/visualize_stanford_embeddings.py`, same as above but for the `stanford_cuis_svd_300.txt` embeddings.

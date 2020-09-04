# elNER: Datasets for Greek Named Entity Recognition

With the data provided in this directory, we introduce a manually annotated corpus of Greek newswire articles, coined as **elNER**, comprising of named entity tags to facilitate Greek named entity recognition (NER). Motivated by CoNLL-2003 and OntoNotes 5 datasets in English, two versions of elNER are described, namely elNER-4 and elNER-18, respectively. Current state-of-the-art NER models are trained on these datasets. The performance metrics disclosed here are comparable to those achieved by the respective approaches in English.  For the creation of the elNER dataset, we drew inspiration from the work carried out in the project called "[Greek language support for spacy.io python NLP software](https://github.com/eellak/gsoc2018-spacy)" during Google Summer of Code 2018 (gsoc2018)

For the preprocessing task of our corpus, [spaCy](https://spacy.io/) was used. Further text annotation was performed employing the [Prodigy](https://prodi.gy) tool, because of its ease of use and its straightforward integration with spaCy.

## Results

### Best Performace for 5 DNN models

|            | Precision | Recall | F1
-------------|--------|--------|--------
biLSTM-CRF     | 91.59  | 91.13  | **91.36**
biGRU-CRF      | 89.95 | 91.73  | 90.93
biLSTM-CNN-CRF* | 90.30 | 92.39  | 91.33
biLSTM-CNN*     | 87.11 | 91.60  | 89.30
spaCy NER | 89.16 | 90.10  | 89.63  

**Best performance metrics in % for NER in elNER-4. (\* fastText w/ ELMo)**

|            | Precision | Recall | F1
-------------|--------|--------|--------
biLSTM-CRF     | 91.65  | 92.45  | **92.05**
biGRU-CRF*      | 90.73  | 91.42  | 91.08
biLSTM-CNN-CRF* | 91.27  | 92.59  | 91.92
biLSTM-CNN*     | 87.93  | 90.99  | 89.43
spaCy NER      | 90.93  | 91.14  | 91.04

**Best performance metrics in % for NER in elNER-18. (\* fastText w/ ELMo)**

### spaCy model elNER4

|             | Precision | Recall | F1  
-------------|--------|--------|--------
LOC  |     89.30 |  93.92 | 91.55
ORG   |   87.61 |  86.10 |  86.85
PERSON |  94.46 |  95.72 |  95.09
MISC |     78.75 |  78.31 |  78.53
**all**   | **89.16** | **90.10** | **89.63**

**Best performance metrics in % for spaCy in elNER-4.**

### spaCy model elNER18

|             | Precision | Recall | F1  
-------------|--------|--------|--------
ORG           |  87.76 |  86.74 |  87.25
GPE           |  88.44 |  93.58 |  90.94
CARDINAL      |  96.93 |  96.93 |  96.93
FAC           |  71.01 |  63.64 |  67.12
TIME          |  91.49 |  94.16 |  92.81
PERCENT       |  98.06 |  98.06 |  98.06
PERSON        |  93.66 |  95.62 |  94.63
NORP          |  93.66 |  94.33 |  93.99
DATE          |  94.10 |  93.32 |  93.71
LOC           |  82.18 |  80.34 |  81.25
EVENT         |  74.82 |  80.00 |  77.32
WORK_OF_ART   |  68.12 |  55.95 |  61.44
ORDINAL       |  95.91 |  95.35 |  95.63
MONEY         |  98.17 |  96.40 |  97.27
QUANTITY      |  85.71 |  83.08 |  84.38
LAW           |  90.00 |  64.29 |  75.00
PRODUCT       |  76.92 |  72.29 |  74.53
LANGUAGE      | 100.00 |  88.89 |  94.12
**all**           | **90.93**  | **91.14**  | **91.04**

**Best performance metrics in % for spaCy in elNER-18.**

## Citation

if you use this dataset in your machine learning experiments please cite this work by using the following bibtex entry:

```bibtex
@InProceedings{bartziokas2020datasets,
  author = {Nikos Bartziokas and Thanassis Mavropoulos and Constantine Kotropoulos},
  title = {{Datasets and Performance Metrics for Greek Named Entity Recognition}},
  booktitle = {11th Hellenic Conference on Artificial Intelligence (SETN 2020)}},
  pages = {160-167},
  year   = {2020},
  location = {Athens, Greece},
  series = {SETN 2020}
  isbn = {9781450388788},
  publisher 	= {Association for Computing Machinery},
  address 	= {New York, NY, USA},
  url 	= { https://doi.org/10.1145/3411408.3411437},
  doi 	= {10.1145/3411408.3411437},
}
```
## Presentation slides 
https://nmpartzio.github.io/elner_slides/index.html#/  

## Recorded presentation
https://drive.google.com/file/d/120k8ZkfdMb_iPIjmSR9V8TJK2N_gczVQ/view 

## Credits
Authors:
Nikos Bartziokas, Thanassis Mavropoulos, Constantine Kotropoulos

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

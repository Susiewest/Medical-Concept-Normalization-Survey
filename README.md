# Medical-Concept-Normalization-Survey

Generate and rank
|Authors    | Paper     | idea     |  Dataset     |  Eval     |  Code     |
| ---------- | :-----------:  | :-----------: |:-----------:  | :-----------: |:-----------:  |
| Yan et al. (2020)     | A Knowledge-driven Generative Model for Multi-implication Chinese Medical Procedure Entity Normalization     | multi-implication, generating and ranking, constraint decoder    | CHIP-2019    | accuracy，按beamsize统计recall    |      |
| Xu et al. (2020)      | A Generate-and-Rank Framework with Semantic Type Regularization for Biomedical Concept Normalization     | generate and rank (generate = select)    | AskAPatient /TwADR-L /SMM4H-17 /MCN    | accuracy   | https://github.com/dongfang91/Generate-and-Rank-ConNorm     |

Supervised multi-class classifiers
|Authors    | Paper     | idea     |  Dataset     |  Eval     |  Code     |
| ---------- | :-----------:  | :-----------: |:-----------:  | :-----------: |:-----------:  |
| Belousov(2017)    | Using an Ensemble of Generalised Linear and Deep Learning Models in the SMM4H 2017 Medical Concept Normalisation Task     | logistic    | medDRA    | accuracy    |      |
|       | A Hybrid Normalization Method for Medical Concepts in Clinical Narrative using Semantic Matching     | "Exact Match + Edit Distance Deep Learning（Embedding layer+bilstm+dense+softmax）   | ShARe/CLEF 2013   |   |     |
+ 
| Belousov(2017)    | Multi-task CharacterLevel Attentional Networks for Medical Concept Normalization     | medical named entity recognition(CNN embedding+BiLSTM sequence labeling) and normalization    | BC5CDR task corpus/ NCBI Disease corpus    | F1    |      |

|      | Medical concept normalization in social media posts with recurrent neural networks     |    | CADEC    |    |      |

Dataset
|Dataset    | Paper | Mention     | Standard entities     |  Source     |  
| ---------- | :-----------:  | :-----------: |:-----------:  | :-----------:  | 
| CHIP-2019   |       |      | 9867    | CHIP-2019    |
| Ask patient   |       |  17324    | 1036 concepts, 22 semantic types    |  blog post     |
| TwADR-L   |       |    5074  | 2220 concepts, 18semantic types   | social media    |
| SMM4H-17   |       |   9149   | 22500 concepts(513 in trainset), 61 semantic types    |  tweets     |
| MCN  |       |  13609    | 434056 concepts(3792 in trainset), 125 semantic types    | from the MIMIC II31 database    |
| ShARe/CLEF 2013   |       |    199 notes in the training set and 99 notes in the test set   |    |     |
| BC5CDR task corpus   |       |  1500 PubMed abstracts     |     |     |
| NCBI Disease corpus   |       |  793 PubMed abstracts   |    |     |
| CADEC   |       |      | mapped to SNOMED CT-AU    |     |


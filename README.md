# Medical-Concept-Normalization-Survey

Generate and rank
|Authors    | Paper     | idea     |  Dataset     |  Eval     |  Code     |
| ---------- | :-----------:  | :-----------: |:-----------:  | :-----------: |:-----------:  |
| Yan et al. (2020)     | A Knowledge-driven Generative Model for Multi-implication Chinese Medical Procedure Entity Normalization     | multi-implication, generating and ranking, constraint decoder    | CHIP-2019    | accuracy，按beamsize统计recall    |      |
| Xu et al. (2020)      | A Generate-and-Rank Framework with Semantic Type Regularization for Biomedical Concept Normalization     | generate and rank (generate = select)    | AskAPatient /TwADR-L /SMM4H-17 /MCN    | accuracy   | https://github.com/dongfang91/Generate-and-Rank-ConNorm     |

Supervised multi-class classifiers
|Authors    | Paper     | idea     |  Dataset     |  Eval     |  Code     |
| ---------- | :-----------:  | :-----------: |:-----------:  | :-----------: |:-----------:  |
| Belousov(2017)    | Using an Ensemble of Generalised Linear and Deep Learning Models in the SMM4H 2017 Medical Concept Normalisation Task     | logistic    | medDRA    | Acc   |      |
|   Tutubalina(2018)   | Medical concept normalization in social media posts with recurrent neural networks     |  RNN/LSTM/GRU + Similarity feature（TF-IDF/w2v） | CADEC    | Acc    |      |
|  Luo et al.(2019)     | A Hybrid Normalization Method for Medical Concepts in Clinical Narrative using Semantic Matching     | "Exact Match + Edit Distance Deep Learning（Embedding layer+bilstm+dense+softmax）   | ShARe/CLEF 2013   | Acc+Macro+Micro  |     |
| Niu et al.(2019)    | Multi-task CharacterLevel Attentional Networks for Medical Concept Normalization     | medical named entity recognition(CNN embedding+BiLSTM sequence labeling) and normalization    | BC5CDR task corpus/ NCBI Disease corpus    | F1    |  |

Rank
|Method   | Paper     | Author     |  Disadvantage  |
| ---------- | :-----------:  | :-----------: | :-----------: |
| Direct Rank（字典查找、字符串匹配） |   |   |  不能找到字面上不相似但语义相同的concept |
| Direct Rank（Classfication） |   |   |  输出空间太大 |
| Point-wise Learing to Rank|   |   |  KB规模大时效率不佳  |
|Pair-wise learning to rank |   A combined recall and rank framework with online negative sampling for Chinese procedure terminology normalization（https://github.com/sxthunder/CMTN） |  Liang et al.(2021 Oxford) | 还在看 |
| List-wise learining to rank |  A Generate-and-Rank Framework with Semantic Type Regularization for Biomedical Concept Normalization        |  Yan et al. (2020)     |  multi-implication未解决, rank本质上还是按list送进bert+分类层？ |

Dataset
|Dataset    | Paper | Mention     | Standard entities     |  Source     |   Link |
| ---------- | :-----------:  | :-----------: |:-----------:  | :-----------:  | :-----------:  | 
| CHIP-2019   |    A Knowledge-driven Generative Model for Multi-implication Chinese Medical Procedure Entity Normalization（EMNLP2020）   |   4000   | 9867    | clinical procedures extracted from Chinese electronic medical records    | | 
| Ask patient   |   Normalising Medical Concepts in Social Media Texts by Learning Semantic Representation（ACL2016）    |  17324    | 1036 concepts, 22 semantic types    |  blog post     | https://github.com/dongfang91/Generate-and-Rank-ConNorm/tree/master/Generator/Multiclass/data/askapatient   https://zenodo.org/record/55013#.YOVHKPkzZaQ|
| TwADR-L   |   Normalising Medical Concepts in Social Media Texts by Learning Semantic Representation（ACL2016）    |    5074  | 2220 concepts, 18semantic types   | social media    | https://github.com/unt-iialab/medical-concept-normalization  https://zenodo.org/record/55013#.YOVHKPkzZaQ |
| SMM4H-17   |  Data and systems for medication-related text classification and concept normalization from Twitter: insights from the Social Media Mining for Health (SMM4H)-2017 shared task（JAMIA 2018）     |   9149   | 22500 concepts(513 in trainset), 61 semantic types    |  tweets     | https://metatext.io/datasets/social-media-mining-for-health-(smm4h)|
| MCN  |   Data and systems for medication-related text classification and concept normalization from Twitter: insights from the Social Media Mining for Health (SMM4H)-2017 shared task（JAMIA 2018）    |  13609    | 434056 concepts(3792 in trainset), 125 semantic types    | from the MIMIC II31 database（https://www.sciencedirect.com/science/article/pii/S1532046419300504）    |
| ShARe/CLEF 2013   |       |    199 notes in the training set and 99 notes in the test set   |    |     |https://sites.google.com/site/shareclefehealth/data|
| BC5CDR task corpus   |       |  1500 PubMed abstracts     |  MeSH/OMIM concepts(according to e Comparative Toxicogenomics Database (CTD) MEDIC disease vocabulary) 9700 concepts, 67000terms(including synonyms)   |     | https://paperswithcode.com/dataset/bc5cdr   https://www.researchgate.net/figure/The-overall-corpus-statistics_tbl2_302593945|
| NCBI Disease corpus   |       |  793 PubMed abstracts   |    |     | https://www.ncbi.nlm.nih.gov/CBBresearch/Dogan/DISEASE/|
| CADEC   |       |      | mapped to SNOMED CT-AU    |     | https://researchdata.edu.au/cadec/494923|


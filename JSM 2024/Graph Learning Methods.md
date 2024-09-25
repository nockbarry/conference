
I caught 2 talks in this session

https://ww3.aievolution.com/JSMAnnual2024/Events/viewEv?ev=1628

### Program

 

# Frontiers in Graph Learning: Novel Methods and Emerging Applications

**Ivor Cribben** Chair  
University of Alberta  

**Ivor Cribben** Organizer  
University of Alberta  

**Martin Ondrus** Organizer  

Monday, Aug 5: 10:30 AM - 12:20 PM  
1398 Invited Paper Session 

Oregon Convention Center 

Room: CC-F149 

  

#### Applied

Yes

#### Main Sponsor

Section on Statistical Learning and Data Science

#### Co Sponsors

JASA Theory and Methods

Technometrics

## Presentations

### [Challenges in Causal Representation Learning and Deep Generative Models](https://ww3.aievolution.com/JSMAnnual2024/Events/viewEv?ev=1630 "Challenges in Causal Representation Learning and Deep Generative Models")

Interpretability and causality have been acknowledged as key ingredients to the success and evolution of modern machine learning systems. A crucial step in this pipeline is to identify latent representations from observational data along with their causal structure. In many applications, the causal variables are not directly observed, and must be learned from data. Under parametric assumptions, this resembles familiar factor models, however, in modern applications we aim to use flexible, nonparametric models such as deep neural networks. These settings present new statistical and computational challenges that will be focus of this talk. We will discuss our recent work on developing methods for identifying and learning causal representations from data with rigourous guarantees. Along the way, we will explore the connections between causal graphical models, deep generative models, and nonparametric mixture models, and how these connections lead to a useful new theory for causal representation learning. 

  

#### Speaker

_Bryon Aragam_, The University of Chicago  

---

### [Change Point Detection in Graph Clustering for Early MCI Classification in High-dimensional fMRI Data](https://ww3.aievolution.com/JSMAnnual2024/Events/viewEv?ev=1632 "Change Point Detection in Graph Clustering for Early MCI Classification in High-dimensional fMRI Data")

Early mild cognitive impairment is a precursory stage to more debilitating forms of dementia such as Alzheimer's disease, but classification of this disorder is extremely difficult. We demonstrate the efficacy of change point detection in estimating dynamic functional connectivity (DFC) estimation for early mild cognitive impairment (eMCI) detection from functional magnetic resonance imaging (fMRI) using Alzheimer's Disease Neuroimaging Initiative studies (ADNI2 and ADNIGO). In our study, we compare window-based methods across different window and step sizes to FaBiSearch, a method for change point detection in the graph structure of multivariate high-dimensional time series data, as well as static functional connectivity (SFC). We find that change point detection is generally superior to window-based DFC, even over many combinations of window and step sizes. Additionally, we find that both these DFC methods are generally superior to SFC. All together, our results suggest that classification for eMCI is a dynamic, multi-scale process and that different methods can capture varying amounts of information useful for classification. 

  

#### Speaker

_Martin Ondrus_  

---

### [Joint Semi-Symmetric Tensor PCA for Integrating Multi-modal Populations of Networks](https://ww3.aievolution.com/JSMAnnual2024/Events/viewEv?ev=1629 "Joint Semi-Symmetric Tensor PCA for Integrating Multi-modal Populations of Networks")

Multi-modal populations of networks arise in many scenarios including in large-scale multi-modal neuroimaging studies that capture both functional and structural neuroimaging data for thousands of subjects. A major research question in such studies is how functional and structural brain connectivity are related and how they vary across the population. Motivated by this, we develop a novel PCA-type framework for integrating multi-modal undirected networks measured on many subjects. Specifically, we arrange these networks as semi-symmetric tensors, where each tensor slice is a symmetric matrix representing a network from an individual subject. We then propose a novel Joint, Integrative Semi-Symmetric Tensor PCA (JisstPCA) model, associated with an efficient iterative algorithm, for jointly finding low-rank representations of two or more networks across the same population of subjects. We establish one-step statistical convergence of our separate low-rank network factors as well as the shared population factors to the true factors, with finite sample statistical error bounds. Through simulation studies and a real data example for integrating multi-subject functional and structural brain connectivity, we illustrate the advantages of our method for finding joint low-rank structures in multi-modal populations of networks.  

  

#### Speaker

_Lili Zheng_  

---

### [Multimodal Functional Graph Estimation with Application to Concurrent Measurements of EEG-fMRI](https://ww3.aievolution.com/JSMAnnual2024/Events/viewEv?ev=1633 "Multimodal Functional Graph Estimation with Application to Concurrent Measurements of EEG-fMRI")

Joint multimodal functional data acquisition, where functional data from multiple modes are measured simultaneously from the same subject, has emerged as a modern approach enabled by recent engineering breakthroughs in the neurological and biological sciences. For example, concurrent EEG-fMRI technique is able to record EEG and fMRI signals from a patient simultaneously. One motivation to acquire such data is to enable new discoveries of the underlying connectivity by combining multimodal signals. In particular, multimodal data integration often collects richer information, e.g., fMRI features high spatial resolution while EEG has high temporal resolution. Despite the scientific interest, there remains a gap in principled statistical methods for estimating the graph underlying multimodal functional data. We propose a new integrative framework that models the data generation process and identifies the latent graphical model, the brain connectome. Our approach is built on neighborhood regression and has been extended to the functional setting that accommodates multimodality. The goal is to understand, in the presence of rich information, what is shared across data modalities. 

  

#### Speaker

_Katherine Tsai_  

---

### [Topological Pooling on Graphs](https://ww3.aievolution.com/JSMAnnual2024/Events/viewEv?ev=1631 "Topological Pooling on Graphs")
https://arxiv.org/pdf/2303.14543
https://github.com/topologicalpooling/TopologicalPool

Graph neural networks (GNNs) have demonstrated a significant success in various graph learning tasks, from graph classification to anomaly detection. There recently has emerged a number of approaches adopting a graph pooling operation within GNNs, with a goal to preserve graph attributive and structural features during the graph representation learning. However, most existing graph pooling operations suffer from the limitations of relying on node-wise neighbor weighting and embedding, which leads to insufficient encoding of rich topological structures and node attributes exhibited by real-world networks. By invoking the machinery of persistent homology and the concept of landmarks, we propose a novel topological pooling layer and witness complex-based topological embedding mechanism that allow us to systematically integrate hidden topological information at both local and global levels. Experiments on 11 diverse benchmark datasets against 18 baseline models in conjunction with graph classification tasks indicate that Wit-TopoPool significantly outperforms all competitors across all datasets. 

  

#### Speaker

_Yuzhou Chen_, Temple University  

---
### Talk 1

### Talk 2
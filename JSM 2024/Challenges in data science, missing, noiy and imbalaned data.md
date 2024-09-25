 

# Talks

**Matthew Fried** Chair  

Tuesday, Aug 6: 8:30 AM - 10:20 AM  
5088 Contributed Papers 

Oregon Convention Center 

Room: CC-D140 

#### Main Sponsor

Section on Statistical Learning and Data Science

## Presentations

### [A Sparse Logistic Regression for Handling Block-wise Missing Data in High-Dimensional Multimodal Contexts](https://ww3.aievolution.com/JSMAnnual2024/Events/viewEv?ev=3553 "A Sparse Logistic Regression for Handling Block-wise Missing Data in High-Dimensional Multimodal Contexts")

High-dimensional multimodal data are increasingly utilized in various domains, such as biomedical imaging, multi-omics, and multi-source deep learning inputs. A significant challenge in multimodal data analysis is block-wise missing data. Our goal is to propose a sparse logistic regression for high-dimensional block-wise multimodal missing data without deleting or imputing missing values. The main idea is to construct the Gram matrix using only available data and to use it in a modified objective function for parameter selection and estimation, employing a LASSO penalty. In our proposed method, we further address the issue of a high false positive rate in variable selection by implementing a threshold technique. We compare our proposed method in terms of variable selection and classification performance with other methods through both simulation and empirical studies. 

#### Keywords

High-dimensional data  
  
Multimodal data  
  
Block-wise missing data  
  
DISCOM  
  
Sparse regression 

  

#### Abstracts

- [3651 - Direct Sparse Logistic Regression Estimation in High-Dimensional Block-wise Multimodal Missing Data](https://ww3.aievolution.com/JSMAnnual2024/Abstracts/viewAbs?abs=3650 "3651 - Direct Sparse Logistic Regression Estimation in High-Dimensional Block-wise Multimodal Missing Data")

  

#### Co-Author

_Man Sik Park_, Sungshin Women's University  

#### First Author

_Seong-Tae Kim_, NC A&T State University  

#### Presenting Author

_Seong-Tae Kim_, NC A&T State University  

---

### [An efficient algorithm for missing data imputation with high-dimensional data](https://ww3.aievolution.com/JSMAnnual2024/Events/viewEv?ev=3555 "An efficient algorithm for missing data imputation with high-dimensional data")



Motivation: Missing data leads to loss of information and statistical power. Existing imputation methods struggle with the high dimensionality of the data and the long computation times. We propose a new multiple imputation algorithm for sparse high-dimensional data that iteratively imputes based on selected variables, significantly reducing computation time.  
Method: We proposed iterative imputation methods using pre-selected attributes. Correlated attributes were selected for each variable with missing values using LASSO for further iterative imputation. Several iterative imputation methods proceeded after pre-selection, including MICE, missForest, and XGBoost. By selecting important attributes, the proposed algorithm could handle sparse, complex non-linear relations and high dimensional data without losing information.  
Result: Evaluation was performed on simulated and real-world datasets with missing values from 10% to 40%. Using root-mean-square error, we compared our algorithm with MICE, missForest, and XGBoost. Our algorithm outperformed others under different missing patterns including missing-at-random and missing-not-at-random data patterns with varying missing rates. 

#### Keywords

multiple imputation  
  
missing patterns  
  
MAR  
  
MNAR 

  

  

#### Co-Author(s)

_Jiajia Zhang_, University of South Carolina  
_Ruilie Cai_  
_Hao Zhang_, University of Arizona  

#### First Author

_Yunqing Ma_  

#### Presenting Author

_Yunqing Ma_  


Mean imputation, underestimates variablity, distorts distr

MICE assumes missing not at random





---

### [Efficient Inference on High-Dimensional Linear Models with Missing Outcomes](https://ww3.aievolution.com/JSMAnnual2024/Events/viewEv?ev=3556 "Efficient Inference on High-Dimensional Linear Models with Missing Outcomes")
https://arxiv.org/abs/2309.06429
https://github.com/zhangyk8/Debias-Infer

This paper is concerned with inference on the regression function of a high-dimensional linear model when outcomes are missing at random. We propose an estimator which combines a Lasso pilot estimate of the regression function with a bias correction term based on the weighted residuals of the Lasso regression. The weights depend on estimates of the missingness probabilities (propensity scores) and solve a convex optimization program that trades off bias and variance optimally. Provided that the propensity scores can be pointwise consistently estimated at in-sample data points, our proposed estimator for the regression function is asymptotically normal and semi-parametrically efficient among all asymptotically linear estimators. Furthermore, the proposed estimator keeps its asymptotic properties even if the propensity scores are estimated by modern machine learning techniques. We validate the finite-sample performance of the proposed estimator through comparative simulation studies and the real-world problem of inferring the stellar masses of galaxies in the Sloan Digital Sky Survey.  

#### Keywords

High-dimensional inference  
  
Missing data  
  
Semi-parametric efficiency  
  
Lasso 

  

  

#### Co-Author(s)

_Alexander Giessing_, University of Washington  
_Yen-Chi Chen_, University of Washington  

#### First Author

_Yikun Zhang_, University of Washington  

#### Presenting Author

_Yikun Zhang_, University of Washington  

---

### [Gaussian Mixture of Factor Analyzers with Measurement Errors](https://ww3.aievolution.com/JSMAnnual2024/Events/viewEv?ev=3557 "Gaussian Mixture of Factor Analyzers with Measurement Errors")

Observations on measurement error are commonly available in many physical and engineering applications. We develop methodology for model-based clustering in the presence of measurement error, and use that to classify gamma ray bursts (GRBs) from the Reuven Ramaty High Energy Solar Spectroscopic Imager (RHESSI) mission. Our statistical model incorporates the observations on measurement error along with a mixture of Gaussian factor analyzers that can explain the variability in each cluster via a small set of latent factors, and is equipped with a matrix-free computational framework that enables efficient parameter estimations. The proposed method allows for the characterization of different kinds of GRBs in terms of a few underlying variables, and provides a more comprehensive understanding of the spectral characteristics governing the different kinds of GRBs. 

#### Keywords

Gaussian mixture model  
  
profile likelihood  
  
EM algorithm  
  
factor analysis 

  

  

#### Co-Author

_Ranjan Maitra_, Iowa State University  

#### First Author

_Fan Dai_, Michigan Technological University  

#### Presenting Author

_Fan Dai_, Michigan Technological University  

---

### [Mixed Model Imputation for Missing Data in Social Networks](https://ww3.aievolution.com/JSMAnnual2024/Events/viewEv?ev=3554 "Mixed Model Imputation for Missing Data in Social Networks")

Network models are widely used in many areas from social networks to protein interactions to international trade. Most studies assume the ties observed constructs complete case, however in reality, many network data sets have missing data either due to unit/item-nonresponse or censoring. Therefore, the use of observed cases only assumes that all missing observations are not interacting. This causes estimated network-level statistics such as degree or closeness to be biased. In This paper proposes a multiple imputation method that uses latent actor effects as well as reciprocity estimates to impute missing values in the adjacency matrix and compares the proposed model to mostly used imputation techniques via a 2 factorial simulation study. 


### Notes


#### Keywords

imputation  
  
mixed models  
  
social networks  
  
simulation  
  
networks 

  

  

#### First Author

_Burcu Eke Rubini_, University of New Hampshire  

#### Presenting Author

_Burcu Eke Rubini_, University of New Hampshire  

---

### [Representative Sampling by Analytic Differentiation of the Sinkhorn Loss](https://ww3.aievolution.com/JSMAnnual2024/Events/viewEv?ev=3558 "Representative Sampling by Analytic Differentiation of the Sinkhorn Loss")

In this paper, we present a novel method for condensing a probability distribution into a core subset of representative points, utilizing Sinkhorn loss as a key tool. Sinkhorn loss, known for its computational efficiency, serves as an effective entropic regularized approximation to the Wasserstein distance. Our significant contribution lies in developing an analytic expression for the gradient of the Sinkhorn loss with respect to the input cost matrix. This development effectively mitigates the instability issue in current Sinkhorn algorithms. Leveraging this analytic gradient, we have formulated an efficient gradient-based algorithm for the strategic selection of the core subset. Our methodology demonstrates a tighter upper bound on the Wasserstein distance compared to Monte Carlo methods. Further, through extensive simulation studies and practical applications with real-world data, we establish that prediction models trained on subsets identified by our algorithm show superior accuracy. This breakthrough in representative sampling techniques holds substantial potential for managing large-scale datasets in the realm of machine learning. 

## Notes
What samples can we label to get the best classification examples if we have cost constraints around labelling

choose different distance functions that mnimizethe difference between points.

#### Keywords

Representative points  
  
Optimal Transport  
  
Sinkhorn Loss  
  
Wasserstein Distance  
  
Active Learning 

  

  

#### Co-Author(s)

_Yixuan Qiu_, Shanghai University of Finance and Economics  
_Xiao Wang_, Purdue University  

#### First Author

_Haoyun Yin_  

#### Presenting Author

_Haoyun Yin_  

---

### [The Strategic Synthetic Minority Oversampling TEchnique (S-SMOTE) for Imbalanced Classification](https://ww3.aievolution.com/JSMAnnual2024/Events/viewEv?ev=3559 "The Strategic Synthetic Minority Oversampling TEchnique (S-SMOTE) for Imbalanced Classification")

We present a novel and flexible synthetic minority oversampling technique for binary classification with an imbalanced response variable and overlap in the feature space. Imbalance and overlap are well-known data difficulties that can inhibit classifier performance (e.g. Li et al. 2021; Shahee and Ananthakumar 2021). Most solutions to this problem build on the popular and influential Synthetic Minority Oversampling TEchnique (SMOTE) (e.g. Chawla et al. 2002; Elreedy and Atiya 2019). Limitations of SMOTE include inflexibility in determining which minority examples to oversample and the treatment of categorical variables. We first use simulations to characterize the impacts of imbalance and overlap in a variety of scenarios where other data difficulty factors (e.g. missing minority data) and classifiers change. These simulation results are then used to inform our novel algorithm which addresses the limitations of SMOTE. The application of our algorithm to an imbalanced classification problem in student success research gave improved predictive performance in certain cases. We also briefly study the hyperparameters of our algorithm and give guidance on possible future work. 

#### Keywords

imbalance  
  
overlap  
  
oversampling  
  
SMOTE  
  
classification  
  
machine learning 

  

  

#### Co-Author(s)

_James Molyneux_, Swyfft, LLC  
_Claudio Fuentes_  

#### First Author

_Njesa Totty_, Framingham State University  

#### Presenting Author

_Njesa Totty_, Framingham State University  

---
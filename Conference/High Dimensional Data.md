### Statistical Significance of Clustering with Multidimensional Scaling
presented by Hui Shen UNC Chapel Gill

Questions is how do we determine the stat sig of clusterss, and how do choose # of clusters

solve this through hypothesis testing
null hypoth is data with 1 cluster

motivating example, clustering in single cell RNA seq
can apply clustering algorthim we can get to different visualizations with different # of clusters

High dime low sample size (HDLSS) SigClust liu et al 2006 
use gaussian cluster def
H0 data come fromr sindle d dimen gaussian
Ha datacame from a d dim non gaussian eg a mix of gaussians
Test Stat, 2-means cluster index CI
estimate null dis via monte carlo sim
strucutreassumion on Sig = M^MT

limitation of sigclust
est of cov matrix is hard in HDLSS Setting
hard to use sigclust when there is no access to orgiinal data, only dissimilarity matrix eg naturla language dataset
beyond gaussian

propose new multidimension scaling MDS based SigClust method for assessing the sig of clusters usin the test statistics, k means cluster index

extension to cluster def beyond gaussian

generalize to multiple clusters setting
theoretical prop control type 1 and 2 prop
sim and real data: competitive performance

beyond gaussian 
- the test sta is not sensitive to gaussain
- conver of cluster index under general dist
- gaussian as ref distr

considergeneral gypth
H0: data from a singld d dim unimodal distr
Ha1: data come from a mix of d dim unimodal

main idea
- MDS rep Y exists on R nxr, using only dissimilarity matrix
- Y preserves signle unimodal or mix of unimodal prop
- signal can be captured by cluster index
- apply sigclust on the space of Y

Generalized MDS based Sig
motiv: evaluate the exact number of clusters when there is more than one cluster

Method
- consider K-1 test stat Ci2..Cik
- for each CIk calc p value pk
- multiple comparison adjustment
- estimate number of cluster by argmin(2....k)pk

Theoretical prop

suppose data is a mix of 2 gausians with mean mu and -mu

Real data analyiss

Two datsets multi cancer hene expres 100 HNSC 100 LUSC 100 LUAD
d - 500
breat cancer gene expression data 97 lUMA, 91 basal like, 47 normal breast like, and 48 HER2-enriched samples d= 1645
![[20230525_133547.jpg]]
deal with more thna two clusters
paiwise comparison
joint comparison
null expeirment on single cluster

methosd for compare
original siglcust
MDS sigclust

cancer gene expr data

method indetifies number of discernable clusters

summary propose cluster evaluation method using multidimensional scaling than can deal with high dimensionality and work if only dissimilarity matrix is abilable
extend the notion of stat signig

future directions
effect of dimension reduction tasks, in particular multidim scaling on clustering prop
notion of stat sign of cluster(beyond the types of hypothesis (unimodal) above)
starting pointin understanding more complicated techniques such as UMAP and T-sne and then explore other poperties of project data

megan asks how to strucutre the data

generally speaking cluster index is used if the cluster definition is concentrated inthe middle, especially for uniformly distributed 

### Regularized Multivariate Functional Principle Components Analysis via Penalized Functional SVD Approach
yue zhao reMFPCA
background PCA is dimension reductio ntechnique to extract ccomponents as linear combo of observations

functional data anaylsis is an area of research that deals with the obervations of continuous funcitons

functional PCSA is a dim reduction tech in functional data analysis to extract component functions as a linear combi of functional observations

pic of FPCA and reg FPCA slide
![[20230525_135014.jpg]]

pic Lit review slide 1
![[20230525_135222.jpg]]
pic lit review slide 2
![[20230525_135312.jpg]]
Our work
Two ReMFPCA approaches are propese
cross covariance operator approach, we studied mathmetical prop of ReMFPCA and extend silverman to multivariate
Penalized function SVD we studied foundations of function SVD and extend huang et al 2008

Why this penalized function SVD approach is useful
- closed form GCV criteria can be derived from this penalized functiona SVD, it can sig improve comp efficiency
- it suggest and efficient power algorithm with two felxible choices
	- joint power: simultaneously estimate all FPCs with consistent smoothingparameter (FPC will strictly follow the orthogonality in Sobolev Space)
	- squential power: estimate each FPC sequentially, differnet smoothing parameers are allowed for each FPC(multiple smoothing parameters perform more suitable smoothing)
- Propsed GCV criteria can be sunoky embeded in the power algorithim

Prelim Notations slide pic

![[20230525_135731.jpg]]



### Novel spatial clustering based on delaunay triangulation
motivation, traditional clustering, kmeans dbscan
failes to handle datasets that differe in size shape denisty noise outliers,
touching issues multiple bridges, neck proble, adjacent problem
basically it chains multipel clustering methods together to solve these issues
![[20230524_155140.jpg]]
![[20230524_155332 1.jpg]]

![[20230525_100811(1).jpg]]
### Sandwich smoother for spatio temporal data
questions of interest 
can we represent our data in a functional form and estimate therelvent parameters using only a laptop in a large data context
represent data as a 2d matrix, 1 spatial, 1 time dimension
used radial basis functions based on wendland covariance functions instead of bsplines
STSS penalty, penalize coefficients based on spatial proximity instead of linear adjaceny
applied data to NA CORDEX 
want to smooth150 years worth of daily temperature data
930k spatial x 365 dayx 150 years
5 billion response values
11.9gb and 19.9 gb
31gb of data process unparallelized 3 hours, parallelized 20 min, smoother data can be reconstructed from a set of evaluated basis functions

### Denoising Nueral networks for nuclear resonance spectroscopy
motivation develop tech capable of detecting opiods in opened packages in the mail
pulse excitation signal into package, which causes opiod molecules to return a resonant signal, similar to MRI
tried DRNN dual real, 2 networks 1for real comp 1 for complex
DRC-NN concat both obs in 1 signal
CV-NN operates directly on complex valued signalsDR scales faster with parameters and levels off early, CN performs ebst overall (complexNet)
complex values convtasnet (CV-CTN) blows everything out of the park
has a paper and python package
https://arxiv.org/abs/2211.00080

### ollivier Rici curvature Community Detection on Hierarchical networks
community is a subset of verticies in  hrapg that have a higher thna average density edges between them
gierarchical community find communites embedded in other communities

usually use Louvain algo
girvan newman algo

Ollivier ricci curvature
discretized ricci curvature defined on weighted graohs
property: nridges between communities have negative cuvature

applied to NCAA College football data
each nodei s football team, edges are games
adjust the curvature threshold to identify communities groups
UNC Dept biostatistics Didong Li?

![[20230525_101418.jpg]]
### gausian process spatial clustering
Spatial Clustering
goal cluster NC census tracts based on regionalization and distr. of socienvrionmental cancer risk factors
Spatial domain and curvature domain
propose algorithim GPSC 
start random intialization each step fit a different faussian process, and reassign pointsto clusters, converges
applied to NC dataset, produces 'better' clusters

![[20230525_101515.jpg]]

### Generalization of two well known indicies in choice of number of clusters within an agllomerative hierarchical clustering
hes french i cant understand him
choice of number of clustes with indicies,
two are well known calinksi harbasz index
hartigan index
CH index is defined as a ratio of between clusters sum of squares and within clusters
these two are designed for eculidean distance and wards criterion
outside of this, these indicies do not perform well

solution
showing properties to compute these indicies with ony the dendrogram in euclidean distance/wards criterion
adapting these two indicies to all cases
important remarks
with euclidean distance and ward criteron, these formulas are exactly

available in XLstat software

### Does misclassification of binary outcome affect model prediciton on the true label
motivation
gow does data acciracy affect the performanceof predicive model
problems in data accuracey, from surveys, webscraping, semi supervised learning 
generate data > misclassify Y > fit logistic regression

evaluated
1 misclassified, crossvalidated performance
true: generate test data set and predict true Y
corrected: correct misclassification using MCSIMEX kuchenhoff 2006, generate test dataset and predict true Y

### manifold clustering in the setting of generalized random dot graphs
how might we cluster the nodes of a network
connecting block models to GRDPG
works for linear network

challenging for non linear community structure

develped k curves clustering algorithim
example drosophila connectome

asymptotic results
https://github.com/johneverettkoo/manifold-block-models
![[20230524_162420.jpg]]
![[20230525_101646.jpg]]
### markov chain montecarlo convergence assessments under truncation
intro truncated distribution are sometimes used in modeling of proportion data
motivated by obersvations from bivariate hierarchical bayseian modeling for small area estimation, using county level arcsine square root transformed proportion data
while there are severalways to evaluate convergence in MCM
gelman-rubin
- used parallel chains with dispersed intiial values totest convergence
geweke
- test whether mean estimates have converged by comparing means from ealt/latter part of the markov chain

using hierarchical bayseian paproah the perofrmance of these convergence stats was simulated fr 2 us states

gelman-rubin R and heidelberher-welch appear to be more in aggrement with each other than with geweke, gelman-rub test reuslts generally consistent with traceplots
	although geweke and heidelberger are not 


### pragmatic solutions for longitudinal cluster randomized trials

clustered random trial

cluster image

complicated correlation structure
intracluster correlation
longitudinal correlation
cross-subject correlation

propose sample size estimation approahc
has closed form and can be exetnded to calculate power or cluster size
si applicaple to all longitudinal clinical trials through design vectores
incorporates unbalanced randomization through randomization ratios
accomated arbitrary missing scenarios throug missing pattenr and observational

could be easily extended with varying cluster size

### regularized singular spectrum analysis
SSA ins a non  parametric technique for time series
makes time series smoother, a couple of different methods

### Rejection Sample for Weighted Densities by majorization
we revisit vertical strip method "ahrens method" of rejection sampling
this work focuses on weighted target densities
andrewraim.github.io

### sparse subspace clustering in diverse multiplex dimple network

consider an undirected netowrk consiting of n nodes with k communities,
stochastic block model assumes that eahc node i belongs to one of k distint block or communities
communiy assignment is described by clustering function witha a clustering matrix
in some applications we may have multi layer networks, or a sequence of networks, may have layers that have the same community strcture
want to group layers

diverse multiplex network model (DIMPLE)

we propose novel spectral clustering based clustering algo for between layer clustering, method 
arxiv 2206Majid norwiz



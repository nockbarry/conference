## Mobility Loci: identifying spatial areas where people move to and though using new zealand census data

What is it 
Human mobility describes phyiscal patterns of movement of peopel within a spatial system
tends to by cyclic
not very well understood at scale
fundmaental to other areas of study
epdiemiology
tend to be oppourtunisitc in the data, lots of brittle 
urban planning

focus of this talk is on how more commuting type movements

Overall Goal
develop useful methods and tools for understanding patterns of human mobility
goal for this project, identify ares people move to and thoruhg at a high rate given patterns of movement
needs to be agnostic to pop denisty,
needs to maintain individual level anonymity

in urban planning could be useful to reduce chokepoints etc

New zealand stats
sspeaker recommends new zealand for plethora of stats/data 
2023 census
commuting data
NZ uses spatial areas call SA2's like census tracks, statistical areas
include commuting data
work SA2 area for each home SA2 area
r package ghroute gives routing data (solves routes for a from and to location)
we can estimate morning commutes for everoyone in NZ

mobility graph pic

![[20230526_120428.jpg]]
represents this as a directed graph, edge weights are number of peoples

Strong compnents in a directed graph means you can from one vertex in a compnenet to any other vertex in that component

PTM from mobility graph
P be a matrix that results from normalizingover the rows of the mobility graph
sparse matrix m

scaling provides a mobility measure relative to individuals rather than total movement between SA2s
allowing us to directly compare movement patterns between ares with differen pop densities
equivelent to estimating the transition probabilities between SA2 area using the maximum likeligood estimator

Stationary Distribution

to quantify mobility we use the stationary distr of SA2 ares which as defined as pi = Ppi where P is the PTM
in order to calculate, two conditiosn need to be met
the matrix P must be irreducible (from any point in the graph, you must be able to get to another point)
P must be aperiodic

calculating the stationary distr

0 = Ppi - pi
0 = (P-I)pi
we now have a linear system of n equation of n variables. to constrain pi so that its sum is one we add the following row to the system
(0,1) = (P-I,pi)

Loci

Which pis are larger than expected given the mobility structure
how do we test this
how do we specify this
let PI be the vector of stationary distributions of each of the sites
define loci as pi_i for which P{PI_i >= pi_i} <= alpha

How do we estimate this a permutation test on the non zero entries of the sparse matrix
not going to bootstrap, just permute, to maintain the total amount of mobility in the system

results pic
![[20230526_121608.jpg]]
red is the stationary distr under the null
on the evening commute, we see no spikes, as they are commuting away from a city center

we recover the urban locations as the loci

he has a package called graph loci that will be on cran eventually

## Graphical group ridge logistic regression for high dimensionaldatasets
Saeed Aldahmani
UAE University

Intro
it is common in rcenet real life classificaiton problems to find that the sample size is smaller than the number of predictors
typically refered to has high dimensional data
ordinay classification methods sucj s logistic are not applicable because the maximum likelihood estimates can not be obtained

Lasso and ridge attempt to make sparse coefficient matrix

variuos approaches have been proposed to estimate the optimal value of tuning parameter gamma, the most well known is cross validation

all these methods attempt to find the optimal shrinkage tunign aparameter for all predictors without taking into consideration the interdependence between the predictors
this results in having some of the predictors over-shrunk
therefore defining different groups of dependent predictors and finding the appropriate penalty for each group of predictors...

propose new metho based on graphical models which use the conditional correlation structure between the predictor variables to classify them into disjoint groups and estimate the optimal value of the penalty (shrinkage parameter) for each group

this approach tends to decrease shrinkage of variables

focus in undirected graph
graphs has a set of cliques with separators
cliques are subgrapghs
1 connected to 2 and 3, 2 connected to 3, 3 connected to 4 and 5, 4 and 5 connected
2 cliques in this graph
3 is the seperator

proposed method slide
![[20230526_123120.jpg]]
an algorithim is proposed to finds groups of predictors and the optimal tuning parameter Lambda1...q to estimate the GG ridge logistic

model selection algo slide 1 and 2
![[20230526_123239.jpg]]
![[20230526_123431.jpg]]

sim data results
![[20230526_123822.jpg]]
real data
two different real datsets are used
madelon dataset, 500 predictors and 200 observation of which 75% ie 150 use to train, 25 test

LSVT voice rehabilitation dataset, 310 pred and 126 obs, highly imbalanced classification problem with class wise distr of 84/42 

real data results
![[20230526_124032.jpg]]
conclusion 
new mthod called GGR-logist regresion is developed for estimating logisit reg coefficient of he model in the context of high d data, by grouping the predictors int osets of partially correlated variables and applying different shrinkage parameters to eahc group

## Generalized Influence Maximization Problem
Sumit Kumar Kar

influence maximization problem, IMP a tool to solve optimization problems on social networks
applicaitons in viral marketing epidemiology, cell cycle regulatory analysis

Goal
a marketer wants to gain customers all over the USA

Strategy they give away k free products at time 0, these k people influence their friends at time 1, these friends recommend their fraiends at time 2 and so on

influence function sigma(A) = expected total numberof people influenced in the long run

Stochasticity
Some firends would lsiten to you, others wont

stochasticity in fluence spread captured vy standad influence difussion models
we will use trigerring model throughoutthis work

Triggering model: each peson has a random triggering set of friends who can only influence them
Lienar threshold moldel: a person gets influenced if the wirghted influence of their neighbors crosses a threshold
Independent Cascade Mode: every influenced person gets a signle change to influence their neighbors with a certain prob
Other models...

Kempe et al 2003
IMP is NP hard
sigma(.) is submodular
Let S* be an optimal solution and Sg be a greedt solution obtained by choosing one element at a time that provides the larges marginal increase in sigma(.) then 
sigma(Sg) >= (1-1/e)sigma(S*)

Pracitcal Concerns
Finite/infinite gorizon
marketer wants to gain influence within a finite time

multiple/zero seeds
a person may be given multiple free products, each person has their limit, some people may be unreachable

vertex and time dependatn rewards, people have different value, earlier a person is influenced more reward they bring

stochastic seeding, people are influenced stochastically, influence prob increases with number of free products

our work generalized IMP
notations G = (V,E)
Horizon T0 <= inf
reward lambdaV earnied if v is influenced at time tv for all v

person vi has seed limit ri
person vi is given bi seeds,=
influence probabilty qvibi is non dreasing in bi
vi is in triggering set of w with prop pibi vi w
pi bi vi w is non decreasing and concave in bi

find argmax of object function
where objective is expectation of the lamdaV for all the people
challenges two layers of stochasticity
first from triggering model, second from influence probability
possible nonlinear reward function
vecotr allocations instead of sets

Theorem 3, let v* be an optimal solution of the generalized IMP then we construct a freedy solution bg such that zeta(bg) >= (1-1/e)zeta(b*)
greedy soltuion with multiple seeding brings at least as much expected reward as that without multiple seeding

Theorem 1; G can be expanded into a graph G' such that solving generalied IMP on G without stochastic seeding is equivalent to solving gnerelazed IMP on G' without stochastic and multiple seeding

theorem 2: zeta(.) is equal to a non negative monotone increasing submodular function


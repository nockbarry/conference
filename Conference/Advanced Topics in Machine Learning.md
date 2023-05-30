### Reproducible Feature Selection for Accelerated Failure Time Models via Knockoffs
Daoji Li

Motivation
consider accelerated failur etime model Wei 1992
logT = alpha = X1B1 + ... XpBp +e
T is failure time
x1...xp vector of covariates

Motivation slide pic with references
![[20230526_100620.jpg]]
practical use is, grow to control fraction of false discoveries effectively with limited sample size

None of the existing approaches can control the false discovery rate

FDR is the expected proportion of falsely selected variables
first formally described by yoav benjaminin and yosef hochberg in 1995

goal develop an approach that can not only identify truly important variables, but also control the FDR at a preassigned level q for survival data in the finite sampling setting 

main idea in our proposed methos is to used knockoffs, another framework for variable selction

knockoff filter, or simply knockoffs is a framework for fariable selection with FDR control introdduced by Barber and Candes in 2015 (Fixed X knockoffs)
Model X knockoffs in JRSSB 2018 (candes, Fan, Janson, Lv)

model x dont need to assume the relationship between the response varialbe and the covariates, so model free?
covariate is not assumed to be fixed

key idea is to create a knockoff copy of the design matrix to mimic the correlation strucutre found withth the original variable. Knockoff variables will play a key role in controlled feature selection by serving as negative controls that allow us to estimate and limit the number of false positives

the constuction is cheap: does not reqiore collecting any new data, does not use the information in the response varialbe
the knockoffs serve as negative controls and they allow one ot indetify the truly important predictors by distribution free and powerful FDR controlling algorithims
no need to calculate p-value
informationally speaking, knockoffs has the property that no methodcan statistically distinguisshthe original matrix from its knockoffs without lookign at the response variables

Applications of knockoffs picture

most of the papers used this idea for complete data

when distr of x is known, one can constict exact knockoffs

when distr of x is unknown, one can construct approximate second order knockoff features x~, the invariance of the mean can be easily satified by forceing the E(x)=E(x~) and the second order pairwise exchangeability. Cconstruct cov(x,x~)

Our approach
step 1Construct knockoff by M-X knockoffs in Candes eta al 2018
step 2, weighting, we apply kaplan meir weights developed in stute 1993 to deal with censored data
step 3 construct knockoff statistics Wj, where large Wj indicate importance of Xj, 
step 4 estimate set of relevant predictors using thresholds 

Numerical Studies

Compare our method with the regularized weighted least squares regressin in Huang et al 2006

In general knockoff+ selects the least number of features as relveant 



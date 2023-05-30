## Non parametric Estimation of Multivariate Spectral Density Function using Bassi Expansion

presented by Shirin Nezampour

Univariate Spectral Density Estimatonn
spectral anaylsis to get frequency information

anlysis of spectral densityfunction or spectrum in frequency domain helps to
understand dynamics
explore periodicites
analyze and estimate


Classic non parametric
periodogram naive pnonparametric spetral estimator,
inconsistent

Smootherperiodogram
can be obtained by averaging band of frequeneys, centered averaging, tapering methods

parametricapprouch model mispecificationcna lead to a poor estimate so we use non parametric

non parametric spectral estimation and basis models

question is how we can estimate model parameters to estimate the sdf and avoid overfitting

if we violate normailty, LS estimation should not be used

at each frequency the spectral density matrix *SDM* is a positive definit and hermitian matrix
pic
so spectral analysis of multivariate ime series is more compl

pawitan 1996 estimaed SDM for bivariate time series by minimizing penalized profile likligood
not generalizable

moved toward penalized likelihood through minimization of penalized whittle likligood

SDM is a convariance matrix function of the fourier transform

whittle likeligood 
for stationary gaussian process wgittle is asymptoticall equaly to -2log of likelihood

direct minimiation of whittle likelhood is challenging to do positive definite constraint of spectral density

use a basis of freqencies and prob estimate
to smoothlt approximatite cholesky components
to miimize the penalized whittle likeligood applied fisher-scorig algorithim

smoothing parater by AIC

simulation setup run a bivariate time series

appleid to el nino southernoscillation

iregullarly periodical disruption in the climate sysmte over the tropical pacific

entral pacific warms every 3 to 7 years due ot this effect

osciliation of warm water traveling between australia and south america

used time series of ENSO for a period of 453 months between jan 1950 and sep 1987

souther osciliation index measures change in air pressure ralted to sea suface temperatrue 
and temperature
goal is to find the relationship between these

have frequency plots for the two time series

and can use squared coherence, a kind of correlation of time series

Questions
discrete time series with different sampling rates
missing values in data

## Project dynamic linear modle for time series on the sphere
presented by john zito

motivation, what do we do when we have time series that is non standard, not real valued discontinuous data
what if its continuos surface, what if its count data, what its a mix

today it is what if thje data comes fromthe unit n sphere

these data aris in sdirectional dtatiics where we record mesaurements on the orientation or direcvtion and travel of an objectthese can be measured as points on a sphere

on unit circle can represent as vector, or an angle

wind direction at black mountain australia, collecting high frequency time series on wind direction over hour. Time series of angles
we seespikes in data thatrepresent when theangle crosses over 2pi to 0 again, and it looksl ike in time series spikes, when its actually not spikey

goal is to represent the strucutre of the data in models, as when you represent some data without taking in the strucutre, you may get what appear to be discontinuties

my question is can you cut the time series into chunks,change where your braking point/singularity is, and the restitch it together

going to use a normalized gaussian that repesents data as a distribution along the unit circle, going to repsent it as a state space model for spgerical data
ie our mesaurments are measured from some unobserved latent distribution

could take a time varying coefficients of a regression model
can split models into static and dynamic components

want full posterior

two data environments,
batch/offline, MCMC algorithim (slice within gibbs)
streaming/online, rao blackwellized particle filter

MCMC does break the baysean goal of having yesterdays posterior being todays prior

generate forcasts using posteriro predicitve distrivution

going to compile portfolio of models
linear gaussian naive models
autoregressive 
wrapped autoregressive, fisher and lee 1994 jRSSB


## Wavelet based method in aggregated finctional data analysis
presented by alex rodrigo dos S Sousa

problem of estimating individual mean curves from aggregated curves appears in several aresa

in spectroscopy there is an interest in estimating indivual mean absobance curves of the composition of a given substance from samples of absobance curves of a substance itself

electricity grid, overall curve of usage is based from everyones indidual curves
in data with peaks, discontinuous, oscilations

when composing multiple types of curves, spikes, step like, and chirp freq, we have a distributionthat is hard to introspcet on, want to recover each fo those curves

can use wavelets for this 
propses wavelets vasis to estimate individual mean curves from aggregated curves
wavlet coefficients are typicall sparse
can be ovtained by fast computational algorithims
magnitudes of coefficients are linked withsmoothness properties of functions they represent
propses applicaitons of bayseian wavelet shrinkage rule based on a mixture of a point mass function at 0 and logistic distribution as a prior to the wavelet coefficients

we expand compnenet curves in a wavelet basis, decompose each componenet function by wavelets

apply discrete discrete wavelet transform on both sides of 
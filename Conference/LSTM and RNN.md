### Biometric Data driven model for predicting fatigue while performing manualmaterial handlijng tasks using an LSTM RNN

Research Gap and motivation 

digital twin framework deveoped by sharotry 2022,
create a way to rpedict human fatigue to prevent injury before it occurss

objetive

identify ML model than can predict time series
securequlity physio data (foundhexoskin data manual material handling, lifting and lowering operations)
develop ml model
implement ml model
predit rate of percevied exertion RPE

problem and application

manual material handling contributed to over 247,620 musculoskeletal disorders MSD cases in 202
further 2.6 million non fatal injuries occured in the workplace in 2021
31% upper extremities, primarily shoulder
47% trunk, primarily back
16%lower extremities, primary knee

my Q can you use this for predictive maintenance in machines with similar sensor type data

Human Digital Twin HDT
virutal repr of an indivdual that is updated from realtime data, using sim and ML to simulate characterstics , behavior and individual physiological parameters

compnents
sensors (hexoskin)
physio data
data analysis and optimization
real time feedback, AR

data collection

video human material handing
task lift and lower
active sensor, hexoskin smart garmet
hexoskin smar suit includes textile sensors embedded in garments for precise data measurements
cont hear rate, breating rate, minute ventiliation?

linking BOrgs scale RPE to hexoskin data,
Borgs rating of percieved exertion, 6 to 20

experiment protocal

fiftenn lifts and 15 lowers every 9 seconds, for a total of 30 repitions

fatigue protocol until subject reaches RPE of 17 (get subject on a treadmill, increas inclination every 5 min)

then lift again same routine

model and results

model selection LSTM 
model selection slide pic

need LSTM instead of just RNN to capture long term dependicies due to RNN having vanishing gradient problems.

file shape, 10030 values in total time series
59 time steps in each sequenct
3 input features

multiclass classifiers
6

accuracy and loss plots show minimal overfitting, and the validation and training curves follow eacj other            

lots of audience questions
and potential for future work, adjsutingthe tiem window, chaningthe layers/parameters to see if the model starts underfitting/overfitting
apparently this did better than xgboost
future work including mutilple subject of different age, gender body type etc

### Oracle LSTM a NN approach to mixed frequency timeseries prediciton
alessandor bitetto, italy pavia
![[20230525_104423.jpg]]
motivation
in contxt of macro economic indicators there are two main concerns regarding the frequency of the variables
soem indicators are reported annyally, some quarterly, others monthly

there is a need for forcasting predictors between reporting dates, eg before the end of the uear

we develop a two steps algorithim that makes use of two recurrent nueral networks

MIDA approach 

miles tone in modeling mxied freq time series is the mixed freq data sampling model (MIDAS) hysels, santa clara, valkanov 2004

it extendes autoregrssive strucutre with a wise alignment of diff freq

it weights the lagged freq subject to parsimony constraints

advantage of requring few parameters to be estimated

polynomial limitation in modeling time series

any estimation algo can be used toestimatethe parameters, this leads to unrestricted midas

given the high number of parameters it is possibleto impose some spare constraints so that the contribution of fixed lag an be 

in ANN MIDAS the high freq time series are alignedand combined through decaying weights and then fed into a fully connected NN to predict lowfreq targets
(Xu et al 2019, li et al 2021)

the problem is when you want to forcast GDP, no matter how many high freq time series you have, monthly, weekly, you are still constrained by the ?

both methods have limitations

MIDAS can model only a small set of non linearites

ANN_MIDAS can suffer form the small amount of available target variables, which all high freq time series must be aligned to

Proposed methodoloy

Oracle LSTM
Oracle aims to produce reliable high freq pred ofthe low freq target variable, eg GDP, but at a higher freq
it is a depp autoregressive netwrok MLP (multi layer perceptrons)
the predictor learnshte relationship between the predicted high fre tager and high freq input, it is a LSTM recurrent netowrk

Adv in this way the oracel can generate many target observations at once, that are thne used as target by the predictor 

model arch picture
![[20230525_110812.jpg]]

oracle trained in rolling window fashion, makes prediciton of 1 of the low freq target
predictor takes the true varialbe, and hte predicted valuable 

loss takes into account the predictive power ofthe oralce, one weighted loss term for the oracle, predictor, and the Oracle+predictor

loss plot pic
![[20230525_111211.jpg]]

two sets of data were tested

simulation with a mix of sinusodal function and time decayfunction, so as to simulate seasonilty with differnt periodict and trends, the target variable has been evaluated applying a different non linear function to each input variable with the additon of noise

a real data set, withannual GDP as target and monthly inflation, unemplotment, balance of trades and current account for ital from 1960 to 2021 as predictors

results pic 
![[20230525_111438.jpg]]
conclusion and future owkr

oracle lstm can be a good candidate in the set of tools used by central banks and governments to nowcast macroeconomivariales in a reliable way

different arch for both oracle and pred should be tested (transformer other models etc)

test additional mixed freq input data

evaluate feature imporatnce(shapley values and gradient based explained to make the approach less opaque and more explainable )

statslab pavia

future work with ablation ,adjusting parameter size
atm the oracleis 2 layer fully connected, and 3? layers lstm?
smallish models more work on evaluating the parameter size on overfitting inthe future

used pytorch for the models

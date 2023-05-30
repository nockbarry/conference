## Interaction selection and prediciton performance in High Dimensional Data: A compartice study of statistical and tree based methods

presented by Chinedu Jude Nzekew
![[20230524_134431.jpg]]
problem statment is machine learning algorithim better than traditional approach to interaction slection
large predictors p >> n for interaciton selection
hierarchical structure dependance and interaction slection restriction
capturing of non linea nad non parametric interaction selection relation in big data
there is a gap in the literature comapring machine learning models

aim to investifate relative prediction performance of two difference approacjes
stat regression and tree based
- regularization path RAMP
- iterative random forest
address regression and classifcation
compare on sim and real data

interaction terms grow exponentially with number of parameters

RAMP uses marginality principle to maintain hierarchical structures in variavle selection process

step 1 initialize main effects fitting using LASSO
step 2 path building, repeat this step

![[20230524_135207.jpg]]

tree based models provide a measure of feature importance which can be used to indentify potentiall important interactions

Iterative random forest sequentiall frows feature weighted random forest to minimize the feature space and stabilize decision paths

Summary
Ramp algortithm shows better prediction performance thanthe iRF in the presence of hierarchical strucutre, regardless linearity
IRF has overfitting approaches
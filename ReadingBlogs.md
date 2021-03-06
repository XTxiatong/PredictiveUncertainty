## Why Bayesian Neural Networks?
Quantifying the uncertainty from data and model.
A comparison between standard NN and Bayesian NN can be found [here](https://towardsdatascience.com/why-you-should-use-bayesian-neural-network-aaf76732c150).


<!--Note: ## NeurIPS Overview
![image](https://user-images.githubusercontent.com/26398708/149753171-677305c9-a5cf-44c7-ac10-32c2b43bfe58.png) -->

## Paper connections
<!--Note![image](https://user-images.githubusercontent.com/26398708/149754970-7cf046c7-3712-45de-8ec5-d18ffc2e5571.png)-->
![image](https://user-images.githubusercontent.com/26398708/151996312-75580eb6-5440-4281-9372-587ad2879374.png)
![image](https://user-images.githubusercontent.com/26398708/151996184-33e9dba3-f477-4714-aba6-1d5ae0eccb32.png)


## Evidential Network/ PriorNetwork/ Posteroir Network

Instead of estimiating the distribition on weights, i.e., Beyasian learning, evidential deep learning is to find the distribution over predictors. \
Assume that what we obatin from a nueral network is not the categorical probability *P* usually presented by softmax probability vector (0.1,0.8,0.1), but a distribution *u* over *P*, pamaraterised by (1,8,1). 

<!--Note: If the prior of the distribution is Dirichlet, then the posterior is still Dirichlet because Mulitnomial distribution is conjugated to that. -->
 


How Dirichlet looks like:
![image](https://user-images.githubusercontent.com/26398708/144232674-8744daa1-7ca4-47f8-984a-8817c772fc89.png)
Advantages:
1. Keep the model size. No extra parameters.
2. One pass during inference.
3. Distingish the source of uncertainty. 


<!--Three strong but non-realistic assumptions of PriorNet:
1. An arbitary target prior *D(1)*
2. OOD exposure during training
3. Differential entropy can be nagetive (no sense)
4. No bound for alpha. 

NIPS2020 (2021 with graph based) paper overcame those limitations: -->

*Posterior Network: Uncertainty Estimation without OOD Samples via Density-Based Pseudo-Counts* 

![image](https://user-images.githubusercontent.com/26398708/144252840-c937d419-df0a-4005-b378-ff9f7c07fb38.png)

![image](https://user-images.githubusercontent.com/26398708/151996587-7066e901-bbb4-499a-afcb-7069e7c2732b.png)

Research questions:
1. To what degree is the estimated uncertainty calibrated? (ECE)
2. How to transfer the Pseudo-Counts into human-interpretable confidence score?
3. How to determine the threhold to distingish the incorrect and OOD samples?


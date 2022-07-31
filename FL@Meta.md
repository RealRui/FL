Back to https://github.com/Kwangkee/FL

## Papers 
Where to Begin? Exploring the Impact of Pre-Training and Initialization in Federated Learning, https://arxiv.org/abs/2206.15387

## Simulator
https://github.com/facebookresearch/FLSim

***

## Where to Begin? Exploring the Impact of Pre-Training and Initialization in Federated Learning
[Where to Begin? Exploring the Impact of Pre-Training and Initialization in Federated Learning](https://arxiv.org/abs/2206.15387)

*All experiments were performed using the open-source federated learning simulation framework FLSim [[1]]*(https://github.com/facebookresearch/FLSim)

How does the initialization (random, or pre-trained) impact the behavior of federated optimization methods?

6. Recommendations  
In this work, we study the affect of pre-training on federated optimization methods. Our results inform a series of the following recommendations:
- When evaluate FL algorithms, researchers should experiment with both pre-trained (if available) and random weights as they have different behaviors.
- When deploying FL to production environment, researchers should use adaptive server optimizers such as FedAdam and SGD at client. This setup works well and should be used a baseline before trying out more complex methods.
- Heterogeneity is not as a big of a problem when there is public data to pre-trained a model. We encourage researchers to pay attention other more complex tasks when there is no public data such as recommendation systems or semi-supervised learning.

Conclusion  
In this paper we present a thorough empirical analysis of initialization on federated learning by evaluating it on twelve federated learning algorithms across four vision and text tasks. We find that
pre-training on public data can recover most of the accuracy drop from heterogeneity. We show that client updates starting from pre-trained weights have higher cosine similarity, which explains why initialized with pre-trained weights can speed up convergence and achieve high accuracy even in heterogeneous settings. We further show that using simple SGD locally can be as good as other local optimizers.. 

## Federated Learning Simulator (FLSim)
https://github.com/facebookresearch/FLSim
Federated Learning Simulator (FLSim) is a flexible, standalone library written in PyTorch that simulates FL settings with a minimal, easy-to-use API. 
FLSim is domain-agnostic and accommodates many use cases such as computer vision and natural text. 
**Currently FLSim supports cross-device FL**, where millions of clients' devices (e.g. phones) train a model collaboratively together.

FLSim is scalable and fast. It supports differential privacy (DP), secure aggregation (secAgg), and a variety of compression techniques.

In FL, a model is trained collaboratively by multiple clients that each have their own local data, and a central server moderates training, e.g. by aggregating model updates from multiple clients.

In FLSim, developers only need to define a dataset, model, and metrics reporter. All other aspects of FL training are handled internally by the FLSim core library. 

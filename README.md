HAFL - FL 6G Edge Federated Learning 

Basically building a Federative Learning Framework For AI Native 6G edge networks where 
devices train locally and share the model updates instead of private data .

The Problem here is the real edge devices have Non-IID data , Limited Bandwidth, Latency, Random Client Droupouts, 
Unreliable clients. 

So the baselines models like Fedavg, Fedprox wont usually work over here as the problems mentioned above exists.

THE SOLUTION WE CAME UP WITH :
														 Clients
																|
														 Training
																|
													HAFI Intelligence   
																|
													Top-K Compression
																|
													Edge Aggregation 
																|
													Regional Aggregation
																|
													 Global Model 
In HAFI the features which are taken into considerations are :



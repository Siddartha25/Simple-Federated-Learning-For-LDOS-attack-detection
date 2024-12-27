# Simple-Federated-Learning-For-LDOS-attack-detection

This repository will contain my progress in designing and implementing an LDOS attack detection architecture using federated learning
The dataset used throughut this project has been custom generated using Ryu controller in an SDN network to simulate the attack and non-attack traffic.


*Federated_LDOS*
contains a simple federated ML model which uses a bidirectional lstm to classify the traffic as attack and non-atttack, in which there is a pretrained base model which is sent to 3 clients and each of these 3 clients locally train this model using their own data(which has been simulated by the dataset split), after local training each of these local models is sent to the centralised server which updates the global base model in every iteration using a synchronous simple weighted average.


*Federated_LDOS_modification-2*
it is an improvement over Federated_LDOS which contains a better ML model and it also incorporates differential privacy and homogenous encryption in order to secure the communication between the federated clients and the central server, differntial privacy reduces the accuracy inorder to improve privacy so I need to find a better method to provide privacy of client data without compromising accuracy in the learning process 

# Differentially_Private_Wireless_Federated_Learning_With_Integrated_Sensing_and_Communication

[![Status](https://img.shields.io/badge/status-building-yellow)](https://github.com/DataWizard1631/Differentially_Private_Wireless_Federated_Learning_With_Integrated_Sensing_and_Communication)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)


### Statement of Purpose
This work is a reproduction and implementation effort of the research paper titled ["Differentially Private Wireless Federated Learning With Integrated Sensing and Communication"](https://ieeexplore.ieee.org/document/10948161?denied=), published in the ["IEEE Transactions on Wireless Communications"](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=7693/). The primary objective is to gain a deeper understanding of the methodologies and frameworks proposed in the paper, particularly in the context of integrating differential privacy mechanisms within wireless federated learning systems enhanced by joint sensing and communication.

As the original publication does not provide source code, this implementation is developed independently for educational and research purposes only. All efforts are directed toward faithfully replicating the core algorithms and validating the theoretical claims made in the paper.

### Overview:
This paper develops a novel framework for differ- entially private (DP) wireless federated learning (FL) with inte- grated sensing and communication (ISAC). In this framework, which is referred to as DP-ISAC-FL, wireless devices sense data and upload the trained local models using ISAC technique. The local training can take place concurrently with sensing at each device. We analyze the convergence upper bound of DP-ISAC- FL and rigorously capture the impact of device selection (for model training), time allocation between sensing/training and model uploading for the selected devices, and the allocations of channels, modulations, and transmit powers. We also develop an algorithm that enforces the convergence of DP-ISAC-FL by minimizing the convergence upper bound in an OFDMA system with discrete modulations. The beamforming for sensing, device selection, and the allocations of time, subchannels, modulations, and transmit powers are jointly optimized using successive convex approximation (SCA), adapting to the channels and computing capabilities of the devices. Experiments on multilayer perceptrons (MLPs) and convolutional neural networks (CNNs) show that DP-ISAC-FL with optimal allocations can significantly improve the learning convergence and accuracy under different privacy levels, e.g., by 7% and 18%, compared with its benchmarks. This is attributed to 68% more sensing data that DP-ISAC-FL can admit for model training. Index Terms—Federated learning, differential privacy, inte- grated sensing and communication, resource allocation.

### Versions : 
#### [baseVersion1](https://github.com/DataWizard1631/Differentially_Private_Wireless_Federated_Learning_With_Integrated_Sensing_and_Communication/tree/main/baseVersion1)
#### [baseVersion2](https://github.com/DataWizard1631/Differentially_Private_Wireless_Federated_Learning_With_Integrated_Sensing_and_Communication/tree/main/baseVersion2)
#### [baseVersion3](https://github.com/DataWizard1631/Differentially_Private_Wireless_Federated_Learning_With_Integrated_Sensing_and_Communication/tree/main/baseVersion3)




### License

This project is licensed under the [MIT License](./LICENSE.txt).

It is an independent implementation based on the following research paper:

> **["Differentially Private Wireless Federated Learning With Integrated Sensing and Communication"]**  
> [https://ieeexplore.ieee.org/document/10948161?denied=]

This repository is not affiliated with or endorsed by the original authors or IEEE. The implementation is written from scratch and follows the methodology described in the above publication.

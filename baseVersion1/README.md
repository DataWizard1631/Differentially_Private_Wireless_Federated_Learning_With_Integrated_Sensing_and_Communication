# baseVersion1 : 

## Objective : 
Implement a simple synchronous FL baseline (no differential privacy, no sensing/communication modeling). At the end of this level, user should be able to run multiple “clients” training locally and a central “server” aggregating model weights every fixed number of local epochs.

## Concepts :
<b>Federated Learning basics:</b> client‐server architecture, local updates, global aggregation, partial vs.full participation.
<b>Synchronous FedAvg algorithm </b>
<b>PyTorch (or TensorFlow/Keras):</b> building simple neural networks, optimizer loops, loss functions.

## Deliverables :
A minimal FL script (e.g., in PyTorch) that simulates M clients, each with its own local dataset (e.g., a partition of MNIST).

Each client runs A local SGD steps (or epochs) on its local data, then sends its model weights (no noise) to a central aggregator. The server averages the weights and broadcasts the new global model. Repeat for G rounds.

Logging: track train/test accuracy and loss on a held‐out global test set. Plot convergence vs. global round.

## Author of Blog :
[Deep Patel](https://www.linkedin.com/in/deeppateldw1611/)
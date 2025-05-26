# baseVersion2

## Explanation of This Version

This version implements a federated learning (FL) framework with differential privacy (DP) using the MNIST dataset. Multiple clients train a simple MLP model locally and share only differentially private model updates with a central server, which aggregates them. The experiment investigates the impact of different privacy budgets (ε) and local epochs (A) on model performance.

- **Model:** 2-layer MLP
- **Dataset:** MNIST
- **Clients:** 8 (IID split)
- **Privacy:** Differential Privacy (per-client gradient clipping and Gaussian noise)
- **Global Rounds:** 100
- **Batch Size:** 64
- **Privacy Budgets:** ε ∈ {1, 2, 5, 10}
- **Local Epochs (A):** Varied (see below)

---

## Results with A=1

**Setting:** Each client trains for 1 local epoch per global round.

<table>
  <tr>
    <td><img src="Output With 1 Local Round/output.png" width="350"/></td>
    <td><img src="Output With 1 Local Round/output1.png" width="350"/></td>
  </tr>
  <tr>
    <td align="center">Test Loss vs. Global Rounds</td>
    <td align="center">Test Accuracy vs. Global Rounds</td>
  </tr>
  <tr>
    <td><img src="Output With 1 Local Round/output2.png" width="350"/></td>
    <td><img src="Output With 1 Local Round/output3.png" width="350"/></td>
  </tr>
  <tr>
    <td align="center">Final Test Loss vs. ε</td>
    <td align="center">Final Test Accuracy vs. ε</td>
  </tr>
</table>

**Explanation:**  
With only 1 local epoch, clients contribute less updated information per round, leading to slower learning and less stable aggregation. The effect of DP noise is more pronounced, as fewer updates are averaged. This results in higher test loss and lower accuracy.

---

## Results with A=10

**Setting:** Each client trains for 10 local epochs per global round.

<table>
  <tr>
    <td><img src="Output With 10 loacl Round/output.png" width="400" /></td>
    <td><img src="Output With 10 loacl Round/output1.png" width="400" /></td>
  </tr>
  <tr>
    <td align="center">Test Loss vs. Global Rounds</td>
    <td align="center">Test Accuracy vs. Global Rounds</td>
  </tr>
  <tr>
    <td><img src="Output With 10 loacl Round/output2.png" width="400" /></td>
    <td><img src="Output With 10 loacl Round/output3.png" width="400" /></td>
  </tr>
  <tr>
    <td align="center">Final Test Loss vs. ε</td>
    <td align="center">Final Test Accuracy vs. ε</td>
  </tr>
</table>

**Explanation:**  
With 10 local epochs, clients learn better representations before aggregation, making the global model improve faster. The averaging effect across clients also helps mitigate DP noise, resulting in lower test loss and higher accuracy.

---

## Other Notes:

- **Privacy-Utility Tradeoff:** Lower ε (stricter privacy) leads to more noise and reduced accuracy; higher ε improves accuracy but weakens privacy.
- **Communication Efficiency:** FL reduces communication by sending only model updates instead of raw data.
- **Scalability:** Clients train in parallel, improving scalability over centralized approaches.
- **Regulatory Fit:** No raw data leaves clients, supporting data sovereignty and privacy regulations.

---

## Author of Blog:

[Deep Patel](https://www.linkedin.com/in/deeppateldw1611/)

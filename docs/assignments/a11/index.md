# A11 – Motor Selection

## Objective


## Analyze

Solidworks Simulation XPress cannot model moments or torques. This means no twisting analysis. The torque from the motor was added on as extra downward force.

| Design I | Iteration I | % Difference  | Iteration II | % Difference | Iteration III | % Difference | Convergence | Under Min Parameter?
|-----------|-------------------|-------------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Max Stress | 8075 psi | - | 8570 psi | 5.95% | 9242 psi | 7.55% | Converged | Yes - < 31,180 psi |
| Max Deflection | 4.154e-3 in | - | 4.180e-3 in | 0.62% |  4.193e-3 in | 2.10% | Converged | |
| Safety Factor | 3.86159 | - | 3.63849 | 5.95% | 3.37403 | 7.54% | Converged | Yes - < 4 |
| Size of Elements | Default - 0.08341 in | - | Fine - 0.06048 in | - | Very Fine - 0.03024 in | - | - | - |
|-----------|-------------------|-------------------|---------------|---------------|---------------|---------------|---------------|---------------|
| **First Iteration Images** | <img width="960" height="564" alt="Iter1 (1)" src="https://github.com/user-attachments/assets/1cf3e10c-cc6f-4286-9670-8e63b159ca93" /> Safety Factor | | <img width="960" height="564" alt="Iter1 (2)" src="https://github.com/user-attachments/assets/67cd7b8b-7953-4e87-802d-464684f03ec0" /> Deflection | | <img width="960" height="564" alt="Iter1 (3)" src="https://github.com/user-attachments/assets/c2d71614-b6e2-498f-a06e-f67dbef82a90" /> Stress |
| **Second Iteration Images** | <img width="960" height="564" alt="Iter2 (1)" src="https://github.com/user-attachments/assets/60551ba8-6667-40d6-b2e0-52f7daa9ee79" /> /> Safety Factor | | <img width="960" height="564" alt="Iter2 (2)" src="https://github.com/user-attachments/assets/bdfaf2b1-25a7-497a-8e6a-ad7733c71664" /> Deflection | | <img width="960" height="564" alt="Iter2 (3)" src="https://github.com/user-attachments/assets/12fb6c53-99cc-43db-aab1-695de0e50614" /> Stress |
| **Third Iteration Images** | <img width="960" height="564" alt="Iter3 (1)" src="https://github.com/user-attachments/assets/0d3929ee-9d4c-4cb4-a793-9184ba28231b" /> Safety Factor | | <img width="960" height="564" alt="Iter3 (2)" src="https://github.com/user-attachments/assets/0472f9ef-e63d-4125-b3ee-a4ee786202d1" /> Deflection | | <img width="960" height="564" alt="Iter3 (3)" src="https://github.com/user-attachments/assets/34470005-acc8-41a7-8a4d-9c03491273cc" /> Stress |

* _The percent difference is calculated with the equation 2(xf-xi)/(xi+xf) where xi is the original number and xf is the new number_

0.1 inch fillet to every edge.

| Design I | Iteration I | % Difference  | Iteration II | % Difference | Iteration III | % Difference | Convergence | Under Min Parameter?
|-----------|-------------------|-------------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Max Stress | 8118 psi | - | 8399 psi | 3.04% | 8869 psi | 5.44% | Converged | Yes - < 31,180 psi |
| Max Deflection | 4.110e-3 in | - | 4.124e-3 in | 0.34% |  4.142e-3 in | 0.44% | Converged | |
| Safety Factor | 3.84135 | - | 3.71269 | 3.41% | 3.51594 | 5.44% | Converged | Yes - < 4 |
| Size of Elements | Default - 0.08341 in | - | Fine - 0.06048 in | - | Very Fine - 0.03024 in | - | - | - |
|-----------|-------------------|-------------------|---------------|---------------|---------------|---------------|---------------|---------------|
| **First Iteration Images** | <img width="960" height="564" alt="Iter1 (1)" src="https://github.com/user-attachments/assets/646fdf70-4424-44c5-83ec-eb45d28af034" /> Safety Factor | | <img width="960" height="564" alt="Iter1 (2)" src="https://github.com/user-attachments/assets/8483ebe8-0d3c-4b65-b96a-f3c71d8a1f24" /> Deflection | | <img width="960" height="564" alt="Iter1 (3)" src="https://github.com/user-attachments/assets/d7d94d8b-6127-48dd-95a7-8bc93c125aae" /> Stress |
| **Second Iteration Images** | <img width="960" height="564" alt="Iter2 (1)" src="https://github.com/user-attachments/assets/42be7226-206c-48e8-8523-6367985423f4" /> Safety Factor | | <img width="960" height="564" alt="Iter2 (2)" src="https://github.com/user-attachments/assets/9fb211b9-0cdd-43ef-a045-1d5e84f2dd72" /> Deflection | | <img width="960" height="564" alt="Iter2 (3)" src="https://github.com/user-attachments/assets/f9ccb40f-fa7d-4a31-9961-4c1a4889ec2b" /> Stress |
| **Third Iteration Images** | <img width="960" height="564" alt="Iter3 (1)" src="https://github.com/user-attachments/assets/24ea4b52-fcf0-44a4-9413-fe4452bfcbc7" /> Safety Factor | | <img width="960" height="564" alt="Iter3 (2)" src="https://github.com/user-attachments/assets/5125f45a-45b1-4bcc-adcf-1422c37e2b04" /> Deflection | | <img width="960" height="564" alt="Iter3 (3)" src="https://github.com/user-attachments/assets/857b3afa-fbba-4ed4-9e9d-941dd8f6014a" /> Stress |


## Decide
_Reference your concept selection (Pugh matrix) here. How does this design follow from that decision?_

## Communicate

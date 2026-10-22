# A7 – Finite Element Analysis of Bracket

## Objective

The objective of this assignment was to perform Finite Element Analysis of the bracket created in assignment 5.

## Goals

For the goals of the assignment are to evaluate the bracket and linkage CAD models to ensure they fulfill the criteria of the assignment. The criteria were to not exceed the yield strength of the material, in my case Titanium (Ti-6Al-4V), not exceed the maximum deflection, and stay above the necessary safety factor. The bracket should have already been calculated to withstand the force without exceeding the limits.

| Criteria | Value |
|-------|-------|
| Force | 1200 lbf |
| Yield Strength | 120,000 psi |
| Maximum Deflection | 0.05 inches |
| Safety Factor | 4 |

For the FEA of the bracket and linkage, there is an outer loop which consists of operations like changing the geometry and there is an inner loop which consists of operations such as changing the mesh density. The assignment limited the amount of loops for both the inner and outer loops to stop at three. This means there are a maximum of three iterations per design and three designs total.

## FEA Analysis Iteration - Bracket

* _The free Solidworks simulation software doesn't display element count. It has been replaced with "Size of Elements"_

### Design I

The first Finite Element Analysis used the original bracket design that I had made for assignment 5 and 6. The inside surfaces of the bracket were fixed, as when the bracket was on top of the structure meant to be holding it, it would be unable to move or deflect. And the force was on the length of the cylinder. 

<img width="960" height="564" alt="Bracket Design 1 (1)" src="https://github.com/user-attachments/assets/5ab92f0d-b4ec-46cc-9b29-d70a8b78db13" />

<img width="960" height="564" alt="Bracket Design 1 (5)" src="https://github.com/user-attachments/assets/2799c417-357a-4b44-b601-eba92571c411" />

<img width="960" height="564" alt="Bracket Design 1 (8)" src="https://github.com/user-attachments/assets/ae2cd2e0-5f85-4825-9e08-87b787a6eac7" />

* This setup would be the basis for every iteration of the bracket.

With the fixtures and forces setup, I ran the three iterations of the inner loop for the first design.


**Inner Loop Iteration Table 1**

| Design I | Iteration I | % Difference  | Iteration II | % Difference | Iteration III | % Difference | Convergence | Under Min Parameter?
|-----------|-------------------|-------------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Max Stress | 144,100 psi | - | 188,600 psi | 26.75% | - | - | Not Converged | No - Not < 120,000 psi |
| Max Deflection | 0.05946 | - | 0.06010 | 1.07% | - | - | Converged | No - Not < 0.05 in |
| Safety Factor | 0.83252 | - | 0.63099 | 27.54% | - | - | Not Converged | No - Not > 4 |
| Size of Elements | Default - 0.08341 in | - | Fine - 0.06048 in | - | Very Fine - 0.03024 in | - | - | - |
|-----------|-------------------|-------------------|---------------|---------------|---------------|---------------|---------------|---------------|
| **First Iteration Images** | <img width="960" height="564" alt="Bracket Design 1 (16)" src="https://github.com/user-attachments/assets/5ceb5d0d-0334-4704-9bbd-643d2ed668e9" /> Safety Factor | | <img width="960" height="564" alt="Bracket Design 1 (17)" src="https://github.com/user-attachments/assets/d4da1ea5-2df0-4900-8e68-c983d579f7dc" /> Deflection | | <img width="960" height="564" alt="Bracket Design 1 (18)" src="https://github.com/user-attachments/assets/bc4fda9e-d2a0-44e7-9147-36a0c502a92c" /> Stress |
| **Second Iteration Images** | <img width="960" height="564" alt="Bracket Design 1 (20)" src="https://github.com/user-attachments/assets/309e6716-b070-4bc8-91cf-065e865a1a6c" /> Safety Factor | | <img width="960" height="564" alt="Bracket Design 1 (21)" src="https://github.com/user-attachments/assets/88248baa-4dd5-49ce-b581-b4f920db2ec3" /> Deflection | | <img width="960" height="564" alt="Bracket Design 1 (22)" src="https://github.com/user-attachments/assets/522d96b8-2a47-4186-bcc1-aa5c83a4aabd" /> Stress |


* _The percent difference is calculated with the equation 2(xf-xi)/(xi+xf) where xi is the original number and xf is the new number_

I actually ended up only running two iterations after nothing converged and every parameter was over the minimum needed value. After the two iterations, I abandoned the design and started working a new design.

### Design II

For the second design of the bracket, I added some simple supports to both sides of the supporting beam to give the cylinder more support. 

<img width="960" height="564" alt="Bracket Design 2 (1)" src="https://github.com/user-attachments/assets/1a6d2c33-961f-46d6-9eb7-91fd1d6e7dd8" />

<img width="960" height="564" alt="Bracket Design 2 (2)" src="https://github.com/user-attachments/assets/98da7de5-f7bc-4867-8d06-bd20a174619d" />

<img width="960" height="564" alt="Bracket Design 2 (3)" src="https://github.com/user-attachments/assets/ee37e97e-f678-4a03-9e16-ee492adbb01f" />

I made these extra supports the same thickness and terminate at the midpoints of the lower lines on the bracket body. 

With the extra support in place, I set up the forces and fixture again.

<img width="960" height="564" alt="Bracket Design 2 (4)" src="https://github.com/user-attachments/assets/7692a262-135a-406f-807a-077bb741b82a" />

And I ran the three iterations of the inner loop for the second design.

**Inner Loop Iteration Table 2**

| Design II | Iteration I | % Difference  | Iteration II | % Difference | Iteration III | % Difference | Convergence | Under Min Parameter?
|-----------|-------------------|-------------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Max Stress | 85,740 psi | - | 108,400 psi | 23% | 144,700 psi | 28.7% | Not Converged | No - Not < 120,000 psi |
| Max Deflection | 0.02677 | - | 0.02709 | 1.2% | 0.02724 | 0.55% | Converged | Yes - Is < 0.05 in |
| Safety Factor | 1.39956 | - | 1.10711 | 23% | 0.829084 | 28.7% | Not Converged | No - Not > 4 |
| Size of Elements | Default - 0.08341 in | - | Fine - 0.06048 in | - | Very Fine - 0.03024 in | - | - | - |
|-----------|-------------------|-------------------|---------------|---------------|---------------|---------------|---------------|---------------|
| **First Iteration Images** | <img width="960" height="564" alt="Bracket Design 2 (5)" src="https://github.com/user-attachments/assets/ca8c6c65-1290-4006-b4a7-1a98346b0601" /> Safety Factor | | <img width="960" height="564" alt="Bracket Design 2 (6)" src="https://github.com/user-attachments/assets/5dbb33e2-ab33-407d-9253-2a8f5593e9ff" /> Deflection | | <img width="960" height="564" alt="Bracket Design 2 (7)" src="https://github.com/user-attachments/assets/5f859dca-906f-4480-9f65-c735379d8732" /> Stress |
| **Second Iteration Images** | <img width="960" height="564" alt="Bracket Design 2 (9)" src="https://github.com/user-attachments/assets/a9f0cf23-2f3e-4744-916d-6887c33f7ebe" /> Safety Factor | | <img width="960" height="564" alt="Bracket Design 2 (10)" src="https://github.com/user-attachments/assets/6874cdac-bbec-4dcb-ad7e-31f32b47dddd" /> Deflection | | <img width="960" height="564" alt="Bracket Design 2 (11)" src="https://github.com/user-attachments/assets/8b667b54-9b00-4500-9c58-8d9b3cc29857" /> Stress |
| **Third Iteration Images** | <img width="960" height="564" alt="Bracket Design 2 (14)" src="https://github.com/user-attachments/assets/be389ba2-a5f0-4bea-9aca-e6adca6e44e4" /> Safety Factor | |  Deflection | | <img width="960" height="564" alt="Bracket Design 2 (15)" src="https://github.com/user-attachments/assets/a9128b06-35da-45ce-a513-a7584f1ba572" /> Stress |

However, the second design met very similar results only converging the deflection, which was under the minimum parameter. The stress was under the yield strength until the third iteration but it didn't converge anyway. The safety factor was higher on the second design but only very slightly. Overall, not really any better than the first design.

### Design III

For the third design, I tried focusing on resolving the stress. The maximum stress was located right above the top of the cylinder when it connects to the beam. To fix this, I made the bottom of the cylinder filleted so there would ideally be no stress concentrations.

I had to first extrude out the bracket some more to make sure there was space for the fillet.

<img width="960" height="564" alt="Bracket Design 3 (1)" src="https://github.com/user-attachments/assets/640114e9-f34f-4958-8adf-4ee7002dccbe" />

<img width="960" height="564" alt="Bracket Design 3 (2)" src="https://github.com/user-attachments/assets/05fd2171-ae31-4567-896d-fa5283ea5ae6" />

<img width="960" height="564" alt="Bracket Design 3 (3)" src="https://github.com/user-attachments/assets/d71399fb-b9ed-4352-87cb-0302386ac501" />

<img width="960" height="564" alt="Bracket Design 3 (4)" src="https://github.com/user-attachments/assets/bc00e826-f3e9-4b61-a83b-fd589d2899aa" />

<img width="960" height="564" alt="Bracket Design 3 (5)" src="https://github.com/user-attachments/assets/31a5f87c-e0ae-4bb5-9519-855c96b0e10d" />

<img width="960" height="564" alt="Bracket Design 3 (6)" src="https://github.com/user-attachments/assets/38f5b950-307a-4379-993c-e48e0bc7d6b4" />

* Needed to try a couple radii to find one I deemed suitable.

<img width="960" height="564" alt="Bracket Design 3 (7)" src="https://github.com/user-attachments/assets/0b6584f0-7947-4cf8-a733-1cccba4e6594" />

<img width="960" height="564" alt="Bracket Design 3 (8)" src="https://github.com/user-attachments/assets/c037f4c0-c45a-46f1-9ad4-0dabc30fa3d8" />

<img width="960" height="564" alt="Bracket Design 3 (9)" src="https://github.com/user-attachments/assets/6ccfcb05-7f13-4ff5-83f4-2383376a85e4" />

With this new bracket design, I hoped that at least the stress would be underneath the yield strength because I wasn't sure how else to achieve suitable values without adding significantly more bulk or another supporting beam on the other side of the cylinder.

**Inner Loop Iteration Table 3**

| Design III | Iteration I | % Difference  | Iteration II | % Difference | Iteration III | % Difference | Convergence | Under Min Parameter?
|-----------|-------------------|-------------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Max Stress | 136,100 psi | - | 152,700 psi | 11.5% | 165,000 psi | 7.74% | Not Converged | No - Not < 120,000 psi |
| Max Deflection | 0.02677 | - | 0.02765 | 0.91% | 0.02774 | 2.77% | Converged | Yes - Is < 0.05 in |
| Safety Factor | 0.881561 | - | 0.785659 | 11% | 0.727399 | 7.70% | Not Converged | No - Not > 4 |
| Size of Elements | Default - 0.08341 in | - | Fine - 0.06048 in | - | Very Fine - 0.03024 in | - | - | - |
|-----------|-------------------|-------------------|---------------|---------------|---------------|---------------|---------------|---------------|
| **First Iteration Images** | <img width="960" height="564" alt="Bracket Design 3 (11)" src="https://github.com/user-attachments/assets/ea7d249d-56ee-46bb-a894-7ac65702c63b" /> Safety Factor | | <img width="960" height="564" alt="Bracket Design 3 (12)" src="https://github.com/user-attachments/assets/7140c876-22a7-494a-b349-c0a3e8cd9163" /> Deflection | | <img width="960" height="564" alt="Bracket Design 3 (13)" src="https://github.com/user-attachments/assets/0556ca22-ad86-4788-bab6-9425c7cb3ba1" /> Stress |
| **Second Iteration Images** | <img width="960" height="564" alt="Bracket Design 3 (15)" src="https://github.com/user-attachments/assets/f564ca0a-4104-46de-910b-ee30d81cb738" /> Safety Factor | | <img width="960" height="564" alt="Bracket Design 3 (16)" src="https://github.com/user-attachments/assets/fc8f6c9d-b369-46dd-b294-061453636bce" /> Deflection | | <img width="960" height="564" alt="Bracket Design 3 (17)" src="https://github.com/user-attachments/assets/a8df4c63-aa0b-4a89-a763-99825d2f5678" /> Stress |
| **Third Iteration Images** |  Safety Factor | |  Deflection | |  Stress |

Somehow, the fillet seemed to make the numbers worse. The stress wasn't even close to being under the yield strength and the safety factor was also worse. Both were at least close to converging so that was some progress. However, at this point, I had run three all three iterations of the outer loop changing the geometry twice, meaning I couldn't iterate the design anymore.

### Bracket Outer Loop Table

**Outer Loop Iteration Table**

|  | Design I | Design II | Design III |
|-----------|-------------------|-------------------|---------------|
| Max Stress | 188,600 psi | 144,700 psi | 165,000 psi |
| Max Deflection and Location | 0.06010 - Located at free end of Cylinder | 0.02724 - Located at free end of Cylinder | 0.02774 - Located at free end of Cylinder |
| Mass | 0.2361 lbs | 0.2828 lbs | 0.2850 lbs |
| Safety Factor | 0.63099 | 0.829084 | 0.727399 |
| Size of Elements | Fine - 0.06048 in | Very Fine - 0.03024 in | Very Fine - 0.03024 in |
| | <img width="960" height="564" alt="Bracket Design 1 (19)" src="https://github.com/user-attachments/assets/e3794fb7-1e62-47bb-b1ce-a38b1f669702" /> | <img width="960" height="564" alt="Bracket Design 2 (3)" src="https://github.com/user-attachments/assets/eac40f54-e4a2-480a-9812-c853adbdbddc" /> | <img width="960" height="564" alt="Bracket Design 3 (9)" src="https://github.com/user-attachments/assets/f726a804-60ff-4cf6-bc61-c552fc51423d" /> |

The final results were quite unsatisfactory. The only parameter that converged was the deflection. Everything else both didn't converge and was above the minimum value. I'm not sure what went wrong in my math to cause nothing to work out. The FEA certainly revealed the mistakes I made.

### FEA Iteration 1 Problems

When I first started the assignment, I was getting even lower values than I was here. I found it strange how low the values were as I was working through the process. Despite what I changed and added, nothing helped much and I ended up making the original design very bulky. I looked at my equations and realized that I had my force set to 600 lbf instead of 1200 lbf. 

<img width="780" height="503" alt="Bracket Design 1 (9)" src="https://github.com/user-attachments/assets/c5ab4c33-c1dd-4e4e-b825-8ac57d642a5a" />

This caused the supporting beam between the cylinder and the bracket body to be half as thick as it should have been. 

<img width="780" height="503" alt="Bracket Design 1 (10)" src="https://github.com/user-attachments/assets/f305e378-dffe-4d9a-a020-d4d052f2cc6d" />

<img width="960" height="564" alt="Bracket Design 1 (4)" src="https://github.com/user-attachments/assets/f2efa303-538c-4e1f-8a4c-5dfe63a3296d" />

<img width="960" height="564" alt="Bracket Design 1 (12)" src="https://github.com/user-attachments/assets/e8fccf0e-397c-47ae-b6e8-b2356ea4d611" />

Fixing the force only changed the supporting beam thickness and even then it didn't end up helping that much ultimately. But it was still a good thing to find so I can keep it in mind for the future to make sure I double check my equations. This was likely one among many mistakes I made during my original calculations of the bracket.

----------------------------------------------------------------


## FEA Analysis Iteration - Linkage

The next segment of the assignment was to repeat the process with the linkage that was designed alongside the bracket. 

<img width="960" height="564" alt="Linkage-Design-1 (3)" src="https://github.com/user-attachments/assets/e5e1fa39-c7f3-422f-8b00-712b74fb8d6f" />

### Design I

The first design was FEA of the unchanged linkage as it was designed in assignment 5. I once again set up the forces and fixtures for the linkage. The top hole which mounts onto the cylinder on the bracket would be fixed and the bottom hole would hold the load of 1200 lbf.

<img width="960" height="564" alt="Linkage-Design-1 (4)" src="https://github.com/user-attachments/assets/48daa7a9-93a9-4d83-9c1b-28888202934b" />

<img width="960" height="564" alt="Linkage-Design-1 (5)" src="https://github.com/user-attachments/assets/235b2e3f-3d56-4d49-83af-a0c0c4479b09" />

<img width="960" height="564" alt="Linkage-Design-1 (7)" src="https://github.com/user-attachments/assets/8523b494-6c16-4e4e-94a7-7bbac83788f8" />

With that, I started the FEA and moved through the mesh densities.


**Inner Loop Iteration Table 1**

|  | Iteration I | % Difference  | Iteration II | % Difference | Iteration III | % Difference | Convergence | Under Min Parameter?
|-----------|-------------------|-------------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Max Stress | 27,120 psi | - | 27,490 psi | 1.36% | - | - | Converged | Yes - Is < 120,000 psi |
| Max Deflection | 0.003032 | - | 0.003057 | 0.82% | - | - | Converged | Yes - Is < 0.05 in |
| Safety Factor | 4.42448 | - | 4.36478 | 1.36% | - | - | Converged | Yes - Is > 4 |
| Size of Elements | Default - 0.08341 in | - | Fine - 0.06048 in | - | Very Fine - 0.03024 in | - | - | - |
| **First Iteration Images** | <img width="960" height="564" alt="Linkage-Design-1 (8)" src="https://github.com/user-attachments/assets/68ce067a-6429-4e56-a41b-e5fbc55a01ec" /> Safety Factor | | <img width="960" height="564" alt="Linkage-Design-1 (9)" src="https://github.com/user-attachments/assets/8698195f-00bb-453c-b9a0-c8252efd7b0a" /> Deflection | | <img width="960" height="564" alt="Linkage-Design-1 (10)" src="https://github.com/user-attachments/assets/bf4f46f1-1b07-4286-8aea-3f246e7897d2" /> Stress |
| **Second Iteration Images** | <img width="960" height="564" alt="Linkage-Design-1 (12)" src="https://github.com/user-attachments/assets/7a5ddd30-aa5e-4912-a1d6-71fb95e31734" /> Safety Factor | | <img width="960" height="564" alt="Linkage-Design-1 (13)" src="https://github.com/user-attachments/assets/b850513f-b5ca-400b-a5fc-89a3c34ac699" /> Deflection | |  Stress |

The linkage performed substantially better than the bracket converging immediately on the second iteration and it stayed under the minimum parameters. This meant I was able to optimize the design for the second set of iterations.

### Design II

For the second design, I decided to remove the chunk of material in the metal that was all blue in the evaluations. 

<img width="960" height="564" alt="Linkage-Design-2 (1)" src="https://github.com/user-attachments/assets/c1e0f108-74f2-4207-a0bd-0fe297df7ae2" />

<img width="960" height="564" alt="Linkage-Design-2 (2)" src="https://github.com/user-attachments/assets/7304331a-0d53-4522-a1ba-3d2fb2cd6f2a" />

<img width="960" height="564" alt="Linkage-Design-2 (3)" src="https://github.com/user-attachments/assets/d7650949-348d-48f9-899a-666829f31a63" />

I used the same thicknesses for the walls as the walls surrounding the bottom hole since those walls were able to support the stress.

<img width="960" height="564" alt="Linkage-Design-2 (4)" src="https://github.com/user-attachments/assets/0a819024-4e12-4ee9-9952-df67e98781ed" />

<img width="960" height="564" alt="Linkage-Design-2 (5)" src="https://github.com/user-attachments/assets/d82cfcdc-98a9-4416-9272-66b273834e2e" />

<img width="960" height="564" alt="Linkage-Design-2 (6)" src="https://github.com/user-attachments/assets/cb0b3429-2d38-44d6-8b8a-90b70356b888" />

<img width="960" height="564" alt="Linkage-Design-2 (7)" src="https://github.com/user-attachments/assets/9848e002-4a0a-4db5-ba17-2dfde1227577" />

<img width="960" height="564" alt="Linkage-Design-2 (8)" src="https://github.com/user-attachments/assets/6bd262d8-f657-461c-88e0-ae6904abef60" />

<img width="960" height="564" alt="Linkage-Design-2 (9)" src="https://github.com/user-attachments/assets/a73f0dff-c9fe-4eec-a5d8-f5676c3d4f0c" />

I made sure to fillet the edges to prevent stress concentrations and I performed another inner loop of iterations.

<img width="960" height="564" alt="Linkage-Design-2 (16)" src="https://github.com/user-attachments/assets/b8e16432-5901-4597-8229-7406e2bb6b90" />


**Inner Loop Iteration Table 2**

|  | Iteration I | % Difference  | Iteration II | % Difference | Iteration III | % Difference | Convergence | Under Min Parameter?
|-----------|-------------------|-------------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Max Stress | 24,850 psi | - | 25,710 psi | 3.40% | - | - | Converged | Yes - Is < 120,000 psi |
| Max Deflection | 0.003021 | - | 0.003034 | 0.43% | - | - | Converged | Yes - Is < 0.05 in |
| Safety Factor | 4.82842 | - | 4.66723 | 3.40% | - | - | Converged | Yes - Is > 4 |
| Size of Elements | Default - 0.08341 in | - | Fine - 0.06048 in | - | Very Fine - 0.03024 in | - | - | - |
| **First Iteration Images** | <img width="960" height="564" alt="Linkage-Design-2 (11)" src="https://github.com/user-attachments/assets/2553cf32-2a49-4568-9db5-c012fa884ffb" /> Safety Factor | | <img width="960" height="564" alt="Linkage-Design-2 (13)" src="https://github.com/user-attachments/assets/0ced40b9-f961-46af-afee-584c5eda6f05" /> Deflection | | <img width="960" height="564" alt="Linkage-Design-2 (14)" src="https://github.com/user-attachments/assets/39b48b36-e894-4b9e-be60-877148e52029" />
 Stress |
| **Second Iteration Images** | <img width="960" height="564" alt="Linkage-Design-2 (17)" src="https://github.com/user-attachments/assets/b0b7e3fb-6a57-4e23-940f-614ca3ee3529" /> Safety Factor | |  Deflection | | <img width="960" height="564" alt="Linkage-Design-2 (18)" src="https://github.com/user-attachments/assets/a8417407-6a10-4993-8a2a-232011cfafe0" /> Stress |

The geometry change certainly altered the form of the deflection and stress but the design was still way above the minimum parameters. 

There was probably more optimization I could do but I couldn't think of anything. I didn't want to touch the thickness sense that was parametrically put in and there wasn't really much blue left on the linkage that had no stress on it. So I left it at that and called the linkage optimized.

### Linkage Outer Loop Table

**Outer Loop Iteration Table**

|  | Design I | Design II | Design III |
|-----------|-------------------|-------------------|---------------|
| Max Stress | 27,490 psi | 25,710 psi | - |
| Max Deflection and Location | 0.003057 in - At the bottom of the Lower Hole | 0.003034 in - At the bottom of the Lower Hole | - |
| Mass | 0.13 lbs | 0.09 lbs | - |
| Safety Factor | 4.36478 | 4.66723 | - |
| Number of Elements | Fine - 0.06048 in | Fine - 0.06048 in | - |
| | <img width="960" height="564" alt="Linkage-Design-1 (3)" src="https://github.com/user-attachments/assets/68307ca8-e009-44e1-9a4d-157e8a1fd15b" /> | <img width="960" height="564" alt="Linkage-Design-2 (7)" src="https://github.com/user-attachments/assets/d528d607-d23a-4a3b-94f2-8966f2d66e3d" /> |  |

The linkage performed significantly better than the bracket and had really no issues. The math seemed to work out better for the linkage probably because of it's simpler design.

## Lessons Learned

This assignment taught me a lot about different computational methods to verify an engineering design. The fact that the simulation seemed to disagree with my math for the bracket is better to know ahead of time than afterwards. Certainly a great way to double check your work before actually creating the part. I also learned about meshes and how the density and size changes the precision and computational time. However, I was kind of limited in this aspect using Solidworks' free "Simulation Xpress" software that only allows you to change the size of the mesh objects and gives no further details.

**Time Spent:** 5 Hours

### CAD File Download

[Bracket Download Design I](A05-bracket-3-1.SLDPRT)

[Bracket Download Design II](A05-bracket-3-2.SLDPRT)

[Bracket Download Design III](A05-bracket-3-3.SLDPRT)

[Linkage Download Design I](A05-Linkage-1-1.SLDPRT)

[Linkage Download Design II](A05-Linkage-1-2.SLDPRT)


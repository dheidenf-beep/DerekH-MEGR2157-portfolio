# A11 – Motor Selection

## Objective

The purpose of this assignment is to continue upon the leadscrew project to select and spec a proper motor for the strain gauge. This includes frame design and bearing design, ensuring the crosshead moves smoothly under designed torque and loads. 


### Motor Selection: Victor Gaskin 

Before the calculations could proceed, I needed to recall the rotational speed range and Torque applied to a single leadscrew, then carry those values to help me ascertain the figures I needed to match in terms of selecting the motor. 

<img width="955" height="1280" alt="image" src="https://github.com/user-attachments/assets/59dcb88a-1b43-4efb-9117-66d73d71596c" />

As a result of the calculations, I ended up choosing a McMaster-Carr DC Gearmotor. There was multiple gearmotors to choose from but the majority of them either provided speed much larger than the safety factor would account for or a torque force that is significantly too large for leadscrews to sustain consistently. 
Chosen Motor: https://www.mcmaster.com/6409K17/

The aditional torque that this Gearmotor provides above the calculations would be sustained by the safety factor of which the leadscrew was chosen under, as it's diameter is larger than the diameter used for the calculations(i.e, it was calculated using the most conservative estimate under the highest expected loading conditions.) 

<img width="1050" height="811" alt="image" src="https://github.com/user-attachments/assets/3f61c596-1255-4897-9608-81976bb6ac19" />


The provided Speed-Torque Chart helped verify this decsion: 

<img width="1250" height="947" alt="image" src="https://github.com/user-attachments/assets/40e6ac0f-a9f5-42a1-b755-d25a38faa2f0" />



Motor Dimensions: 
Length: 3.5"
Width: 2.75"
Height: 3" 
Mounting Hole Locations
  Main Mount 1.86 in x 1.43 in
    Screw Holes at edges

### Motor Mount Design
(Note: the gearmotor provides a very generous mount already)

Through the calculations, the factor that determined the leading thickness was the bending moment(t = 2.34mm). Despite this, I choose to use a thickness of 4mm(approximately 1/8") in order to standardize the CAD Modeling process later 

#### Bending Moment Calculation

<img width="976" height="1280" alt="image" src="https://github.com/user-attachments/assets/44dcb89c-2a20-408b-ba9f-a183d89ab478" />

#### Deflection Thickness Calculation: Victor Gaskin 

<img width="1179" height="720" alt="image" src="https://github.com/user-attachments/assets/314cbf9f-9c91-41be-8f1a-c1f477ed37fd" />

#### Motor Mount Design: Victor Gaskin

Regarding the motor mount design, my initial concept was to have the mount align with the preexisting "mount" and only provide additional support and a metal surface to screw onto. Later in the design process, Derek further optimized this design in order to accommodate guiderails. 

<img width="608" height="613" alt="image" src="https://github.com/user-attachments/assets/111a9f9c-b931-4b2f-86c2-be869c74ea7a" />

#### Coupler Design: Victor Gaskin

I was tasked to calculate the minimum diameter that the coupler that would fit between the motor mount and the leadscrew. I needed to take into account that the diameter's between the "entrance" and "exit" holes on each side would have to differ, and that this would affect the calculations. 

These calculations would assist me in choosing a coupler: 
  The coupler I chose was: https://www.ruland.com/pcr16-6-5-a.html

(Note, the diameter of the larger entrance hole, which is where the leadscrew would be inserted into, was the driving diameter.) 

<img width="933" height="1280" alt="image" src="https://github.com/user-attachments/assets/7f56a662-d06b-453a-a8d9-334ae7e47e89" />


## Motor Mount CAD Modeling - Derek Heidenfelder

The design I came up with for the motor mount work around the motors to mount onto the channels because I couldn't find a channel with a hole. I started with the motor dimensions from McMaster and went from there. 

<img width="1163" height="736" alt="A11-WorkMotorMountConcept" src="https://github.com/user-attachments/assets/8a360f7e-1724-453e-89c5-d77ef9b91ee6" />

<img width="996" height="760" alt="McmasterMotorPic" src="https://github.com/user-attachments/assets/be56ac3f-b95b-4014-92e2-b931684a4b21" />

<img width="960" height="564" alt="MotorMount (2)" src="https://github.com/user-attachments/assets/247873c1-8293-45c1-9a76-e4f2726b84ea" />

<img width="960" height="564" alt="MotorMount (3)" src="https://github.com/user-attachments/assets/25ca73dc-7de1-43cd-9f69-dc0e6ee581aa" />

<img width="960" height="564" alt="MotorMount (5)" src="https://github.com/user-attachments/assets/87305e9c-764e-4c92-89ee-473c4a0f3741" />

I used the McMaster image to get the position and sizing. For the shaft hole, I made it 0.35 inches to ensure clearance for the axle. The screws I kept as 10-32 screws but I did have some issues getting the screw holes correct initially but I would figure it out later.

<img width="960" height="564" alt="MotorMount (6)" src="https://github.com/user-attachments/assets/81847d8b-7c1a-4a9b-be67-8612f87c65b4" />

<img width="960" height="564" alt="MotorMount (9)" src="https://github.com/user-attachments/assets/b1401235-d862-4a3e-a687-a4dd1fd24431" />

<img width="960" height="564" alt="MotorMount (10)" src="https://github.com/user-attachments/assets/f07a1aec-69c3-450e-ab4b-98c2b8c48cb7" />

<img width="960" height="564" alt="MotorMount (11)" src="https://github.com/user-attachments/assets/350cc2cd-9bc9-4857-9f23-7376a041207a" />

I created holes in the bracket to be able to be mounted to the channels.

<img width="960" height="564" alt="MotorMount (13)" src="https://github.com/user-attachments/assets/267efb1a-365e-4512-b0fc-d68c44f1c37c" />

<img width="960" height="564" alt="MotorMount (14)" src="https://github.com/user-attachments/assets/c10c1fd9-e051-46a1-b036-73cb5b032503" />

Next, I got rid of the top bracket of the assembly, added in the coupling, and the motor mount. 

<img width="960" height="564" alt="MotorMount (17)" src="https://github.com/user-attachments/assets/360d7808-99dd-4a3e-b73f-c3253fafc2b6" />

I realized that the spacing between the coupler and the bracket was too small, so I went back and edited it to ensure there were no issues with clipping or rubbing. Using the measurements from the website for the coupling, I made sure there was ample clearance.

<img width="960" height="564" alt="MotorMount (18)" src="https://github.com/user-attachments/assets/87d42065-71e5-4ef0-bc46-32c3240c10e0" />

<img width="960" height="564" alt="MotorMount (20)" src="https://github.com/user-attachments/assets/338ecea2-fddc-40a1-8160-7dbd5df0464b" />

I added in the second mount for the second motor.

<img width="960" height="564" alt="MotorMount (21)" src="https://github.com/user-attachments/assets/78e74ac2-7dfd-4798-838d-ca468cb6b5fc" />

After playing around a bit, I noticed that nothing was lining up. Since the motor shaft isn't centered, that made it more difficult to line everything up. Also, after some investigating, I learned that the smallest channel length was half a foot, which was a bit too long for what I needed. So, I went back to the design. I decided on making one single top piece with the motor mounts built in. I used the Solidworks measurement tool to determine the distances from the existing motor mounts to the edges in order to get my dimensions.

<img width="960" height="564" alt="MotorMount (23)" src="https://github.com/user-attachments/assets/ec178851-9813-4014-8222-160ad9e2bc6b" />

<img width="960" height="564" alt="MotorMount (27)" src="https://github.com/user-attachments/assets/dbd36477-9a3a-4e1b-983c-2fba6894b9ef" />

I made essentially a second motor mount with pieces connecting them. I put holes in the ends that would line up with the McMaster bracket holes so that they could just be screwed directly together.

<img width="960" height="564" alt="MotorMount (30)" src="https://github.com/user-attachments/assets/6fc18d91-9484-4cfc-8e9a-9d9db8c598e6" />

<img width="960" height="564" alt="MotorMount (29)" src="https://github.com/user-attachments/assets/2eb62577-83b6-490d-9adb-8ad3380681f7" />

I finally fixed the screw holes to make them actual 10-32 holes.

<img width="960" height="564" alt="MotorMount (31)" src="https://github.com/user-attachments/assets/10edc54a-8d5c-4240-bd61-8aafe0729ff7" />

With that, I was satisfied with the motor mount and moved onto the FEA portion, evaluating the motor mount. The assignment instructions were to evaluate the whole top brace. However, I only have access to Solidworks' free Simulation Xpress software which cannot perform FEA on an assembly. This made having the motor mount being all one piece very helpful. For the FEA, I changed the material to Aluminum 6063-T6. This is the same material the channels are made of.

<img width="612" height="483" alt="MotorMount (33)" src="https://github.com/user-attachments/assets/c6f8f1f9-0925-4db2-8fca-279dbf66b308" />

<img width="960" height="564" alt="MotorMount (34)" src="https://github.com/user-attachments/assets/0a323380-bd8b-4fe6-b852-248aae3f442c" />

* It's blue now!


### Bracket Verification

I ran some quick stress calculations on the rectangular bracket from McMaster to verify it would hold the stress of the top motor mount. I used 6063-T6 aluminum for the material because that is what it is made of on the McMaster website. I applied the max force to the bracket I figured it would see which was 2 kN both transversely and axially.

<img width="1035" height="906" alt="A11-WorkBracketVerification" src="https://github.com/user-attachments/assets/6191cebc-a8fc-4db1-9806-323e38abdb11" />

The bracket was able to sufficiently hold the force under the safety factor which meant no change of part was needed.


## Finite Element Analysis - Derek Heidenfelder

### Motor Mount FEA

Solidworks Simulation XPress cannot model moments or torques. This means no twisting analysis. The torque from the motor was added on as extra downward force. The calculated torque was about 1 kN-m, so I made the force on each hole be 2 kN downward.

<img width="960" height="564" alt="MotorMount (37)" src="https://github.com/user-attachments/assets/fc267eed-bdbf-49dd-be4c-8496b3accad6" />


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

The first pass saw all of the values converge while remaining under the necessary values.

To improve the model, I add a 0.1 inch fillet to every edge, including the inside edges.

<img width="960" height="564" alt="MotorMount (38)" src="https://github.com/user-attachments/assets/38605acd-7fce-4d68-9220-d855e536f8e2" />

<img width="960" height="564" alt="MotorMount (39)" src="https://github.com/user-attachments/assets/ac437574-e6ad-452c-97dc-9a8e11ab2d89" />

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

This improvement seems to have slightly decreased the stress on the bracket. The deflection stayed mostly the same and the safety factor decreased by a small amount. 


### Failed Channel FEA

For the next FEA section, the part that was being used for the sides of the tensile tester to support it was meant to undergo an FEA evaluation. Since I used the 3ft channel from the McMaster website, I intended to analyze it using FEA. However, due to the limitations of the free Solidworks Xpress simulation software, the part was too complex to be meshed no matter how much I decreased the mesh density.

<img width="960" height="564" alt="AttemptedChannelFEA (3)" src="https://github.com/user-attachments/assets/6df5902c-288c-4c37-b7a2-a5abf1dab455" />

<img width="960" height="564" alt="AttemptedChannelFEA (4)" src="https://github.com/user-attachments/assets/c5b41c07-6110-43c0-952d-40ea105a0459" />

## Engineering Drawings - Derek Heidenfelder


**Assembly Drawing with Bill of Materials**

<iframe src="TensileTesterAssem-A11-4.pdf" width="100%" height="650px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="A02-Truss-weight-calc.pdf">Download the PDF</a>.</p>
</iframe>


**Motor Mount Drawing**

<iframe src="MotorMount2.pdf" width="100%" height="650px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="A02-Truss-weight-calc.pdf">Download the PDF</a>.</p>
</iframe>


**Crosshead Drawing**

<iframe src="A10Crosshead2.pdf" width="100%" height="650px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="A02-Truss-weight-calc.pdf">Download the PDF</a>.</p>
</iframe>



## Final Tensile Tester Design

This is the final design for our tensile tester, fully modeled and assembled in Solidworks.

<img width="960" height="564" alt="MotorMount (40)" src="https://github.com/user-attachments/assets/dbc63856-ea3f-4d9a-86cb-b820777dfd25" />

## Bill of Materials and Labor Costs



## Lessons Learned - Derek Heidenfelder



### CAD File Downloads

[Tensile Tester Assembly Downlaod](TensileTesterAssem-A11-4.SLDASM)

[Motor Mount Download](MotorMount2.SLDPRT)

[Crosshead Download](A10Crosshead2.SLDPRT)


## Resources

Machinery's Handbook 32nd Edition

[McMaster Website](https://www.mcmaster.com/)

[Ruland Website](https://www.ruland.com/)

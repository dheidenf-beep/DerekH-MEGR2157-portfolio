# A10 – Lead Screw Translating System

## Objective
The objective of this assignment was to analzye and a design and model a leadscrew alongside other components in order to create a analogue tensile loader than could consistantly measure 2kN forces. 

## Analyze

### LeadScrew Design: Victor Gaskin
The minimum dimensions for the leadscrew was found by applying the safety factor(4) to the yield strength of the stainless steel leadscrew(205 MPa) Each of the two screws supports a 1 kN design load, requiring
a minimum core diameter of 4.98 mm. 

<img width="768" height="1024" alt="image" src="https://github.com/user-attachments/assets/926a3e4e-01ac-4868-87e9-7f3936fa6501" />

The 3/8"‑12 Thread Acme stainless steel lead screw (McMaster‑Carr 95061A813) was selected because its root diameter of  7.5 mm more than satisfies the minimum diameter requirement. 

Following the calculations onward, the range of speeds that the leadscrew would undergo was to be determined
<img width="770" height="505" alt="image" src="https://github.com/user-attachments/assets/8d0e20d7-c7d0-45e5-a483-df70d2025590" />

Results: The Screw’s lead of 2.117 mm/rev produces a rotational speed range of 0.473–23.6 rpm


The next Step was to determine the amount of torque to be applied to one leadscrew 
Using the screw torque equation with a friction coefficient of 0.15, the torque per screw is 1 N·m, giving a total drive
torque of 2 N·m. This configuration ensures smooth, controlled motion and sufficient strength for
the 2 kN tensile load.
<img width="695" height="505" alt="image" src="https://github.com/user-attachments/assets/e782d2d0-c75f-48d9-adc9-306eb42c5e46" />

### Nut Design: Victor Gaskin

Through the choice of the leadscrew, I assumed a nut of a similar diameter to the leadscrew would have to be chosen. 

The nut’s 25 mm thread engagement provides approximately 12 engaged threads, distributing the 2 kN load evenly. This provides a considerable factor of safety as only about 4 engaged threads would be been required in order to properly distribute this load

The forces sustained on the bearing utilizing the bending stress equation reaches about 8 MPa, which is considerably below 932 Bearing Bronze's Yield Strength of 105 MPa. This ensures that these nuts can be properly loaded and considerably overloaded without risk of failure.

A 932 bearing‑bronze Acme flange nut (McMaster‑Carr 95120A592) was chosen to pair with the 3/8‑12 lead screw due to the results of the calculations. 

<img width="768" height="1024" alt="image" src="https://github.com/user-attachments/assets/fd010587-d8fd-4c14-9b9e-31dfa96deba9" />


### CrossHead Design: Victor Gaskin

The crosshead was analyzed through the  simply supported steel beam assumption. spanning 150 mm between the
two lead screws, with  load applied at midspan. Under the 4 kN design load, the
maximum bending moment is 45MPa( 45 N mm)  for 25 mm × 20 mm rectangular section—below the 250 MPa allowable stress for stainless steel.
The corresponding deflection under the 2 kN test load is 0.0437 mm, far less than the 0.1 mm limit,
this verifies that the crosshead maintains adequate stiffness. The selected geometry provides both strength and rigidity while keeping to a realistic size that the machine would be able to accomodate. 

Mounting holes at each end accommodate the bronze flange nuts, ensuring smooth transfer of load and lower stress concentrations 

This design achieves safe operation, minimal deflection, and streamlined assembly for repeatitious tensile tests. 

<img width="785" height="672" alt="image" src="https://github.com/user-attachments/assets/0dcc8fad-71f1-4ef2-9475-695a07700cbb" />

#### Sketch

<img width="725" height="270" alt="image" src="https://github.com/user-attachments/assets/a17d9150-32c8-4fe4-affc-c8c17c17f70a" />


## Tensile Tester CAD Model - Derek Heidenfelder

Using the calculated parameters for the lead screws and crosshead, I began modeling and tensile tester in Solidworks.

### Crosshead Modeling

The crosshead was fairly simple to model, just an extruded rectangular prism with three holes cut out of it. In the parametric equations, the only change I needed to make was to increase the hole size from 8mm to 0.375 inches to support the diameter of the lead screw.

![CrossheadCAD7](CrossheadCAD7.png)

![CrossheadCAD4](CrossheadCAD4.png)

![CrossheadCAD5](CrossheadCAD5.png)

![CrossheadCAD9](CrossheadCAD9.png)

![CrossheadCAD10](CrossheadCAD10.png)

For the material, Solidworks didn't have 301 stainless steel as an option. Instead, I searched for the next closest steel with nearly the same properties. The steel I found was wrought stainless steel which has a yield strength of 206 MPa and an elastic modulus of 200,000 MPa. This was slightly above the original yield strength and elastic modulus of 205 and 193,000 MPa respectively.

![CrossheadCAD11](CrossheadCAD11.png)

![CrossheadCAD12](CrossheadCAD12.png)

With the crosshead modeled, I had a starting point for the rest of the tensile tester.


### Tensile Tester Modeling

For the tensile tester, I started with a basic frame using the CAD files from the McMaster website. However, the frame I initially created was too small for the lead screw and I had to get a new length of channel.


![TensileTesterCAD4](TensileTesterCAD4.png)

![TensileTesterCAD1](TensileTesterCAD1.png)

![TensileTesterCAD5](TensileTesterCAD5.png)

I then went ahead and got the lead screws and lead screw bases in so that I could add in the crosshead and get an idea of how wide the structure was going to be. I would use the crosshead to center the lead screws and internal assembly relative to the outer frame.

![TensileTesterCAD7](TensileTesterCAD7.png)

![TensileTesterCAD8](TensileTesterCAD8.png)

![TensileTesterCAD9](TensileTesterCAD9.png)

For the flange nuts, I created a special mate to give the lead screw and nuts a screw connection. This meant the flange nuts could move up and down the lead screws and the lead screws would visually spin on the assembly. 

![TensileTesterCAD10](TensileTesterCAD10.png)

![TensileTesterCAD11](TensileTesterCAD11.png)

Next, I added in the side channels and brackets that would hold the channels together.

![TensileTesterCAD12](TensileTesterCAD12.png)

![TensileTesterCAD15](TensileTesterCAD15.png)

![TensileTesterCAD16](TensileTesterCAD16.png)

Finally I added on channels that the tensile tester would stand on and replaced the bottom square brackets with corner brackets.

![TensileTesterCAD20](TensileTesterCAD20.png)

I also added in a force tester to see how it would fit in. The CAD file came with additional parts that I needed to remove to just get the load cell on its own. 

![TensileTesterCAD21](TensileTesterCAD21.png)

![TensileTesterCAD23](TensileTesterCAD23.png)

![TensileTesterCAD24](TensileTesterCAD24.png)

The only thing I wasn't able to add to the tensile tester assembly were small bench vises that I found that would be used to hold the sample as these did not have CAD files. Two of these bench vises would be needed. One would connect to the crosshead and the other would connect to the load cell.

![TensileTesterCAD25](TensileTesterCAD25.png)

With this, the tensile tester was complete.


### Crosshead FEA

The next step was to perform Finite Element Analysis on the crosshead. I used the free Solidworks Simulation Xpress tool to evaluate the crosshead. For the analysis, I made the two outer holes be fixed in place and the inner hole have a downward pointing force of 2000 newtons. Two iterations with different mesh densities were performed and checked for convergence using the equation: 2|(xf-xi)|/(xf+xi) * 100. Where xi is the initial measurement and xf is the final measurement.

![CrossheadFEA1](CrossheadFEA1.png)

![CrossheadFEA2](CrossheadFEA2.png)

![CrossheadFEA3](CrossheadFEA3.png)

![CrossheadFEA4](CrossheadFEA4.png)

**Convergence: > 7%**

**First Iteration:**

| Max Quantity | Initial Value (Standard Mesh Density) | Final Value (Finest Mesh Density | Percent Discrepancy | Convergence |
| -------- | :-------: | :-------: | :-------: | :-------: |
| Stress: 206.807e^8 N/mm^2  | 5.463e^7 N/mm^2 | 5.551e^7 N/mm^2 | 1.5979% | Converged |
| Displacement: 0.1 mm  | 1.329e^-2 mm | 1.336e^2 mm | 0.5253% | Converged | |
| Safety Factor: 4  | 3.78568 | 3.7256 | 1.5997% | Converged |
| ----- | <img width="320" height="188" alt="CrossheadFEA8" title="Stress" src="CrossheadFEA8.png" /> Stress | <img width="320" height="188" alt="CrossheadFEA7" title="Displacement" src="CrossheadFEA7.png" /> Displacement | <img width="320" height="188" alt="CrossheadFEA5" title="Safety Factor" src="CrossheadFEA5.png" /> Safety Factor | ----- |


Iteration 1 Mass: 1.69 pounds

For the first iteration, the only parameter that was not below the desired value was the safety factor. To rectify this, an extra 5 mm was added to each side of the crosshead.

![CrossheadFEA15](CrossheadFEA15.png)

![CrossheadFEA16](CrossheadFEA16.png)

**Second Iteration** (5 mm added to length, base, and height):

| Max Quantity | Initial Value (Standard Mesh Density) | Final Value (Finest Mesh Density | Percent Discrepancy | Convergence |
| -------- | :-------: | :-------: | :-------: | :-------: |
| Stress: 206.807e^8 N/mm^2  | 2.874e^7 N/mm^2 | 3.015e^7 N/mm^2 | 4.7886% | Converged |
| Displacement: 0.1 mm  | 6.530e^-3 mm | 6.381e^2 mm | 2.3081% | Converged |
| Safety Factor: 4  | 7.19514 | 6.85999 | 4.7691% | Converged | 
| ----- | <img width="320" height="188" alt="CrossheadFEA19" title="Stress" src="CrossheadFEA19.png" /> Stress | <img width="320" height="188" alt="CrossheadFEA17" title="Displacement" src="CrossheadFEA17.png" /> Displacement | <img width="320" height="188" alt="CrossheadFEA18" title="Safety Factor" src="CrossheadFEA18.png" /> Safety Factor | ----- |


Iteration 2 Mass: 2.617 pounds

The second iteration converged well below every parameter. The extra 5 mm made the crosshead about a pound heavier. A more efficient design could certainly be achieved but this design was sufficient for the assignment.

### Crosshead CAD Drawing

A drawing of the final crosshead design was created. The holes were toleranced using an RC2 running sliding fit for the lead screw that would be running through it.

<iframe src="A10Crosshead2.pdf" width="100%" height="650px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="A02-Truss-weight-calc.pdf">Download the PDF</a>.</p>
</iframe>


### Cost Table

| Item Number | Quantity | Name | Cost/Item | Cost | Purchase Link |
| -------- | :-------: | :-------: | :-------: | :-------: | :-------: | 
| 95120A592 | 2 | 932 Bearing Bronze Acme Flange Nut | $111.78 | $223.56 | https://www.mcmaster.com/product/95120A592 |
| 95061A813 | 2 | 18-8 Stainless Steel Acme Lead Screw | $64.53 | $129.06 | https://www.mcmaster.com/product/95061A813 |
| 47065T107 | 2 | T-Slotted Framing 3ft | $29.86 | $59.72 | https://www.mcmaster.com/47065T107-47065T419/ |
| 47065T107 | 4 | T-Slotted Framing 1ft | $10.82  | $43.28 | https://www.mcmaster.com/47065T107-47065T418/ |
| 47065T255 | 4 | Silver Straight Surface Bracket | $10.16 | $40.64 | https://www.mcmaster.com/47065T255/ |
| 60755K12 | 4 | Lead and Ball Screw End Support | $796.24 | $3184.96 | https://www.mcmaster.com/60755K12/ | 
| 3487N294 | 1 | Force Sensor | $1,034.12 | $1,034.12 | https://www.mcmaster.com/3487N294/ |
| 47065T239 | 4 | Silver Corner Bracket | $8.54 | $34.16 | https://www.mcmaster.com/47065T239/ |
| 6015A57 | 2 | Miniature Bench Vise | $11.45 | $22.90 | https://www.mcmaster.com/6015A57/ |
|  |  |  | Total Cost: | $4772.40 |  |


## Lessons Learned - Derek Heidenfelder

This assignment was very interesting and fun. It was a real test of my ability to create assemblies in Solidworks. Not having to design as many parts manually was nice but part searching was a big part of the process. I needed to make sure everything would fit together properly. Luckily, the parts on McMaster are all pretty standardized so It often wasn't an issue. The only time I had to create some weird mates was when adding in the crosshead since it was designed with metric units and everything from McMaster is in imperial units. Trying to get the crosshead centered was a challenge but it mainly took some math to determine the center of base of the frame. I learned a lot about different and more complicated mates, such as the screw mate I applied to the flange nut and lead screws. Overall, this assignment has definately improved my ability to create assemblies in Solidworks.


### Solidworks CAD File Downloads

[Crosshead Download](A10Crosshead2.SLDPRT)

[Tensile Tester Assembly Download](TensileTesterAssem3.SLDASM)


### Resources

Machinery's Handbook 32nd Edition

[McMaster Website](https://www.mcmaster.com/)

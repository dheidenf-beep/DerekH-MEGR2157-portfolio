# A2 – Truss Stress Analysis

For the second assignment of MEGR 2157, we were tasked with designing a simple truss to support two loads while attaching to two supports. The assignment is meant to introduce us to designing and analyzing engineering systems from scratch. The truss structure wasn't required to be of any particular shape, allowing for creativity on how to complete the assignment.

## Objective

The truss is meant to support two equal loads P which are between 20 and 30 kilonewtons pointing in opposite directions. The truss is mounted to a roller on the left at point B and a pin support on the right at point A. The distances between the points were given with a = 0.4 meters being the horizontal distance between each point and b = 0.3 meters being the vertical distance from the lower points to the higher points. We were given complete freedom on how to design the truss that we best solved the problem.

<img src="Problem-Picture.png" alt="Image of the given Problem" width="500" height="600">

## Truss Design

The truss I drew is the simplest and most direct one that could be drawn. However, there are benefits in the simplicity of the design, such as needing a fewer number of total parts and a lesser chance of connection points failing. 

The truss I designed is composed of three equilateral triangles directly attached to the four points. This creates five points of intersections and seven beams composing the truss. To connect the seven beams, five pins are needed to hold the truss together. The design of the truss maximizes stability using the most amount of triangles possible while also minimizing the number of parts, thus minimizing weight and complexity. 

The forces of the truss was broken down and analyzed to determine the highest internal force which would be used to find the minimal cross-sectional area the beams and pins should have to ensure the truss can support the loads safely. The forces were first calculated symbolically then numerically. The external support forces were calculated first, which consisted of two forces at point A, Ay and Ax, and one force at point B, By, since it is a roller.

**External Force Calculations**

<iframe src="A02-Ext-force-calc.pdf" width="100%" height="900px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="A02-Ext-force-calc.pdf">Download the PDF</a>.</p>
</iframe>

Once the external forces Ay, By, and Ax were calculated, the internal forces were analyzed using method of joints. The internal forces were calculated using four of the five points since the fifth point would be redundant. Pin A, B, C, and D were analyzed to obtain all seven internal forces.

**Internal Force Calculations**

<iframe src="A02-Int-forces-work.pdf" width="100%" height="4200px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="A02-Int-forces-work.pdf">Download the PDF</a>.</p>
</iframe>

Once the equations for all of the external and internal forces were found symbolically, numbers could be plugged in. The distances of a = 0.4 meter and b = 0.3 meters were used to the hypotenuse distances of the triangles. The distance d of the outside triangles was found using the Pythagorean theorem to be 0.5 meters. The distance of the internal triangle was smaller because the x-distance was in the center of an 0.4 meter segment. The distance h of the internal triangles was found to be ~0.361 meters. 

The Assignment gave a range for the P values to be between 20 and 30 kilonewtons. I chose the value right in the middle and set P = 25 kN. With the force of P and the all of the distances solved for, all internal forces could be solved numerically. 

**Numerical Force Calculations**

<iframe src="A02-Numerical-work.pdf" width="100%" height="900px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="A02-Numerical-work.pdf">Download the PDF</a>.</p>
</iframe>

I used my Ti-84 calculator to create variables and equations for each support force, distance, and load to try and minimize mathematical error and save time.

<img src="CalcPic1.jpg" alt="Calc1-Pic" width="500" height="600">

<img src="CalcPic2.jpg" alt="Calc2-Pic" width="500" height="600">

<img src="CalcPic3.jpg" alt="Calc3-Pic" width="500" height="600">

The support forces were verified by plugging into back into the sum of forces equations used in the individual pin analysis. Since the internal forces should sum to zero, plugging back in the numbers acquired for the internal forces will verify that the numbers are correct if the results are zero. 

**Numerical Force Verification**

<iframe src="A02-Verifying-Numbers.pdf" width="100%" height="1900px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="A02-Verifying-Numbers.pdf">Download the PDF</a>.</p>
</iframe>

If the calculations are correct, the forces summed to zero meaning that the numbers should be correct. This meant the largest internal forces were DE and CE at 20.031 kN in tension and compression respectively. The interesting result was the math showing that the force CD between the points with the loads was zero. This implies that the beam between C and D could be removed to save weight or cost but that could potentially cause stability issues.

This was the second attempt at calculating the internal forces. The first attempt had the wrong sign on the external force By by which led to all of the internal forces being wrong. CE ended up around 40 kN of force, which was unreasonable and the verification of the forces using the sum of forces equations did not sum to zero. 

**Incorrect Force Calculations**

<iframe src="A02-Initial-Wrong-Work.pdf" width="100%" height="4200px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="A02-Initial-Wrong-Work.pdf">Download the PDF</a>.</p>
</iframe>

Using the new correct numbers, the internal cross sectional area need for the beams could be found using the largest force, being 20.031 kN, and a safety factor of 3.5. The yield strength used was 33,000 psi or 228 megapascals for Grade A A500 steel which was found using multiple sources that listed a range of 33,000 to ~50,000 psi. I went with the low end of 33,000 psi for an additional level of safety. 

**Safety and Stress Calculations**

<iframe src="A02-Beam-Safety-Calc.pdf" width="100%" height="900px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="A02-Beam-Safety-Calc.pdf">Download the PDF</a>.</p>
</iframe>

The minimum cross-sectional area that would fulfill the given restrictions was found to be approximately 307.49 mm^2. Solving for the radius, the radius ended up being ~9.8933 mm. I decided to round up to 10 mm though to make calculations easier. This meant that the diameter would be 20 mm. 

Using the same sources that listed the yield strength of grade A A500 steel, the number given for the density of A500 steel was 7800 kg/m^3. This density was then used to calculated the weights of the seven individual beams. The weights were then summed to find the total weight of the truss.

**Weight Calculation**

<iframe src="A02-Truss-weight-calc.pdf" width="100%" height="2800px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="A02-Truss-weight-calc.pdf">Download the PDF</a>.</p>
</iframe>

The total wight of the 20 mm diameter beams was calculated to be 8.138 kg. 

## Pin Calculations

The minimal cross-sectional area of the pins was then calculated using the given numbers from the assignment. The assignment listed a shear yield strength of 170 ksi (converted to 1172.11 MPa) and a density of 0.278 lbs/in^3 (converted to 7695.0135 kg/m^3). The pin at point E was sampled because four beams overlap at that point meaning the shear stress would be the highest. 

**Shear Stress Pin Calculation**

<iframe src="A02-Pin-force-calc.pdf" width="100%" height="1800px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="A02-Pin-force-calc.pdf">Download the PDF</a>.</p>
</iframe>

After a couple math mistakes (such as incorrectly calculating the area without the safety factor), the minimum cross-sectional area was determined to be ~35.426 mm^2. Solving for the radius gave a radius of 3.36 mm and thus a pin diameter of 6.72 mm. The longest length chosen was 80 mm which was needed for the pin at point E to pass through the four 20 mm diameter beams. The weight of one pin was determined using the density of 7695.0135 kg/m^3. 

**Pin Weight Calculations**

<iframe src="A02-Pin-weight-calc.pdf" width="100%" height="900px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="A02-Pin-weight-calc.pdf">Download the PDF</a>.</p>
</iframe>

The weight of one pin with the given density was determined to be 0.0218 kg or 21.8 grams. To find the weight of all five of the needed pins, the found weight was multiplied by five giving a total weight of 0.109 kg for all five pins. 

The total calculated weight of the truss could then be calculated by adding the weight of the beams and the weight of pins. The calculation yielded a weight of 8.247 kg for the entire assembly.

With the numbers calculated, the CAD modeling could begin.

## CAD Modeling the Truss

<img src="TrussPic-1.png" alt="Truss Picture 1" width="500" height="600">

I modeled the truss using Solidworks. The hardest part about modeling the truss was figuring out how to start. I drew a 2D sketch template with the right dimensions and tried a couple different ways to create the points where the pins would go and then create the beams to connect those points. The truss was not an assembly of multiple parts, I decided to model it as one thing and didn't put much time into where the beams intersected to save time and the assignment didn't require it. My first thought to try and create the truss structure was to create the points of intersection first and then try to build the beams off of those. 

<img src="TrussPic-2.png" alt="Truss Picture 2" width="500" height="600">

<img src="TrussPic-3.png" alt="Truss Picture 3" width="500" height="600">

However, I quickly figured out that I didn't know how to do that in Solidworks, and I tried a different plan. 

<img src="TrussPic-4.png" alt="Truss Picture 4" width="500" height="600">

<img src="TrussPic-5.png" alt="Truss Picture 5" width="500" height="600">

I made the truss in 2D out of rectangles with the appropriate thickness of 20 mm and extruded it to a depth of 80 mm. The reason I went with the 80 mm is because at pin E, four beams intersect. And while I wasn't modeling the connections between the beams, I still didn't want them to overlap. Thus, the 80 mm was so I could offset each beam so that the beams wouldn't be directly on top of each other. It did mean the truss was less symmetric so I couldn't shortcut as many processes but it was slightly more realistic. 

After the whole 2D base was extruded, I cut away the parts on the lower three beams where the round beams needed to go in between the points of overlap.

<img src="TrussPic-6.png" alt="Truss Picture 6" width="500" height="600">

I then extruded the round beams on the flat surfaces left over so that everything lined up nicely. 

<img src="TrussPic-7.png" alt="Truss Picture 7" width="500" height="600">

<img src="TrussPic-9.png" alt="Truss Picture 9" width="500" height="600">

After extruding the three beams, I went ahead and put in three of the pin holes at a diameter of 6.72 mm. In hindsight, it would probably be safer in practice to do a slightly larger whole since that is the exact diameter of the pins, but for the CAD model, it sufficed.

<img src="TrussPic-8.png" alt="Truss Picture 8" width="500" height="600">

<img src="TrussPic-10.png" alt="Truss Picture 10" width="500" height="600">

<img src="TrussPic-11.png" alt="Truss Picture 11" width="500" height="600">

After putting in the initial three pin holes, I fixed the two corners of the truss to make room for the last two holes. 

<img src="TrussPic-12.png" alt="Truss Picture 12" width="500" height="600">

<img src="TrussPic-13.png" alt="Truss Picture 13" width="500" height="600">

<img src="TrussPic-14.png" alt="Truss Picture 14" width="500" height="600">

<img src="TrussPic-15.png" alt="Truss Picture 15" width="500" height="600">

With all of the pin holes in, I worked on creating the last four beams, starting with removing the necessary material from the base structure. I also squared up the intersection points around points C and D. 

<img src="TrussPic-16.png" alt="Truss Picture 16" width="500" height="600">

<img src="TrussPic-17.png" alt="Truss Picture 17" width="500" height="600">

<img src="TrussPic-18.png" alt="Truss Picture 18" width="500" height="600">

Since I squared up the intersection points, I needed to extend the beam between the points. I tried to go back and edit the original extrusion to make it go through further. However, I couldn't figure out how to extend the extrude and ended up adding another sketch to extend the beam.

<img src="TrussPic-19.png" alt="Truss Picture 19" width="500" height="600">

Then I put in the two middle diagonal beams in the same way as before, making sure the offset was correct so the beams wouldn't overlap.

<img src="TrussPic-20.png" alt="Truss Picture 20" width="500" height="600">

<img src="TrussPic-21.png" alt="Truss Picture 21" width="500" height="600">

<img src="TrussPic-22.png" alt="Truss Picture 22" width="500" height="600">

<img src="TrussPic-23.png" alt="Truss Picture 23" width="500" height="600">

The middle diagonal beams were offset to the edges so there would be room for the last two beams to be in the middle of the intersection. 

<img src="TrussPic-24.png" alt="Truss Picture 24" width="500" height="600">

<img src="TrussPic-25.png" alt="Truss Picture 25" width="500" height="600">

With the last two beams put in, the model of the truss was completed. 

<img src="TrussPic-26.png" alt="Truss Picture 26" width="500" height="600">

<img src="TrussPic-27.png" alt="Truss Picture 27" width="500" height="600">

While not the most detailed or realistic model of the truss that could be made, it is a good approximation and visual for what it would look like.

With the truss finished, the pins were next to model. I modeled one 80 mm long, 6.72 mm diameter cylinder to represent all of the pins. 

<img src="PinPic1.png" alt="Pin Picture 1" width="500" height="600">

<img src="PinPic2.png" alt="Pin Picture 2" width="500" height="600">

<img src="PinPic3.png" alt="Pin Picture 3" width="500" height="600">

With the truss and pins modeled, materiels could be set for both and the properties, primarily mass, could be deduced.

## CAD Truss Analysis

Once the truss and pins were modeled, materiels were selected for both based off of yield strength and mass density. For the truss, Plan Carbon Steel was the closest material to Grade A A500 steel I could find, with a yield strength of 220 MPa which is slightly less than the actual 228 MPa but Plain Carbon Steel has the same density of 7800 kg/m^3. 

<img src="TrussPic-28.png" alt="Truss Picture 28" width="500" height="600">

<img src="TrussPic-Mat.png" alt="Truss Material Selection" width="500" height="600">

<img src="TrussPic-Mass.png" alt="Truss Mass Calculation" width="500" height="600">

The weight of the truss given by Solidworks was 9.80 kilograms which is higher than my calcualted 8.138 kilograms. The difference likely comes from the beam intersections which are solid in Solidworks while I only calculated the isolated beam weights. 

For the pins, the closest material I could find was Alloy Steel which has a yield strength of 620 MPa which is about half of the true 1172.11 MPa yield strength. However, it has the closest density at 7700 kilograms/m^3 while the true density is 7695.0135 kg/m^3. 

<img src="Pin-Steel.png" alt="Steel Pin" width="500" height="600">

<img src="Pin-Steel-Mat.png" alt="Alloy Steel Material" width="500" height="600">

<img src="Pin-Steel-Mass.png" alt="Mass Calculated by Solidworks" width="500" height="600">

The mass of one pin calculated by Solidworks was 21.85 grams. The result was really close to my calculated 21.8 grams. The weight for all five pins then would be 109.25 grams or 0.10925 kg. Adding the masses together would give a total wieght of the truss of 9.90925 kg, which is much higher than the calculated 8.247 kg. 

## Truss Component Failure Modes

Truss Failures depend heavily on the nature of the specific truss being analyzed. However, there are specific common failures such as buckling or yielding that are the most likely to occur in each member, both the beams and the pins, of the truss I designed. The truss being made of Grade A A500 structural steel means that it is ductile and able to withstand a large amount of stress before undergoing plastic deformation. 

Analyzing the truss beams, each member is either under compression or tension due to the opposite loads of P. Looking at the internal forces on each member starting at A at the top right and moving counter-clockwise around the points, we can see which forces are compressive or tensile. Forces AD, DE, and BC are all tensile and AE, CE, and BC are all compressive. The member CD has an internal force of zero meaning there is no stress on it and it is purely there to hold the frame together. 

For the tensile forces, AD, DE, and BC, the expected failure mode for the associated members would be yielding when the stresses exceed the yield stress of the steel. Under the ideal conditions, especially with the safety factor, yielding should not happen but if the loads were to change and increase, the structure of the truss might not be able to handle the loads. The easiest way to fix an issue like yielding would be to add more support either by increasing the cross-sectional area of the members or adding more beams to distribute the force. However, this obviously comes with tradeoffs like increasing cost, weight, and stress on the pins. 

For the compressive forces, AE, CE, and BC, the expected failure mode for the associated members would be buckling when the compressive force reaches the point needed to bend the materiel suddenly causing it to deform or fracture. The left force of P is the cause of most of the compressive force due to it pointing up towards the stress versus down or away. Much like with yielding, the easiest solution to buckling would be to add more support. Either, larger cross-sectional area or thicker members to prevent the load from possibly being able to bend it. Although, at a certain point, the truss could buckle under its own weight if too much material is added and the pins don't break first. 

The pins in trusses undergo massive amounts of shear stress while trying to hold the structure together. Shear stress can cause the pins to undergo shear failure which breaks apart the pins in the direction parallel to the force. Creep can also occur in the pins which causes them to sink into the member the pin is in which can weaken and deform the member. One solution would be to add redundant or multiple pins to each connection to distribute the stresses over. And if there are redundant pins, if a pin fails, the redundant pins could prevent the truss from collapsing entirely.

## Conclusions

During this assignment, I was forced to learn a lot about designing and creating a structure from scratch. I had to perform various mathematical checks and verifications to ensure my calculations were correct since there was no answer key. Modeling a truss structure in Solidworks was very different from anything I've done before which had me thinking very differently about how to go about it. THe truss modeling ended up needed a lot of trial and error before a successful method was devised. Researching failing modes was very enlightening to see what specific problems engineers need to design around in order to ensure the safety and stability of a structure. I ended up making a lot of simple math errors that ended up causing me to lose time and effort but it also reinforced checking my work to make sure the numbers were actually correct. Had I more time, I would've been able to more realistically model the truss with actual connections and assemblies. However, I chose to go simpler due to the time constraints.

Time Spent on this assignment: 18 Hours

[Truss STL File](Truss-Model-Finished.STL)

[Pin STL File](Truss-Pin.STL)

## Resources

[Solidworks](https://www.solidworks.com/)

-------------------------------------------

**Sources for A500 Steel Numbers**

[Alro Steel](https://www.alro.com/divSteel/Metals_Gridpt.aspx?gp=0108&gpn=A500&Mat=CARBON%20STEEL&Type=Pipe%20/%20Tube)

[Altitube Inc](https://www.altitube.com/en/astm-a500-grade-b-vs-c/)

[Tus Pipe](https://www.tuspipe.com/standards/astm-a500/)

[Totten Tubes Inc](https://www.tottentubes.com/astm-a500-specification-information)

[Beam Dimensions](https://beamdimensions.com/materials/Steel/ASTM/ASTM_A500/#Grade_A)

[Online Metals](https://www.onlinemetals.com/en/product-guide/alloy/a500-a513)

----------------------------------------------

**Source for Failure Mode Analysis**

[Learning from failure propagation in steel truss bridges](https://www.sciencedirect.com/science/article/pii/S1350630723004429)

[Truss Failure Analysis](https://broadtechengineering.com/truss-failure-analysis/)

[Metal Plated Wood Truss Failure Causes](https://www.engr.psu.edu/ae/thesis/failures/MKP/failures/failures.wikispaces.com/Wood_Truss_Failures.html)

[Predicting the Probability of Failure in Truss Structures Using Artificial Neural Networks](https://www.jsoftcivil.com/article_209137.html)

[Experimental study and numerical analysis on the failure mode of staggered truss framing system](https://www.sciencedirect.com/science/article/pii/S0141029624004401#sec0110)

[Experimental Study on System Reliability of Cold-Formed Steel Roof Trusses](https://scholarsmine.mst.edu/cgi/viewcontent.cgi?article=1156&context=ccfss-aisi-spec)

[Brittle and Ductile](https://www.engineeringarchives.com/les_mom_brittleductile.html)

[Buckling and Yielding](https://www.surescreenmaterials.com/failure-mechanisms/buckling-and-yielding)

[Shear Failure](https://www.sciencedirect.com/topics/engineering/shear-failure)

[What Is Creep In Materials? – And How Does It Work?](https://www.fidelisfea.com/post/what-is-creep-in-materials-and-how-does-it-work)


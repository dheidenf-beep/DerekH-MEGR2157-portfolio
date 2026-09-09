# A3 – Parametric & FEA

## Objective

Given maximum elongation of 0.009 inches. 300 lbs < Force < 500 lbs.

## Analyze

After looking through the different Aluminum Alloys Solidworks had preinstalled, I went with 1100-H26 Rod (SS) which had an Elastic Modulus of 10.007604*10^6 psi. 

![Aluminum Alloy Stats](Alumininum-Stats.png)

With the material decided, I first performed my hand calculations with multiple sizes of the diameter. I decided on a force of 450 pounds to be a little closer to the high end. I used 2, 1, and 0.5 inches for the diameter and settled for the 0.5 inch diameter because it had the shortest length of 40.03 inches. Calculating the 2 inch diameter produced a length of 630 inches, which felt a bit large for my purposes. I then used my length, area, force, and Elastic Modulus to calculate the approximate elongation which came out to be approximately 0.0089999 inches or essentially 0.009 inches which was the maximum.

**_INSERT WORK_**

With the parameters decided on, I could start creating the variables in Solidworks and playing around with the dimensions. I played with the diameter a bit more but the numbers the calculations gave were about the same as I had calculated by hand. Thus, I still ended up using 0.5 inches as my diameter.  

![Diameter 2 inch](Diamter-2.png)

* Very unreasonable length for the 

![Diameter 0.5 inch](Diamter-0.5.png)

* Much more reasonable length relative to the diameter.

The length calculated by Solidworks was closer to 39.30 inches or about 0.73 inches shorter than the 40.03 inch length I calculated by hand. This meant there was a 2.53% difference in the lengths.

**_Insert PERCENT DIFF WORK_**



## Bar Design

Once I had the variables in place, I began modeling. The beam was very simple, just a cylinder with the dimensions bounded to the variables. 

![Making 1](Making-1.png)

![Making 2](Making-2.png)

![Making 6](Making-6.png)

* The Circle at the Base with the diameter bounded to the variable "d".

![Making 3](Making3.png)

![Making 4](Making-4.png)

* The bar was then extruded to the length of "L" or 39.30 inches.

Once the length and diameter parameters were in, those were all the measurements I needed for the bar and I could move on to the Finite Element Analysis and parametric testing in Solidworks. However, before that, I calculated the weight of the bar. The Aluminum Alloy 1100-H26 Rod (SS) I used had a density of 0.10 lbs/in.^3. I calculated the volume to be 8.006 in.^3 by multiplying the Area of the base, 0.20 in.^3, by the calculated height of 40.03 inches. This produced a weight of 0.8006 pounds. This felt light for a beam that was 40 inches long, but Solidworks produced a similar result at 0.75 lbs.

**_INSERT WEIGHT WORK_**

![Bar Mass](Bar-Mass-Properties.png)

Calculating the potential difference gave a percentage difference between the two masses of 6.53%, which is reasonably small. One cause of error is the difference in lengths from my hand calculations with the Solidworks calculations with the Solidworks calculations likely being more precise.

**_INSERT PERCENT DIFF WORK_**

### Initial Incorrect Bar Calculations

Initially, when I started making the bar, I thought it was a hollow circular bar with an inner and outer diameter. This made the length calculations output a much larger number than I felt seemed reasonable. However, I went ahead and started modeling a hollow beam.

![Wrong Making 1](WRONG-Making-1.png)

![Wrong Making 2](WRONG-Making-2.png)

![Wrong Making 3](WRONG-Making-3.png)

![Wrong Making 4](WRONG-Making-4.png)

![Wrong Making 5](WRONG-Making-5.png)

![Wrong Making 6](WRONG-Making-6.png)

![WRONG-Variables](WRONG-Variables.png)

The plan was to have an outer diameter of 2 inches and an inner diameter of 1.8 inches. This produced a length of approximately 120 inches which seemed like far too much. And, after double checking my calculations, I finally looked back through the instructions and saw that it didn't say anything about a hollow beam. I then redid my calculations and CAD modeling, this time with a solid beam. 

## Finite Element Analysis

The next step in the process was to simulate the bar with the chosen load of 450 lbs on one side with the other being fixed. I used Solidworks' free Simulation Xpress Analysis Wizard tool to perform the Finite Element Analysis. I first had to set up the bar with correct conditions by fixing the beam in place on one end and applying the tensile force on the other end.

![Fixing Surface](Fixing-Surface.png)

* Fixing one end of the bar

![Applying Force](Applying-Force.png)

* Application of the 450 pound force to the other end of the bar

![Force and Fixed Surface](Force-and-Fixed.png)

* Both the force and fixed surface applied

Once I had the force applied and one end fixed, I had verify the material. 

![Verifying Material](Modulus-Material-Data.png)

With the correct material, force, and fixed surface, I could then simulate the bar under load. 

The Solidworks Simulation Xpress produced Von Mises stress, Displacement, Factor of Safety, and Deformation in the form of an animation. Solidworks does exaggerate how far the bar actually displaces to make it more obvious since real world changes are generally near invisible to the naked eye.

![Stress](Stress-Screenshot.png)

* Von Mises stress graph with the maximum stress at 2.395 * 10^3 psi

![Displacement](Displacement-Screenshot.png)

* Displacement Graph with the maximum displacement reaching 9.001 * 10^-3 inches

![Safety Factor](Safety-Factor-Screenshot.png)

![Safety Factor 2](Safety-Factor-8.png)

* The first picture shows where the safety factor is below 1 and the second is where it is below 8. The lowest factor of safety found was 7.18255

With the data collected, I could draw some actual results from the FEA study.

### FEA Results

Using the numbers given from the result of the study, it can be determined that the maximum stress of 2,395 psi is below the yield point of the Aluminum Alloy at 17,200 psi. This means the force of 450 pounds isn't even close to breaking the bar.

The results from the displacement show a maximum displacement of 0.009001 inches which is very close to the maximum allowed elongation of 0.009 inches. 


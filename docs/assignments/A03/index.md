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



## Decide

Once I had the variables in place, I began modeling. The beam was very simple, just a cylinder with the dimensions bounded to the variables. 

![Making 1](Making-1.png)

![Making 2](Making-2.png)

![Making 6](Making-6.png)

* The Circle at the Base with the diameter bounded to the variable "d".

![Making 3](Making3.png)

![Making 4](Making-4.png)

* The bar was then extruded to the length of "L" or 39.30 inches.



## Communicate


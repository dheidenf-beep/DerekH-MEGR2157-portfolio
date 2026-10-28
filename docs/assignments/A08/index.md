# A8 – Gears

## Objective

The objective of this assignment was to design and create a gearbox using pre-made gears.

## Gearbox Calculations



## CAD Modeling

For the design of the gearbox, I went as simple as I could. I decided that there would be a wall for the gears and a base to hold it up using LC2 fits to hold the pieces together. 

To start, I began with the shafts. The shafts were simple, I only had to change the diameters and tolerances for each shaft. I used an RC2 Sliding Fit for the shafts. 



For the gearbox itself, I started with an arbitrarily sized rectangle of 3 inches by four inches that was the same thickness of the journal bearings. 


On the rectangle, I extruded the two holes for the shafts with appropriate tolerances for an RC2 Sliding Fit. I made the holes the same diameter of the journal bearings. The distances between the holes were the two pitch diameters of the two gears added together. 


I then created two rectangles on the bottom to fit into a base using LC2 clearances for **_Interference fits?_**. I extruded the rectangles to be an arbitrary 0.25 inches which would be the thickness of the base.


For the base of the gear box, I created another arbitrarily sized rectangle. 



I cut in the complimentary LC2 Rectangular holes. 

### Gearbox assembly

For the assembly of the gearbox, I needed to download the bearings and gears from the McMaster website.
I needed the pinion gear, the large gear, the bearing for the pinion shaft and the bearing for the gear shaft. 


I could then add in the different parts and create the final product.


Putting together the gearbox made me realized that I had used the wrong distances between the gears. I used the full pitch diameter pitch diameter when I should've used the radius. This could be easily fixed by updating the equations. 


However, I realized I should have probably made another wall to hold the other side of the axles. Instead of building a new gearbox, I modified the base to be able to support two of the wall segments so that I could reuse the wall with the fits in place. 





This makes the gearbox Three individual parts but it has only two unique parts. 




### CAD Drawings




## Lessons Learned



**Time Spent:** 5 Hours

### CAD File Download

[GearBox](GearBox.SLDPRT)

[Gearbox Base](GearBoxBase.SLDPRT)

[Input Shaft](shaft-1.SLDPRT)

[Output Shaft](shaft-output.SLDPRT)

[Metal Gear](Gear_Metal Gear - .SLDPRT)

[Pinion Gear](Pinion_Metal Gear.SLDPRT)

[Gear Journal Bearing](gear_journal_bearing.SLDPRT)

[Pinion Journal Bearing](pinion_journal_bearing.SLDPRT)

[Gearbox Assembly](GearboxAssembly.SLDASM)


## Resources

[Pinion Gear](https://www.mcmaster.com/7880K19/)

[Metal Gear](https://www.mcmaster.com/7880K24/)

[Metal Gear Journal Bearing](https://www.mcmaster.com/9368T14/)

[Pinion Gear Journal Bearing](https://www.mcmaster.com/9368T97/)


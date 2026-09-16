# A4 – Motor Mount

## Objective

The objective of Design a motor mount around a motor (the Brushed 24V DC Gear Motor 3.6Kg.cm/46RPM w/ 99.5:1 Planetary Gearbox). The goal was to create a motor mount capable of holding the motor with a load on the shaft within the specific constrictions.

![Motor Mount Example](MotorMountEx.png)

The mount was split into two features. The first was the part that held the motor and the second was the part attached to the wall. The constrictions of the design included the force of 300 newtons, a maximum strain of 0.30 mm in Feature 1, the material had to be ABS, PLA, or PETG, the design had a safety factor of 3, and the dimensions of the motor.

![Motor Dimensions](MotorDims.png)

## Feature Analysis

### Feature 1

To design the mount, the necessary dimensions needed to be chosen and solved for mathematically. The assignment gave a lot of freedom, allowing the base or height to be chosen. My first objective was to find the cross sectional area of the first feature. I went ahead and selected the material to be PETG so I would have the yield strength and elastic modulus. 

To start, I drew a picture which had the necessary motor dimensions I needed to design around. I then drew a free body diagram of the motor to determine the couple produced by the force on the screws that would be acting on feature 1. I started by solving symbolically.

![Page 1](MEGR-2157-A04-work_page-0001.jpg)

I had some trouble figuring out the couple but I realized later my mistake and it actually simplified my equations. Once I had the moment determined, I looked up the sizes of the screws in the Machinery Handbook. The screws on the motor specifications were M3 screws and I found the maximum head diameter to be 5.50 millimeters. To create some space between the screw holes and the edges of the feature, I took the distance between the screw holes and added 2 times the diameter of the screw heads to each side. Since the distance between the screws was 22 mm, this made the total base dimension 3 times the distance between the screws or 66 mm. I used the 66 mm as my minimum base length and started solving for the height. 

![Page 2](MEGR-2157-A04-work_page-0002.jpg)

![Page 3](MEGR-2157-A04-work_page-0003-cropped.jpg)

I rearranged the equations that were solved to find the base and instead solved for the height. The maximum height or thickness the feature could be was the length of the motor shaft or about 18 mm. I chose a maximum height of 12 mm to give some space on the shaft so the motor would be usable. I assumed the base and length of the feature were the same because the feature is a square. I then solved for the height of feature 1 numerically. 

The minimum yield strength of PETG listed on the [MatWeb website](https://www.matweb.com/search/DataSheet.aspx?MatGUID=4de1c85bb946406a86c52b688e3810d0&ckck=1) is 28.3 MPa. Dividing by the safety factor gave a maximum stress of 9.44 MPa. 

The elastic modulus for PETG was listed as 1100 MPa.

The max deflection given for the assignment was 0.30 mm for feature 1. 

![Page 4](MEGR-2157-A04-work_page-0004.jpg)

The height needed to be under 12 mm in order to pass the criteria I set.

![Page 5](MEGR-2157-A04-work_page-0005-Cropped.jpg)

Solving both equations for the height gave an initial minimum height of 7.3 mm which was below the 12 mm threshold. The second equation exceeded both the 12 and 18 mm thresholds meaning it wouldn't work since the design uses the maximum dimensions to ensure safety and usability. 

I tried again, this time solving for the base with the constraint of a minimum base of 66 mm and a height of 12 mm. 

![Page 6](MEGR-2157-A04-work_page-0006.jpg)

Solving for the bases with both equations did not satisfy the criteria of being greater than 66mm. This meant the base of 66 mm was sufficient for the design and the minimum I would go with for Feature 1. Although, I was curious if I could drop the height any because there were very big discrepancies between the 66 mm and what I calculated, so I tried the calculations with a height of 10 mm to see what the base limits would be.

![Page 7](MEGR-2157-A04-work_page-0007-cropped.jpg)

The bases solved for with a height of 10 mm stayed within the 66 mm diameter meaning the feature would still be sufficient with a height of 10mm. This gave feature 1 the final dimensions of 66 x 66 x 10 mm.

### Feature 2

For feature 2, the feature needed to support feature 1 while being able to mount to a rigid wall or ceiling. To start, I drew a free body diagram of the two features together and then I separated them, drawing individual free body diagrams for each feature. I needed to solve for the reaction force in feature 2 on feature 1 to counteract the couple, which I solved to be dependent on the height of feature 2. Whether or not this made my calculations more accurate, I'm not sure but it did lead to a lot of interesting math later.

![Page 8](MEGR-2157-A04-work_page-0008.jpg)

Using the force solved in feature 1, I calculated the couple in the screws that would be supporting feature 2. I used the same base of 66 mm for feature 2 and made it a square. I kept the material choice of PETG to stay consistent and so the design could be 3D printed in one piece if desired. I solved for the couple in feature 2 using the reaction force from feature 1. I forgot a negative sign here that I would notice later as I started calculating the heights. 

Since I had already solved the equations for the height, I didn't need to perform the algebra again and could begin with the numerical calculations. It was here I decided to use the same base to make the two features consistent. It wouldn't make since to have one feature be wider than the other. I decided to use the same M3 screws as before and increases the distance between them to 25 mm. Most of the numbers were the same as before since I kept with PETG. I continued with the same stress factor of 3. Since I assumed the deflection in feature 2 would be zero, that made one of the equations unsolvable. This meant I only had one equation to worry about, which was nice considering the work I put into it. 

![Page 9](MEGR-2157-A04-work_page-0009.jpg)

To start, I had to solve the equation for the height again. Since I made the moment dependent on the height, this made for a very difficult task. 

![Page 10-1](MEGR-2157-A04-work_page-0010-cropped-1.jpg)

I ended up creating a polynomial equation of degree three. Since I knew the height couldn't be zero, that meant I could drop it down to a polynomial of degree two. I then used the quadratic formula to solve for the height.

![Page 10-2](MEGR-2157-A04-work_page-0010-cropped-2.jpg)

![Page 11](MEGR-2157-A04-work_page-0011-cropped.jpg)

![Page 12](MEGR-2157-A04-work_page-0012-cropped.jpg)

A number of math errors made it take longer than it should have and I got worried when I got out very large heights. But, I eventually figured it out and ended up with 2 minimum heights of -4.518 and 11.51 mm. Since height couldn't be negative, that meant my minimum height for feature 2 would be 11.51 mm which I round up to 12 mm. 

With all of the dimensions determined, I could start modeling the motor mount in Solidworks.

* **Isometric Hand Drawing**

![Isometric Hand Drawing](MEGR-2157-A04-work_page-0013-isometric.jpg)

## CAD Modeling

With the dimensions of the motor mount solved for, I went to modeling the mount in CAD, specifically Solidworks.

### Feature 1

I started with feature 1 which was a 66 x 66 mm square to start. 

![Motor Mount CAD 1](MotorMountCad-1.png)

![Motor Mount CAD 2](MotorMountCad-2.png)

* I then extruded it to the height of 10 mm.

Construction geometry was useful to get everything aligned nicely without needing to dimension it.

![Motor Mount CAD 3](MotorMountCad-3.png)

![Motor Mount CAD 4](MotorMountCad-4.png)

![Motor Mount CAD 5](MotorMountCad-5.png)

![Motor Mount CAD 6](MotorMountCad-6.png)

![Motor Mount CAD 7](MotorMountCad-7.png)

Once I had the construction lines in place, I put in the M3 screw holes using Solidworks' "Hole Wizard" feature to get the correct dimensions automatically.

![Motor Mount CAD 8](MotorMountCad-8.png)

![Motor Mount CAD 9](MotorMountCad-9.png)

![Motor Mount CAD 10](MotorMountCad-10.png)

![Motor Mount CAD 11](MotorMountCad-11.png)

Once I put in the M3 holes, I put in the center hole for the shaft of the motor. I included the tolerances but would later change the hole to be a little bigger to give the motor more room. 

![Motor Mount CAD 12](MotorMountCad-12.png)

![Motor Mount CAD 13](MotorMountCad-13.png)

![Motor Mount CAD 14](MotorMountCad-14.png)

With the hole for the shaft in place, I then moved on to creating feature 2.

### Feature 2

To create feature 2, I started with a rectangle at the base of feature 1. I set the height to the correct 12 mm and didn't need to worry about the base since it was the same as feature one and the sketches were coincident. I extruded it to the length of 66 mm to make it a square.

![Motor Mount CAD 15](MotorMountCad-15.png)

![Motor Mount CAD 16](MotorMountCad-16.png)

![Motor Mount CAD 17](MotorMountCad-17.png)

I used the same method with construction geometry to put in the M3 holes into feature 2.

![Motor Mount CAD 18](MotorMountCad-18.png)

![Motor Mount CAD 19](MotorMountCad-19.png)

![Motor Mount CAD 20](MotorMountCad-20.png)

![Motor Mount CAD 21](MotorMountCad-21.png)

![Motor Mount CAD 22](MotorMountCad-22.png)

![Motor Mount CAD 23](MotorMountCad-23.png)

* I realized I put in the wrong diameter and corrected it from 22 mm to 25 mm.

![Motor Mount CAD 24](MotorMountCad-24.png)

![Motor Mount CAD 25](MotorMountCad-25.png)

![Motor Mount CAD 26](MotorMountCad-26.png)

![Motor Mount CAD 27](MotorMountCad-27.png)

### Finishing Touches

There were a couple more changes I made to the mount to finish it off.

* I then proceeded to increase the diameter of the shaft hole by 0.1 mm to add extra clearance.

![Motor Mount CAD 28](MotorMountCad-28.png)

![Motor Mount CAD 29](MotorMountCad-29.png)

* I also added in an indent to the inside of feature 1 because the motor extends out as it gets closer to the shaft and I wanted it to rest flush.

![Motor Mount CAD 30](MotorMountCad-30.png)

![Motor Mount CAD 31](MotorMountCad-31.png)

![Motor Mount CAD 32](MotorMountCad-32.png)

![Motor Mount CAD 33](MotorMountCad-33.png)

![Motor Mount CAD 34](MotorMountCad-34.png)

With that, the motor mount was finished in CAD.

![Motor Mount CAD 27](MotorMountCad-27.png)



## Engineering Drawing

Once I finished the CAD modeling, I needed to create an engineering drawing of it in the CAD program, following ASME standards. The drawing consists of an isometric view in the top right, a top image, front image, and right side image. All of the necessary dimensions should be in place so that an engineer or manufacturer would be able to reproduce it. I am not sure if it holds up to ASME standards but it was difficult to find documentation on the standards. I used the built in Solidworks template on A size, U.S. paper. 

<iframe src="MotorMountDrawing.pdf" width="100%" height="400px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="MotorMountDrawing.pdf">Download the PDF</a>.</p>
</iframe>

[Motor Mount Drawing](MotorMountDrawing.pdf)



## Lessons Learned

Overall, this assignment was good practice for complicated statics problems and designing a model while being able to control nearly every parameter. Dealing with cantilever and other suspended beams is a completely new topic that was interesting to learn. It was also an unexpected exercise in my math ability. I had also never made a CAD drawing with Solidworks before which was good practice since every CAD software is different.

[Motor Mount STL File](MotorMountFinal.STL)

**Time Spent: 7 Hours**



## Appendix & Resources

[ABS Specifications | MatWeb website](https://www.specialchem.com/plastics/guide/acrylonitrile-butadiene-styrene-abs-plastic)

[ASME Standards and Drawings](https://blog.ansi.org/ansi/what-are-the-asme-y14-5-and-asme-y14-100-standards/)

[Brushed 24V DC Gear Motor 3.6Kg.cm/46RPM w/ 99.5:1 Planetary Gearbox](https://www.omc-stepperonline.com/brushed-24v-dc-gear-motor-3-6kg-cm-46rpm-w-99-5-1-planetary-gearbox-pa28-28245800-g100)

Machinery's Handbook 32nd Edition

[Overview of ASME Y14 Series Drawing Standards](https://grabcad.com/tutorials/overview-of-asme-y14-series-drawing-standards)

[PETG Specifications | MatWeb website](https://www.matweb.com/search/DataSheet.aspx?MatGUID=4de1c85bb946406a86c52b688e3810d0&ckck=1)

[PLA Specifications | MatWeb website](https://www.matweb.com/search/DataSheet.aspx?MatGUID=ab96a4c0655c4018a8785ac4031b9278&ckck=1)








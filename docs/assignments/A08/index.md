# A8 – Gears

## Objective

The objective of this assignment was to design and create a gearbox using pre-made gears.

## Gearbox Calculations

### Determing Sufficient Diameter

The assignment listed two geats to use from the McMaster website with a pinion gear and larger gear. The pinion gear had 9 and was the input gear. The larger gear had 24 teeth and was the output gear. The diameter of each shaft was given at 0.25 inches for the input shaft and 0.125 inches for the output shaft. Both shafts were the same length at 1 inch long. The rotation of the output gear was given at 1100 RPM with a torque of 1.25 lbf-in. The material was assumed to be steel. 

Using the rotation of the output gear and the gear ratio, I was able to calculate the speed and torque of the pinion gear. 

<img width="1163" height="681" alt="A08-gears_work_pic_1" src="https://github.com/user-attachments/assets/61ff18ee-e32f-41d5-bacd-dba1dcc2663d" />

For the pinion gear, the rotation was 2933.33 RPM with 0.4688 in.-lbf of torque. 

When I had the torques, I could then calculate if the given diameters were sufficient for the torque load. The loading shaft shear stress had to remain under 4000 psi and the output shaft needed to remain under 6000 psi. I used the shear stress equation combining torque, radius, and polar moment of inertia to solve for the actual shear stresses. 

<img width="1132" height="692" alt="A08-gears_work_pic_2" src="https://github.com/user-attachments/assets/9b76c055-8db2-433b-a4d1-43576564d505" />

The calculated shear stress on the shafts was found to be well below the maximum values meaning the shaft diameters were sufficient for the load. 


### Determining PV Values for Bearings

With the shear stress determined and shaft diameters verified, the next step was calculating the PV values on the affective area of the shaft in order to find suitable bearings. 

I chose a thickness of 3/8 inches meaning the affective area would be the diameter times the thickness. To solve for the pressure, I needed the tangential force on the gears. To determine the tangential force on the gears, I used the equation for tangential force that is 2 times the torque on the gears divided by the gears pitch diameter. To find the pitch diameter, I looked on the McMaster website. 

From the website, I found the pitch diameter of the larger gear to be 1 inch and the pinion gear to be 3/8 inches.

With that, I could then calculate the tangential force and pressure.

<img width="1033" height="756" alt="A08-gears_work_pic_3" src="https://github.com/user-attachments/assets/b9a72d22-372d-4942-b395-cbffe53706c4" />

Next to calculate the velocity, I needed to convert from RPM to radians and then multiply by the diameter. This meant I just needed to multiply by an extra factor of pi to get the correct units of ft/min.

Once I had the velocity, I then just needed to multiply it by the pressure to get the PV values. 

<img width="1070" height="592" alt="A08-gears_work_pic_4" src="https://github.com/user-attachments/assets/612adb03-a043-477d-b42c-a1ef140a4dc6" />

I referred to the bearing material chart in the Machinery's Handbook and found the material with the minimum PV value that could support the shafts was dry graphite at 15,000 psi-ft/min. 

Using this information, I looked for bearings on the McMaster website that had a sufficient PV value. The bearings I found were high-temperature graphite-lubricated sleeve bearings with a PV value of 40,000 psi-ft/min that were 3/8 inches long.

**Input Shaft**

<img width="960" height="564" alt="GearboxScreenshot (68)" src="https://github.com/user-attachments/assets/385ca60b-89fd-4602-91a6-3f86a5c8e1eb" />

<img width="540" alt="InputShaftStats" src="https://github.com/user-attachments/assets/d7bb34be-ef3b-4fd7-96bb-ad1b29362d26" />

---------------------------

**Output Shaft**

<img width="960" height="564" alt="GearboxScreenshot (67)" src="https://github.com/user-attachments/assets/93c8662e-917f-4592-b1b7-8108afcc4c96" />

<img width="540" alt="OutputShaftStats" src="https://github.com/user-attachments/assets/f9250049-3257-4a1f-b235-00a3d414704b" />

These shafts were more than sufficient for the application. The last step I needed to go through before I could model the gearbox the was to determine the tolerances.


### Fit Selection

For the shafts, I went with an RC2 Running Sliding fit. And to put the gearbox together, I used an LC2 Locational Clearance Fit. The tolerances for each respective fit from the table in the Machinery's Handbook are shown below.

<img width="1275" height="1606" alt="A08-gears_work_pages-to-jpg-0003" src="https://github.com/user-attachments/assets/5800e25f-1fb6-4033-a339-2904d06c394d" />

With this final part done, I could finally move onto modeling the gearbox.


## CAD Modeling

For the design of the gearbox, I went as simple as I could. I decided that there would be a wall for the gears and a base to hold it up using LC2 fits to hold the pieces together. I tried to parametrically design everything I could to make it easier, using variables like the journal bearing length and shaft diameters. 

<img width="780" height="503" alt="GearboxScreenshot (6)" src="https://github.com/user-attachments/assets/ede3320d-28f1-4943-b0d2-c76297097878" />

I would export this file into a text document and use it across all of the different models. This way, I could just edit that text file and change the equations for every model. 

To start, I began with the shafts. The shafts were simple, I only had to change the diameters and tolerances for each shaft. I used an RC2 Sliding Fit for the shafts. 

* Input Shaft

<img width="960" height="564" alt="GearboxScreenshot (3)" src="https://github.com/user-attachments/assets/56289c55-9392-4ffd-bd04-b249ed8c6412" />

<img width="1920" height="1128" alt="GearboxScreenshot (28)" src="https://github.com/user-attachments/assets/24c6f31f-74ff-4977-90c1-aa3ff8903147" />

<img width="960" height="564" alt="GearboxScreenshot (4)" src="https://github.com/user-attachments/assets/05fe4e1f-6dce-472f-a8e5-282e79a71b03" />

<img width="960" height="564" alt="GearboxScreenshot (5)" src="https://github.com/user-attachments/assets/45f18229-cd04-4bd3-9403-d1aa2c2567f9" />

* Output Shaft

<img width="960" height="564" alt="GearboxScreenshot (7)" src="https://github.com/user-attachments/assets/c4e9f7e1-eb3b-4f66-9289-444211cf1ea2" />

<img width="1920" height="1128" alt="GearboxScreenshot (29)" src="https://github.com/user-attachments/assets/02e27fdd-428d-4440-ab20-b011e6e0ab84" />

<img width="960" height="564" alt="GearboxScreenshot (8)" src="https://github.com/user-attachments/assets/eeb67fe5-71f0-4402-8592-8c78bfce0a91" />


For the gearbox itself, I started with an arbitrarily sized rectangle of three inches by two inches that was the same thickness of the journal bearings. 

<img width="1920" height="1128" alt="GearboxScreenshot (9)" src="https://github.com/user-attachments/assets/23002dd3-074a-4ded-9aff-b343f9427bbb" />

<img width="1920" height="1128" alt="GearboxScreenshot (10)" src="https://github.com/user-attachments/assets/7f9801c4-7b4e-4477-810d-a149e29e565d" />

<img width="1920" height="1128" alt="GearboxScreenshot (11)" src="https://github.com/user-attachments/assets/d40fdc00-18ec-454a-8415-7bb60f0b3aab" />

My original idea was to extrude it the whole shaft length and then cut out a space inside for the gears. However, having each wall be the thickness of the journal bearings didn't leave enough room for the gears.

<img width="1920" height="1128" alt="GearboxScreenshot (12)" src="https://github.com/user-attachments/assets/87864c8d-808c-4464-983f-eb9f33b955f7" />

<img width="1920" height="1128" alt="GearboxScreenshot (13)" src="https://github.com/user-attachments/assets/a8180b16-a988-4416-bf1a-08c6633a9b18" />

<img width="1920" height="1128" alt="GearboxScreenshot (14)" src="https://github.com/user-attachments/assets/461e1301-1ee8-4787-a620-4fa808f521cf" />

So I switched off this idea and went back to the single rectangle.

On the rectangle, I extruded the two holes for the shafts with appropriate tolerances for an RC2 Sliding Fit. I made the holes the same diameter of the journal bearings. The distances between the holes were the two pitch diameters of the two gears added together. 

<img width="1920" height="1128" alt="GearboxScreenshot (15)" src="https://github.com/user-attachments/assets/c2cb816e-06f3-47b5-9b22-11c332a0dfc2" />

<img width="1920" height="1128" alt="GearboxScreenshot (18)" src="https://github.com/user-attachments/assets/733140ef-7271-41fe-9f70-4de6ec9844a9" />

<img width="1920" height="1128" alt="GearboxScreenshot (19)" src="https://github.com/user-attachments/assets/3d5b02b9-ff70-4452-b58c-a7b9ffa95db7" />

<img width="1920" height="1128" alt="GearboxScreenshot (27)" src="https://github.com/user-attachments/assets/0fbad402-a1dd-45d1-adab-e868a13f7397" />


* I made the distance from one gear to the center be half of the added pitch diameters.

<img width="1920" height="1128" alt="GearboxScreenshot (20)" src="https://github.com/user-attachments/assets/514ff056-0c63-4936-a3f3-55a9a6aa0298" />

* Adjusted diameters for the journal bearings.

<img width="1920" height="1128" alt="GearboxScreenshot (21)" src="https://github.com/user-attachments/assets/a428efd0-e4e3-44ab-8034-5e505f261a8e" />

<img width="1920" height="1128" alt="GearboxScreenshot (22)" src="https://github.com/user-attachments/assets/c5418bac-973e-401f-a7da-38b467ce6b93" />

<img width="1920" height="1128" alt="GearboxScreenshot (23)" src="https://github.com/user-attachments/assets/4e513946-088e-469b-aa10-367b74acff2e" />

I then created two rectangles on the bottom to fit into a base using LC2 clearances for Locational Clearance Fits, since LC Fits are meant for parts that are normally stationary but can be freely assembled or disassembled. I extruded the rectangles to be an arbitrary 0.25 inches which would be the thickness of the base. 

<img width="1920" height="1128" alt="GearboxScreenshot (24)" src="https://github.com/user-attachments/assets/d250f6c1-ff91-4cef-acf4-b50ab645d2b0" />

<img width="1920" height="1128" alt="GearboxScreenshot (25)" src="https://github.com/user-attachments/assets/01e56b5c-fe35-462b-abb1-bd5c2322fba8" />

<img width="1920" height="1128" alt="GearboxScreenshot (26)" src="https://github.com/user-attachments/assets/35afa917-c51a-4d95-b6c9-0835be05d5a1" />


For the base of the gear box, I created another arbitrarily sized rectangle, which was again two by three inches and 0.25 inches thick. 

<img width="1920" height="1128" alt="GearboxScreenshot (30)" src="https://github.com/user-attachments/assets/066385b5-a795-453a-a820-83adfe253c7d" />

<img width="1920" height="1128" alt="GearboxScreenshot (31)" src="https://github.com/user-attachments/assets/b0e50932-614f-432d-9c56-9b2914b98db1" />

I cut in the complimentary LC2 Rectangular holes with the proper clearances. 

<img width="1920" height="1128" alt="GearboxScreenshot (33)" src="https://github.com/user-attachments/assets/a204141f-7ed7-4f87-95dd-20a156a2c70a" />

<img width="1920" height="1128" alt="GearboxScreenshot (34)" src="https://github.com/user-attachments/assets/33e8a254-e43c-4f07-b6d9-0d1068562c1e" />

<img width="1920" height="1128" alt="GearboxScreenshot (35)" src="https://github.com/user-attachments/assets/6fbf6b15-19c4-46fe-96d9-bc24cca50826" />

With all the pieces modeled, I could put it together in an assembly.

### Gearbox assembly

For the assembly of the gearbox, I needed to download the bearings and gears from the McMaster website.
I needed the pinion gear, the large gear, the bearing for the pinion shaft and the bearing for the gear shaft. 

<table>
  <tr>
    <img width="300" alt="GearboxScreenshot (65)" src="https://github.com/user-attachments/assets/8aac760c-b1e8-4629-805c-aa47c5649881" /></td>
    <img width="300" alt="GearboxScreenshot (66)" src="https://github.com/user-attachments/assets/c5515eb1-cf4c-484f-8e59-fb9d9b694704" /></td>
  </tr>
  <tr>
    <img width="300" alt="GearboxScreenshot (68)" src="https://github.com/user-attachments/assets/b2cd33e9-926e-4e18-aaae-e9c4c1caf1ca" /></td>
    <img width="300" alt="GearboxScreenshot (67)" src="https://github.com/user-attachments/assets/a32071a4-5e53-4e84-9f79-4ec9bb5a9c2d" /></td>
  </tr>
</table>


I could then add in the different parts and create the final product.

* Putting the base and wall together.

<img width="1920" height="1128" alt="GearboxScreenshot (36)" src="https://github.com/user-attachments/assets/29d170c5-bf68-4d9d-93b4-b92133ad63c9" />

<img width="1920" height="1128" alt="GearboxScreenshot (37)" src="https://github.com/user-attachments/assets/e62782fd-7274-48d4-bbdc-5a7b3de3f546" />

<img width="1920" height="1128" alt="GearboxScreenshot (38)" src="https://github.com/user-attachments/assets/7a5dbe3c-1408-4ce9-8164-5d2e75a3ae28" />

* Adding in the bearings

<img width="1920" height="1128" alt="GearboxScreenshot (39)" src="https://github.com/user-attachments/assets/87601f0c-25b7-48e0-8b3e-260fae355f5b" />

<img width="1920" height="1128" alt="GearboxScreenshot (40)" src="https://github.com/user-attachments/assets/75fc8da3-a1f6-4327-9899-234d5db1bbec" />

<img width="1920" height="1128" alt="GearboxScreenshot (42)" src="https://github.com/user-attachments/assets/4a87b729-2861-479c-92af-fac157d79f06" />

<img width="1920" height="1128" alt="GearboxScreenshot (43)" src="https://github.com/user-attachments/assets/bb339997-45e7-4b0e-993f-17d8fbf4e1c9" />

<img width="1920" height="1128" alt="GearboxScreenshot (44)" src="https://github.com/user-attachments/assets/f3e530e1-2591-4a16-884b-745c94e59c80" />

* Adding in the shafts

<img width="1920" height="1128" alt="GearboxScreenshot (45)" src="https://github.com/user-attachments/assets/c98dd354-10bd-4070-9fb6-836e830863b3" />

<img width="1920" height="1128" alt="GearboxScreenshot (46)" src="https://github.com/user-attachments/assets/63ebbaf8-a3be-4328-bfc9-33b277021f3c" />

<img width="1920" height="1128" alt="GearboxScreenshot (47)" src="https://github.com/user-attachments/assets/dd98234a-3aeb-4906-9fee-ba0d73b1bb9d" />

<img width="1920" height="1128" alt="GearboxScreenshot (49)" src="https://github.com/user-attachments/assets/d0771cdf-005a-4ded-bb70-59ab9659c293" />

* Adding in the Gears

<img width="1920" height="1128" alt="GearboxScreenshot (51)" src="https://github.com/user-attachments/assets/d5c3eb28-c560-4fee-88c6-6810b29cf087" />

<img width="1920" height="1128" alt="GearboxScreenshot (52)" src="https://github.com/user-attachments/assets/1fa72706-b7c0-4f2d-8b99-e966e79e4b9d" />

<img width="1920" height="1128" alt="GearboxScreenshot (54)" src="https://github.com/user-attachments/assets/3292c41b-b55b-4558-83f2-68b2727b828f" />


Putting together the gearbox made me realized that I had used the wrong distances between the gears. I used the full pitch diameter pitch diameter when I should've used the radius. This could be easily fixed by updating the equations. 

<img width="1920" height="1128" alt="GearboxScreenshot (55)" src="https://github.com/user-attachments/assets/095a8f72-d5e5-45ad-bbf1-b08d5af8bd35" />

<img width="1920" height="1128" alt="GearboxScreenshot (56)" src="https://github.com/user-attachments/assets/018f4994-11ad-46fd-bc33-9842b11bb0a1" />

<img width="1920" height="1128" alt="GearboxScreenshot (57)" src="https://github.com/user-attachments/assets/5dadd1cf-3084-4473-93b8-9330b495488a" />

<img width="1920" height="1128" alt="GearboxScreenshot (58)" src="https://github.com/user-attachments/assets/2ad60085-1469-4506-b047-0090da161af7" />

<img width="1920" height="1128" alt="GearboxScreenshot (59)" src="https://github.com/user-attachments/assets/ae5fe777-2eca-4b18-adcb-8b38f6b896f7" />

<img width="1920" height="1128" alt="GearboxScreenshot (60)" src="https://github.com/user-attachments/assets/dffaa6d2-5ad0-49df-95db-bd9c712b1452" />

* I had to adjust the gears slightly to be in line because they were different thicknesses

<img width="1920" height="1128" alt="GearboxScreenshot (61)" src="https://github.com/user-attachments/assets/2a9ced13-aacb-4fd3-b927-b2504836f0ea" />

<img width="1920" height="1128" alt="GearboxScreenshot (62)" src="https://github.com/user-attachments/assets/86f04288-3a2c-4e56-9855-57eb99537316" />

<img width="1920" height="1128" alt="GearboxScreenshot (63)" src="https://github.com/user-attachments/assets/8893cc42-a165-482e-9447-333a2178acb6" />

<img width="1920" height="1128" alt="GearboxScreenshot (64)" src="https://github.com/user-attachments/assets/9ef83797-0808-48c2-961e-46ffd6b25b41" />

However, I realized I should have probably made another wall to hold the other side of the axles. Instead of building a new gearbox, I modified the base to be able to support two of the wall segments so that I could reuse the wall with the fits in place. 

* I measured the larger gear to determine the width I would need between the walls

<img width="960" height="564" alt="GearboxScreenshot (70)" src="https://github.com/user-attachments/assets/29ece067-5eb1-4978-af3b-e2c0be782758" />

* I then added a new equation to the global variables to control the width of the base. I gave the gears a spacing of .02 inches from each wall.

<img width="593" height="551" alt="GearboxScreenshot (81)" src="https://github.com/user-attachments/assets/37111c0d-2073-4a74-a2fa-98bf09fb7094" />

<img width="960" height="564" alt="GearboxScreenshot (73)" src="https://github.com/user-attachments/assets/ee97a53a-3f47-48bc-b1c7-b06648dd24a9" />

<img width="960" height="564" alt="GearboxScreenshot (74)" src="https://github.com/user-attachments/assets/bd648cfc-a074-429b-9d4f-38803a793377" />

<img width="960" height="564" alt="GearboxScreenshot (75)" src="https://github.com/user-attachments/assets/1f9591fd-0e02-4f1f-8d47-46397894448b" />

<img width="960" height="564" alt="GearboxScreenshot (82)" src="https://github.com/user-attachments/assets/1d01c68b-21c5-4281-9cfa-bf3b8b618c98" />

<img width="960" height="564" alt="GearboxScreenshot (83)" src="https://github.com/user-attachments/assets/fa6a2419-8f51-4a0f-8a4f-bafe9d05e76e" />


* I could then reuse my wall segment and add another one on the opposite sides of the gear

<img width="960" height="564" alt="GearboxScreenshot (84)" src="https://github.com/user-attachments/assets/c2782f6d-3771-43fb-a415-ed3ceacfce6c" />

<img width="960" height="564" alt="GearboxScreenshot (86)" src="https://github.com/user-attachments/assets/dafb1f5c-2aba-4636-b0b8-547beba80dc7" />

<img width="960" height="564" alt="GearboxScreenshot (87)" src="https://github.com/user-attachments/assets/fb353a35-1bc2-4177-b875-7d01a743610f" />

* The gears with the 0.02 inch spacing between the walls

<img width="960" height="564" alt="GearboxScreenshot (88)" src="https://github.com/user-attachments/assets/9bbb79ff-d531-42f1-8118-baa064558f7f" />

<img width="960" height="564" alt="GearboxScreenshot (89)" src="https://github.com/user-attachments/assets/a31dd7bd-7fd2-45b6-b20d-f99adde0211c" />

<img width="960" height="564" alt="GearboxScreenshot (90)" src="https://github.com/user-attachments/assets/180d0748-9a29-493e-9522-63313bbeeea7" />

This makes the gearbox Three individual parts but it has only two unique parts, not including the gears and bearings. 

With this design, the shafts aren't fully support. The distances from the outsides of the wall is greater than an inch, but at least the shafts aren't floating. And it is still able to be assembled and disassembled easily. 


### CAD Drawings

**Gearbox Drawing**

<iframe src="GearBox.pdf" width="100%" height="800px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="GearBox.pdf">Download the PDF</a>.</p>
</iframe>

**Gearbox Base Drawing**

<iframe src="GearBoxBase2.pdf" width="100%" height="800px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="GearBoxBase2.pdf">Download the PDF</a>.</p>
</iframe>

**Input Shaft Drawing**

<iframe src="shaft-1.pdf" width="100%" height="800px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="shaft-1.pdf">Download the PDF</a>.</p>
</iframe>

**Output Shaft Drawing**

<iframe src="shaft-output.pdf" width="100%" height="800px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="shaft-output.pdf">Download the PDF</a>.</p>
</iframe>

**Pinion Journal Bearing Drawing**

<iframe src="pinion_journal_bearing.pdf" width="100%" height="800px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="pinion_journal_bearing">Download the PDF</a>.</p>
</iframe>

**Gear Journal Bearing Drawing**

<iframe src="gear_journal_bearing.pdf" width="100%" height="800px" type="application/pdf">
  <p>Your browser does not support PDFs. <a href="gear_journal_bearing.pdf">Download the PDF</a>.</p>
</iframe>

## Lessons Learned

This assignment taught me a lot about applying gear equations and determining safe limits for various real parts. Needing to determine the minimum safe limit for the bearings and then needing to search and find bearings that fulfilled that minimum requirement was a good exericse in website searching and checking the specifications of different parts. Determining tangential forces and PV values was all entirely new to me. This assignment also continued to test and improve my ability to create assemblies and drawings in Solidworks. 

**Time Spent:** 9 Hours

### CAD File Downloads

[GearBox](GearBox.SLDPRT)

[Gearbox Base](GearBoxBase.SLDPRT)

[Input Shaft](shaft-1.SLDPRT)

[Output Shaft](shaft-output.SLDPRT)

[Gearbox Assembly](GearboxAssembly.SLDASM)


## Resources

**CAD Files:**

[Pinion Gear](https://www.mcmaster.com/7880K19/)

[Metal Gear](https://www.mcmaster.com/7880K24/)

[Metal Gear Journal Bearing]()

[Pinion Gear Journal Bearing](https://www.mcmaster.com/9368T97/)

-----------------------------------

Machinery's Handbook 32nd Edition


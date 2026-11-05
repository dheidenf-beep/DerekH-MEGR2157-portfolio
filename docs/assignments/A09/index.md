# A9 – Pulleys

## Objective

The objective of this assignment was to design and mathematically solve a pulley system. The system is pictured below.

<img width="511" height="204" alt="ProblemFigure" src="https://github.com/user-attachments/assets/59632656-0e91-4076-8f70-4ae800e850fc" />


## Pulley System Analysis

The assignment required the algebraic and numeric solving for the belt, pulleys, and shafts. 

### Pulley System Dimensions

Certain dimensions were able to be chosen. 

The distance between the centers of the pulleys was to be between 4 and 6 inches. I chose 5 inches.

The rotational speed was between 1000 and 2000 rpm. I chose 1500 rpm. 

The static belt tension was between 4 and 6 lbf. I chose 4 lbf.

A safety factor of 3 was required for the system.

The material of the belt was polyurethane and the material of the pulleys and shafts was 1060 hardened steel. 

For the polyurethane belt, the yield strength was 471 psi at 20% strain. 

The numbers of the 1060 hardened steel were sourced online. The yield strength was 400 - 620 Mpa or 58 to 79 * 10^3 psi. The shear strength was 370 to 450 MPa or 54 to 65 * 10^3 psi.

For all the material numbers, I used the smallest of the range for maximum safety. 

<img width="1143" height="1151" alt="A09-PulleyWork_Belt-1" src="https://github.com/user-attachments/assets/e979a08b-3baa-4e96-9c01-bce820eb95dc" />


### Belt Analysis

The belt was the first piece to be analyzed. 

#### FBD

I started with a static free body diagram of the belt on the pulley. I used this static state, the power equation, and the angle of wrap to determine the two forces on each side of the pulley. 

<img width="1141" height="931" alt="A09-PulleyWork_Belt-2" src="https://github.com/user-attachments/assets/6da03e79-17d8-4078-8305-cdcfe6358207" />


#### Symbolic Solving

<img width="1100" height="318" alt="A09-PulleyWork_Belt-3" src="https://github.com/user-attachments/assets/6e49c080-73f9-4b90-b1bc-2b2a700e3404" />

<img width="1275" height="1556" alt="A09-PulleyWork_page-0003" src="https://github.com/user-attachments/assets/92733348-c233-4513-9e04-580df6bba4e5" />

I ended up with three equations but only two unknowns (F1 and F2), meaning I only needed the static equilibrium equation and angle of wrap equation to solve for the forces. 


#### Numeric Solving

<img width="1275" height="1594" alt="A09-PulleyWork_page-0004" src="https://github.com/user-attachments/assets/bd0f5f64-c74f-4d11-95d0-5f85ced25114" />

Plugging in the numbers I knew, I calculated F2 to be 0.3314 lbf and F1 to be 7.6686 lbf which add up to the total 2F force of 8 lbf. 


#### Belt Circumferance

For the belt circumference, I used the stress equation to find the area and subsequently the diameter of the belt. I used F1 for all calculations because it is the largest individual force. 

<img width="1275" height="1554" alt="A09-PulleyWork_page-0005" src="https://github.com/user-attachments/assets/7cb620e4-e1fa-4c1c-929c-cea866b96b21" />

<img width="1275" height="1640" alt="A09-PulleyWork_page-0006" src="https://github.com/user-attachments/assets/c8057774-4162-4a32-9d6d-75d6a5d61e6a" />

<img width="1275" height="1445" alt="A09-PulleyWork_page-0007" src="https://github.com/user-attachments/assets/93663d35-f2ce-4580-9261-4baf5f9d534b" />

For the belt diameter, I got approximately 1/4 of an inch and for the total belt circumference, I calculated approximately 26 and 3/4 inches. 


#### Belt Choice

Using the dimensions I calculted, I went onto the McMaster website to find a polyurethane belt with the appropriate circumference and diameter. After a bit of searching, I found the following belt. 

<img width="1920" height="1032" alt="BeltChoice" src="https://github.com/user-attachments/assets/8e9d00ab-b34c-462d-9a89-44db0be03d15" />

[Belt Choice](https://www.mcmaster.com/3044K706-1835T411/)

This belt was the closest I could find to the needed dimensions and was pretty spot on. 


### Shaft Analysis

The next part of the pulley system to analyze was the shafts attached to the pulleys.


#### FBD

The free body diagram was very simple because only two opposing torques on the pulley from the shaft and belt. 

<img width="1275" height="444" alt="A09-PulleyWork_Shaft-1" src="https://github.com/user-attachments/assets/c3e775e9-6cd3-4c72-bb8b-7f589a16c485" />


#### Symbolic Solving

To symbolically solve for the diameter of the shafts, I used the same equations from the first part, that being the power equation and the max shear stress equation to remove the torque from the equations and get only terms I had. 

<img width="1275" height="1176" alt="A09-PulleyWork_Shaft-2" src="https://github.com/user-attachments/assets/76c98310-0818-4960-a740-0b3ad3f32a81" />

<img width="1275" height="528" alt="A09-PulleyWork_Shaft-3" src="https://github.com/user-attachments/assets/dd8fcb02-f995-46c9-8365-0e678ffc31af" />

This gave me an equation for the shaft diameter.


#### Numeric Solving

The numeric solving was very straightforward because most of the terms cancelled. I just needed to bring in the shear stress of the 1060 hardened steel.

<img width="1275" height="925" alt="A09-PulleyWork_Shaft-4" src="https://github.com/user-attachments/assets/4a47c904-11d4-4479-8752-7507d7951c90" />

<img width="1275" height="1549" alt="A09-PulleyWork_page-0010" src="https://github.com/user-attachments/assets/6bdb5efb-d5ac-4880-955a-cde228fa75ac" />

The final shaft diameter was 0.032 inches, giving a cross sectional area of 0.025 inches^2.


### Journal Bearing Analysis

The final component to analyze were the journal bearings. The journal bearings turned out to be the trickiest due to the required projected force. 


#### FBD

The free body diagrams of the bearings were confusing. The one on the left confirmed that the torque was conserved from the shaft to the bearing. The free body diagram on the right was trying to figure out how to get the projected force, Fj. 

<img width="1275" height="612" alt="A09-PulleyWork_JournalBearings-1" src="https://github.com/user-attachments/assets/19177cc6-0762-4d32-b7e2-5f759311e908" />


#### Symbolic Solving

The symbolic solution was a bit messy, and I had to redo it a couple times before I found something reasonable for the projected force. 

<img width="1275" height="1029" alt="A09-PulleyWork_JournalBearings-2" src="https://github.com/user-attachments/assets/1be9f31b-42f1-4d99-96b0-10c8112524ce" />

The variables I solved for were the projected area and the projected force on the shaft.


#### Numeric Solving

The numeric solving was fairly simple. The journal bearing calculations introduced a new variable l or the length of the bearings which was needed to solve for the area. I chose a length of 0.5 inches for the journal bearings.

<img width="1275" height="1220" alt="A09-PulleyWork_JournalBearings-3" src="https://github.com/user-attachments/assets/474bbb38-2a65-4141-b2a1-c3d472dc3093" />

<img width="1275" height="850" alt="A09-PulleyWork_JournalBearings-4" src="https://github.com/user-attachments/assets/afa55844-c90b-4436-8e15-1a87eb74b78d" />

After some trial and error with the velocity calculations, I calculated a PV value of 4898.44 psi-ft/s. Using the material from the Machinery's Handbook, I chose graphite (dry) to be the material of the bearings. Most materials would have been sufficient but I settled on graphite. 

<img width="985" height="662" alt="MachinerysHandbook-JournalBearingMatTable" src="https://github.com/user-attachments/assets/275018be-de6a-42a0-8c00-253306926420" />


#### Bearing Selection

Using graphite as my material for the journal bearings, I once again went to the McMaster website to select a bearing for the pulley system. The dimensions of the bearing needed to be an inner diameter of 0.032 inches for the shafts and a length of 0.5 inches. 

However, there were no bearings with an inner diameter of 0.032 inches, so I went with the smallest diameter which was 0.126 inches. There was also not a bearing 0.5 inches ling so I switched to a 0.25 inch thick bearing. 

<img width="1920" height="1032" alt="BearingChoice" src="https://github.com/user-attachments/assets/07869156-45ea-42eb-8476-eed99b9d1c4b" />

[Journal Bearing Choice](https://www.mcmaster.com/9368T96/)

This was the bearing I chose. It had a PV value of 40,000 psi-ft/s which was way over what was necessary (4898.44 psi-ft/s calculated). However, it was still a big deviation from the original calculated measurements which would require those to be redone with the new much larger shaft diameter.


### Pulley Frame

For the pulley frame, I went very simply. I focused on calculating the minimum area that would be necessary to support the greatest force of 8 lbf without breaking the mount. To do this, I solved for the minimum area using 1060 hardened steel for the material and solving for the single shear force between the journal bearing hole and the edge of the frame. 

<img width="1275" height="1531" alt="A09-PulleyWork_page-0014" src="https://github.com/user-attachments/assets/2b3345f4-fd5e-435e-bef1-7ecf3285ec7c" />

<img width="1275" height="634" alt="A09-PulleyWork_PulleyFrame-1" src="https://github.com/user-attachments/assets/3411f6b0-19e7-4d79-919a-e072238828a3" />

<img width="1275" height="716" alt="A09-PulleyWork_JournalBearings-2" src="https://github.com/user-attachments/assets/1b79c6e8-561c-4dd0-8a99-722741e55f3d" />

This gave me a very small minimum area of 4.44 * 10^-4 in^2. This meant that pretty much whatever dimensions I chose would be sufficient. I used the journal bearing length of 0.25 inches and a width of 0.1 inches for the dimensions around the hole. I then drew a basic picture and dimentioned it using the values I had calculated or were required to use such as the bearing length. 


## Lessons Learned

This assignment was a very interesting one. It combined a lot of theory together to be able to make things work, which I enjoyed. I learned about angle of wrap and how the angle of the warpped belt or could increases the force by an exponential degree. I also learned to think more about dynamic forces on pulleys. When the pulley is static, the forces point in the same direction but while the pulley is moving, form a static point of view, the forces are acting in opposite directions. But if you think about how the belt is actually moving, it makes sense that the forces are opposite since the belt is moving around the pulley. 

**Time Spent:** 5 hours


### Resources

Machinery's Handbook 32nd Edition

[McMaster-Carr](https://www.mcmaster.com/)

[SAE-AISI 1060 (S58C, G10600) Carbon Steel](https://www.makeitfrom.com/material-properties/SAE-AISI-1060-S58C-G10600-Carbon-Steel)

[FERROBEND AISI 1060](https://www.sheetsplates.com/carbon-steel/aisi-1060/)

[The Ultimate Guide to 1060 Carbon Steel: Properties, Applications, Heat Treatment & Buying Tips](https://www.huaxiaometal.com/blogs/the-ultimate-guide-to-1060-carbon-steel.html)

[AISI 1060 Carbon Steel (UNS G10600)](https://www.azom.com/article.aspx?ArticleID=6542)

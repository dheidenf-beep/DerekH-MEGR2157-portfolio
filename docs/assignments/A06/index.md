# A6 – Bracket Drawing

## Objective

The objective of the 6th assignment was to create a parametric CAD model of the bracket and linkage designed in the previous assignment to hold a certain force using a specific cable and create an engineering drawing based on that CAD model.

![Problem Prompt](A05-visual-problem.png)


## Parametric Design

### Bracket Model

For the bracket in the previous assignment, I had chosen the material to be Titanium (Ti-6Al-4V). For the calculations of the dimensions for the bracket, I had used the numbers listed in Solidworks. That meant that all of the material property numbers were already there.

![Titanium Material](TitaniumSolidworks.png)

After that, I put it every number, equation, and parameter I could in to the "equations" tab. 

![Bracket Equations](BracketEquations.png)

This meant every single measurement and parameter were now in a single place and easy to manage. Inputting the equations also corrected any math errors that I didn't catch before. I incorrectly calculated the height of the lower rectangle in the bracket as 0.370 inches while Solidworks calculated it to be 0.2376 inches. Having all of the equations and measurements in place made it much easier to edit a dimension if I made an error since I wouldn't have to manually redo the equations each time. I included Several of the linkage dimensions because I made the supporting beam for the cylinder dependent on the values from the linkage. At some point, I made a mistake of making the diameter of the linkage 1.005 inches instead of 1 inch.  But since I had all my equations in place, all I had to do was change the dimension to 1 inch and everything fixed itself for me. The only dimension I still wasn't sure about was the thickness of the middle section. On the finished design, the middle supports are very thin, but no matter how many times I ran the math either by hand or in Solidworks, I ended up with the same thin width. The use of parametric dimensions was incredibly helpful throughout the modeling process.

For the bracket, I chose the dimensions of stress for every equation because the stress values ended up higher than the deformation values. 

To start, I first modeled the top of the bracket, utilizing symmetry where I could. 

![Bracket Image 1](BracketImg1.png)

![Bracket Image 2](BracketImg2.png)

![Bracket Image 3](BracketImg3.png)

![Bracket Image 4](BracketImg4.png)

![Bracket Image 5](BracketImg5.png)

![Bracket Image 6](BracketImg6.png)

With the dimensions already determined, it saved a lot of time since I didn't have to enter in every number as I was creating the model.

I then made the supporting beam attached to the back of the main bracket body and added the cylinder onto it. The supporting beam had its width as the diameter of the cylinder.


![Bracket Image 7](BracketImg7.png)

![Bracket Image 8](BracketImg8.png)

Here is where I used the linkage radius to determine the height of the supporting beam.

![Bracket Image 9](BracketImg9.png)

![Bracket Image 10](BracketImg10.png)

![Bracket Image 11](BracketImg11.png)

Since the diameter of the cylinder was the width of the supporting beam, I could make the cylinder cotangent with the edges of the supporting beam and I wouldn't then have to worry about the diameter of the cylinder.

![Bracket Image 12](BracketImg12.png)

![Bracket Image 13](BracketImg13.png)

![Bracket Image 14](BracketImg14.png)

![Bracket Image 15](BracketImg15.png)

I had to create some weird sketches to curve the bottom of the supporting beam.

![Bracket Image 16](BracketImg16.png)

![Bracket Image 17](BracketImg17.png)

![Bracket Image 18](BracketImg18.png)

![Bracket Image 19](BracketImg19.png)

I did add the tolerances to the CAD model. However, the tolerances didn't do much since I would need to add them back onto the drawing.

![Bracket Image 20](BracketImg20.png)

Once everything was properly dimensioned, I was finished with the bracket CAD model.


### Linkage Model

The linkage model was much the same as the bracket model. I started by putting every number and equation I could think of into the "equations" tab in Solidworks.

![Linkage Equations](LinkageEquations.png)

Many of the equations I had already created in the bracket model to use for the supporting beam, so I was mostly just copy and pasting.

I then started the design and laid out the 2D sketch of the model.

![Linkage Image 1](LinkageImg1.png)

![Linkage Image 2](LinkageImg2.png)

![Linkage Image 3](LinkageImg3.png)

![Linkage Image 3-5](LinkageImg3-5.png)

![Linkage Image 4](LinkageImg4.png)

At this point, I realized I had made an error in my original calculations. I made the height of the linkage 3 times the radius of the larger 1 inch hole. However, this turned out to be too little space requiring me to increase the total height of the linkage.

![Linkage Image 5](LinkageImg5.png)

![Linkage Image 6](LinkageImg6.png)

I instead dimensioned the centers of the two holes, which were in line with the arcs on the ends of the linkage, and made the distance between the centers the radius of the 1 inch hole plus the diameter of the 1 inch hole to get a spacing of 1.5 inches instead of dimensioning the height. I did it this way to keep every dimension equation driven.

Once I had the distance sorted out, I extruded the sketch.

![Linkage Image 7](LinkageImg7.png)

![Linkage Image 8](LinkageImg8.png)

With that, the linkage model was finished. It was nice having relative dimensions with the bracket. The diameter of both holes were calculated in both the bracket and linkage model since they're used for both and the height of the linkage and the supporting beam are connected through their dimensions.


## Engineering Drawings

### Bracket Drawing

Creating the bracket drawing was fairly straight forward. The trickiest part was ensuring that the drawing was dimensioned enough but not too much and trying to account for the space in for that.

![Bracket Drawing](A05-bracket-drawing.jpg)

[Bracket Drawing PDF](A05-bracket-drawing.pdf)

Since the bracket was created over three sliding fits, the inside dimensions of the bracket all needed sliding fit tolerances. I included the third angle projection symbol but could not figure out how to properly incorporate it into the pre-generated table Solidworks makes, so it's kind of just floating there which doesn't look very professional. For the generic tolerances, I left them fairly strict at 0.05 and 0.005 inches. For the bracket, I could've been much more lenient considering the inside tolerances are the ones that really matter. And the tolerance on the shaft coinciding with the hole for the link. The multiple views of the drawing needed to be scaled down to a 1:2 scale but the isometric view is in 1:1 scale. Overall, the drawing conveys the necessary information and I tried to keep it as neat as I could despite how much there was to dimension. 


### Linkage Drawing

Creating the linkage drawing was mostly the same as the bracket drawing. There was much less to dimension, making the drawing look cleaner by comparison. 

![Linkage Drawing](A05-Linkage-drawing.jpg)

[Linkage Drawing PDF](A05-Linkage-drawing.pdf)

The Linkage had two sliding fits for both of the holes for the two shafts. These tolerances directly coincidence with the tolerances for the shafts, at least the shaft on the bracket. I also included the third angle projection symbol here but it I didn't make it look any better. For the generic tolerances, I was much more lenient. There is enough space between the cylinder and the bottom of the bracket to support fairly large changes. The bracket really didn't need to be that precise except for the holes. Since the linkage is much smaller than the bracket, the images fit in 1:1 scale and I didn't have to change any parameters there. Overall, the drawing conveys the necessary information and I tried to learn from the bracket drawing as to what I can improve. The drawing looks less cluttered but that is likely because there is much less that needs to be dimensioned. 


## Lessons Learned

* **Identify the analytical equation (stiffness or strength) you used to drive at least one dimension in your parametric model, and name which specific dimension it controlled. Describe how you expressed that equation directly in the CAD software (e.g., as an equation/expression tied to the parameter) rather than typing in a value you calculated by hand elsewhere. If your calculation changed later in the assignment, describe exactly what happened to that dimension and whether the rest of the model responded on its own or required manual rework.**

Stress drove every equation and parameter. Every calculation I performed had a higher stress value. All of the height values in the bracket components (the three rectangles) were all stress driven. The thickness of the supporting beam was also stress driven. Stress was the primary component driven every equation I had. I wrote all of the equations directly into Solidworks because I figured it would catch any errors and made (which it did) and it made it so every time I wanted to iterate a single dimension, I didn't have to recalculate every other dimension by hand. Whenever I modified a length or base dimension, the height of each component would automatically be solved for, which allowed me to test dimensions at a very quick pace.


* **Pick one dimension on your drawing where you applied a tighter tolerance class (e.g., X.XXX ± .005) and one where you applied a looser class (e.g., X.X ± .02). For each, identify whether that feature is a mating/functional surface (like a sliding fit interface) or a non-critical feature, and explain why that functional role justified the tolerance class you chose. If you applied the tightest tolerance across your drawing by default, describe what happens to manufacturing cost or feasibility when a non-critical feature is held to an unnecessarily tight tolerance.**

The sliding fits on the bracket cylinder and holes on the linkage as well as the sliding fits on the bracket were very tight tolerances, to 0.0005 inches. This was necessary to allow the bracket to be able to slide on and off while also keeping a fairly good connection. There weren't many places I used less strict tolerances. On the bracket especially, I could've used a looser tolerance like X.X = +- 0.2 inches or something similar. Since I kept the tolerances tighter, that would make machining the part and producing it much more difficult and expensive due to the needed precision on each part of the bracket.


* **Describe lessons learned about ensuring part-to-part compatibility through tolerancing.**

The tolerance on the sliding fits taught me the most about part-to-part compatibility since the shaft and hole have different tolerances needed to be able to fit together. The tolerances on shafts and holes for sliding fits cannot be larger than the maximum size. For example, the diameter of the cylinder on the bracket is about 0.337 inches. The tolerances for the shaft can be slight under 0.337 inches but cannot be over. It is the same for the hole as well. This fact made it more clear the connection of parts through tolerance.


* **Reflect on how dimensioning and tolerancing communicates design intent and functional requirements in your design.**

Dimensioning and tolerancing communicates design intent by describing what should be created and to what level of detail, acting as guidelines and rules. Looser tolerances correlates to a cheaper, less precise, or less important level of detail while high tolerances are for parts that need high detail, accuracy, or are meant to fit together tightly. Dimensioning and tolerancing also describe the functional requirements of a part by displaying what the part needs to be able to fit with and how tightly or precisely. Something that has very tight tolerances is likely going to end up closer to a precision instrument or something complicated like a small electrical circuit while something with loose tolerances is more likely something independent that has more degrees of freedom and isn't constrained to a precise box.

[Bracket Solidworks CAD Download](A05-bracket.SLDPRT)

[Linkage Solidworks CAD Download](A05-Linkage.SLDPRT)


**Time Spent:** 5 Hours

## Resources

Machinery's Handbook 32nd Edition

[Uline Heavy Duty Polyester Cord Strapping](https://www.uline.com/Product/Detail/S-12925/Poly-Cord-Strapping/Heavy-Duty-Polyester-Cord-Strapping-3-4-x-2500?pricode=WA9239&gadtype=pla&id=S-12925)

Solidworks Material Selection

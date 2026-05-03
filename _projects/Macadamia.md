---
layout: project
title: Macadamia Nutcracker Project
description: Tool Design Through Statics Concepts
technologies: [Pen and Paper]
---

1 & 2. Problem statement, objective, and parameters:
- For a statics and mechanics class, we were asked to design a macadinia nutcracker. We needed to find typical values for inputs like nut size and average grip strength and the average load needed to crack a macadamia nut.
- The nutcracker was implied to be a tabletop, because macadamia nuts are incredibly hard to crack and could not be cracked by handheld devices.
- As a given in the design process: the average grip strength is around 300 Newtons (~30kg), the macadamia nut needs 220kg (~2200N) of load to crack, and its size is around 13-20mm.
- We must find a working design that would crack the nut using the inputs and ensure the output force exceeds the one that macadamia nut needs to crack.

3. Approach to the problem
- To achieve a required load of 220kg on the nut, we must use a lever arm mechanism to amplify output force.
- The macadamia nut needs to be put in compression in a secured spot that is around its size.
- Due to the significant size of the lever arm required to go from the grip strength of around 300N to 2200N, the nutcracker should be a tabletop with a large base of easily manufacturable material like wood.
- The initial lever arm design should be long, but reasonable in length for a table. This prompted my use of 20 cm for the lever arm from the handle to the piston driver pin. The orientation of the lever on the picture is made for demonstration of dimensions, the angle between the lever and base should be no greate than 60 degrees. 
- The cracker should employ a piston mechanism because pistons easily slide through a cylinder and would thus only output a force in one direction even if there is resistance to other axis. A cylinder is necessary to ensure stability of the piston given the large forces at play.
- The holders of the nut should be jagged to concetrate forces and prevent sliding of the nut when it is in the process of being cracked.
- The first iteration (lenght of 20cm) was sufficient to supply a high enough force to crack the nut through analysis of reaction forces at joints, as seen on the paper, the output force directed at the nut is 3300 Newtons which exceeds that needed to crack it of 2200N. 

4. 
<img width="458" height="600" alt="Screenshot 2026-03-03 at 22 45 28" src="https://github.com/user-attachments/assets/181e5b58-060e-4450-ad25-fea738f9ff23" />

5. 
- The design is very reasonable in dimensions and outputs significantly higher force than that required to crack a macadonia nut. Given that all parts are made from steel or a harder material, the design will withstand the high forces at play.
- The handle and the actuation mechanism, assumed to be cylindrical with a rubber grip, are assumed to be able to withstand the bending force because of their significant diameter of 2 centimeters. 
- The design is very relatively easy to manufacture because of a lack of complex geometry and relative small number of parts.

6. To incorporate a linear actuator to the system, we can securely attach the linear actuator in the middle of the base, at the far right of the picture and point the actuation mechanism 45 degrees clockwise. We can attack a bike chain to the point of application of force on the lever securely and its other end to the linear actuator's end and a plate to prevent sliding. The chain should be made tight in the resting position to prevent it from sliding off. The actuator extends 8 inches, or around 18 cm, which would adequately adjust for the loosening caused by the lever moving in to the base.

**References:**

The average macadamia nut size is in the range of 13-20mm: https://alohafarmshawaii.com/services/macadamia-nuts/

The average grip strength is around 300 Newtons: https://nonprofitrisk.org/resources/grip-strong-and-prosper/

A bike chain can withstand 8 thousand newtons of tensile force: https://zerofrictioncycling.com.au/wp-content/uploads/2020/01/Converting-Pedalling-Watts-to-Newtons-v6.pdf

Linear actuator https://www.progressiveautomations.com/products/pa-mc2

Part 2


To further enhance the Macadamia nutcracker project with newfound knowledge in of beams and bending in Statics and Mechanics, we are tasked with the following: 


"Initially, the handles were considered in your design to be rigid. Now, assume the
nutcracker handles are no longer rigid. In fact, they are now best described as
beams which bend due to the combined action of the forces from the nut and from the
actuator.
Consider only the components of these forces transverse to your beam:
a) Find the location of maximum elastic deflection in your handles. State your
assumptions clearly and describe your analysis.
b) Choose a “beam” design (cross-section, material) such that the vertical elastic
deflection is below 2% of its length and is the most mass-efficient possible.
c) Present your final design in an image or drawing"

The problem statement limits the bending amount in my beam to 
                        δmax​=0.02×L=0.02×0.2=0.004m     =     4mm

In my situation, the lever arm can be assumed to be a free end with applied force P at its end. Through appendix E of the Statics and Mechanics textbook used, the maximum deflection can be said to occur at the end of the free hanging beam. The magnitude of the maximum deflection is FL^3/(3EI) where F is the force applied, E is young's modulus and I is the moment of inertia. 

We must set the maximum deflection to 4mm, or 0.004m.

We must next optimize the moment of inertia. Previously, a solid circular rod was assumed to be used. However, the moment of inertia is much better if we remove low-stress core material and make a hollow circular tube. 
The tube's inertia would be I=pi/64(D^4-d^4) where D is the larger radius and d the smaller. 
This could be done, though an even better option would be a rectangular hollow section tube, since the problem statement somewhat implies beams must be rectangular. This results in I=bh^3/12-b_i-h_i^3/12 relationship for inertia, where i is an index to differentiate one height from the other. This operation also removes the low stress inner parts of the tube. 

Since there are no material limitations for this project, we can utilize titanium. Titanium is a lightweight material that will be greatly efficient for mass efficiency part of the prompt. Titanium has an elastic modulus of around 110 GPA at 20 degreees celsius.

Given F=300, L=0.2m, E=110GPA, we can solve for I. 

δ=Fb^3/(3EI) becomes
I>=Fb^3/(3Eδ)

​I>=300*0.18^3/(3*(110*10^9*0.004))
I>=1.33*10^-9m^4

Now we use I=bh^3/12-b_i-h_i^3/12 to check for an optimal dimension.

To maintain a handle's ability to be usable, we assume base to be half the height. We must make height as great as possible to make use of the cube relationship in the inertia equation. 

Try: height = 20mm
width = 10mm 
thickness t = 1.5mm

This gives us a result of: 
I = 2.0×10−9 m^4

This is greater than 1.33*10^-9m^4, satisfying the constraint. However, anything less than these dimensions would be uncomfortable to hold and max experience greater metal fatigue due to repeated use. Thus it is best to stick the provided dimensions at the cost of some mass efficiency. This allows us to achieve a factor of safety as well, preventing catastrophic failure and potential injury.


[updated design.pdf](https://github.com/user-attachments/files/27320794/updated.design.pdf)




Titanium elastic modulus: https://www.azom.com/article.aspx?ArticleID=1341






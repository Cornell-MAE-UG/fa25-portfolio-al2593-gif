---
layout: project
title: "Functional Prototype - Team BuzzKill"
description: Spotted lanternfly egg removal mechanical system concept
image: /assets/images/spotted-lanternfly.jpg
hidden: true
---
# Design Documentation
Our part list is as follows:

Table 1: Parts List
<img src="{{ "/assets/images/Table_Part1.jpg" | relative_url }}" alt="System diagram" width="500">
<img src="{{ "/assets/images/Table_Part2.jpg" | relative_url }}" alt="System diagram" width="500">

# Design Intent and Functionality
We used the calculations and design estimates from our proof of concept and the feedback we received 
to refine our design and build our functional prototype.

Our bucket and jaw assembly, made out of lightweight 3D-printed plastic, is designed to hold 100 egg masses. 
For our first prototype, we decided to use PLA because it is cost-effective and the RPL can print it quickly.
We designed the bucket to have an angled opening and curved bottom, so it works at different angles. 
The springs attach to the inside of the bucket and jaw, and the assembly moves with the help of the hinge and string on top.

Figure 1: Bucket and Jaw Side View Closed
<img src="{{ "/assets/images/Figure1.jpg" | relative_url }}" alt="System diagram" width="200">

Figure 2: Bucket and Jaw Side View Open
<img src="{{ "/assets/images/Figure2.jpg" | relative_url }}" alt="System diagram" width="200">

Figure 3: Inside Bucket with Jaw Springs
<img src="{{ "/assets/images/Figure3.jpg" | relative_url }}" alt="System diagram" width="200">

Figure 4: Overall Bucket and Jaw with String Attached
<img src="{{ "/assets/images/Figure4.jpg" | relative_url }}" alt="System diagram" width="200">

After feedback on our mock-up prototype, we designed a 3D-print shoulder stock attachment to the other end of the PVC pipe and attached padding on the end to further reduce user discomfort.

Figure 5: Shoulder Stock Rear View
<img src="{{ "/assets/images/Figure5.jpg" | relative_url }}" alt="System diagram" width="200">

Figure 6: Shoulder Stock Side View
<img src="{{ "/assets/images/Figure6.jpg" | relative_url }}" alt="System diagram" width="200">

The handle-trigger assembly is made up of 2 pieces of 3D-printed plastic. 
The handle is slid onto and screwed in place to the PVC pipe. The string that 
operates the jaw is attached to the trigger, which slides along guide rails on the inside of the handle.

Figure 7: Handle-Trigger Side Profile
<img src="{{ "/assets/images/Figure7.jpg" | relative_url }}" alt="System diagram" width="200">

Figure 8: Handle Back Profile and Trigger Guide Rails
<img src="{{ "/assets/images/Figure8.jpg" | relative_url }}" alt="System diagram" width="200">

Figure 9: Handle-Trigger Assembly
<img src="{{ "/assets/images/Figure9.jpg" | relative_url }}" alt="System diagram" width="200">

This then yields the larger, more surface-level operation of the functional prototype in which a user squeezes the trigger to open the jaw, and then releases to scrap off an egg mass.

Figure 10: Entire CAD Prototype
<img src="{{ "/assets/images/Figure10.jpg" | relative_url }}" alt="System diagram" width="200">

# Assembly Process:
After 3D printing the parts shown above and ordering the rest of the parts from McMaster or sourcing from the Taylor Design Studio, we began the assembly process. Due to larger than expected tolerances of the RPL, we had to sand down the diameter of the PVC pipe in order for it to fit into the slots on our components. We then drilled ¼ in holes in the pipe at the locations needed to bolt the components to the pipe and run string where needed.

First, a through hole was drilled in the back of the pipe and the shoulder stock was bolted on. For consistency, will use red arrows denoting functional/mechanical motion (intended use) and blue arrows for assembly processes.

Figure 11: Shoulder Stock Attached
<img src="{{ "/assets/images/Figure11.jpg" | relative_url }}" alt="System diagram" width="200">

Next, we drilled holes both for the bolt attaching the handle to the pipe and also to run string from the handle to inside the pipe. 

Figure 12: Sliding on Handle
<img src="{{ "/assets/images/Figure12.jpg" | relative_url }}" alt="System diagram" width="200">

Figure 13: Running String Through Handle
<img src="{{ "/assets/images/Figure13.jpg" | relative_url }}" alt="System diagram" width="200">

Figure 14: Trigger and Handle Assembled and Bolted
<img src="{{ "/assets/images/Figure14.jpg" | relative_url }}" alt="System diagram" width="200">

Following this, we drilled a hole to bolt the bucket-jaw assembly to the pipe, as well as a hole before thai attachment at the top of the pipe to allow the string to exit the inside of the pipe and move towards its guide ramp on the bucket for actuation.

Figure 15: Inserting Pipe to Bucket
<img src="{{ "/assets/images/Figure15.jpg" | relative_url }}" alt="System diagram" width="200">

Figure 16: Attached Bucket-Jaw Assembly
<img src="{{ "/assets/images/Figure16.jpg" | relative_url }}" alt="System diagram" width="200">

The subassemblies include the handle-trigger and bucket-jaw assemblies. The handle-trigger assembly can be seen through the images above, as the trigger simply slides in the handles guide rails while the string ties to it. The bucket-jaw assembly is made using four M6 bolts and the ordered hinge as shown below.

Figure 17: Bucket-Jaw Assembly
<img src="{{ "/assets/images/Figure17.jpg" | relative_url }}" alt="System diagram" width="200">

This concludes the assembly process. Below is an image of the functional prototype as built in the lab.

Figure 18: Final Assembled Prototype in Operating Position
<img src="{{ "/assets/images/Figure18.jpg" | relative_url }}" alt="System diagram" width="200">

# Design Testing
## Test One: 
*Part*: Bucket and Jaw Assembly
*What it is Testing*: Scraping/Hinging Force of the Jaw When Attached to Bucket, Durability
*How to Perform Test*: 
- Using spring scale, measure output force of the jaw mechanism, and using ruler measure opening gap of the jaw due to spring rest length. Then, cycle the actuating system 100 times, and measure the output force and rest length again. Observe any changes in force or rest length. 
*Test Results*: 
Initial: 
- Output force of jaw mechanism when fully open: 12.5N
- Opening gap of jaw due to spring rest length: 1.05 inches
After 100 cycles: 
- Output force of jaw mechanism when fully open: 11.5N
- Opening gap due to jaw due to spring rest length: 1.15 inches
*Conclusion for Next Iteration*: Opening gap increased by 0.1 inch and force decreased by 1N over 100 usage cycles. The springs we used for this prototype are too long and too prone to wear, so we will find shorter and more durable springs for the next prototype.

## Test Two: 
*Part*: Handle/Trigger Assembly
*What it is Testing*: Ergonomics of the handle as well as the force required to squeeze the handle.
*How to Perform Test*: 
- We first took images of a group member using the prototype in three different positions. One where they held the prototype upwards as if scraping egg masses from above, one straight in front, and one downwards. The RULA (Rapid Upper Limb Assessment) was completed. We used CUErgo (1) to guide us through the process of conducting this test, with our client feedback providing information we could use to estimate how long the user would be in each position.
*Test Results*: 
- Low position: scored a 3
- Middle position: scored a 4
- High position: scored a 4
- Total RULA score: 3.9
- Took over 40 pounds of force to squeeze handle when not perfectly aligned
*Conclusion for Next Iteration*: Our goal for this prototype was to get a RULA score below 5, which means that users will be at a low risk of MSD (musculoskeletal disorders) from our device, based on the below graphic from Ergo-Plus (2). See images below for further information. We calculated our prototype to have a total RULA score of 3.9, indicating low risk and achieving our goal of <5. For our next prototype, we aim to keep our score at or below 3.9. The handle and trigger will also be redesigned because the rail system often jams, causing the trigger to be stuck even for large squeezing forces.

Figure 19: RULA Score Meanings (2)
<img src="{{ "/assets/images/Figure19.jpg" | relative_url }}" alt="System diagram" width="200">

Figure 20: RULA Calculations with CU Ergo Template (1)
<img src="{{ "/assets/images/Figure20.jpg" | relative_url }}" alt="System diagram" width="200">



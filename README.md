[![en](https://img.shields.io/badge/Readme-tr-red.svg)](https://github.com/antinucleus/homemade-3000-watt-electric-motorcycle/blob/master/README.tr.md)

# Handmade 3000 Watt Electric Motorcycle

> This document contains a general summary of the 3000-watt electric motor I built in August-September 2024. More detailed information will be added to the document in the future.

<h4 align="center">
  Project Summary Video
</h4>

<div align="center">
  <a href="https://www.youtube.com/watch?v=YHWjSGBKVd8">
    <img src="https://img.youtube.com/vi/YHWjSGBKVd8/0.jpg" width="400" />
  <a/>
</div>


## Introduction

I had previously used both electric and gasoline motorcycles. Due to the high prices of gasoline motorcycles, I started researching electric motorcycles with a power of 3000 watts. The prices of 3000-watt electric motorcycles ranged between $1,500 and $2,500.

Since the prices of electric motorcycles were also high, I wondered if I could build a 3000-watt electric motorcycle myself and made a rough cost estimate. According to my calculations, with the design and craftsmanship being my own, the cost would be around $750. The desire to improve myself and the happiness I feel when my ideas come to fruition motivated me to build the motorcycle. I will generally explain the process under a few headings.

## Desing Phase

In the design phase of the motorcycle, my main focus was on the chassis. I designed this part in its simplest form to carry a specific load and to use readily available materials, adding the remaining components on top of it step by step. Since I concentrated solely on the chassis design, I did not create designs for parts such as the seat, mirrors, headlights, turn signals, or side stand.

After working on the design for about 10 days, I came up with three different models. I designed the first model using box profiles, as I thought it would be easier for welding. However, I didn’t complete it because it wasn’t visually appealing, and I continued with tube profiles for the other designs. Once I finalized the last design, I selected the tube profiles based on the wall thicknesses available in the market and calculated how much load the profiles would bear.

### Mechanical Phase

- Since I designed the frame using tube profiles, I had two options for bending the profiles. The first was to weld the bending points together using "butt weld fittings", and the second was to have the tubes bent by a tube bending specialist according to the design. Since the first option would be laborious, I chose to have the tubes bent in line with the design.

- For the steering column, I selected a tube profile with a greater wall thickness compared to the ones used in the chassis. I needed to secure the handlebar to the steering shaft using a headset assembly. Therefore, I had external threads cut on the steering column to match the desired dimensions and the threads of the headset nut.

- For the rear wheel, I needed a front fork assembly that matched the rim size of the electric motor I selected. Instead of buying this part brand new, I preferred to source it from scrap dealers.

### Electronic Phase

- At this stage, I first researched 3000-watt electric motors (these types of motors are called "Hub Motors") and suitable hub motor controllers for them. I found the hub motor, but since the controllers available in Turkey did not meet the requirements of a 3000-watt hub motor, I ordered the controller from China (before the customs formalities update).

- Since this motor controller could operate in the range of 48 to 72 volts, I configured the system to be powered by 72 volts. For this, I used six 12V - 24Ah batteries. Additionally, for the components that would run on 12V, I opted for a 72V - 12V step-down converter (DC/DC converter).

- For the speed and battery level display, I used an ESP32, a 1.44-inch OLED screen, and a voltage divider circuit to measure the battery level.

- Normally, the motor signals could be controlled analogically with a signal flasher. However, since the signals I used for the motor consumed high wattage and I was already using the ESP32 in the system, I controlled the signals using a relay.

### Software Phase

- I wrote the necessary code to display the battery level using the data from the voltage divider circuit and to control the signals. In addition, to further enhance the system, I plan to add features such as remote control of the motor and       location tracking.


## Motorcycle Construction Phase

After welding the bent tube profiles and completing the chassis in 4 days, I connected the motor controller and batteries and took a test ride at night. It was an exciting ride because basic equipment such as brakes and headlights were missing. I hadn't accounted for this before the ride, but the motor accelerated with much more force than I had expected. The cause of this acceleration could be attributed to factors like the hub motor power, the maximum current the controller could supply, and the chassis being built only as a skeleton. The skeleton completed in four days was only about 20% of the motor. The real work started after this stage. The next phases involved long and exhausting steps, which I will briefly summarize as follows:

- Re-setting the angle of the steering column
- Adding sheet metal to necessary areas
- Fabricating the side stand
- Making the rear brake cable fastening bracket
- Making the seat cushion
- Creating the rear frame attachment points
- Installing the electrical wiring (a very tedious task)
- Adding the turn signals, headlights, taillights, horn, and mirrors
- Installing side support stands
- Making a backrest for the rider
- Creating the rear fender attachment bracket
- Fabricating the battery enclosure
- Cleaning the front discs, replacing the hydraulic hose, and installing brake levers
- Painting


## Mistakes in the Construction Phase

- I had designed the support piece holding the steering column at a 60-degree angle in the horizontal plane. However, when I made it, I mistakenly cut the piece to leave a 45-degree angle instead. Due to the 15-degree difference, the motor became   too long, and when passing over bumps or dips, most of the load was transferred to the part where the steering column was mounted, instead of the front suspension, which was bending the chassis. The position of the steering column was similar to   chopper motorcycles; it was fun to ride but not reliable. So, I cut the piece holding the steering column and welded it again with a part that would ensure the steering column had a 60-degree horizontal angle.

- While designing, instead of fully modeling the front suspension, I had added a shape to represent it. However, since I welded the part that holds the steering column at a 60-degree angle, when I installed the steering column, the middle support of the chassis started touching the tire. Even though I cut and repositioned the middle support inward, it didn't resolve the issue, so I installed the front suspension upside down. Later in the process, this caused an issue as it prevented me from adding the front fender.

- Another issue I hadn’t accounted for in the motorcycle design was its length. Since it was 30 cm longer than standard motorcycles, the cables going to the rear brake drum were too short. To resolve this, I cut a longer brake cable to fit and completed that part.

- I added a shock-absorbing backrest for the rider. In the next phase, I placed seat foam on top of the luggage, but since the foam was too thick, the luggage couldn't open and close properly. As a result, I had to make the backrest non-functional.

- In the front section, the area where the rider's feet rest needed to be a bit wider.

## Current Status of The Project

The unfinished parts due to time constraints are as follows;

- The front part of the motor is open, and all the wires coming out are messy, so this area needs to be closed.
    
- The side covers of the seat area are missing, and these parts need to be closed as well.
    
- Displaying the motor speed on the screen.
    
- Since I installed the front suspension upside down, standard front fenders don't fit. Therefore, the front fender needs to be 3D printed.
    
- In the future, the seat foam could potentially be made in a more aesthetic shape instead of rectangular, and the backrest could regain its functionality.
    
- To prevent the electric motor's shaft from spinning and tangling the wires while reversing, a locking washer needs to be fixed to the rear swing arm.

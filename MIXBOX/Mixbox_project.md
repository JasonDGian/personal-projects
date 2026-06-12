<!--
I started this project because I am a fan of fighting games and with some friends I've met online I often play titles like Street fighter, Soul Calibur or Tekken. 
I've played for years and for a lot of time I've wanted to get myself a fightstick or a mixbox. I've tried many times to fetch a decent one but these things are quite pricey and the models i like the most go for up to 700€ which might be excusable for some pros but for noobs like me that play casually that's just too much.
In my 3d printing adventures i started modifying stuff and one day a friend, one of them who plays with me, complained his fightstick (expensive one) broke and was no longer working. That day my lightbulb turned on and i decided to make a fightstick out of a normal contgroller. 
What was stopping me or anyone to turn a normal PS4 controller into a custom fightstick, and a customized one for that?  And that made me follow a path of investigation, learning and i ended up creating one of the gifts I am the proudest i ever gave anyone. 
IT took many hours but the final result I believe spoke for itself. 
I tested my most of the skills i accumultaed over the hears as a hobbist. It involved knowledge in many fields:
- Printing media
- Photographi paper handling and long term protection.
- Image edition for customization.
- 3d Printing
- 3d modeling and prototyping
- Soldering and electronics in general.
- Patience, patience, patience.

This is the final result of the piece i gifted my brother from another mother.
![T-29 controller](https://github.com/JasonDGian/personal-projects/blob/main/MIXBOX/T-29.png)

In this document i will gather the steps i have followed to obtain the final result, but this time i will be building it for myself, years later, with a different 3d printer and different 3d modeling software. Hopefully i can achieve the same result or better. 

# Step 1, get a base controller for the motherboard.
The controller i Chose is the T-29 Wireless controller. I tested it with my PC and works fine, it connects easily on bluetooth and reconnects automatically once turned off, this did not happen with previous controllers i bought for some reason, perhaps my bluetooth device, perhaps the contgroller themsevels, but this controller i am happy with the product and i believe it to be a decent base for my project.

# Step 2, analyze the motherboard.
This part is crucial to know if viable and how difficult the soldering step will be.
I have to identify the test pads for each button i want to extract to my fightstick and solder to each one a very small wire that will activate the related input.

# Step 3, motherboard box prototyping.
Once I've identified the testing pads I will use as solderpoints i will start measuring the motherboard and will prototype a holder for it. 
The idea her is to create sort of a box that will contain the motherboard and protect it from unintentional pulling of wires that may strip the pad from the board or break the wire. 
HAving the motherboard enclosed also allows me to design a mounting place for it within the mixbox and replace it with another motherboard in the future with different fucntion, like one compatible with PS5 or something else.
The key here is to decide whether you are going to apply constructive changes or destructive changes. In my case, i do not plan on reusing the motherboard within the controller so i do not really mind making destructive changes or hard to reverse ones. 

To start prototyping the mobo-box the first thing is to decide how to secure the motherboard to it's new home. In my case i decided to go for 3 specific holes in the middle of it with screws, this will give me enough freedom to design the box as i may need it and is pretty easy to measure. In the past I have used more convoluted ways that were quite annoing and needed many prototypes before i was satisfied with the result, so this time i will simplify things and improve as may be needed. 



- Get a base controller with an easy to work on motherboard. It must have the functionalities you are looking for in a mixbox.
- Analyze and measure the motherboard.
  - Identify the testing pads for the inputs.
  - Identify the mounting points for the screws.
- Prototype and test a mounting box.
  - It must secure the motherboard precisely.
  - Keep in mind the charging port and battery.
  - Decide wether to keep the analog sticks or to remove them, do you want them in your mixbox or get rid of them?
- Once the mounting box is done, you can start designing the mixbox itself.
- Test your hands claw position, imagine you are pressin buttons.
  - Create a drawing, or scan your hand to check your claw position.
- Once your claw is clear, start thinkin of the buttons you want to include, you want anything custom?
- Once the design is clear, decide if you want big or small buttons, keyboard style or arcade style? a mix of both?
- Then you can start designing, positionin and testing stuff.
- Once your design is completed, you have to calculate the height of the box considering the mobo-box and the buttons profile, then start fitting them together to create the main body.


# Threaded Arcade buttons.
This part was a little bit tricky because i never did this before in any print of mine, and even more so when using blender in which i am still rather new.
I've used the bolt factory addon to easily create bolts and manipulate properties to create test pieces before starting messing around with the real body of the controller.

Metric bolts use a code like M8x1.25x30 to convey key details: M: Indicates the metric measurement system, with sizes in millimetres. 8: Specifies the bolt's nominal diameter, here 8mm. 1.25: Defines the thread pitch, or the gap between threads, in millimetres. Smaller numbers indicate finer threads. 
Analyzing and measuring my arcade buttons I see that the external diameter is 23.55 (rounded up to 24) and the internal diameter seems to be of 1.4 less so about 

So my bolt is 22 mm in height, 23.55 in external diameter and 22.15 internal diameter. I cloned these details in blender to use as a template to carve out the threaded inserts for the main body. 
I used a margin of about 0.10 for tolerance.
The formula for calculating thread pitch is P = L / n, where P represents thread pitch, L denotes thread length, and n stands for the number of threads.
But since that is too complicated for my simian brain i just measured from the crest to crest and calculated that it would be a pitch of 1.7mm and tested. It worked fine so I was happy with that.

The arcade buttons that gave me the best feedback were some pricey ones that used a threaded insert instead of a fit-and-click friction system. 
This brought problems regarding the ergonomics because while the external diameter was the same the "nut" it came with was way too wide to fit in the designed prototype.
My solution to this problem was to flip the table and cry in a corner thinking i could not materialize what i wanted.
When my tears dried up i realised that if the nut did not fit in the current design, then design the nut INTO rather than using an external nut. 
I found out about interesting things like M measurements, pitch calculations and more.
<img width="981" height="483" alt="image" src="https://github.com/user-attachments/assets/6fc5cc07-a8a3-401f-88fb-14a39955c0e2" />
<img width="711" height="387" alt="image" src="https://github.com/user-attachments/assets/9b5b6933-459f-4f39-8bf2-8c645e42769d" />
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/33decb0a-cda5-407a-bb1c-3ed4e26806bf" />
<img width="1011" height="360" alt="image" src="https://github.com/user-attachments/assets/64378744-1244-49ad-9884-bea733f0b459" />

Testing around with first measurements i realised i was wrong so then i just said i would recalculate.
I measured the body of the screw, i counted how many threads, and then divided the distance by the threads and the result was something like this:
20.75 length of threaded body.
11 threads.
about 1.88 mm pitch was the result.
So i started testing with certain tolerances this new pitch.
The positive i used was 24.2mm external diameter and 22.40mm internal diameter with 1.88mm pitch.
The extra 0.2 to both internal and external diameter was just for tolerance.
<img width="1137" height="764" alt="image" src="https://github.com/user-attachments/assets/b3685cb0-f92b-4538-b7d8-5c673c644d1e" />
    
<img width="1318" height="622" alt="image" src="https://github.com/user-attachments/assets/bb1646d5-90a6-4ec2-b5e7-f04716a0c6e1" />
    
<img width="1227" height="534" alt="image" src="https://github.com/user-attachments/assets/c9356bf1-7c07-43fb-9e41-6c590069e1a7" />





   
---
   
---
   
# Design and customization.

## Choosing action buttons.
Chossing the action buttons was a trip in itself. There were so many options it was hard to choose. In the end I decided to go with the backlit led buttons. I tried two main sized, one had a circumference of 33mm of diameter and the other 27mm diameter.



## Choosing direciton buttons.

# Buttons layout.
In this section i will discuss how I decided to place the buttons the way i did.

## Action button ergonomics .
This part of the build is crucial to make the controller feel comfortable and your own.
I wanted to have two arrays of buttons and make them both feel natural and comfortable for my hand.
    
1. I positioned my hand on a piece of paper and allowed my fingers to rest in a comfortable position, a position i called "the claw".   
<img width="1554" height="900" alt="ergonomics" src="https://github.com/user-attachments/assets/ea21dbd3-6ff5-40be-8a89-858dbfd8d0ce" />
     
2. Once my hand was comfortable I tried moving my fingers up and down and regulated the position again.    
Once I was sure of the position i marked the place where the fingers touched the paper, sort of a "tear drop" shape. This would become the main array of buttons.   
<img width="1554" height="900" alt="ergonomics_study_1" src="https://github.com/user-attachments/assets/7e0fd43c-d5be-4650-916e-fcdbc00216b3" />
     
3. After the main array was traced I moved my fingers in a more closed position, keeping a comfortable position and marked again the points of contact, again the inverted tear drop shape.   
This would become the second buttons array.   
<img width="1554" height="900" alt="ergonomics_study_2" src="https://github.com/user-attachments/assets/b25514f1-1684-40c1-a2bb-f259943f4984" />
    
4. I then used the resulting drawing as a reference image to develop the first ergonomics test piece.    
<img width="1125" height="694" alt="ergonomics_proto_design" src="https://github.com/user-attachments/assets/4afa50fa-a055-4dde-85ce-b0974755a993" />

5. Then I printed a small test piece to save time and plastic to fit the buttons in and see how it felt.
<img width="1554" height="900" alt="ergonomics_prototype_1" src="https://github.com/user-attachments/assets/65edc0cc-0215-4e6f-9068-a90db07faa1f" />
<img width="1554" height="900" alt="ergonomics_proto_1" src="https://github.com/user-attachments/assets/bd6c3bd3-2dc2-4114-86e9-768225cd480e" />

> [!IMPORTANT] 
> Following this process eliminated much of the guesswork and trial-and-error. In the end, I discarded several buttons that I had previously tested and initially considered good candidates. Although those buttons were only a few millimeters larger than the ones I ultimately chose, that small difference accumulated enough to make the overall hand position uncomfortable. The smaller buttons allowed me to keep my fingers in a more natural, compact position while also leaving room to fit two additional buttons for potential future functions.

# Choosing the action buttons.
For the action buttons I decided to go with led-backlit buttons that looked quite cool and an idea bloomed in my mind to make it look cooler (upon which i will expand later). 
I tested both cheap and not so cheap buttons and landed on these three sets. All these are backlit and felt decent. While testing ergonomics though I discarded the first set and with further details i notice i preferred the feeling of the third set, which was more pricey but given the overall feeling was worth the money.

<table border="1">
    <thead>
        <tr>
            <th><strong>33 mm diameter</strong></th>
            <th><strong>27 mm diameter</strong></th>
            <th><strong>27 mm diameter</strong></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><img width="2235" height="1001" alt="BTN_SET_1" src="https://github.com/user-attachments/assets/214e95f4-178d-46ef-a982-85e84cdd8f1e" /></td>
            <td><img width="2234" height="1001" alt="BTN_SET_2" src="https://github.com/user-attachments/assets/46f90910-fa56-4e3f-999c-62560dd0e919" /></td>
            <td><img width="2235" height="1001" alt="BTN_SET_3" src="https://github.com/user-attachments/assets/b36b048d-3483-4a1e-8439-fc733937605c" /></td>
        </tr>
        <tr>
            <td>
              Diameter: 33mm </br>Total height: 40mm </br>Snap-fit or snap-lock system.
            </td>
            <td>Diameter: 27mm </br>Total height: 30mm </br>Snap-fit or snap-lock system.
            </td>
            <td>Diameter: 27mm</br>Total height: 36mm </br>Threaded plastic nut system.
            </td>
        </tr>
    </tbody>
</table> 

The ergonomics and comfort played a major role in the selection of the buttons since the bigger ones (33mm diameter) were just too big to be compact enough to secure comfort. Once i started testing i felt the difference between set 2 and 3 and even if Set 3 depended on a big plastic nut that was too big I was certain i would be able to fix it somehow. Set 3 was the one i neded up choosing. 







    
---    
    
---   
    
---   
       
# Revised text
    
---    
    
## 🔸 Action buttons ergonomics.
The ergonomics of the action buttons are one of the most important aspects of the controller. A good layout should feel natural, reduce strain during long play sessions, and allow every button to be reached comfortably without forcing awkward finger movements.
   
Rather than copying the layout of an existing controller, I decided to design the button placement around the natural resting position of my own hand.
    
1. I placed my hand on a sheet of paper and allowed my fingers to settle into a relaxed position. I referred to this posture as "the claw".
<img width="1554" height="900" alt="ergonomics" src="https://github.com/user-attachments/assets/ea21dbd3-6ff5-40be-8a89-858dbfd8d0ce" />    
     
2. Once my hand felt comfortable, I moved my fingers up and down several times and readjusted them until they consistently returned to the same resting position. I then marked the points where my fingertips contacted the paper. The resulting pattern resembled an inverted teardrop shape and became the basis for the primary button array.
<img width="1554" height="900" alt="ergonomics_study_1" src="https://github.com/user-attachments/assets/7e0fd43c-d5be-4650-916e-fcdbc00216b3" />     
     
3. Next, I brought my fingers into a slightly more closed position while maintaining comfort and repeated the process. This produced a second set of contact points that would later become the secondary button array.
<img width="1554" height="900" alt="ergonomics_study_2" src="https://github.com/user-attachments/assets/b25514f1-1684-40c1-a2bb-f259943f4984" />    
    
4. Using these markings as a reference, I created the first ergonomic prototype in Blender.
<img width="1125" height="694" alt="ergonomics_proto_design" src="https://github.com/user-attachments/assets/4afa50fa-a055-4dde-85ce-b0974755a993" />    
    
5. To validate the design before committing to a full print, I produced a small test piece containing only the button layout. This allowed me to evaluate the spacing, reachability, and overall comfort while minimizing both print time and material usage.
<img width="1554" height="900" alt="ergonomics_prototype_1" src="https://github.com/user-attachments/assets/65edc0cc-0215-4e6f-9068-a90db07faa1f" />
<img width="1554" height="900" alt="ergonomics_proto_1" src="https://github.com/user-attachments/assets/bd6c3bd3-2dc2-4114-86e9-768225cd480e" />

> [!IMPORTANT]
> This process significantly reduced the amount of guesswork involved in the design. Instead of adapting my hand to a predetermined layout, the layout was designed around my hand. The resulting prototype also established several dimensional constraints that would later influence the selection of the action buttons themselves.
    
---    
    
## 🔸 Direction buttons ergonomics.
The ergonomics of the directional controls were just as important as those of the action buttons. During my research, I noticed that several commercial Mixbox-style controllers, including some premium models, used a fixed key orientation that did not feel particularly natural for my hand position.

Rather than accepting a predetermined angle, I wanted the directional controls to adapt to my preferred playing posture.

To achieve this, I designed the directional button assembly as a rotating platform. This allowed me to experiment with different orientations and evaluate them during actual gameplay instead of committing to a fixed position from the start.

The adjustable design made it possible to test multiple angles and determine which one provided the most comfortable wrist and finger alignment. Once a preferred position was identified, I could either leave the assembly adjustable or permanently fix it in place.

The final decision depended on the overall finish of the controller. For example, applying a custom vinyl overlay would require the directional controls to remain in a fixed orientation to preserve the visual design and alignment of the artwork.

As with the action button layout, the goal was not to replicate an existing controller but to create a control scheme tailored to the natural resting position of my hand. By prioritizing adjustability during the prototyping phase, I was able to evaluate different configurations and select the one that felt most comfortable during extended play sessions.

<table border="1">
    <thead>
        <tr>
            <th><strong>Mixbox</strong></th>
            <th><strong>Mayflash</strong></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><img width="2235" height="1001" alt="BTN_SET_1" src="https://github.com/user-attachments/assets/214e95f4-178d-46ef-a982-85e84cdd8f1e" /></td>
            <td><img width="2234" height="1001" alt="BTN_SET_2" src="https://github.com/user-attachments/assets/46f90910-fa56-4e3f-999c-62560dd0e919" /></td>

        </tr>
        <tr>
            <td>
              Diameter: 33mm </br>Total height: 40mm </br>Snap-fit or snap-lock system.
            </td>
            <td>Diameter: 27mm </br>Total height: 30mm </br>Snap-fit or snap-lock system.
            </td>
            <td>Diameter: 27mm</br>Total height: 36mm </br>Threaded plastic nut system.
            </td>
        </tr>
    </tbody>
</table>

# Choosing the action buttons.
For the action buttons I decided to go with led-backlit buttons that looked quite cool and an idea bloomed in my mind to make it look cooler (upon which i will expand later). 
I tested both cheap and not so cheap buttons and landed on these three sets. All these are backlit and felt decent. While testing ergonomics though I discarded the first set and with further details i notice i preferred the feeling of the third set, which was more pricey but given the overall feeling was worth the money.

<table border="1">
    <thead>
        <tr>
            <th><strong>33 mm diameter</strong></th>
            <th><strong>27 mm diameter</strong></th>
            <th><strong>27 mm diameter</strong></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><img width="2235" height="1001" alt="BTN_SET_1" src="https://github.com/user-attachments/assets/214e95f4-178d-46ef-a982-85e84cdd8f1e" /></td>
            <td><img width="2234" height="1001" alt="BTN_SET_2" src="https://github.com/user-attachments/assets/46f90910-fa56-4e3f-999c-62560dd0e919" /></td>
            <td><img width="2235" height="1001" alt="BTN_SET_3" src="https://github.com/user-attachments/assets/b36b048d-3483-4a1e-8439-fc733937605c" /></td>
        </tr>
        <tr>
            <td>
              Diameter: 33mm </br>Total height: 40mm </br>Snap-fit or snap-lock system.
            </td>
            <td>Diameter: 27mm </br>Total height: 30mm </br>Snap-fit or snap-lock system.
            </td>
            <td>Diameter: 27mm</br>Total height: 36mm </br>Threaded plastic nut system.
            </td>
        </tr>
    </tbody>
</table> 

The ergonomics and comfort played a major role in the selection of the buttons since the bigger ones (33mm diameter) were just too big to be compact enough to secure comfort. Once i started testing i felt the difference between set 2 and 3 and even if Set 3 depended on a big plastic nut that was too big I was certain i would be able to fix it somehow. Set 3 was the one i neded up choosing. 













# Building a Custom Fightstick Controller

# 1. Project Goals

## Motivation

Since I started playing fighting games, I have always wanted to own a dedicated fight stick or MixBox-style controller. The precision, tactile feedback, and overall experience offered by these devices appealed to me far more than a standard gamepad. However, when I began researching commercial options, I quickly realized that quality controllers are often expensive, while more affordable alternatives frequently lack features such as ergonomic layouts, suitable dimensions, or the overall quality I was looking for.

This is not my first attempt at building an arcade controller. Several years ago, after getting into 3D printing, I designed and built a custom controller for a close friend. That project involved a great deal of experimentation and problem-solving, while helping me develop skills in design, manufacturing, electronics, and prototyping. This time, I want to apply those skills to create a controller for myself.

Cost is one of the motivations behind this project. Building a custom controller can be considerably cheaper than purchasing a high-end commercial product. More importantly, it provides complete freedom over the design. Every aspect of the controller—from its size and ergonomics to its appearance and functionality—can be tailored to my own preferences. Even if the final cost is similar to that of a commercial product, the result should be a much better fit for my needs.

Although I do not currently participate in official tournaments, one of the design goals of this project is to keep the controller as compliant with common competitive regulations as possible. Features such as macros, turbo functions, or any form of input automation will be avoided, and accepted standards for custom and leverless controllers will be considered throughout the design process. While comfort and customization remain the primary objectives, maintaining compatibility with tournament rules will help ensure that the controller remains a practical, versatile, and fair input device.

Finally, I decided to document the entire process. By sharing both the successes and challenges encountered during development, I hope this project can serve as a useful reference for others interested in building their own custom arcade controller.

## Design Objectives

The primary objective of this project is to design an ergonomic controller that is comfortable, practical, and enjoyable to use. In addition to functionality, the controller should have a personalized appearance, incorporating custom colors and button designs that reflect my own tastes and interests.

## Desired Features

One of the key features is a keyboard-style directional input system. Instead of a traditional joystick, the controller will use directional buttons similar to keyboard cursor keys, creating a hybrid between a keyboard and an arcade fight stick. This layout, commonly known as a MixBox, combines the precision of keyboard inputs with the tactile feel of arcade buttons.

The controller is primarily intended for PC use, but compatibility with PlayStation systems is also desirable. PlayStation 4 support is a practical goal, while PlayStation 5 compatibility would be a welcome addition if it can be achieved without significantly increasing the project's complexity or cost.

## Constraints

The main constraints for this project are time and budget. As a personal project, it must be developed within the limits of my available resources while maintaining a balance between quality, functionality, and affordability.

Another important constraint is tournament legality. While the controller is not being designed specifically for competitive play, it should comply with commonly accepted tournament regulations whenever possible. This requirement will influence both the hardware and firmware design choices throughout the project.

Size and portability are also important considerations. The controller should be as compact and lightweight as possible, both to minimize desk space requirements and to improve comfort during transportation and extended use.
  

---

# 2. Ergonomics and Layout Design

## 2.1 Action Button Ergonomics

- Hand tracing process.
- Primary and secondary button arrays.
- Prototype testing.
- Ergonomic findings.

## 2.2 Direction Button Ergonomics

- Problems found in existing Mixbox layouts.
- Rotating platform concept.
- Testing different orientations.
- Final directional layout.

---

# 3. Component Selection

## 3.1 Choosing the Action Buttons

- Candidate sets.
- Comparison.
- Why Set 3 was selected.

## 3.2 Choosing the Direction Buttons

- Keycaps.
- Switches.
- Feel and travel considerations.

## 3.3 Choosing the Controller PCB

- Requirements.
- Compatibility.
- Final motherboard choice.

## 3.4 LEDs and Lighting

- Backlighting goals.
- LED selection.
- Power considerations.

## 3.5 Battery and Charging System

- Why a battery was included.
- Charging solution.
- Runtime expectations.

---

# 4. Case Design

## 4.1 Overall Design

- Design language.
- Dimensions.
- Internal organization.

## 4.2 Mounting System

- Button mounting.
- PCB mounting.
- Battery mounting.
- Serviceability considerations.

---

# 5. Wiring and Electronics

## 5.1 Wiring Layout

- Signal wiring.
- Power distribution.
- Cable management.

## 5.2 Final Assembly

- Installing components.
- Connecting electronics.
- Testing.

---

# 6. Finishing Touches

## 6.1 Vinyl Cover Design

- Artwork.
- Alignment considerations.
- Manufacturing process.

## 6.2 Final Appearance

- Completed controller.
- Lessons learned.
- Future improvements.


---



# Building a Custom Fightstick Controller

## 1. Project Goals

- Why I decided to build my own controller.
- Design objectives.
- Features I wanted to include.
- Constraints (size, portability, budget, aesthetics, etc.).

---

# 2. Ergonomics and Layout Design

## 2.1 Action Button Ergonomics

- Hand tracing process.
- Primary and secondary button arrays.
- Prototype testing.
- Ergonomic findings.

## 2.2 Direction Button Ergonomics

- Problems found in existing Mixbox layouts.
- Rotating platform concept.
- Testing different orientations.
- Final directional layout.

---

# 3. Component Selection

## 3.1 Choosing the Action Buttons

- Candidate sets.
- Comparison.
- Why Set 3 was selected.

## 3.2 Choosing the Direction Buttons

- Keycaps.
- Switches.
- Feel and travel considerations.

## 3.3 Choosing the Controller PCB

- Requirements.
- Compatibility.
- Final motherboard choice.

## 3.4 LEDs and Lighting

- Backlighting goals.
- LED selection.
- Power considerations.

## 3.5 Battery and Charging System

- Why a battery was included.
- Charging solution.
- Runtime expectations.

---

# 4. Case Design

## 4.1 Overall Design

- Design language.
- Dimensions.
- Internal organization.

## 4.2 Mounting System

- Button mounting.
- PCB mounting.
- Battery mounting.
- Serviceability considerations.

---

# 5. Wiring and Electronics

## 5.1 Wiring Layout

- Signal wiring.
- Power distribution.
- Cable management.

## 5.2 Final Assembly

- Installing components.
- Connecting electronics.
- Testing.

---

# 6. Finishing Touches

## 6.1 Vinyl Cover Design

- Artwork.
- Alignment considerations.
- Manufacturing process.

## 6.2 Final Appearance

- Completed controller.
- Lessons learned.
- Future improvements.







   

To properly mount the motherboard within the controller and secure it and organize the connections and wiring I decided to create sort of an enclosure of the motherboard of the controller. 
To build the motherboard I went a little bit overkill and decided to first model an aproximation of the motherboard itselt to see how could i play around with it in the controller body space.
To model the motherboard I went and measured every detail and checked for precision with simple tests. 
I would measure one side with it's details and print the piece and write down the mistakes if there were any. 
The result would be precise enough to have decent aproximation of the motherboard and 

<img width="949" height="588" alt="image" src="https://raw.githubusercontent.com/JasonDGian/personal-projects/refs/heads/main/MIXBOX/IMG/motherboard-measurements-intro-blender.png" />



To build the motherboard box I started by modeling an aproximation of the motherboard itself. I wanted it as exact as possible in case I wanted something extremely specific but this approach was unnecesary. 
It took me a while to measure and model and I as i went on i test fitted the pieces I were creating in order to avoid a snowball of mistakes, and catch errores in time before they created a cascade effect. 
In 


As I printed the test fitting pieces I wrote down the points that needed fixing and then tested again. I made sure to analyze well each test print to know what should be changed. In the end I created 6 test fittings to find a satisfactory positive for the mother board box. 



## 1. Rough external shape.
At first I measured the external outline of the motherboard's shape. The idea is to recreate an aproximate yet still somewhat precise shape to use as a base. It is important to keep one single point as the fixed starting point, the fixed point in the shape to take as a reference. I took the bottom left corner to use as the reference point for all the other measurements where possible. Once I had the rough image on paper y brought that into blender and started testing sides one by one to see how they fit.

>![Tip]
>The drawing on paper must no be perfect, it must be clear enough to understand the part being measured and the value assigned to it, it must not be 1:1 precise. The precision must come into the program. Also, using the paper is not mandatory, you can measure and create the 2d image as you go, but this is my modus operandi.

_Drawing with the aproximate measurements._
<img width="1847" height="1080" alt="ROUGH MEASURE" src="https://github.com/user-attachments/assets/5e9dfca1-7d3a-412c-8c75-c2f786a90103" />

## 2. Creating first rough version.
When creating the object in blender with the found measurements I kept in mind I wanted to leave a tolerance value of 0.30 mm to make sure stuff would fit. The idea is not to replicate exactly the motherboard but a slightly bigger piece to make sure stuff does not fit "too exactly" introducing friction or whatever kind of problems that can originate from low tolerance.

_Measures passed into blender vertices_
<img width="1235" height="770" alt="image" src="https://github.com/user-attachments/assets/c13131eb-2f4f-46da-aef0-3bc89619cc43" />


## 2. Test fit and corrections.
Once the initial image was created I started testing every side to see how each side individually would fit. Once every side was tested and confirmed a good fit I started combining LEFT with TOP then RIGHT and finall BOTTOM SIDE, testing each new combination and taking notes of what was colliding impropperly, what needed to correct tolerance values and more.
    
>![CAUTION]
> I found useful to keep one vertix as the "fixed reference point" to apply all the corrections from, this way correcting one measure would not mess up another.

_Testing sides and writing down impropper collision or measurements, noting tolerances_
<img width="1385" height="900" alt="TEST-FITS" src="https://github.com/user-attachments/assets/0751385f-0856-45f6-b70a-361d08ead9b9" />



-->

# Motherboard box.
The Motherboard Box (from now on MO-Box) is the enclosure designed to house the controller's motherboard after it has been extracted from the original assembly. Its primary purpose is to protect the fragile wire connections soldered to the motherboard's test pads while also providing a secure and organized mounting solution inside the mixbox body or shell.
    
Beyond protection, the MO-Box serves as a structural component that helps manage cable routing and prevents unnecessary stress from being applied to the soldered connections during assembly and maintenance.
    
## Design Methodology
My initial approach was intentionally thorough. Before designing the enclosure itself, I created a detailed 3D model of the motherboard. The goal was to understand exactly how the board occupied the available space inside the controller and to provide a reliable reference for future design decisions.
    
>[!Note]
>In hindsight, this level of detail was more extensive than strictly necessary for the enclosure design. However, the process provided a highly accurate representation of the motherboard and allowed me to confidently explore different mounting solutions.
    
To achieve this, I carefully measured the motherboard and repeatedly validated the measurements through physical test prints. Rather than measuring everything at once and hoping for the best, I modeled and verified individual sections incrementally. This approach allowed errors to be identified early before they accumulated into larger dimensional inaccuracies.
   
The mother board box (from now on mo-box), is the piece that will hold the motherboard extracted from the controller. This piece will protect the fragile connections of the wires soldered to the motherboard testing pads. 
I decided, because i

## Modeling the Motherboard 
   
### 1. Defining the External Shape
The first step was to capture the motherboard's overall outline. The objective was not to create a perfect digital twin but rather a sufficiently accurate approximation that could serve as a reliable design reference.
    
To maintain consistency throughout the measurement process, I selected a single fixed reference point: the bottom-left corner of the motherboard. Whenever possible, all measurements were taken relative to this point. Using a common reference minimized the risk of cumulative measurement errors and simplified later corrections. 
     
After sketching the motherboard outline and recording the dimensions, the information was transferred into Blender, where the initial 2D profile was created.

>[!Note]
>The paper sketch does not need to be perfectly scaled or highly detailed. Its purpose is simply to record dimensions and identify measured features clearly. The actual precision is achieved during the digital modeling stage.
   
_Drawing showing the dimensions of the motherboard._
<img width="1847" height="1080" alt="ROUGH MEASURE" src="https://github.com/user-attachments/assets/5e9dfca1-7d3a-412c-8c75-c2f786a90103" />
    
### 2. Creating the Initial Model
Once the measurements had been collected, I recreated the motherboard outline in Blender using the recorded dimensions. At this stage, the model was intended to match the measured geometry as closely as possible, without any additional tolerance applied.

This initial version served as the baseline from which all future fitting tests and adjustments would be made.

_Dimensions transferred into Blender to create the initial motherboard profile._
<img width="1235" height="770" alt="image" src="https://raw.githubusercontent.com/JasonDGian/personal-projects/refs/heads/main/MIXBOX/IMG/motherboard-measurements-intro-blender.png" />
    
### 3. Validation Through Test Fitting
After creating the initial model, I began an iterative test-fitting process to validate the measurements and refine the geometry.

At this stage, a dimensional tolerance of approximately 0.30 mm was introduced. The objective was not to replicate the motherboard exactly, but to create a slightly oversized model that would provide sufficient clearance when designing the surrounding enclosure.

> [!Tip]
> Adding a small tolerance helps prevent issues caused by excessively tight fits, such as assembly difficulties, friction, and dimensional variations introduced by the 3D printing process.

Rather than validating the entire model at once, <mark>individual sections were tested independently</mark>. Each edge and contour was checked before progressing to larger combinations of features. This approach made it easier to identify the source of any fitting issues and prevented small errors from propagating throughout the model.

The validation process followed these stages:

1. Verify each side independently.
2. Combine and verify the left and top sections.
3. Add and verify the right side.
4. Integrate the bottom section and validate the complete outline.

For every iteration, a test piece was printed and physically fitted against the motherboard. **These test pieces were not replicas of the motherboard itself; instead, they represented the surrounding enclosure geometry that would eventually contain the motherboard.** In practice, the printed parts were the **negative** of the motherboard shape; the cavity into which the motherboard would fit. This approach allowed the enclosure dimensions to be validated directly while reducing print time and material usage.

After each fitting test, any discrepancies were documented and analyzed before modifications were made to the model. Once the necessary corrections were applied, a new test piece was printed and evaluated.
       
_Test-fitting a printed section and documenting areas requiring correction._
<img width="1385" height="900" alt="motherboard-test-fit-and-corrections-steps" src="https://raw.githubusercontent.com/JasonDGian/personal-projects/refs/heads/main/MIXBOX/IMG/motherboard-test-fit-and-corrections-steps.png" />

> [!Important]
> Throughout the validation process, a single reference vertex was maintained as the fixed origin for all measurements and corrections. Applying modifications relative to the same reference point ensured that changes made to one feature would not unintentionally affect dimensions that had already been validated.

### 4. Creating the Final Motherboard Model
Once the overall dimensions had been validated and the test pieces demonstrated a satisfactory fit, I proceeded to model the remaining features of the motherboard.

The same workflow used to validate the external outline was applied to the board's other significant elements. Each feature was measured, modeled, and adjusted while maintaining the established tolerance values. The objective was to create a rather a sufficiently accurate representation that could be reliably used as a reference when designing the motherboard enclosure and its mounting features.

By this stage, the validated external geometry provided a solid foundation, allowing additional details to be incorporated with confidence while preserving the dimensional accuracy achieved during the test-fitting phase.

_Approximate motherboard model used as the reference geometry for the enclosure design._
<img width="1774" height="766" alt="image" src="https://raw.githubusercontent.com/JasonDGian/personal-projects/refs/heads/main/MIXBOX/IMG/motherboard_modeled_reference%20(1).png" />
        
By using the validated motherboard reference model and incorporating the defined tolerance values, the final printed test piece fits as intended, requiring little to no additional adjustment.
   
<img width="1774" height="676" alt="motherboard_positive_fitting_test" src="https://raw.githubusercontent.com/JasonDGian/personal-projects/refs/heads/main/MIXBOX/IMG/motherboard_positive_fitting_test.png" />


## Modeling the motherboard enclosure.
At this point i had my reference to start working on the MO-box. 



----
    

# LED module and Touch Sensor.
The LED module is responsible for communicating the controller's status to the user. It provides visual feedback for Bluetooth connectivity, battery level, charging state, and other system functions.
   
My goal was to integrate the original LED module into the Mixbox enclosure while preserving all of its functionality. By reusing the original component, I could retain not only the status indicators but also the capacitive touch sensor and the integrated push button without requiring any modifications to the controller electronics.    
   
_Led module vs Controller_
<img width="1774" height="865" alt="lightmodule_presentation" src="https://github.com/JasonDGian/personal-projects/blob/main/MIXBOX/IMG/lightmodule_presentation.png" />
         
## Design Methodology
Unlike the motherboard, the LED module contains several complex curved external surfaces that are difficult to measure directly using conventional tools. Accurately reproducing these features was necessary to ensure proper fitment and alignment within the Mixbox enclosure (mainly to remain aesthetically coherent).

Rather than relying exclusively on direct measurements or repeated trial and error, I adopted a combination of measurement techniques. These included traditional caliper measurements, custom 3D-printed gauges, and profile tracing. The traced profiles were later scanned and imported into Blender, where they could be used as reference images during the modeling process.
   
>[!Note]
>This workflow is neither particularly elegant nor professional, I would guess. but it allowed the geometry to be reproduced with sufficient accuracy using the tools and skills available to me.
    
## Measuring the Module
### 1. Measuring the Corner Fillets

The first challenge was determining the radii of the various corner fillets that define the module's external profile.

To accomplish this, I designed and printed a series of test gauges containing fillets of known radii. Each radius value was labeled directly on the printed part, allowing rapid comparison against the original module.

Rather than attempting to calculate the radii mathematically, I simply compared each gauge against the corresponding corner and selected the radius that provided the closest match. Since different sections of the module used different fillet radii, multiple gauge sets were required to characterize the entire profile.

Once the correct radii had been identified, recreating the module's outline in Blender became significantly more straightforward.
    
_3D-printed fillet gauges compared against the original module._
<img width="1774" height="518" alt="lightmodule_front_side_bevel_measuring" src="https://github.com/JasonDGian/personal-projects/blob/main/MIXBOX/IMG/lightmodule_front_side_bevel_measuring.png" />
   
### 2. Measuring the Front, Top and Side Surface Curvature
Many of the module's curved surfaces could not be measured reliably using the custom gauges described previously. Accurately reproducing these features was important, as even small dimensional deviations become noticeable when the module is mounted flush with the enclosure.
      
The most practical solution I could devise was to trace the difficult-to-measure profiles onto paper and use those tracings as references during the modeling process. The drawings were scanned and imported into Blender, where they served as reference images for creating the initial geometry.
        
Although a number of direct measurements were also taken, I relied primarily on the traced profiles to establish the overall shape. From these references, I modeled a series of test pieces representing the negative geometry of the module and used them to validate the fit against the original component.
   
<img width="1774" height="447" alt="lightmodule_traced_on_paper" src="https://raw.githubusercontent.com/JasonDGian/personal-projects/refs/heads/main/MIXBOX/IMG/lightmodule_traced_on_paper.png" />
    
The process required a fair amount of patience and iteration, but it ultimately produced results that were accurate enough for the project.
   
**Validating the Side Profile Curvature**        
The upper surface of the LED module incorporates a subtle compound curvature that would have been difficult to reproduce through direct measurement alone.

Using the scanned side-profile tracing as a reference, I modeled the corresponding negative geometry and produced a series of test prints. After several fitting iterations and minor adjustments, the printed test piece achieved a satisfactory match to the original module.
   
_Side-profile tracing and curvature validation test pieces._    
<img width="1774" height="447" alt="light_module_top_surface_design" src="https://raw.githubusercontent.com/JasonDGian/personal-projects/refs/heads/main/MIXBOX/IMG/light_module_top_surface_design.png" />
    
**Validating the Front Profile Curvature**    
The front profile proved much easier to reproduce. The traced reference matched the original component closely enough that the first test print required little to no adjustment.

Because the rear fillet radii had already been validated using the printed gauges, the front profile aligned correctly with the surrounding geometry. With the individual features already confirmed, I was able to proceed directly to testing the complete horizontal profile rather than creating additional intermediate validation pieces.
    
_Front-profile model and test fit._
<img width="1774" height="970" alt="lightmodule_front_surface_curve" src="https://github.com/user-attachments/assets/e6a7a111-592e-47f2-9cef-8b626e0ffaf6" />
    
### 3. Measuring the module vertical movement limitation strut.
The click button enclosed within the module is supported by a flexible plastic structure that contacts three support points protruding from the controller's internal button support body.

Two of these support points (highlighted in cyan in the image) serve as contact surfaces for the module's flexible plastic arms. When the module is pressed, these arms deflect against the support points and generate the restoring force that returns the module to its normal resting position. The central support point (highlighted in yellow) is responsible for actuating the internal click button.

The purpose of the vertical movement limitation strut is to **restrict the module's downward travel**, preventing excessive displacement that could damage either the click button mechanism or the flexible plastic arms within the module.
     
_LED module support points and button actuator_
<img width="2191" height="749" alt="lightmodule_support_points" src="https://raw.githubusercontent.com/JasonDGian/personal-projects/refs/heads/main/MIXBOX/IMG/lightmodule_support_points.png" />
     
_LED module assembled in resting position without the controller housing_
<img width="2191" height="749" alt="light_module_resting_place" src="https://raw.githubusercontent.com/JasonDGian/personal-projects/refs/heads/main/MIXBOX/IMG/light_module_resting_place.png" />
     
To determine the correct position of the strut in 3D space in Blender, I first marked the test piece previously used to evaluate the horizontal fillets and measured the maximum vertical travel allowed by the controller. Marking the test piece directly made it easy to transfer the reference locations to subsequent prototypes and position the strut attachments without requiring extensive additional measurements.
    
_Measurements and marked test piece used as reference_
<img width="2191" height="734" alt="lightmodule_rest_bar_measures_and_marks" src="https://raw.githubusercontent.com/JasonDGian/personal-projects/refs/heads/main/MIXBOX/IMG/lightmodule_rest_bar_measures_and_marks.png" />

Using this approach, I established that the module required approximately 0.85 mm of vertical clearance, along with the corresponding relative position derived from the reference test piece. Although some trial-and-error adjustment was still necessary, this feature proved relatively straightforward to iterate and refine.

_3D test model used for iteration_
<img width="2191" height="885" alt="image" src="https://raw.githubusercontent.com/JasonDGian/personal-projects/refs/heads/main/MIXBOX/IMG/lightmodule_rest_bar_model.png" />

_Test-fit result_
<img width="2191" height="726" alt="image" src="https://raw.githubusercontent.com/JasonDGian/personal-projects/refs/heads/main/MIXBOX/IMG/lightmodule_resting_bar_testpiece.png" />
  
---
   
---
   
## Modeling the Module positive



### Combining the vaslidated profiles to creat a positive.
With the top, front and side view measures validated I could now combine them into a single piece that would represent a more accurate aproximation of the light module.




Once the primary dimensions, fillet radii, and surface profiles had been characterized, the information was transferred into Blender to create a reference model of the LED module.
   
As with the motherboard model, the objective was not to create a perfect digital replica. Instead, the goal was to produce a sufficiently accurate representation that could be used to design the mounting features and surrounding enclosure geometry while maintaining the required clearances and alignment.
   
_Completed LED module reference model used during enclosure design._





## Modeling the LED module. 
   
### 1. Defining the External Shape

### 2. Creating the Initial Model

### 3. Validation Through Test Fitting

### 4. Creating the Final Motherboard Model

## Modeling the motherboard enclosure.
   
----
   
<!--
# Integrating the light module.
The LED module is the part of the controller responsible for indicating its status, including Bluetooth connectivity, battery level, and other system information. 
I wanted to integrate the original controller's LED module into the main body of the Mixbox in order to preserve all of its functionality. This includes not only the status LEDs, but also the touch sensor and the integrated click button.
         
_Led module and Controller_
<img width="1774" height="865" alt="lightmodule_presentation" src="https://github.com/JasonDGian/personal-projects/blob/main/MIXBOX/IMG/lightmodule_presentation.png" />
      
>[!NOTE]
>Modeling this part proved more challenging than expected. Rather than relying solely on direct measurements or pure trial and error, I combined several techniques: traditional measuring tools, custom 3D-printed gauges, and paper tracings of the module's profile.
   
## Measuring the module. 
   
**Measuring the Corner Fillets.**   
Determining the radii of the corner fillets was the first challenge. To do this, I designed and printed a series of test pieces, each featuring different fillet radii labeled directly on the model.
The process was simple: compare each test piece against the original module and identify which radius provided the closest match. Since the module did not use the same radius on every profile, I produced multiple sets of test pieces to cover the different geometries.
   
Once the correct fillet radii had been identified, reproducing the outline of the part in BELNDER became much more straightforward.
   
_3D-printed fillet gauges compared against the original module._
<img width="1774" height="518" alt="lightmodule_front_side_bevel_measuring" src="https://github.com/JasonDGian/personal-projects/blob/main/MIXBOX/IMG/lightmodule_front_side_bevel_measuring.png" />

**Measuring the Top Surface Curvature.**
[here i will explain the top side curvature measruement process.]


**Measuring the flex resting bar**
[here i will explain the resting bar measurement process]
-->




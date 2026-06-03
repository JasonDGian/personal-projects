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

## Action button ergonomics.
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

## Direction button ergonomics.




# Building a Custom Fightstick Controller
    
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/1c61ba26-ca54-4d73-951a-0f259d576594" />

   
---
   
# 🔸1. Introduction
## 1.1 Project Overview
Fighting games have been one of my favorite genres for a long time, and this project comes from wanting to build a controller that better fits the way I personally play.

While there are already many commercial fight sticks and MixBox-style controllers available, they often come with compromises in layout, ergonomics, size, or price. Instead of adapting to those limitations, I wanted to design something that matches my own preferences more closely.

This project focuses on building a custom MixBox-style arcade controller from the ground up, including the enclosure, input layout, and overall system integration. It combines Blender modelling, 3D printing, and basic electronics work to create a fully functional controller that can also be iterated on and improved over time.

Beyond just building it for myself, I’m also documenting the entire process. The goal is to create a clear record of the design decisions, prototypes, and mistakes along the way so that other people interested in building their own controllers can learn from it and potentially avoid some of the trial-and-error I went through.
   
## 1.2 Background and previous experience
This is not my first arcade controller project.

A few years ago, I built a custom controller for a friend, which gave me practical experience in Blender modeling, 3D printing, electronics wiring, and general prototyping. That project was relatively simple, but it helped me understand how small design decisions can have a big impact on usability and assembly.

For this project, I wanted to take things further by improving the overall design quality and focusing more on ergonomics, internal structure, and modularity. The goal was not just to build something that works, but something that feels more refined and intentional in its design.
    
## 1.3 Goals and Objectives
The goal of this project is to **build an ergonomic arcade controller** that feels good to use, works reliably, and is enjoyable during long play sessions, **while staying within a reasonable budget**.

**Key design goals include:**
- Keeping the controller compact and easy to transport
- Making the layout comfortable and reducing strain during extended use
- Designing it so internal parts are easy to access, repair, or replace
- Customizing the look and feel, including things like LED lighting
     
## 1.4 Constraints
Like any personal engineering project, the design was shaped by several real-world constraints.
   
**Budget and time:**  
The project had to remain affordable and manageable in scope, without expanding beyond what I could realistically design, print, and test.
   
**Manufacturing method:**   
The enclosure is fully 3D printed using FDM printing, which introduces limitations in terms of tolerances, surface finish, and mechanical strength. These constraints directly influenced design decisions throughout the project.
   
**Tournament legality:**   
Even though the controller is not exclusively designed for competitive play, I wanted it to follow common tournament rules. This means avoiding macros, turbo functions, or any form of input automation.
   
**Platform compatibility:**   
The controller needed to work on both PC and PlayStation 4 without requiring external adapters or custom firmware modifications.
   
**Portability:**   
The final design also had to remain compact and lightweight enough to be practical for transport and everyday use.
    
---
    
# 🔸2. Selection of components.

## 2.1 Motherboard - Base controller.
To simplify the project, I decided to use an existing wireless controller as the base platform instead of designing a custom PCB from scratch. This approach allows me to reuse features such as Bluetooth connectivity, battery management, charging circuitry, and PlayStation 4 compatibility, while focusing my efforts on the enclosure and custom input system.

Although designing a custom motherboard was considered, it would have significantly increased the project's scope and development time. Implementing and validating features such as wireless communication, power management, and console compatibility would have diverted attention from the main objective of the project: designing and building a custom arcade controller. Given the available time, reusing an existing controller was the most practical solution.

The selected controller is the T-29 Wireless Controller. During testing, it connected reliably to both PC and PlayStation 4 systems and automatically reconnected after being powered on. Compared to other controllers I evaluated, it offered more consistent connectivity and better overall usability.

Before selecting it, I inspected the PCB to verify that the button signals were accessible through test pads that could later be connected to the custom button layout. The T-29 provided sufficient access to these signals, making it suitable for modification.
   
<table>
    <tr>
        <th>Controller</th>
        <th>Motherboard</th>
    </tr>
        <td><img width="900" height="900" alt="OIP" src="https://github.com/user-attachments/assets/de0a148b-868f-4a2b-bfec-5acb7c08d841" /></td>
        <td><img width="1573" height="900" alt="controller-motherboard-stripped" src="https://raw.githubusercontent.com/JasonDGian/personal-projects/refs/heads/main/MIXBOX/IMG/controller-motherboard-stripped.png" /></td>
    </tr>
    <tr>
        <td>T29 Wireless Controller</td>
        <td>ZM-T29 MAB1437-B v1.2 (2025.09.29)</td>
    </tr>
</table>

>[!NOTE]
>Several cheaper alternatives were considered but ultimately rejected due to issues such as inaccessible PCBs, missing test pads, unreliable connectivity, or lack of PlayStation 4 compatibility. Although the T-29 was slightly more expensive at €27.99, it offered the best balance of reliability, modifiability, and cost.
    

</br>

Link to the product: [T-29 Wireless controller](https://www.amazon.es/dp/B0CBRC7MKL?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1)
        
## 2.2 Action buttons.
Selecting the action buttons turned out to be more difficult than I expected due to the huge number of available options. From the start, I knew I wanted LED-backlit buttons, both because I like their appearance and because they would support some customization ideas planned for later in the project.

To compare the available options, I tested several button sets in two sizes: 33 mm and 27 mm. Although all of them were functional, ergonomics and overall comfort quickly became the deciding factors.

After some testing, I ruled out the 33 mm buttons because they took up too much space and made it harder to achieve a compact layout. Among the 27 mm options, one set stood out immediately. Despite being the most expensive and using a large mounting nut that complicated installation, it felt noticeably better and had a higher-quality finish than the alternatives.

In the end, I chose set number 3 for the final design. The mounting challenge would later be addressed during the enclosure design process.

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

</br>

Link to the product: [Pssopp Microswitch button](https://www.amazon.es/dp/B08RC4JC1C?ref=ppx_yo2ov_dt_b_fed_asin_title)
   
## 2.3 Arrow buttons.
For the directional inputs, I chose mechanical keyboard switches and keycaps instead of traditional arcade buttons. Since the controller follows a MixBox-style layout, keyboard-style inputs provide a more natural and familiar solution.

Mechanical switches were selected over membrane alternatives due to their serviceability and ease of replacement. Using a hot-swap approach allows individual switches to be replaced without modifying the controller, improving long-term maintenance and user repairability, even if it adds complexity to the design.

During development, linear and tactile mechanical switches were tested using standard keycaps. However, the exact switch type was not a key design factor, as the system is intended to support any MX-compatible mechanical switch.

**The main design decision was between low-profile and full-height switches**, which affects ergonomics, input feel, and adapter.
   
<div align="center">
<img width="900" height="415" alt="cherry-mx-ultra-low-profile-sravnenie" src="https://github.com/user-attachments/assets/96b7a78a-b38c-4285-8ce2-f4538c1c67b5" />
</div>
   
   
Although low-profile switches would allow for a thinner design, full-height switches provided a better overall feel during testing. They also offer greater compatibility with standard keycaps and the wider mechanical switch ecosystem, improving long-term serviceability.
   
As a result, the final design uses full-height MX-compatible switches and standard keycaps for the directional inputs.
        
*Referenced datasheets:*
- https://cdn.shopify.com/s/files/1/0565/8070/2297/files/SPEC-KS-9H10B045NN-Y35-G_Red_PRO_2.0_Switch.pdf?v=1667273849
- https://cdn.shopify.com/s/files/1/0565/8070/2297/files/SPEC-KS-27H10B050NN-X5-Low_Profile_Red_Switch.pdf?v=1667274433
    
</br>

Link to the product: [10Pcs/lot Original Cherry MX Mechanical Keyboard Switch Axis Shaft Switch RGB blue](https://es.aliexpress.com/item/1005005467023965.html?spm=a2g0o.productlist.main.2.761c2154jAsrl2&algo_pvid=663d1580-1a2d-495c-8ce1-5936a79069a1&algo_exp_id=663d1580-1a2d-495c-8ce1-5936a79069a1-1&pdp_ext_f=%7B%22order%22%3A%22522%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21EUR%211.82%211.27%21%21%2113.89%219.72%21%402103890917815484233368128ea07e%2112000033197110242%21sea%21ES%21184981297%21X%211%210%21n_tag%3A-29919%3Bd%3Ae78d15fa%3Bm03_new_user%3A-29895&curPageLogUid=3OhXWIXwbvYz&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005005467023965%7C_p_origin_prod%3A)
  
     
# <mark>TODO</mark>   
<mark>Write section about keycaps types.**</mark></br>
<mark>R1,R2,R3,R4, how could this impact the project design and why R3 was chosen.**</mark>

## 2.4 Momentary switches for auxiliary functions.
Besides the main arcade controls, the controller also needs a few extra buttons for functions such as Home, Share, and Options. Since these buttons are not used as frequently as the gameplay controls, they offered a good opportunity to add some personality to the design without affecting the overall functionality of the controller.

For these functions, I chose a set of momentary push buttons that matched the look of the arcade buttons while helping to give the controller a more polished and finished appearance. Finding suitable options was fairly straightforward, as there is a huge variety of low-voltage buttons available online in different sizes, styles, and finishes.

The final choice came down mostly to aesthetics and how well the buttons fit with the rest of the design. Although they are small components, they play an important role in making the controller feel like a complete product rather than just a collection of parts.

>[!Note]
>At 1.94 € per button, these were one of the more expensive small components used in the build. Even so, I think the extra cost was justified, as they fit the design perfectly and helped achieve the overall look I was aiming for.

<table>
    <tr>
        <th>Available Colors</th>
        <th>Dimensions</th>
    </tr>
        <td><img width="600" alt="image" src="https://github.com/user-attachments/assets/e1b00aa4-d11b-47d2-bc8c-205475f7026e" />
</td>
        <td><img width="600" alt="image" src="https://github.com/user-attachments/assets/9857b338-31ad-4f37-97ad-5c03e7789e34" />
</td>
    </tr>

</table>

</br>

Link to the product: <a href="https://es.aliexpress.com/item/1005009763600457.html?spm=a2g0o.productlist.main.21.450b6311tFjwCL&algo_pvid=b312198c-d084-4474-8f0e-bfb33dbd1c6d&algo_exp_id=b312198c-d084-4474-8f0e-bfb33dbd1c6d-20&pdp_ext_f=%7B%22order%22%3A%221502%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21EUR%211.89%211.75%21%21%2114.52%2113.46%21%40211b65de17817129622565772e7b9b%2112000050090750520%21sea%21ES%21184981297%21X%211%210%21n_tag%3A-29919%3Bd%3Ae78d15fa%3Bm03_new_user%3A-29895%3BpisId%3A5000000209393528&curPageLogUid=f1lF8tP3KxVU&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005009763600457%7C_p_origin_prod%3A">12mm Metal Button Switch Waterproof 1NO 3A High Head Momentary Automatic Reset</a>

## 2.5 Base printing material.   
Since the enclosure would be entirely 3D printed, choosing the right material was an important decision. Several common FDM materials were considered, including PLA, PETG, and ABS.

Although PETG and ABS offer advantages in certain applications, this controller is not expected to experience high temperatures or significant mechanical stress. Because of that, the additional printing challenges associated with those materials did not provide much practical benefit.

For this reason, PLA became the most sensible option. It is easy to print, produces consistent results, and is more than strong enough for this application.
     
<table border="1px">
    <caption><i>Comparison of common FDM printing materials considered for the enclosure design.</i></caption>
    <thead>
        <tr>
            <th>Factor</th>
            <th>PLA</th>
            <th>ABS</th>
            <th>PETG</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>Print difficulty</strong></td>
            <td><strong>Low</strong></td>
            <td>High</td>
            <td>Medium</td>
        </tr>
        <tr>
            <td><strong>Warping tendency</strong></td>
            <td><strong>Low</strong></td>
            <td>High</td>
            <td>Low to Medium</td>
        </tr>
        <tr>
            <td>Heat resistance</td>
            <td>Low</td>
            <td>High</td>
            <td>Medium</td>
        </tr>
        <tr>
            <td>Strength</td>
            <td>High tensile strength, but brittle</td>
            <td>Impact-resistant</td>
            <td>Well-balanced</td>
        </tr>
        <tr>
            <td>Odor during printing</td>
            <td>Minimal</td>
            <td>Noticeable</td>
            <td>Low</td>
        </tr>
        <tr>
            <td>Stringing tendency</td>
            <td>Relatively low</td>
            <td>Moderate</td>
            <td>More prone to stringing</td>
        </tr>
        <tr>
            <td>Transparency</td>
            <td>Difficult</td>
            <td>Difficult</td>
            <td>Achievable</td>
        </tr>
        <tr>
            <td>Typical uses</td>
            <td>Prototypes, decorative parts, learning</td>
            <td>High-temperature and functional parts</td>
            <td>Functional parts, humid environments, general-purpose use</td>
        </tr>
    </tbody>
</table>
        
Afterward, the final decision was between standard PLA and High Speed PLA. Since the development process involved multiple prototypes and design iterations, reducing print time became an important factor. High Speed PLA allows parts to be produced significantly faster while maintaining good print quality, remaining fully compatible with the printer used for this project, and offering slightly improved impact resistance compared to standard PLA.
    
As a result, Anycubic High Speed PLA was selected as the printing material for all components.
    

<div align="center">
<table>
    <caption><i>Comparison between Standard PLA and High-Speed PLA.</i></caption>
    <thead>
        <tr>
            <th>Feature</th>
            <th>Standard PLA</th>
            <th>High-Speed PLA</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Typical Print Speed</td>
            <td>40–100 mm/s</td>
            <td>250–600+ mm/s</td>
        </tr>
        <tr>
            <td>Melt Flow Index (MFI)</td>
            <td>Low to Medium</td>
            <td>Very High</td>
        </tr>
        <tr>
            <td>Viscosity</td>
            <td>High (Thick)</td>
            <td>Very Low (Flows easily)</td>
        </tr>
        <tr>
            <td>Hotend Temperature</td>
            <td>190–220°C</td>
            <td>210–240°C (Generally higher)</td>
        </tr>
        <tr>
            <td>Cooling Requirement</td>
            <td>Standard part cooling</td>
            <td>High-power part cooling (essential)</td>
        </tr>
        <tr>
            <td>Mechanical Properties</td>
            <td>Stiff, but brittle</td>
            <td>Stiff, but tougher (better impact resistance)</td>
        </tr>
        <tr>
            <td>Visual Finish</td>
            <td>Often glossy</td>
            <td>Often matte or satin</td>
        </tr>
    </tbody>
</table>
</div>
     
*Referenced articles:* 
- [Comparison table](https://3dstarter.com/en/material/pla-vs-abs)
- [PLA vs PETG vs ABS](https://ultimaker.com/learn/petg-vs-pla-vs-abs-3d-printing-strength-comparison/)
- [Standard PLA vs High Speed PLA](https://3dprintingcanada.com/blogs/news/pla-vs-high-speed-pla-whats-the-real-difference?shpxid=c09efa71-5de1-4c63-8740-651b2d3c38b0)

</br>

Link to the product: [Anycubic High Speet PLA - Mate Grey 1Kg Spool](https://uk.anycubic.com/products/high-speed-pla-filament?variant=46608821616925)
   

## 2.6 Other small elements.
Other supporting components such as terminal blocks, connectors, and wiring will also be documented throughout the project where relevant. Since these parts are relatively standard, they will not receive dedicated sections unless a particular design decision requires further explanation.
    
---
   
# 🔸3. Design and Prototyping
<!-- the design chapter is organized around individual subsystems (buttons, motherboard housing, LED module, directional controls)--> 
## 3.1 Design Strategy
Rather than designing the entire controller as a single assembly from the start, I divided the project into several smaller subsystems and developed them individually before integrating them into the final design.

**The main subsystems were:**
- Directional input block
- Action button array
- Motherboard enclosure
- LED module housing
- Auxiliary functions button console
        
Each subsystem was designed, prototyped, tested, and refined independently. This made the development process easier to manage and allowed design issues to be identified and corrected without affecting unrelated parts of the controller.
   
Once all subsystems had been validated, they were combined into a complete assembly. Several additional iterations were then carried out to refine the integration between components, improve clearances and accessibility, and arrive at the final controller design.
        
### 3.1.1 Modelling and Prototyping Methodology.
Most of the design work in this project follows the same workflow: measure the component, validate the measurements, create a digital reference model, and then design the surrounding parts around that model.

Rather than trying to measure and model an entire component in one step, I usually break it down into individual profiles or "sides". For each profile, I create a simple negative geometry and 3D print it to test the fit against the real component. This allows me to verify dimensions early and catch measurement errors before spending time modeling more complex geometry.

Once all the individual profiles have been validated, I combine them into a complete negative model and perform another test fit. If the final negative matches the physical component correctly, I then reconstruct the corresponding positive model in Blender.

The positive models are not intended to be perfect replicas. Their purpose is to serve as accurate references during the design process. Having digital versions of the PCB, buttons, switches, battery, and other components makes it much easier to experiment with layouts, check clearances, and understand how everything will fit together inside the enclosure.

This approach allows me to build a virtual prototype before printing the final parts. By arranging the reference models in Blender, I can evaluate spacing, assembly requirements, and overall ergonomics while making design changes much more quickly than through physical prototyping alone.
   
>[!Note]
> Although this process takes extra time at the beginning, it usually saves time later by reducing failed prints and minimizing the number of design iterations needed to reach a working solution.
   
_Prototyping workflow diagram_   
<img width="1313" height="364" alt="image" src="https://github.com/user-attachments/assets/84126c58-6f34-41ba-a83c-7648af24f34e" />
<!--img width="1066" height="421" alt="image" src="https://github.com/user-attachments/assets/cd6d1fda-48f4-40e2-bd62-a442324850ea" /-->
    
The modelling and validation process described above worked well for most components. The control layout, however, depended as much on comfort as it did on dimensions. To guide the design of the action buttons and directional inputs, I first carried out a simple ergonomic study using my own hands as a reference.
    
### 3.1.2 Ergonomic Layout Development
Before starting any design work, I carried out a simple ergonomics study using my own hands as the main reference. The goal was to understand how my fingers naturally rest and move, and use that as the starting point for the layout instead of relying on a standard fightstick template.

The process was intentionally simple: I used a flat sheet of paper and explored different relaxed hand positions while simulating common inputs. This helped me identify natural finger alignment, comfortable spacing, and how my wrist prefers to sit when the hand is not forced into an artificial posture. I started with the action buttons arrays and then followed with the directional input block.
         
**The process:**

1. I placed my hands on a sheet of paper and allowed my fingers to settle into a relaxed position. The overall shape resembled a slightly curved claw or the posture used when holding a baseball.
<!--img width="1241" height="823" alt="image" src="https://github.com/user-attachments/assets/d21e828c-a8a7-4cc2-bfd5-5c44942ccb20" /-->
<img width="1554" height="900" alt="ergonomics" src="https://github.com/user-attachments/assets/ea21dbd3-6ff5-40be-8a89-858dbfd8d0ce" /> 
      
2. Once my hands felt comfortable, I moved my fingers repeatedly and readjusted them until they consistently returned to the same resting position. I then marked the points where my fingertips contacted the paper. The resulting pattern resembled two slightly tilted arches and became the starting point for both the action button array and the directional input block.
<img width="1274" height="635" alt="hands_ergonomics_study_1 (1)" src="https://github.com/user-attachments/assets/09be789c-73ce-4c06-b654-a7f89d98583e" />
<!--img width="1554" height="900" alt="ergonomics_study_1" src="https://github.com/user-attachments/assets/7e0fd43c-d5be-4650-916e-fcdbc00216b3" /-->  
       
3. After tracing the primary action button positions, I repeated the process with my fingers in a slightly more closed position while maintaining comfort. This produced a second set of contact points, which later became the basis for the secondary action button array.
<img width="1274" height="617" alt="hands_ergonomics_study_2" src="https://github.com/user-attachments/assets/0f61a95e-268e-4f71-8d42-24cf3965d7ed" />
   
4. Using these markings as a reference, I created the first ergonomic prototype in Blender.
<img width="1125" height="694" alt="ergonomics_proto_design" src="https://github.com/user-attachments/assets/4afa50fa-a055-4dde-85ce-b0974755a993" />    
    
5. To validate the design before committing to a full print, I produced a small test piece containing only the button layout. This allowed me to evaluate spacing, reachability, and overall comfort while minimizing both print time and material usage.
<img width="1554" height="900" alt="ergonomics_prototype_1" src="https://github.com/user-attachments/assets/65edc0cc-0215-4e6f-9068-a90db07faa1f" />
   
_Test piece used to validate_
<img width="1554" height="900" alt="ergonomics_proto_1" src="https://github.com/user-attachments/assets/bd6c3bd3-2dc2-4114-86e9-768225cd480e" />

6. After reaching a satisfactory result for the action buttons, I applied the same methodology to the directional input system. During this phase, I experimented with several layouts, including non-standard key arrangements. While some of these alternatives felt comfortable in isolation, I ultimately returned to the more conventional cursor-key configuration, with three keys in a row for left, down, and right, and a fourth key above for up.
    
_Considered key configurations_
<img width="2750" height="480" alt="tested_layouts" src="https://github.com/user-attachments/assets/86d53073-6f36-433d-bc02-82a0cdfe37b9" />

The most important result of this stage was not the exact directional key arrangement, but its position relative to the action buttons. Like the action side, the directional inputs naturally settled into a slightly inward-rotated orientation, which would feel more comfortable during extended use.

**Key observations from this study:**
- My fingers naturally fall into a slightly staggered alignment rather than strict straight columns
- There is a clear trade-off between tighter spacing, which improves speed, and wider spacing, which reduces accidental inputs.
- The thumb has a more limited comfortable range of motion than expected.
- My wrists feel most natural when the hands are rotated slightly inward.
    
I did not treat these observations as precise measurements, but as practical design constraints. They served as the baseline for the action button and directional input layouts that are developed in the following sections.

> [!IMPORTANT]
> This process significantly reduced the amount of guesswork involved in the design. Instead of adapting my hand to a predetermined layout, the layout was designed around my hand. The resulting prototype also established several dimensional constraints that would later influence the selection of the action buttons themselves.
    
---

## 3.4 Motherboard housing.
This component is a custom enclosure designed to house the controller's motherboard after it has been removed from the original controller shell. Its primary purpose is to **protect the motherboard and the wires soldered to its test pads**, which are particularly vulnerable to mechanical stress.

The enclosure also provides **mounting points for the terminal blocks** used to connect the button wiring via screw terminals. In addition, it serves as the primary **mounting interface between the motherboard assembly and the MixBox enclosure**, while providing basic protection for the battery and associated wiring.

### 3.4.1 Reference model creation.
This section describes how I created the reference model used for further design.
    
#### 3.4.1.1  Rough external shape.
The first step was to capture the motherboard's overall outline. The objective was not to create a perfect digital twin but rather a sufficiently accurate approximation that could serve as a reliable design reference.

To maintain consistency throughout the measurement process, I selected a single fixed reference point: the bottom-left corner of the motherboard. Whenever possible, all measurements were taken relative to this point. Using a common reference minimized the risk of cumulative measurement errors and simplified later corrections.

After sketching the motherboard outline and recording the dimensions, the information was transferred into Blender, where the initial 2D profile was created.
    
>[!NOTE]
>The paper sketch does not need to be perfectly scaled or highly detailed. Its main purpose is just to record measurements in a clear and structured way. The actual accuracy comes from the digital modelling stage.
    
_Drawing showing the dimensions of the motherboard._
<img width="1642" height="900" alt="motherboard_paper_measures" src="https://github.com/user-attachments/assets/28a842e4-a96b-478f-a692-4df0da457ad2" />
   
#### 3.4.1.2 Translating the measurements into Blender.
Once the measurements had been collected, I recreated the motherboard outline in Blender using the recorded dimensions. At this stage, the model was intended to match the measured geometry as closely as possible, without any additional tolerance applied.

This initial version served as the baseline from which all future fitting tests and adjustments would be made.
    
_Dimensions transferred into Blender to create the initial motherboard profile._
<img width="1235" height="770" alt="image" src="https://github.com/user-attachments/assets/2251d7b0-587f-47a3-af92-c58a49852390" />
    
#### 3.4.1.3 Profile dimensions validations.
Instead of testing the full model at once, I validated it in stages. Breaking it down like this made it much easier to locate issues and adjust specific areas without affecting the rest of the geometry. 
**The validation followed this order:**
- Each side was checked individually
- The left and top sections were combined and tested
- The right side was added and validated
- The full outline was assembled and tested
   
For each iteration, I printed a test piece and physically checked the fit against the motherboard. These parts were not meant to represent the motherboard itself — they were the negative geometry, meaning the cavity the motherboard would eventually sit in. This allowed me to test the enclosure fit directly, while keeping print time and material use low.
   
After each test fit, I noted any areas that needed adjustment, updated the model in Blender, and printed a new iteration. Throughout the entire process, I kept a single reference vertex as the fixed origin. This made sure that any changes stayed consistent and didn’t unintentionally shift dimensions that had already been validated.
   
_Test-fitting a printed section and documenting areas requiring correction._
<img width="1385" height="900" alt="image" src="https://github.com/user-attachments/assets/3b9a1473-c3c0-4f5b-8466-673b2bf19619" />
   
>[!Important]
>Using a fixed reference point throughout all iterations was essential to avoid drifting dimensions and to keep the model stable as changes were made.
   
#### 3.4.1.4 Modelling the final positive.
Once the external outline was validated and fitted correctly, I moved on to modelling the remaining motherboard features. I followed the same workflow here, applying the same tolerance and measurement approach to ensure consistency across the entire model.
    
By the end of this process, I had a fully validated motherboard reference model that I could confidently use for designing the enclosure and mounting system. With the tolerances accounted for, the final printed test fits required little to no additional adjustment.
      
_Approximate motherboard model used as the reference geometry for the enclosure design._
<img width="1774" height="766" alt="image" src="https://github.com/user-attachments/assets/a097c115-bde5-4a28-ab63-93c36b04bfa9" />
     
By using the validated motherboard reference model and incorporating the defined tolerance values, the final printed test piece fits as intended, requiring little to no additional adjustment.
   
_Final test piece_
<img width="1774" height="676" alt="image" src="https://github.com/user-attachments/assets/d5ac14ff-fc4a-4f6c-a5f6-983a98d9e2f8" />
   
### 3.4.2 Initial housing design and prototype.
Before starting the design draft, I first determined how many terminal blocks would be required based on the motherboard model I had selected. Since each terminal block provides two connections, I began by counting all the motherboard test pads that would need to be accessed.

Including the ground connections, I identified approximately 42 signals that would need to be routed from the motherboard to the buttons and LED system. This meant that a minimum of 21 terminal blocks would be required. To provide some flexibility for future modifications and unexpected wiring needs, I added two additional terminal blocks, increasing the total capacity to 46 connections.

This requirement became one of the main constraints that shaped the initial design of the enclosure.
   
_Identified connections_   
<table>
    <tr>
        <td>LA</td>
        <td>AR</td>
        <td>AD</td>
        <td>AL</td>
        <td>AU</td>
        <td>BT1</td>
        <td>KL3</td>
    </tr>
    <tr>
        <td>LX</td>
        <td>KR3</td>
        <td>RX</td>
        <td>RY</td>
        <td>TRI</td>
        <td>SDA0</td>
        <td>KR2</td>
    </tr>
    <tr>
        <td>3.3v</td>
        <td>BT</td>
        <td>RES1</td>
        <td>VDD</td>
        <td>FORK</td>
        <td>SCL0</td>
        <td>5V</td>
    </tr>
    <tr>
        <td>TOUCH</td>
        <td>D-</td>
        <td>D+</td>
        <td>PASD</td>
        <td>KL2</td>
        <td>BL</td>
        <td>INT</td>
    </tr>
    <tr>
        <td>GR</td>
        <td>RE</td>
        <td>PAR</td>
        <td>SQU</td>
        <td>KR1</td>
        <td>KL1</td>
        <td>SDA1</td>
    </tr>
    <tr>
        <td>5V</td>
        <td>SCL1</td>
        <td>P23</td>
        <td>SHA</td>
        <td>GND</td>
        <td>3.3v</td>
        <td>RSE</td>
    </tr>
</table>
    
With these requirements established, I cloned the reference models in Blender and began arranging the main components within the available space. The minimum set of components that needed to be accommodated consisted of:
- The motherboard
- The battery
- Twenty-three terminal blocks

The goal of this stage was not to create the final enclosure, but rather to understand how these components could be positioned relative to one another while maintaining access to important motherboard features such as the USB-C port and headphone jack, minimizing the occupied space.

After experimenting with several layouts, I settled on a preliminary arrangement for the battery, motherboard, and terminal blocks. Once I was satisfied that the major components could coexist without interfering with one another, I began designing the first test for the enclosure itself.
    
<table>
    <caption><i>Initial Blender component layout.</i></caption>
    <tr>
        <td rowspan="2"><img width="1350"  alt="mobo-1" src="https://github.com/user-attachments/assets/dd5d3c9b-e249-48ea-b288-0d429fecd4f5" /></td>
        <td><img width="500" alt="image" src="https://github.com/user-attachments/assets/feddf8f6-828d-4d1b-a732-dcae8a87cec5" />
</td>
    </tr>
    <tr>
        <td><img width="500" alt="image" src="https://github.com/user-attachments/assets/b584ce71-21b0-4db5-a8ec-00515da25339" />
    </td>
    </tr>
</table>
    
The first step was creating a base plate that would support the motherboard. Openings were added to ensure the analog sticks would not collide with the structure, followed by mounting features to hold the PCB in place. I then incorporated multiple wire-routing holes near the test pad locations. Providing several routing options gave greater flexibility when soldering and organizing the wiring later in the project.

<table>
    <th colspan="2">
        Base plate with openings.
    </th>
    <tr>
        <td><img width="1421" height="678" alt="mobo-2" src="https://github.com/user-attachments/assets/ae368053-872e-4185-8091-2aeebc1f60d9" /></td>
        <td><img width="1421" height="678" alt="mobo-3" src="https://github.com/user-attachments/assets/36c0af8e-cd5e-4694-8059-d58df1379802" /></td>
    </tr>
    <tr>
        <th colspan="2">
            Routing paths (red color).
        </th>
    </tr>
    <tr>
        <td><img width="1421" height="824" alt="mobo-4" src="https://github.com/user-attachments/assets/1a4eff92-14f8-4396-b94b-ddf63442425f" /></td>
        <td><img width="1421" height="824" alt="mobo-5" src="https://github.com/user-attachments/assets/1bfbbfa6-eeb8-4d4c-8e34-6d72d73adfb7" /></td>
    </tr>
</table>

The resulting prototype consisted of a simple base structure featuring PCB supports, analog stick clearance openings, wire-routing holes, and mounting locations for the terminal blocks. Although far from the final design, this first iteration served as an important proof of concept by allowing me to evaluate component placement, space requirements, and overall feasibility before investing additional time in more complex geometry.

<table>
    <th colspan="2">
        Base plate starting point.
    </th>
    <tr>
        <td><img width="1450" height="824" alt="mobo-8" src="https://github.com/user-attachments/assets/a00d2d60-8df3-4b6a-97d4-160c82785170" /></td>
        <td><img width="1450" height="824" alt="mobo-9" src="https://github.com/user-attachments/assets/f8e605cf-4bf8-40c9-9b65-eb8869c4fdb3" /></td>
    </tr>
</table>

**Testing the prototype revealed several issues:**
- The PCB mounting holes were correctly sized, but the terminal block mounting holes required a slight increase in diameter.
- Due to the height of the base plate, insufficient metal from the terminal blocks was exposed for comfortable soldering. The base plate height should be reduced by at least 1 mm.
- One support pillar interfered with a nearby IC, creating an uneven support surface. Tightening the PCB in this condition would likely introduce stress and risk damaging the board.
- The available space between the battery, terminal blocks, and PCB was insufficient to accommodate the protective lid planned for the enclosure.

**These observations confirmed that the concept was viable while identifying the dimensional and layout changes required for the next iteration. They also showed that the enclosure would need to be larger than initially intended, with additional space sacrificed in favor of protection, serviceability, and reliable PCB support.**
    
    
<table>
    <caption><i>Initial test results.</i></caption>
    <tr>
        <td>
            <i>Mounted terminal blocks.</i><br>
            <img width="2000" height="780" alt="image" src="https://github.com/user-attachments/assets/90558ae0-7338-468f-89d1-819a5c50397b" />
        </td>
        <td>
            <i>Insufficient pin surface.</i><br>
            <img width="2000" height="780" alt="image" src="https://github.com/user-attachments/assets/a7edb3e5-e020-460f-942f-118e21736ed7" />
        </td>
        <td>
            <i>Overall look</i>
            <img width="2000" height="900" alt="mobo-test-drive" src="https://github.com/user-attachments/assets/1d6a0732-0612-428e-bd24-1fa08f78abf3" />
        </td>
    </tr>
</table>

### 3.4.3 Design iteration and tweaks.
Based on the observations from the first prototype, I implemented several corrections before continuing the development of the enclosure.

The changes included:
- Increasing the diameter of the terminal block mounting holes.
- Reducing the base plate thickness around the terminal blocks area to expose more metal for soldering.
- Increasing the available space allocated to the battery.
- Reshaping the support pillar that was interfering with an integrated circuit on the motherboard.
     
With the initial fitting issues out of the way, I could begin working on the remaining features required to complete the enclosure. These included:
- A method for securing the motherboard enclosure to the mixbox internal body.
- A method to protect and secure the battery to the enclosure.
- A protective lid for the motherboard and wiring.
     
>[!IMPORTANT]
>**About the battery holder**    
>The battery required special attention compared to the other internal components. **Li-Po batteries are sensitive to mechanical stress and can expand slightly during normal operation while reaching temperatures of around 50 °C**. Because of this, the holder needed to keep the battery securely in place without applying excessive pressure while remaining suitable for the expected operating temperatures. These constraints became the main design requirements for the battery retention system.


<table border="1" cellspacing="0" cellpadding="8" style="border-collapse: collapse; width: 100%;">
    <thead>
        <tr>
            <th>Version</th>
            <th>Description</th>
            <th>Key Issues / Outcome</th>
            <th>Picture</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>Version 1</strong></td>
            <td>
                The initial design was overly rigid, lacked flexibility, was not compact,
                and provided little accommodation for battery expansion or ventilation.
                Although the enclosure was oversized and allowed the battery to move
                freely without significant mechanical pressure, battery swelling remained
                a concern.
            </td>
            <td>
                A swollen battery could become lodged within the enclosure, creating
                potential safety concerns and making battery removal difficult.
            </td>
            <td>
                <img width="400" alt="BatteryHolderV1" src="https://github.com/user-attachments/assets/f19f98fa-5eb4-4288-ad6c-5a47ac2233c7" />
            </td>
        </tr>
        <tr>
            <td><strong>Version 2</strong></td>
            <td>
                I based this iteration on a dual spring-loaded retention mechanism
                intended to keep the battery securely in place while accommodating
                dimensional variations.
            </td>
            <td>
                The design proved overcomplicated and required additional space. The benefits did not justify the added complexity,
                so further development was abbandoned.
            </td>
            <td>
                <img width="400" alt="BatteryHolderV2" src="https://github.com/user-attachments/assets/0a960208-c401-48d1-955f-6fb1b2019d8e" />
            </td>
        </tr>
        <tr>
            <td><strong>Version 3</strong></td>
            <td>
                This version focused on simplicity by using hooks and elastic bands
                to secure the battery. The concept provided flexibility and adjustable
                mechanical pressure while minimizing the number of components.
            </td>
            <td>
                The concept worked in principle, but after looking into the long-term effects of heat on elastic materials, I realized elastic bands were not a viable solution. Heat and aging gradually degrade the material, causing it to lose elasticity and retention                  force. Eventually, the bands would no longer be able to secure the battery reliably.
            </td>
            <td>
                <img width="400" alt="BatteryHolderV3" src="https://github.com/user-attachments/assets/37bbfb5e-b2f9-4ea8-bd08-4462665d6b3d" />
            </td>
        </tr>
        <tr>
            <td><strong>Version 4</strong></td>
            <td>
This version uses a thin PLA strip secured between two PLA blocks with screws, which are in turn attached to the main motherboard enclosure base plate. The thin strip acts as a flexible retention mechanism, applying gentle pressure to keep the battery securely in place.

This iteration became the foundation of the final design. From this point onward, development was limited to minor refinements and dimensional adjustments. The design provides secure battery retention while maintaining enough flexibility to accommodate small variations in battery size, and the use of PLA eliminates the long-term degradation concerns associated with elastic materials.
            </td>
            <td>
                Battery retention force can be adjusted using plastic spacers or
                compressible materials such as foam, allowing the mechanical pressure
                applied to the battery to be increased or reduced as needed.
            </td>
            <td>
                <img width="400" alt="BatteryHolderV4" src="https://github.com/user-attachments/assets/372c0ff2-2d8b-4b0a-9063-f40c26093b8f" />
            </td>
        </tr>
    </tbody>
</table>
   
      
_Second iteration virtual assembly_        
<img width="1191" height="764" alt="mobohol-second-gif" src="https://github.com/user-attachments/assets/1442e1d2-5750-4eae-8ae6-71b7a4d9f615" />
    


**Iteration 2 results**    
After assembling and testing the second iteration, a few design oversights became obvious. None of them were particularly difficult to fix, but they exposed a gap between the Blender model and the actual hardware. Most of these problems can be traced back to the reference model I was working from, which was missing the battery connector and rear button assemblies.

<table>
    <caption><i>Issues found and solutions applied</i></caption>
    <tr>
        <td>
            <strong>Battery Retention</strong></br>
            Although the battery fit within the designed enclosure, testing revealed that it was still able to move laterally inside the compartment. This resulted in unwanted movement ("dancing") during handling.   
To resolve this, I designed an additional 'blocker' integrated into the protective lid of the enclosure that sits alongside the battery and prevents side-to-side displacement, securing it more reliably.
        </td>
        <td>
        <i>New blocker to prevent lateral movement.</i></br>
        <img width="802" height="778" alt="image" src="https://github.com/user-attachments/assets/0e1c3be5-b255-4a4b-97e9-7ff121e9bf41" />
        </td>
    </tr>
    <tr>
        <td>
            <strong>Lid Clearance Oversight</strong></br>
            During the design of the lid, I completely overlooked two components mounted on the motherboard:
            <ul>
                <li>The battery connector.</li>
                <li>The rear button assemblies.</li>
            </ul>
                As a result, the first printed lid collided with both features and could not be installed correctly. The revised lid addresses this issue by increasing the internal height of the enclosure and adding the necessary cutouts to provide adequate clearance.
        </td>
        <td>
        <i>Revised lid with the necessary cutouts</i></br>
        <img width="1000" alt="motherboard_revised_lid" src="https://github.com/user-attachments/assets/16c9a3ff-8f0a-4daf-aee6-4b2c1b24d3ae" />
        </td>
    </tr>
    <tr>
        <td>
            <strong>Terminal Block Positioning</strong></br>
            While increasing the height of the base plate, I also adjusted the position of the terminal blocks to better match the real hardware. During this process, I unintentionally shifted them too far, failing to account for the terminal blocks' locking mechanism.
The new position causes the locking tabs of one cluster to interfere with the adjacent cluster, preventing proper installation. This will require repositioning the terminal blocks to restore the necessary clearance while maintaining dimensional accuracy.
        </td>
        <td>
        <i>Locking mechanism colliding with adjacent cluster.</i></br>
        <img width="1000" alt="unaccounted_locking_system" src="https://github.com/user-attachments/assets/2f310ada-2505-425a-bb47-0df097ec00f9" />
        </td>
    </tr>
</table>
 
**Takeaways**    
This iteration reinforced the importance of validating the Blender model against the actual hardware throughout the design process. Several of these issues resulted from focusing on the primary geometry while overlooking secondary features such as connectors, locking mechanisms, and component tolerances. Future iterations should include a systematic interference check before printing to catch these types of collisions earlier.

<!--
<table>
    <thead>
        <tr>
            <th>Issue and Description</th>
            <th>Corrective Action</th>
            <th>Evidence</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
                <strong>Lid Clearance</strong></br>
                The battery connector and rear button assemblies were overlooked
                during modelling, causing the first printed lid to collide with
                both components.
            </td>
            <td>
                Increased the lid height and added clearance cutouts.
            </td>
            <td>
                <img
                    src="https://github.com/user-attachments/assets/530d3c4d-81e5-4bbf-9f78-111af19d05cc"
                    alt="Revised lid"
                    width="500">
            </td>
        </tr>
        <tr>
            <td>
                <strong>Battery Retention</strong></br>
                The battery could move laterally inside the enclosure during
                handling.
            </td>
            <td>
                Designed a side spacer to eliminate lateral movement.
            </td>
            <td>
                <img
                    src="https://github.com/user-attachments/assets/0b19e5e5-a9b7-4019-8730-ab85b452ee49"
                    alt="Battery spacer"
                    width="500">
            </td>
        </tr>
        <tr>
            <td>
                <strong>Terminal Block Positioning</strong></br>
                The locking tabs of one terminal block cluster interfere with the
                adjacent cluster after repositioning.
            </td>
            <td>
                Reposition the terminal blocks to restore the required clearance.
            </td>
            <td>
                <img
                    src="https://github.com/user-attachments/assets/e9ff55a5-3798-4f2f-ab4d-a6d094ac2c5b"
                    alt="Terminal block collision"
                    width="500">
            </td>
        </tr>
    </tbody>
</table>
-->

_Third iteration virtual assembly_    
<img width="1191" height="764" alt="mobohol-third-iteration-gif" src="https://github.com/user-attachments/assets/9ab70a7d-114f-4a87-bf54-f4e728cf5aa6" />


**Iteration 3 results**    
After assembling and testing the third iteration, only one minor design issue became apparent. The battery side stops also serve as the mounting features for the protective lid, housing the screws that secure the lid to the motherboard holder.

While resizing these features to provide slightly more generous battery tolerances and better control of lateral movement, I overlooked the space required for the mounting screws. As a result, the internal clearance of the mounting feature became too small for the screw heads to fit properly during assembly.

The issue was straightforward to resolve by slightly increasing the internal dimensions of the mounting features. This restored the required screw clearance while preserving their secondary function as battery side stops.

<i>Screw clearance issue.</i><br> 
    <img width="2415" height="817" alt="clearance issues" src="https://github.com/user-attachments/assets/9b67905e-e908-4cb6-981f-405ff3144609" />
</td>

<!--table>
    <caption><i>Issues found and solutions applied</i></caption>
    <tr>
        <td> <strong>Screw clearance issue.</strong><br><br>
            To restore the required screw clearance, two of the walls of the mounting feature had to be made thinner in order to preserve the battery tolerances. To compensate for the reduction in wall thickness, I added internal bevels that reinforce the structure. These bevels form two opposing U-shaped ribs that meet in the middle, increasing rigidity around the screw without significantly affecting the available clearance.
        </td>
        <td>
         <i>Screw clearance issue.</i><br> 
            <img width="2415" height="817" alt="clearance issues" src="https://github.com/user-attachments/assets/9b67905e-e908-4cb6-981f-405ff3144609" />
        </td>
    </tr>
</table-->
 
**Takeaways**   
This iteration highlighted the importance of paying close attention to multi-purpose features. A seemingly minor dimensional change made to improve one function can unintentionally affect another. In future iterations, any feature serving more than one purpose should be reviewed to ensure all of its functional requirements are still met after modifications.
        
### 3.4.4 Final housing.
After implementing the changes identified during the previous design iterations, I arrived at the final version of the motherboard housing. The completed design combines the motherboard support, battery retention system, terminal block mounts, and protective lid into a single assembly that fulfils the original design objectives while remaining serviceable.
      
The motherboard is supported at multiple locations to minimise PCB flex while avoiding contact with sensitive components or obstructing wire routing paths. The validated reference model ensured that the USB-C port, headphone jack, and other key features remained correctly aligned with the enclosure.
       
_Enclosure complete assembly_
<img width="2000" height="900" alt="mobo-holder-printed-2" src="https://github.com/user-attachments/assets/dc1af6dc-e4ba-4bf0-91eb-834724e42bc2" />
        
The enclosure accommodates twenty-three terminal blocks, allowing all required signals to be connected through screw terminals. The removable lid protects the motherboard and solder joints while still allowing easy access for maintenance or future modifications.
     
_Final internal layout._
<img width="2000" height="900" alt="mobo-holder-printe-1" src="https://github.com/user-attachments/assets/3435296f-d6ac-473a-99b8-b093cbc19daa" />
          
Battery retention is provided by the flexible PLA strip developed during the final design iteration. Together with the side supports integrated into the lid, it keeps the battery securely positioned without applying excessive pressure.
        
_Battery retaining mechanism_
<img width="1920" height="864" alt="remarked-side-blocker-gif" src="https://github.com/user-attachments/assets/6d284c0a-c4e1-47d9-940c-c34bcc6867d4" />
       
The final enclosure mounts directly to the internal MixBox structure using dedicated mounting points, allowing the complete assembly to be installed or removed as a single unit.
   
<mark>TODO: PICTURE OF MOUNTED MOBO</mark>
        
Overall, the final design is the result of several prototype iterations and physical validation. Although most of the changes between iterations were relatively small, they significantly improved the reliability, serviceability, and overall fit of the enclosure, resulting in a practical solution ready for integration into the completed MixBox.

## 3.4 Action button array.
The action button array consists of the buttons used to perform attacks and other in-game actions, such as punches and kicks. Together with the directional controls, these are the buttons that see the most frequent use during gameplay, making their placement and ergonomics particularly important. The action buttons array must be comfrotable to use, well positioned, as compact as possible and they must easily replaceable in case of malfunction or being eroded by use. Easy to service and replace in case of customization needs. 
 
### 3.4.1 Initial design.
### 3.4.2 Prototyping and testing.
### 3.4.3 Final Design.

## 3.4 Led module enclosure (led module surrounding geometry).
### 3.4.1 Modeling the positive for reference
### 3.4.2 Modeling the enclosure.

## 3.5 Directional input block
One of the main design goals for the directional input block was to **avoid soldering wires directly to the mechanical keyboard switches**. Although this would have been the simplest solution, it would make replacing a faulty switch inconvenient, as every replacement would require desoldering and resoldering the connections.

Instead, I wanted the directional input block to follow the same philosophy as modern mechanical keyboards by using a hot-swappable mounting system. This would allow switches to be replaced easily for maintenance or swapped for different models without modifying the wiring. Since mechanical switches are available with different actuation forces, tactile feedback, and sound profiles, having the ability to experiment with different switch types was an important design objective.

Before beginning the design, I researched different mounting methods and discovered the use of hot-swap sockets. A hot-swap socket is a small connector that is soldered to a PCB and allows a mechanical keyboard switch to be installed or removed without soldering the switch itself. This makes switch replacement quick while keeping the electrical connections permanently attached to the socket. **Since this matched my design goals perfectly, I decided to base the directional input block around this component.**
    
*Hotswap Socket*
<img width="2388" height="900" alt="hss-socket-picture-4" src="https://github.com/user-attachments/assets/87dad44d-551a-4b70-a7e2-e026d6bf5559" />
        
## 3.5.1 Reference model creation. 

Following the same workflow used throughout the rest of the project, I first created reference models of the main components before designing the surrounding geometry. This allowed me to develop the later parts of the directional input block around semi-accurate representations of the real hardware.
       
The first step was measuring the main components required for the directional input block: the hot-swap socket, mechanical keyboard switch, and keycap. The objective was not to create perfect replicas, but models accurate enough to support the design of the surrounding parts.
     
I started with the hot-swap socket, as it was both the smallest and most challenging component to measure, while also being the key element that defined the rest of the design. Due to its irregular shape and small dimensions, obtaining accurate measurements was considerably more challenging compared with the larger components.
    
<table>
    <caption><i>Rough measures on a 10:1 scale drawing.</i></caption>
    <tr>
        <td><img width="2339" height="1130" alt="medidas-hss1" src="https://github.com/user-attachments/assets/b9e2d839-0b12-41e8-822c-bceac6494d8b" /></td>
        <td><img width="2339" height="1130" alt="medidas-hss2" src="https://github.com/user-attachments/assets/147000fe-3b8c-4af2-8edc-836bb4d94d10" /></td>
    </tr>
</table>
    
Once all measurements were taken, I recreated the geometry in Blender. To account for possible measurement errors and the tolerances introduced during 3D printing, I included a small amount of clearance in the initial model.
    
<table>
    <caption><i>Initial Blender model created from the measured geometry.</i></caption>
    <tr>
        <td><img width="1080" height="858" alt="model-hss2" src="https://github.com/user-attachments/assets/958e0904-de85-40b2-b07e-6f239a7852c6" /></td>
        <td><img width="1080" height="858" alt="model-hss1" src="https://github.com/user-attachments/assets/29f04de2-ac70-4729-bac2-b212238a345f" /></td>
    </tr>
</table>

After creating the first version of the model, I validated it using the same negative-geometry workflow described earlier in the report. A test piece containing the socket cavity was printed and fitted against the real component to verify whether the dimensions were correct. The first validation test revealed several dimensional errors that were not obvious during the modelling stage. After adjusting the affected measurements and producing a second iteration, the socket achieved an almost perfect fit.

<table>
    <caption><i>Negative geometry based tests.</i></caption>
    <tr>
        <td><img width="2000" height="900" alt="HSS - test iterations" src="https://github.com/user-attachments/assets/43c0415b-a8f6-4669-a2b2-8066c4641a5b" /></td>
    </tr>
</table>
   
I then repeated the same process for the mechanical keyboard switch and the keycap. Each component was measured, modelled, and validated individually before being used during the design of the final directional input block.
    
<table>
    <caption><i>Keyboard switch and Keycap models.</i></caption>
    <tr>
        <td><img width="2000" height="568" alt="keyboard_switch_last_version" src="https://github.com/user-attachments/assets/f0c3575d-67ad-4e7d-b229-e5f39205664f" /></td>
    </tr>
    <tr>
        <td><img width="2000" height="568" alt="models with reference image" src="https://github.com/user-attachments/assets/411a62a9-b8e7-43dd-b777-6b98dedecf88" /></td>
    </tr>
</table>
         
>[!NOTE]
>Having validated reference models for all three components allowed me to test different mounting concepts, verify clearances, and iterate on the directional input block design with greater confidence.

## 3.5.2 Designing the switch & socket retention module.
Designing the switch and socket housing turned out to be the most challenging part of the directional input block. Although the geometry of a mechanical keyboard switch is relatively simple, achieving the correct fit is surprisingly sensitive to small dimensional errors. Even minor changes in clearance can prevent the switch from locking into place correctly or make it difficult to remove.

My goal was to reproduce the same experience found in commercial mechanical keyboards, where the switch can simply be pressed into the housing until it clicks into place and later removed without damaging either the switch or the housing.

To develop the first working iteration, I began by printing a simple test piece for the retention mechanism. The idea was that a thin wall with an arched indentation would engage the switch's retention latch as it snapped into place. Since I already had a validated reference model of the switch, the test piece could be kept small, allowing me to quickly verify both the dimensions and the behaviour of the mechanism.
   
_Test piece for the retention mechanism._
<img width="2000" height="660" alt="lock-in-system-test-1" src="https://github.com/user-attachments/assets/c3f00302-98b9-4781-85a2-d1f944462562" />

This first test matched the 3D model closely enough that I could confidently use it as a reference for the housing design.

**Retention mechanism - First iteration**    
Using the validated geometry, I designed the first version of the housing around both the switch and the hot-swap socket. At this stage, the main objective was simply to position both components correctly while providing enough support to keep them aligned.
       
<table>
    <caption><i>First iteration model.</i></caption>
    <tr>
        <td><img width="1186" height="882" alt="shi1-front" src="https://github.com/user-attachments/assets/2f4aa09c-4805-4aef-8818-9c766222fba0" /></td>
        <td><img width="1186" height="882" alt="shi1-side" src="https://github.com/user-attachments/assets/ddf0647b-0d65-4208-aa60-5995be8683bc" /></td>
        <td><img width="1186" height="882" alt="shi1-top" src="https://github.com/user-attachments/assets/a9af4b34-1f78-4169-a4ee-48b347c475b2" /></td>
        <td><img width="1186" height="882" alt="shi1-bottom" src="https://github.com/user-attachments/assets/ddd1aa4d-b421-4034-ae51-e4a4ac8ad244" /></td>
    </tr>
</table>
      
The prototype confirmed that the openings for the hot-swap socket tabs and the switch's locating pin were correctly dimensioned. The alignment between the switch and the socket was also correct. However, the internal walls responsible for retaining the switch were slightly undersized. As a result, the switch would not stay in place on its own and relied on the spring force of the hot-swap socket contacts to remain seated.
       
<table>
    <caption><i>First iteration results.</i></caption>
    <tr>
    <td><img width="1186" height="882" alt="shi1 - result 1" src="https://github.com/user-attachments/assets/66d2a8c8-860f-45ba-a285-dc4a000e5dda" /></td>
    <td><img width="1186" height="882" alt="shi1 - result 2" src="https://github.com/user-attachments/assets/57124993-ddcb-4e8b-ba1b-f29168643267" /></td>
    <td><img width="1186" height="882" alt="shi1 - result 3" src="https://github.com/user-attachments/assets/1b6642db-571e-458e-bd70-56c2c5872c7c" /></td>
    </tr>
</table>

**Retention mechanism - Second iteration**   
After slightly increasing the dimensions of the retention walls, the switch locked securely into place. The switch could also be removed with the proper extraction tool without excessive friction, although inserting the tool into the release opening was still somewhat difficult. The socket continued to maintain proper alignment, and switch insertion remained smooth.
   
<table>
    <caption><i>Second iteration model, results and observation.</i></caption>
    <tr>
        <td>
            <img width="1143" height="811" alt="image" src="https://github.com/user-attachments/assets/55c11d1b-5def-493d-b52b-a8967dca3d38" />
        </td>
    <td>        
        <img width="960" height="798" alt="V2 results" src="https://github.com/user-attachments/assets/89250533-c5b7-4f22-ba5a-e8d8524131fb" />
    </td>
    </tr>
</table>
    
>[!Note]
>At this point, I also realized that the switch I had been using as my reference was a **3-pin version** and did not include the two additional plastic locating pins commonly found on **5-pin MX-compatible switches**. This was simply an oversight during the initial design. To make the housing compatible with both switch variants, I added slots for the additional locating pins in the next iteration.

<table>
    <caption><i>Pin difference observation.</i></caption>
    <tr>
        <td>
    <img width="2000" height="621" alt="3vs5-pin-switch" src="https://github.com/user-attachments/assets/3b17beac-9af6-4a85-8ac7-b6f1977bab21" />
        </td>
    </tr>
</table>

 **Retention mechanism - Final iteration**   
The final iteration introduced a small 0.5 mm raised surface for the switch to rest on. I also reshaped this feature to create a wider opening for the extraction tool, making it much easier to access the retention latch. Although this change is barely noticeable by eye, it made a significant difference to the overall feel of the mechanism. The switch remained firmly seated while still being easy to remove, eliminating the excessive clearance that had been present in earlier iterations.

The hot-swap socket maintained its alignment, the switch could be inserted smoothly, and the added locating-pin slots made the design compatible with both 3-pin and 5-pin MX-compatible switches.

<table>
    <caption><i>Final iteration model.</i></caption>
    <tr>
         <td>
             <!-- Final iteration image that shows the model from an isometric point of view"-->
             <img width="921" height="878" alt="final-hss-model-3" src="https://github.com/user-attachments/assets/43576951-b926-4137-a415-e88dd3986763" />
         </td>
         <td>
             <!-- final iteration image that shows the model from the top view -->
             <img width="921" height="878" alt="final-hss-model-2" src="https://github.com/user-attachments/assets/84605dda-9da3-4e94-b816-06f20d82ec45" />
         </td>
         <td>
             <!-- Final iteration image that shows the model from the front -->
             <img width="921" height="878" alt="final-hss-model-1" src="https://github.com/user-attachments/assets/59d34c70-a0cf-44fc-825b-1be4ccb80a00" />
         </td>
    </tr>
</table>

<table>
    <caption><i>Final iteration results.</i></caption>
    <tr>
    <td>
        <!-- Immage from the side that shows the switch within the retention housing and the socket connected to the switch"-->
        <img width="921" height="878" alt="final-socket-housting-3" src="https://github.com/user-attachments/assets/4e9aba92-0a29-4d33-b47b-d3de5e16db4c" />
    </td>
    <td>
        <!-- image that shows the assembly from the bottom, ilustrating that the holes are completely alligned with the switch and the right size as well.  -->
        <img width="921" height="878" alt="final-socket-housing-4" src="https://github.com/user-attachments/assets/2b3aa7e5-8906-43a1-8f86-315cb8352755" />
    </td>
    <td>
        <!-- image from the top front view that shows how the spring loaded mechanism of the switch is perfectly in place within the housing geometry. -->
        <img width="921" height="878" alt="final-socket-housing-2" src="https://github.com/user-attachments/assets/57e27de9-4443-4acd-bb55-c267c2229808" />
    </td>
    <td>
        <!-- image from the tip front side view (sort of isometric) that shows the assembly being held together on its own without any assistance as it should-->
        <img width="921" height="878" alt="final-socket-housing-1" src="https://github.com/user-attachments/assets/4056def4-9fb0-4e24-a241-f04df4c62d2e" />
    </td>
    </tr>
</table>

With the switch retention mechanism working reliably, I could move on to refining the socket mounting features and integrating the assembly into the rest of the directional input block.
   
---
    
**Hotswap Socket mounting mechanism.**  
The next challenge was designing a mechanism to secure the hot-swap socket in place. Since I chose not to use a custom PCB, mainly to reduce both cost and design complexity, the socket needed to be retained entirely by the 3D-printed housing.
    
This introduced an important design challenge. Installing a mechanical switch requires pressing it firmly into the hot-swap socket until the retention clips engage. Without a dedicated mounting system, this insertion force could simply push the socket out of its housing. The design therefore needed to hold the socket securely while still leaving enough room for the attached wires and allowing the switch retention mechanism to function correctly.

The main constraint was the available space. The housing had to fit entirely within the footprint of the keycap so that adjacent switches could be placed close together. Any protruding features extending beyond this footprint would increase the spacing between neighbouring switches, negatively affecting the overall button layout and ergonomics.

Because of this limitation, expanding the design horizontally was not a practical solution. Instead, I explored ways to make use of the available vertical space.

Using the validated hot-swap socket reference model and its corresponding negative geometry, I developed a layered mounting system. **To simplify the design process, the housing was initially divided into three functional layers, each responsible for a single task.** This allowed every function of the mechanism to be designed and refined independently before being integrated into the final design.
     
<table>
    <caption><i>Functional decomposition of the initial three-layer hot-swap socket mounting concept.</i></caption>
<tr>
    <th>Layer</th>
    <th>Function</th>
    <th>Design</th>
</tr>

<tr>
    <td><strong>Switch retention layer</strong></td>
    <td>
        Holds the mechanical keyboard switch in place using its integrated retention clips while maintaining its alignment with the hot-swap socket.
    </td>
    <td>
        <!-- Image: Switch retention layer -->
        <img width="774" height="648" alt="Switch retention layer"
             src="https://github.com/user-attachments/assets/d80d07c9-58c3-4417-bb33-d496d40e9592" />
    </td>
</tr>
<tr>
    <td><strong>Socket alignment layer</strong></td>
    <td>
        Positions the hot-swap socket accurately and prevents horizontal movement, ensuring proper alignment between the switch terminals and the socket contacts.
    </td>
    <td>
        <!-- Image: Socket alignment layer -->
        <img width="774" height="648" alt="Socket alignment layer"
             src="https://github.com/user-attachments/assets/3ef726af-126e-4400-963f-5e619037c135" />
    </td>
</tr>
<tr>
    <td><strong>Socket retention layer</strong></td>
    <td>
        Prevents the hot-swap socket from being pushed out of the housing during switch installation. A protruding feature engages with the socket geometry and transfers the insertion force to the housing, where it is secured using screws.
    </td>
    <td>
        <!-- Image: Socket retention layer -->
        <img width="774" height="648" alt="Socket retention layer"
             src="https://github.com/user-attachments/assets/8a8e3f8e-b7ed-4d27-a49c-e70c061e7685" />
    </td>
</tr>
</table>
    
The first prototype was intentionally built around this three-layer concept. At this stage, my objective was not to produce a final component, but to verify that the mounting mechanism could withstand the forces generated during switch installation while remaining compact enough for the intended button layout.
    

<div align=center>
<table>
    <caption><i>Prototype virtual assembly.</i></caption>
    <tr>
        <td>
            <!-- this gif shows the layers being assembled in an animation in gif format -->
            <img   alt="hss-block-assmbly-gif" src="https://github.com/user-attachments/assets/ddd07b71-c3e2-4d19-ac6c-d9bbaeb64739" />
        </td>
        <!--td>
            <img height="600"  alt="image" src="https://github.com/user-attachments/assets/7df10a3f-0b72-459f-bdac-089969e5f0c0" />
        </td-->
    </tr>
</table>
</div>

<table>
    <caption><i>First assembled prototype of the layered hot-swap socket mounting mechanism.</i></caption>
    <tr>
        <td colspan="4">
            <!-- this image is of the printed pieces and components that will be assembled together including the screws that hold the block assembled -->
            <img width="2000" height="790" alt="POC - HSS - socket complete housing" src="https://github.com/user-attachments/assets/f2546f05-f616-41ab-a90c-90d5437e5535" />
        </td>
    </tr>
    <tr>
        <td>
            <!-- this image shows the bottom and middle layer assembled together supporting and aligning the hotswap socket -->
            <img width="921" height="878" alt="image" src="https://github.com/user-attachments/assets/8935b510-6745-448f-94b2-6b745478aafe" />
        </td>
        <td>
            <!-- this image shows how the layers are held together with screws at the bottom -->
            <img width="921" height="878" alt="image" src="https://github.com/user-attachments/assets/df6b9a14-270e-47f1-96b3-efb39dcccad7" />
        </td>
        <td>
            <!-- This image shows the complete assembly of the pieces printed and assembled of the proof of concept -->
            <img width="921" height="870" alt="image" src="https://github.com/user-attachments/assets/043267e0-5192-46e6-8db3-b1ef75b85cb3" />
        </td>
    </tr>
</table>
    
After confirming that the concept behaved as expected, I refined the design to improve both functionality and structural rigidity. Wire-routing channels were added to provide a clean path for the wires soldered to the hot-swap socket, and the original switch retention layer and socket alignment layer were merged into a single component.
    
<table>
    <caption><i>Before and after merging.</i></caption>
    <tr>
        <td>
            <!-- image of the before and after mergin of the parts -->
            <img width="1664" height="729" alt="image" src="https://github.com/user-attachments/assets/5a093713-bd18-43f8-925c-ebd55641d6b5" />
        </td>
    </tr>
</table>
     
This modification created a much stronger structure. In the initial concept, the bottom cover, which prevents the socket from being pushed out, was fastened primarily to the alignment layer, while the connection between the alignment and switch retention layers was comparatively weak. **Merging these layers produced a more direct load path, allowing the insertion force applied during switch installation to be transferred more effectively through the housing**.
     
<!--mark>TODO : IMAGE -> Comparison between the initial three-layer prototype and the final two-part design. </mark-->
<table>
    <caption><i>Final switch retention and socket mounting mechanism.</i></caption>
    <tr>
        <td colspan="4">
            <i>Final printed result.</i></br>
            <img width="2000" height="578" alt="hss-compelte-result-layers" src="https://github.com/user-attachments/assets/975f4648-0642-4f2f-ae07-7ccba0aab84d" />
        </td>
    </tr>
    <tr>
        <td>
            <i>Retention & alignment layer.</i></br>
            <img width="1034" height="900" alt="hss-complete-result-1" src="https://github.com/user-attachments/assets/aaddb262-5af8-40cd-9971-17ee4ecd60aa" />
        </td>
        <td>
            <i>Secured socket support layer.</i></br>
            <img width="1034" height="900" alt="hss-complete-result-2" src="https://github.com/user-attachments/assets/c9d96424-1cd4-44de-93dc-7a6645e1e398" />
        </td>
        <td>
            <i>Complete assembly.</i></br>
            <img width="1034" height="900" alt="hss-complete-result-3" src="https://github.com/user-attachments/assets/7fbfe3a8-1bc5-4204-8af4-b2011165f5a3" />
        </td>
        <td>
            <i>Side view.</i></br>
            <img width="1034" height="900" alt="hss-complete-result- 4" src="https://github.com/user-attachments/assets/db06dc99-fd52-4b17-bb1d-a57ee93f25b2" />
        </td>
    </tr>
</table>

>[!NOTE]
> Although the final component consists of only two printed parts, the three-layer concept proved valuable during development because it allowed each function of the mounting system to be designed and validated independently before being combined into the final design.
    
---
   
## 3.5.3 Directional input block assembly.
The purpose of this component is to house the four directional input buttons in a single rotating assembly. The idea behind this design was to allow the entire directional input block to rotate inside the controller so that its angle could be adjusted to match the player's most comfortable hand position.

Rather than fixing the directional inputs in a predetermined orientation, I wanted the controller to be adaptable to different preferences. At this stage of the project, I had not yet decided whether the assembly would be permanently fixed after adjustment or left free to rotate under certain conditions. Because of this, the initial design focused on creating a simple and reliable rotating mechanism while leaving both possibilities open.

 To begin the design, I first positioned the individual switch-and-socket modules according to the layout developed during the ergonomics study. 
        
 <i>Switch-and-socket modules positioned to create the directional input layout.</i></br>
<img width="1662" height="523" alt="image" src="https://github.com/user-attachments/assets/074780a6-b5a1-45b5-8655-1afaea6fc5a5" />
        
Once I was satisfied with the modules arrangement, I designed a circular base approximately 75 mm in diameter and 2 mm thick to support the complete input block.
The upper surface of the base was aligned with the top of the switch modules, creating a smooth transition between the individual parts and making the assembly look like a single integrated component rather than several separate pieces.

<i>Main rotating body.</i></br>
<img width="1601" height="523" alt="image" src="https://github.com/user-attachments/assets/37955618-6a28-467c-ad1f-9c525267afbf" />
      
To allow the assembly to rotate, I added a cylindrical guide underneath the base that would mate with a matching recess in the main enclosure. This guide keeps the input block centred while allowing it to rotate freely inside the housing.
       
_Circular base with the integrated rotational guide._   
<img width="1653" height="562" alt="image" src="https://github.com/user-attachments/assets/f400ed4e-23e9-4064-be36-da73f794529d" />
     
Before printing the first prototype, I also added clearance cut-outs around each switch. These openings provide enough space for a standard mechanical keyboard switch puller to reach the retention clips, allowing switches to be removed and replaced without disassembling the entire input block.

<table>
    <tr>
        <td>
        <i>Cutouts close-up</i></bvr>
        <img width="1258" height="900" alt="image" src="https://github.com/user-attachments/assets/d78819ba-2824-42f2-a892-a4b4c8a8645c" />
        </td>
        <td>
        <i>Top View</i></bvr>
        <img width="1108" height="907" alt="image" src="https://github.com/user-attachments/assets/2c5b8d08-bbd3-4ca1-bae3-24a35afd33d8" />
        </td>
    </tr>
</table>

**First iteration results**    
The first prototype confirmed that the overall concept was viable and worth developing further. The key spacing was comfortable and closely matched the keyboard cursor layout I intended to replicate. I also found that the spacing between adjacent switch modules was slightly larger than expected, providing additional room for wire-routing channels.

The assembled test piece met the main design objectives. The switch-and-socket modules integrated correctly with the rotating base and remained securely in place during switch installation, confirming that the hot-swap socket retention mechanism could withstand the insertion forces. The design also allowed easy access for switch replacement and maintenance.

**The prototype also highlighted several improvements for the next iteration:**
- Reshape the switch extraction cut-outs to achieve a more refined surface finish.
- Improve the wire-routing channels utilizing the increased avilable space to simplify cable management.
- Add an internal cut-out and mounting feature for the planned contact LED.
- Reduce the thickness of the second layer and modify the bottom support to reduce material usage and print time while maintaining structural rigidity.

Overall, the first iteration validated the design and provided a clear direction for the next stage of development.
   
<table>
    <caption><i>First assembled prototype of the directional input block.</i></caption>
    <tr>
        <td>
            <!-- image that shows the assembhled piece with the swityches on without caps -->
            <img width="998" height="800" alt="first iteration result uncapped" src="https://github.com/user-attachments/assets/322e9583-80ea-41df-acf1-c6142e1b147a" />
        </td>
        <td>
            <!-- image that shows the assembled piece with the switches and their keycaps -->
            <img width="998" height="800" alt="first iteration result capped" src="https://github.com/user-attachments/assets/6adddef5-04db-4a39-9ce0-ebc718eb46a6" />
        </td>
    </tr>
    <tr>
        <td>
            <!-- image that shows the extraction tool access cutouts -->
            <img width="998" height="800" alt="recess result" src="https://github.com/user-attachments/assets/252d12ce-4510-4ff1-88f9-2bd263d99d72" />
        </td>
        <td>
            <!-- image that demonstrates how the extraction tool or switch puller fits into the recess -->
            <img width="998" height="800" alt="image" src="https://github.com/user-attachments/assets/107a2b51-f4c8-49a7-9c87-08c4e310386e" />
        </td>
    </tr>
</table>
     
**Second iteration**    

The first change I made in the second iteration was to reduce the height of the alignment layer so that it matched the height of the hot-swap socket. As shown in the updated Blender model, this reduced the overall thickness of the assembly while maintaining the required support and alignment for the socket.
   
<table>
    <tr>
        <td>
            <i>Before layer height reduction</i></br>
            <img width="1189" height="584" alt="image" src="https://github.com/user-attachments/assets/fbdd05a5-707d-4193-a567-8bb0772d1723" />
        </td>
        <td>
            <i>After layer height reduction</i></br>
            <img width="1189" height="584" alt="image" src="https://github.com/user-attachments/assets/4c7c67c2-5360-4652-a0b2-9ad3acc38880" />
        </td>
    </tr>
</table>
    
Using the extra space identified during the first iteration, I then redesigned the wire-routing channels to make better use of the available space between modules. The new routing allowed for a better angle to bend the wires, making them easier to install and resulting in a cleaner assembly.   
    
<table>    
    <tr>
        <td>
            <i>Channels adapted to available space.</i></br>
            <img width="888" height="690" alt="image" src="https://github.com/user-attachments/assets/e13f3438-edd1-4800-906c-e57fafd92306" />
        </td>
        <td>
            <i>Before routing channels increse.</i></br>
            <img width="888" height="690" alt="image" src="https://github.com/user-attachments/assets/ba23e1d5-1f1b-4661-9859-c666fc15b7e4" />
        </td>
        <td>
            <i>After routing channels increse.</i></br>
            <img width="887" height="690" alt="image" src="https://github.com/user-attachments/assets/94aa5db3-9dcf-481d-b1de-94504bf03fb5" />
        </td>
    </tr>
</table>
     


<table>    
    <tr>
        <td>
            <i>Before - Side view</i></br>
        </td>
        <td>
            <i>After - Side view</i></br>
        </td>
    </tr>
</table>


For the support layer i simply 

To add the contact status LED I modeled a reference and then used it to position it at a heigh I knew it would not impede the switch from sitting propperly in the retention mechanism.  

<table>
    <tr>
        <td>
            <img width="1044" height="831" alt="image" src="https://github.com/user-attachments/assets/6449812a-72ad-484f-88c1-2b8593c40120" />
        </td>
        <td>
            <img width="1044" height="831" alt="image" src="https://github.com/user-attachments/assets/4732efc1-af3f-4b50-a113-39579df9959f" />
        </td>
        <td>
            <!--img width="1044" height="831" alt="image" src="https://github.com/user-attachments/assets/15a64b38-44be-44e2-a629-7c36cb3cb217" /-->
            <img width="1044" height="831" alt="image" src="https://github.com/user-attachments/assets/a164922f-ede1-4fe8-a2ba-cf3a82c33ce8" />
        </td>
    </tr>
</table>

<!--
Verifying the recess created for the switch puller tool.

**Correcciones a implementar:**   
Tengo que mejorar la calidad de las hendiduras para el uso de la herramienta. Son en tamaño suficientes para facilitar el uso, pero la dirección de impresión de la pieza impiden un acabado estetico.
Por otro lado, conviene aumentar la altura de la guia de rotación.
Hay que mejorar las ranuras de salida para los cables de los zocalos de contacto en capa 2. 
Debo crear el espacio para el led que tengo intención de incluir en la pieza final. 
   
**Posibles mejoras:**    
Podria diseñar un sistema de extracción por presión para facilitar la extracción de los interruptores.
Puedo reducir la altura de la capa 2 y modificar la capa 3 en consecuencia, ahorrando material y tiempo de impresión.
   
**Siguientes pasos:**    
Debo rediseñar el mecanismo de sujeción pàra la capa 3 e incluir los soportes para dicha capa. Debo recalibrar la altura de la geometria protuberante que asegura el zócalo a la capa de alineación. 

---
-->








     




    



## 3.6 LED function switch.
### 3.6.1 Creating the piece that holds the switch.  

## 3.7 Other elements and features.
### 3.7.1 Charging port
### 3.7.2 Resting feet. 
   
---
   
# 🔸4. Reverse Engineering, Wiring, and Hardware Integration
After identifying the main controller IC as the Actions Semiconductor ATS2855, it became much easier to determine the purpose of the motherboard’s test pads and signal connections. The ATS2855 is the central processing unit of the controller, responsible for reading the button matrix and analog joysticks, managing USB and Bluetooth communication, monitoring the battery and charging system, and interfacing with onboard peripherals such as the touchpad through protocols like I²C. To avoid any mistakes or incorrect assumptions, I personally tested each pad using a multimeter and verified behavior through manual input checks on a live device, correlating electrical readings with real-time system responses. Based on the capabilities of the ATS2855 and the PCB layout, the following table summarizes the identified test pads and their functions.
    
While searching online for a datasheet and information about the IC i found this useful [post](https://www.answeroverflow.com/m/1398984785619325016).
    
>[!IMPORTANT]
>While I have not been able to confirm every single connection, the most critical test pads required for the project have been verified. A check mark symbol (✔️) indicates the test pads that were manually tested and confirmed in the table below.
    
<table border="1" cellspacing="0" cellpadding="6" style="border-collapse:collapse;width:100%;"> 
    <thead> 
        <tr> <th>#</th> <th>Name</th> <th>Description (ATS2855)</th> </tr> 
    </thead> 
    <tbody> 
        <tr><td>1</td><td>3.3V</td><td>3.3 V regulated supply rail.</td></tr> <tr><td>2</td><td>5V</td><td>USB 5 V supply input.</td></tr> <tr><td>3</td><td>VDD</td><td>Main ATS2855 core/peripheral supply.</td></tr> <tr><td>4</td><td>GND</td><td>Ground reference.</td></tr> <tr><td>5</td><td>D+</td><td>ATS2855 USB 2.0 D+ line.</td></tr> <tr><td>6</td><td>D-</td><td>ATS2855 USB 2.0 D− line.</td></tr> <tr><td>7</td><td>SDA0</td><td>I²C/TWI bus 0 data line.</td></tr> <tr><td>8</td><td>SCL0</td><td>I²C/TWI bus 0 clock line.</td></tr> <tr><td>9</td><td>SDA1</td><td>I²C/TWI bus 1 data line.</td></tr> <tr><td>10</td><td>SCL1</td><td>I²C/TWI bus 1 clock line.</td></tr> <tr><td>11</td><td>LX</td><td>Left joystick X-axis ADC input.</td></tr> <tr><td>12</td><td>LY</td><td>Left joystick Y-axis ADC input.</td></tr> <tr><td>13</td><td>RX</td><td>Right joystick X-axis ADC input.</td></tr> <tr><td>14</td><td>RY</td><td>Right joystick Y-axis ADC input.</td></tr> <tr><td>15</td><td>KR1</td><td>Button matrix row 1 (GPIO).</td></tr> <tr><td>16</td><td>KR2</td><td>Button matrix row 2 (GPIO).</td></tr> <tr><td>17</td><td>KR3</td><td>Button matrix row 3 (GPIO).</td></tr> <tr><td>18</td><td>KL1</td><td>Button matrix column 1 (GPIO).</td></tr> <tr><td>19</td><td>KL2</td><td>Button matrix column 2 (GPIO).</td></tr> <tr><td>20</td><td>KL3</td><td>Button matrix column 3 (GPIO).</td></tr> <tr><td>21</td><td>BT</td><td>Battery voltage monitoring signal.</td></tr> <tr><td>22</td><td>BT1</td><td>Secondary battery or charging-related signal.</td></tr> <tr><td>23</td><td>INT</td><td>Interrupt input from a peripheral (likely touchpad).</td></tr> <tr><td>24</td><td>RES1</td><td>Reset line for the ATS2855.</td></tr> <tr><td>25</td><td>P23</td><td>ATS2855 GPIO pin 23.</td></tr> <tr><td>26</td><td>TOUCH</td><td>Touchpad communication or wake signal.</td></tr> <tr><td>27</td><td>AR</td><td>Directional/button input (Right).</td></tr> <tr><td>28</td><td>AL</td><td>Directional/button input (Left).</td></tr> <tr><td>29</td><td>AU</td><td>Directional/button input (Up).</td></tr> <tr><td>30</td><td>AD</td><td>Directional/button input (Down).</td></tr> <tr><td>31</td><td>TRI</td><td>Triangle button input.</td></tr> <tr><td>32</td><td>PAR</td><td>Options/Pair button input.</td></tr> <tr><td>33</td><td>SHA</td><td>Share button input.</td></tr> <tr><td>34</td><td>GR</td><td>Status LED or GPIO signal.</td></tr> <tr><td>35</td><td>RE</td><td>Status LED or GPIO signal.</td></tr> <tr><td>36</td><td>BL</td><td>Blue LED or backlight control.</td></tr> <tr><td>37</td><td>FORK</td><td>Factory/diagnostic test signal.</td></tr> <tr><td>38</td><td>PASD</td><td>Factory/diagnostic test signal.</td></tr> <tr><td>39</td><td>RSE</td><td>Reset/diagnostic signal.</td></tr> </tbody> </table>



## 4.1 Wiring the motherboard
## 4.2 Wiring the action buttons
## 4.3 Wiring the arrow buttons
## 4.4 Wiring the led funcionality
## 4.5 wiring the charging port.
   
---
   
# 🔸5. Testing and Validation
## 5.1 Input delay
## 5.2 Tournament legality
## 5.3 Comfort test
## 5.4 LED functionality
## 5.5 Charging and USB connection
## 5.6 Bluetooth connection
   
---
   
# 🔸6. Final Customization
## 6.1 Custom art cover
## 6.2 Custom buttons
   
---
   
# 🔸7. Conclusions and Future Improvements
## 7.1 Lessons Learned
<!-- 
I tested most of the skills I accumultaed over the years as a hobbist. It involved knowledge in many fields:
- Printing media
- Photographi paper handling and long term protection.
- Image edition for customization.
- 3d Printing
- 3d modeling and prototyping
- Soldering and electronics in general.
- Patience, patience, patience. -->

## 7.2 What I Would Do Differently
<!--
- Would've bough a Fillet gauge.
- Would've bought a Screw Pitch gauge.
- Would've organized my blender files differently.
--> 
---
   
# 8. Product showcase.
## 8.1 Final Assembly
## 8.2 Finished Product Images
## 8.3 Key Features Demonstration
   
---

# Costs
Buget notes. 
<table>
<tr>
    <th>Component</th>
    <th>Cost</th>
    <th>Link</th>
</tr>
<tr>
    <td>Controller (Motherboard)</td>
    <td>27.99€</td>
    <td>https://www.amazon.es/dp/B0CBRC7MKL?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1</td>
</tr>
<tr>
    <td>Arcade buttons</td>
    <td>26.68€ (x2 - 13.34€/unit)</td>
    <td>https://www.amazon.es/dp/B08RC4JC1C?ref=ppx_yo2ov_dt_b_fed_asin_title</td>
</tr>
<tr>
    <td>KB Switch Hostswap socket</td>
    <td>4.69€ ( x30 - 0.1563€/unit)</td>
    <td>https://es.aliexpress.com/item/1005006610506123.html?spm=a2g0o.order_detail.order_detail_item.3.1b1858bfTuxPj5&gatewayAdapt=glo2esp</td>
</tr>
<tr>
    <td>2 Pins terminal block</td>
    <td>4.49€ (x50 - 0.0898€/unit)</td>
    <td>https://es.aliexpress.com/item/1005009002216100.html?spm=a2g0o.order_detail.order_detail_item.4.400a58bfZ1Ur7X&gatewayAdapt=glo2esp</td>
</tr>
<tr>
    <td>Anycubic Fast PLA 1Kg Spool</td>
    <td>19.99€ (1Kg)</td>
    <td>https://www.anycubic.es/products/pla-de-alta-velocidad?variant=42797110886576</td>
</tr>
</table>


---

---










# Mistakes and lessons learnd.

<mark>TODO</mark>
<!--
- Undervalued a dedicated motherboard (like brook boards)
- Assumed any motherboard would work
- Relied on a cheap controller that stopped working after a couple of weeks of use.
- First iteration was hard to service and when an issue arised after years of use it was very hard to diagnose.
- Assumed bigger buttons were better and more comfortable.
- Did not initially start measuring from a fixed point for ther motherboard reference.
- Did not keep an organized digital workspace, this way I lost a good prototype in the digital clutter of models, had to create a new blender project and order stuff around.
- Did not initially calculate the nut of the action buttons.
- Undervalued certain tools like pitch gauge, which introduced trial and error.
- Spent more money than necessary due to wanting to test a lot of things.
- Spent a whole ton of time modeling positives while it was probably not necesary.
- Bought a motherboard that had the charing port fused to it, so i had to fight another battle to export it and pay for it.
- Had to edit and re-edit the documentation once and once again because it is hard to organize ideas, i kept fusing sections and having a hard time at separating flows and concepts.
- I based my defgisn process on having the positives of the motherboarda nd other elements and i failed to model the elements on one side of the motherboard PCB thinking it would not be necessary, this ended up in an additional motherboard enclosure iteration because the support pillars did not respect one of the small chips and the buttons on the other side. If i made an accurate representation of both sides from the start this iteration wouldn'tve been necessary.

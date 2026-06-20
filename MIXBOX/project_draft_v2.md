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
## 3.1 Design methodology and approach.
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
 
## 3.2 Action button array.
The action button array consists of the buttons used to perform attacks and other in-game actions, such as punches and kicks. Together with the directional controls, these are the buttons that see the most frequent use during gameplay, making their placement and ergonomics particularly important. 

### 3.2.1 Design requirements.
The action buttons array must be comfrotable to use, well positioned, as compact as possible and they must easily replaceable in case of malfunction or being eroded by use. Easy to service and replace in case of customization needs. 

### 3.2.2 Ergonomics study & Initial design.
### 3.2.3 Prototyping and testing.
### 3.2.4 Final Design.

## 3.3 Motherboard housing (Motherboard container within the enclosure)
### 3.3.1 Reference model creation.
### 3.3.2 Initial housing design.
### 3.3.3 Prototype and Validation.
### 3.3.4 Final housing.

## 3.4 Led module enclosure (led module surrounding geometry).
### 3.4.1 Modeling the positive for reference
### 3.4.2 Modeling the enclosure.

## 3.5 Direction arrows piece
### 3.5.1 Hand ergonomics
### 3.5.2 Modeling the holder piece and retention mechanism.

## 3.6 LED function switch.
### 3.6.1 Creating the piece that holds the switch.  

## 3.7 Other elements and features.
### 3.7.1 Charging port
### 3.7.2 Battery holder
### 3.7.3 Resting feet. 
   
---
   
# 🔸4. Assembly and Electronics Integration
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

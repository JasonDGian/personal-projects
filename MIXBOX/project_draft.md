# Building a Custom Fightstick Controller
    
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/1c61ba26-ca54-4d73-951a-0f259d576594" />

   
---
   
# 1. Introduction
Fighting games have long been one of my favorite genres, and I have always wanted a dedicated arcade controller. While commercial fight sticks and MixBox-style controllers offer a great experience, high-quality options are often expensive and still don’t fully match what I personally want in terms of ergonomics, size, or appearance.

This project is about designing and building a custom MixBox-style controller tailored to my own preferences. Building it gives me full control over layout, dimensions, aesthetics, and functionality, so the final result can fit my needs better than a commercial product.

This is not my first arcade controller project. A few years ago, I built a custom controller for a friend, which gave me hands-on experience with CAD design, 3D printing, electronics, and general prototyping. This project builds on that experience and gives me a chance to improve those skills further.

I will also document the entire process, both as a personal record and so that others interested in building their own controllers can learn from my approach, including what worked and what didn’t.
    
## 1.1 Motivation
The main motivation behind this project is to create a controller that better matches my ergonomic preferences and desired features at an affordable price. Commercial controllers often involve compromises, so building my own gives me the freedom to design something that fits my needs more closely.

A secondary motivation is to document the process in a useful way. By sharing my decisions, methods, and mistakes, I hope it can help others who want to build their own arcade controllers and avoid some of the trial and error.
    
## 1.2 Goals and Objectives
The goal of this project is to **build an ergonomic arcade controller** that feels good to use, works reliably, and is enjoyable during long play sessions, **while staying within a reasonable budget**.

**Key design goals include:**
- Keeping the controller compact and easy to transport
- Making the layout comfortable and reducing strain during extended use
- Designing it so internal parts are easy to access, repair, or replace
- Customizing the look and feel, including things like LED lighting
     
## 1.3 Requirements and Constraints
The project is limited by time and budget, since it’s a personal build. All decisions need to stay realistic in terms of cost, complexity, and what I can actually build and test.

Tournament legality is also important. Even though I’m not building this specifically for competitive play, I want it to follow common tournament rules where possible, so I avoid things like macros, turbo functions, or any form of input automation.
    
The controller is intended for use on both PC and PlayStation 4, so compatibility with these platforms is a key requirement.    
   
Portability is another key constraint. The controller should stay reasonably compact and lightweight so it doesn’t take up too much desk space and is easy to move around when needed.

---
   
# 2. Selection of components.

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
    
<!--
</br>
<div align="center">
<table>
    <tr>
        <th colspan=3>Selected product</th>
    </tr>
<tr>
    <td>T-29 Wireless controller</td>
    <td>27.99€</td>
    <td><a href="https://www.amazon.es/dp/B0CBRC7MKL?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1">CHEREEKI Wireless controller for PS4/Pro/Slim</a></td>
</tr>
</table>
</div>
</br> -->

</br>

Link to the product: [T-29 Wireless controller](https://www.amazon.es/dp/B0CBRC7MKL?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1)
        
## 2.2 Action buttons.
Selecting the action buttons turned out to be more difficult than I expected due to the huge number of available options. From the start, I knew I wanted LED-backlit buttons, both because I like their appearance and because they would support some customization ideas planned for later in the project.

To compare the available options, I tested several button sets in two sizes: 33 mm and 27 mm. Although all of them were functional, ergonomics and overall comfort quickly became the deciding factors.

After some testing, I ruled out the 33 mm buttons because they took up too much space and made it harder to achieve a compact layout. Among the 27 mm options, one set stood out immediately. Despite being the most expensive and using a large mounting nut that complicated installation, it felt noticeably better and had a higher-quality finish than the alternatives.

In the end, I chose this button set for the final design. The mounting challenge would later be addressed during the enclosure design process.

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

<!--
</br>
<div align="center">
<table>
    <tr>
        <th colspan=3>Selected product</th>
    </tr>
<tr>
    <td>Arcade buttons</td>
    <td>26.68€ (x2 - 13.34€/unit)</td>
    <td>https://www.amazon.es/dp/B08RC4JC1C?ref=ppx_yo2ov_dt_b_fed_asin_title</td>
</tr>
</table>
</div>
</br> -->

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
    
<!--          
_Comparison lowprofile vs full height_
<table>
    <tr>
        <th>
            Name
        </th>
        <th>
            Image
        </th>
        <th>
            Spec Sheet
        </th>
    </tr>
    <tr>
        <td>Full-Height Gateron Red Switch</td>        
        <td><img height="450" alt="fp-mx-sw" src="https://github.com/user-attachments/assets/5c2686dc-97cd-46d0-afbc-cba264c61c81" /></td>
        <td><img height="450" alt="image" src="https://github.com/user-attachments/assets/86cba1cb-1c10-4b9f-8dd6-2b188d9bd850" /></td>
    </tr>
    <tr>
    <td>
        Low-profile Gateron Red Switch.        
    </td>
    <td>
        <img height="450" alt="lp-sw" src="https://github.com/user-attachments/assets/016d6c0a-8756-4ee6-9c12-eecdd5179d27" />
    </td>
    <td>
        <img height="450" alt="image" src="https://github.com/user-attachments/assets/d2cd2434-d22a-4a7b-ac02-21c21e07c57c" />
    </td>
    </tr>
</table-->

<!--
</br>
<div align="center">
<table>
    <tr>
        <th colspan=3>Selected product</th>
    </tr>
<tr>
    <td>Arrow buttons</td>
    <td>1.53€ (x10 - 0.153€/unit)</td>
    <td><a href="https://es.aliexpress.com/item/1005005467023965.html?spm=a2g0o.productlist.main.2.761c2154jAsrl2&algo_pvid=663d1580-1a2d-495c-8ce1-5936a79069a1&algo_exp_id=663d1580-1a2d-495c-8ce1-5936a79069a1-1&pdp_ext_f=%7B%22order%22%3A%22522%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21EUR%211.82%211.27%21%21%2113.89%219.72%21%402103890917815484233368128ea07e%2112000033197110242%21sea%21ES%21184981297%21X%211%210%21n_tag%3A-29919%3Bd%3Ae78d15fa%3Bm03_new_user%3A-29895&curPageLogUid=3OhXWIXwbvYz&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005005467023965%7C_p_origin_prod%3A">10Pcs/lot Original Cherry MX Mechanical Keyboard Switch Axis Shaft Switch RGB blue</a></td>
</tr>
</table>
</div>
</br> -->
    
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
    </tr><!--
    <tr>
        <td colspan="2"> Link: <a href="https://es.aliexpress.com/item/1005009763600457.html?spm=a2g0o.productlist.main.21.450b6311tFjwCL&algo_pvid=b312198c-d084-4474-8f0e-bfb33dbd1c6d&algo_exp_id=b312198c-d084-4474-8f0e-bfb33dbd1c6d-20&pdp_ext_f=%7B%22order%22%3A%221502%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21EUR%211.89%211.75%21%21%2114.52%2113.46%21%40211b65de17817129622565772e7b9b%2112000050090750520%21sea%21ES%21184981297%21X%211%210%21n_tag%3A-29919%3Bd%3Ae78d15fa%3Bm03_new_user%3A-29895%3BpisId%3A5000000209393528&curPageLogUid=f1lF8tP3KxVU&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005009763600457%7C_p_origin_prod%3A">12mm Metal Button Switch Waterproof 1NO 3A High Head Momentary Automatic Reset</a></td>
    </tr>-->
</table>

</br>

Link to the product: <a href="https://es.aliexpress.com/item/1005009763600457.html?spm=a2g0o.productlist.main.21.450b6311tFjwCL&algo_pvid=b312198c-d084-4474-8f0e-bfb33dbd1c6d&algo_exp_id=b312198c-d084-4474-8f0e-bfb33dbd1c6d-20&pdp_ext_f=%7B%22order%22%3A%221502%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21EUR%211.89%211.75%21%21%2114.52%2113.46%21%40211b65de17817129622565772e7b9b%2112000050090750520%21sea%21ES%21184981297%21X%211%210%21n_tag%3A-29919%3Bd%3Ae78d15fa%3Bm03_new_user%3A-29895%3BpisId%3A5000000209393528&curPageLogUid=f1lF8tP3KxVU&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005009763600457%7C_p_origin_prod%3A">12mm Metal Button Switch Waterproof 1NO 3A High Head Momentary Automatic Reset</a>
<!--
<table>
    <tr>
        <th>
        Name
    </th>
    <th>
        Type
    </th>
    <th>
        Picture
    </th>
    <th>
        Link
    </th>
    </tr>
    <tr>
        <td>
            FILN Plastic puish button switch.
        </td>
        <td>
            Momentary ON (Plastic) - Non clicky
        </td>
        <td>
            <a href="https://es.aliexpress.com/item/1005009767928131.html?spm=a2g0o.productlist.main.11.450b6311tFjwCL&algo_pvid=b312198c-d084-4474-8f0e-bfb33dbd1c6d&algo_exp_id=b312198c-d084-4474-8f0e-bfb33dbd1c6d-10&pdp_ext_f=%7B%22order%22%3A%22104%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21EUR%212.32%212.16%21%21%212.63%212.45%21%40211b65de17817129622565772e7b9b%2112000050100207033%21sea%21ES%21184981297%21X%211%210%21n_tag%3A-29919%3Bd%3Ae78d15fa%3Bm03_new_user%3A-29895%3BpisId%3A5000000209393528&curPageLogUid=mZ1VAbPUetou&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005009767928131%7C_p_origin_prod%3A#nav-specification"> FILN 10 pieces set.</a>
        </td>
        <td>
            <img width="250" alt="image" src="https://github.com/user-attachments/assets/077ea6a8-ec76-4311-9105-60b50a3fba5c" />
        </td>
    </tr>
    <tr>
        <td>
            FILN Plastic puish button switch.
        </td>
        <td>
            Momentary ON (Plastic) - Non clicky
        </td>
        <td>
            <a href="https://es.aliexpress.com/item/1005009767928131.html?spm=a2g0o.productlist.main.11.450b6311tFjwCL&algo_pvid=b312198c-d084-4474-8f0e-bfb33dbd1c6d&algo_exp_id=b312198c-d084-4474-8f0e-bfb33dbd1c6d-10&pdp_ext_f=%7B%22order%22%3A%22104%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21EUR%212.32%212.16%21%21%212.63%212.45%21%40211b65de17817129622565772e7b9b%2112000050100207033%21sea%21ES%21184981297%21X%211%210%21n_tag%3A-29919%3Bd%3Ae78d15fa%3Bm03_new_user%3A-29895%3BpisId%3A5000000209393528&curPageLogUid=mZ1VAbPUetou&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005009767928131%7C_p_origin_prod%3A#nav-specification"> FILN 10 pieces set.</a>
        </td>
        <td>
            <img width="250" alt="image" src="https://github.com/user-attachments/assets/f2bda21d-85c4-404d-aa27-18da1650d72b" />
        </td>
    <tr>
        <td>
            FILN Plastic puish button switch.
        </td>
        <td>
            Momentary ON (Plastic) - Non clicky
        </td>
        <td>
            <a href="https://es.aliexpress.com/item/1005009767928131.html?spm=a2g0o.productlist.main.11.450b6311tFjwCL&algo_pvid=b312198c-d084-4474-8f0e-bfb33dbd1c6d&algo_exp_id=b312198c-d084-4474-8f0e-bfb33dbd1c6d-10&pdp_ext_f=%7B%22order%22%3A%22104%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21EUR%212.32%212.16%21%21%212.63%212.45%21%40211b65de17817129622565772e7b9b%2112000050100207033%21sea%21ES%21184981297%21X%211%210%21n_tag%3A-29919%3Bd%3Ae78d15fa%3Bm03_new_user%3A-29895%3BpisId%3A5000000209393528&curPageLogUid=mZ1VAbPUetou&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005009767928131%7C_p_origin_prod%3A#nav-specification"> FILN 10 pieces set.</a>
        </td>
        <td>
            <img width="250" alt="image" src="https://github.com/user-attachments/assets/f2bda21d-85c4-404d-aa27-18da1650d72b" />
        </td>
    </tr>
    <tr>
        <td>
            FILN Plastic puish button switch.
        </td>
        <td>
            Momentary ON (Plastic) - Non clicky
        </td>
        <td>
            <a href="https://es.aliexpress.com/item/1005009767928131.html?spm=a2g0o.productlist.main.11.450b6311tFjwCL&algo_pvid=b312198c-d084-4474-8f0e-bfb33dbd1c6d&algo_exp_id=b312198c-d084-4474-8f0e-bfb33dbd1c6d-10&pdp_ext_f=%7B%22order%22%3A%22104%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21EUR%212.32%212.16%21%21%212.63%212.45%21%40211b65de17817129622565772e7b9b%2112000050100207033%21sea%21ES%21184981297%21X%211%210%21n_tag%3A-29919%3Bd%3Ae78d15fa%3Bm03_new_user%3A-29895%3BpisId%3A5000000209393528&curPageLogUid=mZ1VAbPUetou&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005009767928131%7C_p_origin_prod%3A#nav-specification"> FILN 10 pieces set.</a>
        </td>
        <td>
            <img width="250" alt="image" src="https://github.com/user-attachments/assets/f2bda21d-85c4-404d-aa27-18da1650d72b" />
        </td>
    </tr>
</table>
-->


<!--
Other options that were considered:
<table border="1">
    <tr>
    <th>Name</th>
    <th>Summary</th>
    <th>Picture</th>
    </tr>
    <tr>
        <td>
            <a href="https://es.aliexpress.com/item/1005011717869374.html?spm=a2g0o.productlist.main.2.450b6311tFjwCL&algo_pvid=b312198c-d084-4474-8f0e-bfb33dbd1c6d&algo_exp_id=b312198c-d084-4474-8f0e-bfb33dbd1c6d-1&pdp_ext_f=%7B%22order%22%3A%221821%22%2C%22eval%22%3A%221%22%2C%22orig_sl_item_id%22%3A%221005011717869374%22%2C%22orig_item_id%22%3A%221005010485096642%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21EUR%212.94%211.47%21%21%2122.55%2111.27%21%40211b65de17817129622565772e7b9b%2112000056337299710%21sea%21ES%21184981297%21X%211%210%21n_tag%3A-29919%3Bd%3Ae78d15fa%3Bm03_new_user%3A-29895&curPageLogUid=won9y370f3UT&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005011717869374%7C_p_origin_prod%3A1005010485096642">    </a>
        </td>
        <td>Low voltage plastic buttons set. Momentary off-on switch. Size: 12x12x7.3mm. </td>
        <td><img width="250" alt="image" src="https://github.com/user-attachments/assets/ff7ca54d-0112-4243-9ed9-f9bbcee00926" />
        </td>
    </tr>
    <tr>
        <td>
            <a href="https://es.aliexpress.com/item/1005008558481882.html?spm=a2g0o.productlist.main.1.450b6311tFjwCL&algo_pvid=b312198c-d084-4474-8f0e-bfb33dbd1c6d&algo_exp_id=b312198c-d084-4474-8f0e-bfb33dbd1c6d-0&pdp_ext_f=%7B%22order%22%3A%221965%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21EUR%212.35%212.26%21%21%2118.00%2117.31%21%40211b65de17817129622565772e7b9b%2112000045709231087%21sea%21ES%21184981297%21X%211%210%21n_tag%3A-29919%3Bd%3Ae78d15fa%3Bm03_new_user%3A-29895%3BpisId%3A5000000209378863&curPageLogUid=9mJs1fpkfiy9&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005008558481882%7C_p_origin_prod%3A">
            Momentary Pushbutton Switches DS228 DS428
            </a>
        </td>
        <td>
            Low voltage plastic buttons set. Momentary off-on switch. Size: 12mm.
        </td>
        <td>
            <img width="250" alt="image" src="https://github.com/user-attachments/assets/34235389-e47f-4455-9a61-6511d3f07fb5" />
        </td>
    </tr>
    <tr>
        <td><a href=></a></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td><a href=></a></td>
        <td></td>
        <td></td>
    </tr>
</table> -->

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

<!--
<div align="center">
<table>
    <tr>
        <td>
            <strong>Final chosen product:</strong></br> https://uk.anycubic.com/products/high-speed-pla-filament?variant=46608821616925
        </td>
        <td>19.98€</td>
        <td>
            <img width="200" height="200" alt="PLA_high_speed_Texture_Grey_1" src="https://github.com/user-attachments/assets/42b6cac1-6261-41c1-9bbc-791c8e459eda" />
        </td>
    </tr>
</table>
</div>
      
<div align="right">
</div> -->
  
     
*Referenced articles:* 
- [Comparison table](https://3dstarter.com/en/material/pla-vs-abs)
- [PLA vs PETG vs ABS](https://ultimaker.com/learn/petg-vs-pla-vs-abs-3d-printing-strength-comparison/)
- [Standard PLA vs High Speed PLA](https://3dprintingcanada.com/blogs/news/pla-vs-high-speed-pla-whats-the-real-difference?shpxid=c09efa71-5de1-4c63-8740-651b2d3c38b0)

</br>

Link to the product: [Anycubic High Speet PLA - Mate Grey 1Kg Spool](https://uk.anycubic.com/products/high-speed-pla-filament?variant=46608821616925)
   

## 2.6 Other small elements.
Other supporting components such as terminal blocks, connectors, and wiring will also be documented throughout the project where relevant. Since these parts are relatively standard, they will not receive dedicated sections unless a particular design decision requires further explanation.
    
---
   
# 3. Product design
<!-- the design chapter is organized around individual subsystems (buttons, motherboard housing, LED module, directional controls)-->
## 3.1 Design methodology and approach.


## 3.2 Action button array.
### 3.2.1 Hand ergonomics.
### 3.2.2 Button screw in feature.  

## 3.3 Motherboard housing (Motherboard container within the enclosure)
### 3.3.1 Modeling the positive for reference
### 3.3.2 Modeling the housing.

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
   
# 4. Assembly and Electronics Integration
## 4.1 Wiring the motherboard
## 4.2 Wiring the action buttons
## 4.3 Wiring the arrow buttons
## 4.4 Wiring the led funcionality
## 4.5 wiring the charging port.
   
---
   
# 5. Testing and Validation
## 5.1 Input delay
## 5.2 Tournament legality
## 5.3 Comfort test
## 5.4 LED functionality
## 5.5 Charging and USB connection
## 5.6 Bluetooth connection
   
---
   
# 6. Final Customization
## 6.1 Custom art cover
## 6.2 Custom buttons
   
---
   
# 7. Conclusions and Future Improvements
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

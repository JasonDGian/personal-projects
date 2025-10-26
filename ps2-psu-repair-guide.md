# 🗒️ Playstation 2 'fat' PSU repair guide.

>[!CAUTION]
>I’ll assume anyone following these instructions has basic electronics knowledge and understands the risks involved. **I’m not responsible for any injuries or damage caused by mishandling high voltages.**
>To perform these diagnostics and repairs, you’ll need to disassemble your PS2 and remove the power board. If you’re not confident working with electronics, it’s safer and easier to buy a replacement PSU online for around 15€.
>As for why I bother repairing these old power supplies instead of buying new ones, it’s because I value keeping my hardware as original as I can, and there’s something satisfying about bringing discarded parts back to life.


## 📍 Picture and references.
I will be referring often to this picture of my PSU and mention the marked elements to explain the process. Make sure to have the image ready as you read to understand what i am talking about.
    
**In the image we can see the following elements:**
- **A**: Landline connector. This connector connects to live **high voltage (220-240)**. Handle with extreme care. <mark>Do not touch the metal contacts when connected.</mark>
- **B**: Double 12V Output connector. This is the connector where the transformed power should come out and feed the console. 
- **C**: 2.5A/250V fuse. This fuse breaks the circuit in case of over-current or over-voltage to protect the board and console.
- **D**: Capacitor C20. 22uf 50V 105ª
- **E**: Capacitor C3. 33uf 35V 105ª
- **ZD1**: Zener Diode. 18V 
- **ZD3**: Zener Diode. 18V
- **Octocoupler**: The octocoupler is a 4 pin PC123. 

![image 1](https://github.com/user-attachments/assets/cbee254a-dc73-489b-b690-64059d1ac517)

## 📍 Tools required for the job.
- Multimeter or Tester.



## 📍 How to confirm a faulty PSU unit.
Before you start tinkering with a powersupply is best to know if it is actually faulty. If your PS2 is not turning on there may be other issues at hand that may not be related to the PSU. 

### 🔸 Console symptoms
The console wont turn on, no red LED light and no reaction to **`ON`** or **`RESET`** buttons in any way when the console is plugged in and the switch on the back is on.
    
### 🔸 Testing the board.
The fastest way to test if the board is bad is to have another power supply around and swap them out, if the console works again then the power supply is the issue. If you don't have another PSU of the same model laying around
another way to test if the PSU is fault is to test the output pins and check if they give the correct voltage output. 
    
**Testing the pins**     
For this we will need the multimeter.     
Your unit's task is to take in the **`120v`/`240v AC`** from your home's electricty and turn it into **`@12V DC`**.
To test if your unit is doing it's job, place your unit on a **non conductive surface to avoid shortcircuits** (wood,plastic), plug in the unit <mark>**(please be ware; DO NOT TOUCH Point A , is LIVE with 120v/204v)**</mark>, 
and switch it on. Now with a multimeter check the **1st** socket from the left and the **4th** socket from the left for DC Voltage on **Point B**.
         
If the multimeter shows around 24 volts DC, then the unit is fine and working propperly, if the multimeter shows 0v DC then we have some work to do.
     
**TURN OFF AND UNPLUG BEFORE CONTINUING**      
    
## 📍 Possible issues:
Now that we confirmed that the unit is not working propperly, let us see the possible issues.
1. Burned out fuse.
2. Blown capacitors.
3. Capacitors lost capacitance.
4. Octocoupler is not working.
5. Zener Diodes / Diodes broke.
6. Burned Mosfet.
     
---
     
<img align="left" width="180" height="180" alt="Fuse" src="https://github.com/user-attachments/assets/693dc6dc-6301-4ea3-8316-a6c325289aae" />
     
### 🔸 The Fuse
The first thing to test is the F1 Fuse (Point C), simply set the multimeter on "continuity" or "resistance (Ω)" and if the multimeter beeps or shows 0 Ω then the fuse is OK and working.
In case the fuse presents no continuity it would mean it is burned and needs to be replaced. In my case, all units i repaired were PAL units and the fuse was 250V 2.5A but these may differ for other regions, so be sure to check your fuse before you buy a replacement, if you don't find the exact same fuse, buy one slightly lower as close to the original as possible.
     
--- 
      
<img align="left" width="180" height="180" alt="blown-capacitor" src="https://github.com/user-attachments/assets/96776de8-7ab0-4760-92ca-1a3f934eea53" />
      
### 🔸 Blown Capacitors
Most of the time blown capacitors are quite easy to identify as their phisical appearence change and some even smell bad. If a capacitor is showing a "bulge" on top, it means it most certainly needs replacement. To test them with the multimeter, connect one pin to ground or negative (3rd or 4th socket on point B)  and test both "legs" of the capacitor on the under side of the board. One leg should give continuity to ground/negative while the other should NOT give continuity (positve "leg" should not). If one capacitor does give continuity in both legs, means is broken and needs to be replaced.
In case you need to replace one of these capacitors, check what is written on them, the Capacitance, the volts, and the temperature. for istance: 680Uf - 16V - 105º.    
_Click to enhance_   
    
--- 
    
<img align="left" width="180" height="180"  alt="lost-capacitance" src="https://github.com/user-attachments/assets/4f8799cf-cd1a-466d-bf94-d1d9e2b0a2e8" />
    
### 🔸 Capacitors lost capacitance
<mark>**This is the absolutely most common issue i have encountered with these power boards.**</mark>
Mainly C20 and C3 (point D and E) tend to lose capacitance making it impossible for the board to do its job.
To propperly test the capacitance of a capacitor is kind of quirky afaik, so the next best thing is to simply buy one of each online and change them both. I bought 2 packs of 10 each for about 2 euros, and almost finished them due to how common this issue is, so in any case, sooner or later, you may need to replace them so why not now that you are working on it.
    
---
    
<img align="left" width="180" height="180" alt="octocopler" src="https://github.com/user-attachments/assets/93676a63-9843-42cb-8a9c-3df5d02f1251" />    
       
### 🔸 Octocoupler.
This spider looking fella only troubled me once, but is worth checking out nontheless.   
In my case the OC was a PC123 equivalent.    
You can google how to test an octocoupler. Is quite simple.    
<br/>
<br/>
<br/>
    
---   
       
<img align="left" width="180" height="180" alt="zd18v" src="https://github.com/user-attachments/assets/421e197c-d4c9-41f4-8a79-deb3249312c6" />   
      
### 🔸 Zener diodes / Diodes.
Set your multimeter to continuity and test the diodes both way. A working diode gives continuity in only "one way". The diodes have a "direction" in which they block or allow current. Test your diode both ways, in one way it should block the current while in the other it should allow it. If the diode gives continuity both ways, or gives no cintuinity at all, is broken. The most common diode to fail is ZD1 and ZD3. You may also want to check the top left corner diodes D10 D9 D7 D8. Testing all the diodes present in the circuit is not a bad idea, just an extra security and is often among the first things  you want to rule out.   
    
---
      
<img align="left" width="180" height="180" alt="zd18v" src="https://github.com/user-attachments/assets/1586a2b9-fbc1-43b2-a311-c4531e182197" />   
    
### 🔸 Broken mosfets.
I never found an issue with these but i've heard of people that did.    
In the picture you will notice 2 heatsinks running vertically near the capacitors on the left and near the Zener diodes. If everything else you have tested up until now is working well and you still have issues, these little guys may be the problem.    
If you have any doubts please ask, I am not an expert, but will gladly help in what i can.
<br/>
<br/>
    
---
    

## ❓ Questions I answered in the GBA Temp forum.
These are some questions I took time to answer in the GBA Forum and Reddit where I originally posted my guide. 

- Q1 - Can i swap my broken power supply with the power supply of another ps2?
- A1 - Technically  you could but you will probably run into some issues. From one revision to another, or model to another, the PSU could change in phisical shape and probably won't fit into the console correctly. The 12V pins socket will be moved and so will be the L-N connector. This will make it practically impossible to re-assemble the unit correctly giving you some frankentseiny-ps2.

---

- Q2 - I Can't repair my psu, i can't find a replacement, what do i do?
- A2 - You can buy an external PSU with the correct values and hook it up to the console's input pins. I've done this to test consoles and check if it really was the PSU causing issues and it worked fine. You can check original board for the values you need for the PSU.

 Im talking about this kind of external PSU.

---

Q3 - Information about the MOSFET.

A3 - I honestly can't recall the specs and i can't currently check, if you happen to need this information you can take the mosfet out of the board and see what's written on it, googling this should bring info up.

Example: On one of the sides, there is stuff written, one of these is the name of the brand, the voltage and the model, look for the model name.


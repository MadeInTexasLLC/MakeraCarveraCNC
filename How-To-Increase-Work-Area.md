# How To Double Your Work Area / Machine Oversized Stock

## Summary:
###*Need more work area to cut your design?*  
###*Don’t want to buy a bigger machine?*  
#### **This guide will show you how to effectively double the work area of your Carvera CNC.**  
*NOTE: This workaround MAY be possible with the Carvera Air CNC, but it has not been explored.*  

## Items Needed:
1. XYZ Probe (included with Carvera CNC)
2. Carvera Controller Software: v0.9.11 (included on Makera's official website)
    - There is a community version of the Carvera Controller, but the work around has not been tested for that Controller, yet.
3. That's it!  


## Process-Breakdown:
### **Step #1 Ensure stock falls within dimensions of 360mm (x) x 240mm (y) x 140mm (z)**  
  
**IMPORTANT**: Technically, the stock has a maximum dimensional limit of **359mm (x) x 479mm (y) x 140mm (z)**  
- This is to ensure proper usage of the XYZ Probe, but more on this later.  

### **Step #2 Design your part in Computer-Aided Design (CAD) and process the design in Computer-Aided Manufacturing (CAM)**  

**IMPORTANT**: In your CAM software, ensure that the work origin is set to the TOP LEFT corner of your chosen stock.
**NOTE**: - This specific How-To assumes that you have basic knowledge of CAD/CAM, and will NOT go into depth on best practices  
regarding design. However, I am currently working on a quick-start guide for this, and will eventually include it in this repository.

### **Step #3 Adhere stock to the Carvera Bed**  
  
- Step #3a: Place masking tape to the back of your stock and to the bed of the Carvera.
- Step #3b: Place your chosen glue to top of the masking tape of the bed.
- Step #3c: Align the masking tape placed on the stock to the masking tape placed on the bed, and then sandwich the glue between the two.

**IMPORTANT**: During Step #3c, use the side of the Automatic Tool Changer (ATC) as a make-shift straight edge to help properly align your stock whilst adhering it to the bed.  
**NOTE**: This How-To will not go into depth on specific glues/masking tape to use. The most beginner-friendly and budget-friendly option I have experienced, coupled with the auto-leveling capabiltiies of the Carvera, I have chosen to use **Sctoch Beige 2in Wide Masking Tape** and **Gorilla Glue Sticks** with a **Bauer Hot Glue Gun**. Details on this choice will be explored in a separate file in this repository.
              
### **Step #4 Use the manual XYZ Probe**  
- Step #4a: Connect and orient your XYZ Probe to sit flush against the top LEFT corner of your stock.  
- Step #4b: Move the tool head (with the correct tool) until it is hovering over the center of the XYZ Probe.
- Step #4c: Connect the magnetic wire head to the tool head.
- Step #4d: Select your NC Program, and then run the XYZ Probe command from the Config Menu.  
- Step #4e: Once the XYZ Probe command has been completed, exit the File window, and reopen the window to view changes in the stock origin.  
- Step #4f: Take note of the current Offset from Anchor 1 that is displayed.
- Step #4g: Once the measured Offsets from the XYZ probe are recorded, go to the Manual Offset Input page.
- Step #4h: Re-Enter the recorded X-Offset as noted.
- Step #4i: Re-Enter the Y-Offset **BUT add 50mm to that value first BEFORE inputting the value**.
    - The XYZ Probe command touches off in the -Y direction. To correct the machine, and tell it that the edge of the material  
        is actually in the opposite direction, we must add 50mm to the Y-Offset since that is the Edge-Edge distance of the XYZ Probe

### **Step #5 THAT'S IT!!!**
Now, you can effectively cut on a larger piece of stock. Granted, you must process the stock twice. 
Additionally, this guide doesn't show you how to use alignment pins in order to affix your stock accurately for a two-process milling.  
However, the core principle of this guide can be applied once you learn that workflow.

![CNC-bit-naming-diagram](https://github.com/user-attachments/assets/a88cded6-8fb1-4473-a3da-c7aed03a5e3c)

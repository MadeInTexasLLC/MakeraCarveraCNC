# How To Double Your Work Area / Machine Oversized Stock

## Summary:
*Need more work area to cut your design?*  
*Don’t want to buy a bigger machine?*  
#### **This guide will show you how to effectively double the work area of your Carvera CNC.**  
*NOTE: This workaround MAY be possible with the Carvera Air CNC, but it has not been explored.*  

## Items Needed:
1. XYZ Probe (included with Carvera CNC)
2. Carvera Controller Software: v0.9.11 (included on Makera's official website)
    - There is a community version of the Carvera Controller, but the work around has not been tested for that Controller.
3. That's it!  


## Process-Breakdown:
### **Step #1 Ensure stock falls within dimensions of 360mm (x) x 240mm (y) x 140mm (z)**  
  
**IMPORTANT**: Technically, the stock has a maximum dimensional limit of **359mm (x) x 479mm (y) x 140mm (z)**  
- This is to ensure proper usage of the XYZ Probe, but more on this later.  

### **Step #2 Design your part in Computer-Aided Design (CAD) and process the design in Computer-Aided Manufacturing (CAM)**  
  
- This specific How-To assumes that you have basic knowledge of CAD/CAM, and will NOT go into depth on best practices  
regarding design. However, I am currently working on a quick-start guide for this, and will eventually include it in this repository.

### **Step #3 Adhere stock to the Carvera Bed**  
  
**IMPORTANT**: Use the side of the Automatic Tool Changer (ATC) as a make-shift straight edge to properly align your stock.  
- Next, use double-sided tape or masking tape/liquid adhesive to affix your stock to the bed.
        NOTE: This How-To will not go into depth on specific adhering methods. However, a separate file
              will be created to explore the results of different adhering methods.
              
### **Step #4 Use the XYZ Probe on the Top Left of your Stock**  
#4a. Orient your XYZ Probe to sit flush against the top LEFT corner of your stock  
#4b. Move the tool head until it is hovering over the center of the XYZ Probe.
#4c. Plug in your XYZ Probe and connect the magnetic wire head to the tool head
#4d. Select your NC Program, and then run the XYZ Probe command from the Config Menu
#4e. Once the XYZ Probe command has been completed, exit the File window, and reopen the window.
    - This should now move your work origin accordingly
#4f. Take note of the current Offset from Anchor 1 that is displayed.
#4g. Re-Enter the X-Offset and then add 50mm to the Y-Offset and input that number.
    - The XYZ Probe command touches off in the -Y direction. To correct the machine, and tell it that the edge of the material  
        is actually in the opposite direction, we must add 50mm to the Y-Offset since that is the Edge-Edge distance of the XYZ Probe

### **Step #5 Run your NC Program and Watch the Fun!**
THAT'S IT!  
Now, you can effectively cut on a larger piece of stock. Granted, you must process the stock twice. 
Additionally, this guide doesn't show you how to use alignment pins in order to affix your stock accurately for a two-process milling.  
However, the core principle of this guide can be applied once you learn that workflow.

![CNC-bit-naming-diagram](https://github.com/user-attachments/assets/a88cded6-8fb1-4473-a3da-c7aed03a5e3c)

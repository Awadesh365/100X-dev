### **🔹 Ultimate Prompt Format for Best Results**  
 
This structured prompt format ensures **precise, optimized, and high-quality results**, making collaboration smoother and implementation faster. 🚀  
 
---
 
## **1️⃣ Project Context & Goal (🔹 Why are we doing this?)**  
💡 **Task:** *(Clearly define what needs to be done.)*  
- Example: *I need to add two chips (percentage change & difference from yesterday) in the top-right corner of the first energy card while keeping it responsive and optimized.*  
 
📍 **Where does this feature apply?** *(Mention the file/component name.)*  
- Example: *This applies to `CustomCardBox.jsx`, but the new chips should only appear on the "Total Energy Consumed Today" card.*  
 
---
 
## **2️⃣ Reference Materials (📸 Screenshots, Figma, Documentation)**  
🎨 **Visual Reference:** *(Attach any UI design references for accuracy.)*  
- 📸 **Screenshot of Current UI:** *(Attach an image and highlight key points.)*  
- 🎨 **Figma Link:** [Insert Figma Link] *(If available.)*  
- 📜 **Planning Document:** [Insert Link] *(If relevant.)*  
 
🔍 **Expected UI Changes:** *(Describe any changes needed based on the reference materials.)*  
- Example: *The percentage chip should be above the difference chip. Both should have a fixed font and responsive layout.*  
 
---
 
## **3️⃣ Existing Code & Where to Implement (📌 Important Code Blocks)**  
📌 **Existing Code Snippet:** *(Provide the relevant code where changes need to be made.)*  
```jsx
<Grid item xs={12} sm={6} md={4}>
    {renderCustomCardBox(
        "Total Energy Consumed Today",
        getFormattedEnergyValue(energyToday?.data, defaultNumberStyle),
        First,
        defaultTextStyle,
        defaultNumberStyle,
        { showBadge: false }
    )}
</Grid>
```  
 
🛠 **Where to Modify?** *(Specify the exact part of the component or logic that needs updating.)*  
- Example: *We need to modify `CustomCardBox.jsx` to support these new chips but only for this specific card, without affecting others.*  
 
---
 
## **4️⃣ Expected Output (✅ Final Behavior & Requirements)**  
✅ **Final Behavior:** *(List exactly how the feature should work.)*  
- **New Chips:**  
  - 📈 **Percentage Change Chip** (Green if positive, Red if negative).  
  - 🔻 **Difference from Yesterday** (Only the number should be colored, not the text).  
- **Font Rules:**  
  - **Numbers → Montserrat (bold)**  
  - **Text ("than Yesterday") → Lato (bold)**  
- **Number Formatting:**  
  - Convert values to `kWh`, `MWh`, or `GWh` dynamically.  
  - Always show numbers **toFixed(2)**.  
 
🖥 **Responsiveness & Optimization:**  
- No `px` values (since it's for big TV screens).  
- Should **not break UI** if large numbers are displayed.  
- Ensure **future API support** (placeholder JSON for now, actual API later).  
 
---
 
## **5️⃣ Constraints & Future-Proofing (⚡ Optimized Development)**  
⚡ **Performance & Optimization:**  
- **Minimal re-renders** → Avoid unnecessary state changes.  
- **Reusable Utility Function** → Move number formatting logic to a utility file.  
 
📌 **Future API Consideration:**  
- The API is not updated yet, so implement with dummy data for now:  
```json
{
  "data": 506.69,
  "change": "-99.18",
  "difference": "-13333.23"
}
```  
- Later, uncomment the API integration once it’s live.  
 
---
 
## **6️⃣ Additional Notes & Edge Cases (🔍 Important Considerations)**  
🔸 **Handling Negative Values:**  
- Red background for negative difference values.  
- Only the **number should be colored**, not "than Yesterday."  
 
🔹 **Where This Should & Should Not Apply:**  
- ✅ **Show only on "Total Energy Consumed Today"** card.  
- ❌ **Do not affect other `CustomCardBox` instances.**  
 
---
 
### **📌 Example Prompt Using This Format**  
 
💡 **Task:**  
I need to add **percentage change & difference from yesterday** on the **first energy card** (top-right corner). The UI should match our **Figma mockup** and be responsive.  
 
📌 **Where Does This Apply?**  
- `CustomCardBox.jsx`, but only for the "Total Energy Consumed Today" card.  
 
🎨 **Reference Design:**  
- 📸 **Screenshot:** *(Attach a UI screenshot.)*  
- 🎨 **Figma Link:** [Insert Figma Link]  
- 📜 **Planning Document:** [Insert Link]  
 
✅ **Expected Behavior:**  
- Two chips in the **top-right corner**:
  - **Percentage Change:** `📈 +5.67%` (green) / `📉 -3.42%` (red).  
  - **Difference From Yesterday:** `+217.46 MWh` or `-125.32 kWh` (**number in color, text stays black**).  
- **Number background should match the color status** (red/green).  
- **Fonts:**  
  - **Numbers → Montserrat (bold)**  
  - **Text ("than Yesterday") → Lato (bold)**  
 
⚡ **Constraints & Optimizations:**  
- **No px values** (it's for big TV screens).  
- **Applies only to this card**, not all `CustomCardBox` instances.  
- **Future-proofing:** Use a placeholder JSON for now, switch to the real API when available.  
 
---
 
### **🔹 Why This Format Works Best?**  
✅ **Crystal-clear expectations** → No confusion about requirements.  
✅ **Fast & efficient implementation** → Saves time and ensures correctness.  
✅ **Scalable & reusable** → Helps maintain clean, optimized code.  
 
🔥 **Now, every time you make a request, just follow this structure!** 🔥

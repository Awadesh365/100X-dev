### 🚫 **Bad Prompt Practices to Avoid** 🚫  
 
Using poorly structured prompts can lead to **confusing responses, wasted time, and incorrect implementations**. Avoid these common mistakes to ensure **clarity, precision, and efficiency** in your requests.  
 
---
 
## **1️⃣ Vague & Unclear Requests**  
❌ **Example:**  
*"I need to add some values to the card."*  
🔴 **What’s wrong?**  
- **Which card?** *(There could be multiple.)*  
- **What values?** *(Are they from an API? Are they numbers?)*  
- **Where should they be displayed?** *(Inside? Outside? Top? Bottom?)*  
 
✅ **Better Prompt:**  
*"I need to add two new values (percentage change & difference from yesterday) to the **top-right corner** of the **first energy card**. These values will come from an API, but for now, use dummy data."*  
 
---
 
## **2️⃣ No Context or Missing Key Details**  
❌ **Example:**  
*"Make the number look good."*  
🔴 **What’s wrong?**  
- **What does "look good" mean?** *(Bigger? Bolder? A specific font? Different color?)*  
- **Where should this be applied?** *(All numbers or just specific ones?)*  
- **Does it need formatting (kWh, MWh, GWh)?**  
 
✅ **Better Prompt:**  
*"Ensure that energy values dynamically adjust between kWh, MWh, and GWh based on size. Use **Montserrat (bold) for numbers** and **Lato (bold) for text**. Numbers should always show **two decimal places** (`toFixed(2)`)."*  
 
---
 
## **3️⃣ Overloading with Too Many Requests at Once**  
❌ **Example:**  
*"Add the new API values, change the font, fix the responsiveness, and make it future-proof."*  
🔴 **What’s wrong?**  
- **Too many tasks at once.** *(This leads to confusion and longer implementation time.)*  
- **Some tasks depend on others.** *(API might not be ready, so breaking it into steps is better.)*  
 
✅ **Better Prompt:**  
*"Step 1: Add two new values (`percentageChange` and `differenceFromYesterday`) using dummy data for now. Display them in the **top-right corner** with the correct colors and formatting."*  
*"Step 2: Once the API is ready, replace the dummy data with live values."*  
 
---
 
## **4️⃣ Asking for "Best Practices" Without Specific Needs**  
❌ **Example:**  
*"Can you optimize this?"*  
🔴 **What’s wrong?**  
- **Optimize for what?** *(Performance? Readability? Maintainability? UI?)*  
- **What part needs improvement?** *(All of it? A specific function? A certain component?)*  
 
✅ **Better Prompt:**  
*"Can you refactor the number formatting logic to be more reusable? Right now, it’s inside `CustomCardBox.jsx`, but I think it should be moved to a utility function for better maintainability."*  
 
---
 
## **5️⃣ Ignoring Edge Cases & Future-Proofing**  
❌ **Example:**  
*"Just show the number."*  
🔴 **What’s wrong?**  
- **What happens if the number is too large?** *(Should it break the UI? Convert to MWh?)*  
- **What if the API sends `null` or `undefined`?** *(Should it show `N/A`?)*  
 
✅ **Better Prompt:**  
*"Ensure energy values are **formatted properly** (`kWh`, `MWh`, `GWh`) and **always show two decimal places**. If the API returns `null`, display `N/A`. If the number is negative, highlight it in **red**."*  
 
---
 
## **6️⃣ Not Specifying Where the Change Should Apply**  
❌ **Example:**  
*"Update `CustomCardBox.jsx`."*  
🔴 **What’s wrong?**  
- **Update what?** *(The whole file? A specific function? A certain style?)*  
- **Does this affect all instances of `CustomCardBox`?** *(Or just one card?)*  
 
✅ **Better Prompt:**  
*"Modify `CustomCardBox.jsx` **only for the first energy card** to display the new API values in the **top-right corner**, without affecting other instances."*  
 
---
 
## **7️⃣ Providing Only Partial Information**  
❌ **Example:**  
*"Fix the error."*  
🔴 **What’s wrong?**  
- **What error?** *(Frontend? Backend? API? Console? UI issue?)*  
- **What’s the error message?** *(Provide exact logs or screenshots.)*  
 
✅ **Better Prompt:**  
*"I'm getting this error: `Uncaught TypeError: value.toFixed is not a function`. It happens inside `formatEnergyValue()` in `CustomCardBox.jsx` when calling `toFixed(2)`. Can you help fix it?"*  
 
---
 
## **8️⃣ Ignoring Performance & Scalability**  
❌ **Example:**  
*"Just add the new values to the card."*  
🔴 **What’s wrong?**  
- **Will this cause unnecessary re-renders?**  
- **Can the logic be reused in other places later?**  
 
✅ **Better Prompt:**  
*"Create a **utility function** for number formatting (`kWh`, `MWh`, `GWh` conversion) so we can reuse it across multiple components. Use it inside `CustomCardBox.jsx` for now."*  
 
---
 
## **🔥 Conclusion: How to Write a Great Prompt 🔥**  
 
✅ **Use this simple formula for every prompt:**  
**📌 [What] → [Where] → [How] → [Why] → [Edge Cases]**  
 
🚀 **Example of a Perfect Prompt:**  
*"I need to display two new values (`percentageChange` and `differenceFromYesterday`) inside the **first energy card** (`CustomCardBox.jsx`). These should be placed in the **top-right corner**. Numbers should be **bold (Montserrat)** and text should be **bold (Lato)**.  
 
- Positive numbers = **green**, negative numbers = **red**.  
- The **number should have a background matching its color**, but the text ("than Yesterday") should always remain black.  
- Format numbers using `kWh`, `MWh`, or `GWh`, keeping **two decimal places**.  
 
Right now, the API isn’t updated, so use this **dummy data**:  
```json
{
  "data": 506.69,
  "change": "-99.18",
  "difference": "-13333.23"
}
```  
Later, we’ll replace it with live API values. Ensure this **does not affect other cards** that use `CustomCardBox.jsx`."*  
 
---
 
### **🔹 Summary of What to Avoid**  
❌ **Vague Requests** → Be specific about **what, where, and how.**  
❌ **Lack of Context** → Show **code snippets, screenshots, or API examples.**  
❌ **Multiple Requests at Once** → Break tasks into **small, clear steps.**  
❌ **Unclear Error Descriptions** → Provide **error messages, logs, and details.**  
❌ **No Future-Proofing** → Consider **scalability, reusability, and performance.**  
 
🔥 **Follow this structure, and you'll always get fast, accurate, and optimized responses!** 🚀

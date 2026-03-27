# AI Usage Report — Assignment 2

**Student:** Lamees Alharbi  
**Tool:** Gemini 3    
**Date:** March 2026  

---

# 1. Detailed AI Assistance & Problem Solving

### A. UI/UX: Glassmorphism Implementation
* **Prompting Strategy:** I requested a "frosted glass" CSS architecture that would remain legible over a high-contrast background.
* **AI Contribution:** Provided the foundational `backdrop-filter: blur()` and `rgba` background logic.
* **Refinement & Adaptation:** I found the initial AI suggestion (10px blur) was too "see-through" on iPad displays. I manually increased the blur to **20px** and added `saturate(150%)` and `contrast(100%)` to ensure the "Daily Inspiration" text met accessibility standards.

### B. Responsive Debugging (iPad & iPhone)
* **The Problem:** During testing on an **iPhone 16 Pro (402x874px)**, the "About Me" and "Skills" sections were shifting 20px to the left, creating an unprofessional horizontal overflow.
* **AI Troubleshooting:** I shared my CSS structure with the AI to find the conflict. The AI identified that fixed widths were clashing with internal padding.
* **The Solution:** Following AI guidance, I implemented `box-sizing: border-box` and transitioned from fixed pixel widths to **viewport-relative widths (92%)**. This ensured the "Glass" boxes stayed perfectly centered with balanced margins on all mobile dimensions.

### C. Asynchronous Data Handling (API)
* **AI Contribution:** Provided the boilerplate for the `fetch()` logic using the **DummyJSON Quotes API**.
* **Modification:** I insisted on adding a `try/catch` block for robust error handling. I also manually inserted a **"Loading..."** state in the DOM to ensure immediate user feedback during the fetch request, satisfying Requirement #5 of the grading rubric.

### D. Hardware-Specific Optimization
* **The Bug:** A custom "glow" cursor was getting "stuck" on touch-screen devices (iPad), creating "stains" on the UI.
* **AI Solution:** The AI suggested using the JavaScript `matchMedia("(pointer: fine)")` method.
* **Result:** This logic ensures the interactive cursor only activates when a high-precision mouse is detected, providing a clean, "native" feel for touch-screen users.

---

##  2. Evidence of Understanding & Learning
I ensured full comprehension of every AI-suggested line:
1.  **Vendor Prefixes:** I learned that `-webkit-backdrop-filter` is mandatory for **Safari (iPad)** compatibility.
2.  **CSS Box Model:** I now understand how `border-box` prevents padding from increasing a container's total width.
3.  **Media Queries:** I learned to detect **input types** (touch vs. mouse) rather than just screen width.

---

##  3. Benefits & Challenges
* **Benefits:** AI served as a "Senior Developer" partner, helping me solve complex layout shifts in minutes that would have otherwise taken hours of manual trial-and-error.
* **Challenges:** The AI initially suggested solid hex backgrounds (#ffffff). I had to correct the AI and demand **RGBA** transparency levels below `0.2` to achieve the desired "Apple Studio" aesthetic.
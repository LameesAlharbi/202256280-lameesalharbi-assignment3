#  Interactive Software Portfolio — Assignment 2
**Student:** Lamees Alharbi  
**Course:** SWE363: Web Engineering  
**Institution:** KFUPM  

---

##  Project Overview
This project is an advanced, interactive personal portfolio. Building upon Assignment 1, this version transitions from a static site to a dynamic web application featuring **Glassmorphism UI**, **Asynchronous Data Fetching**, and **State Persistence**. It is engineered to be fully responsive across high-end mobile devices (iPhone 17 Pro) and tablets (iPad Air).

##  Key Technical Features
* **Dynamic Greeting Component:** Uses JavaScript `Date()` objects to provide a real-time, context-aware welcome message.
* **Third-Party API Integration:** Utilizes the `fetch` API with `async/await` to pull daily quotes from **DummyJSON**, including a "Loading..." state for better UX.
* **Theme Memory:** Implements the **LocalStorage API** to save user preferences (Dark/Light mode), ensuring the theme persists even after a browser refresh.
* **Responsive Glassmorphism:** A custom CSS architecture using `backdrop-filter: blur(20px)` and `box-sizing: border-box` to ensure pixel-perfect symmetry on mobile viewports.

##  Project Structure
To ensure "Separation of Concerns," the repository is organized as follows:
* `index.html` — The semantic core of the application.
* `css/styles.css` — Contains advanced layout logic, CSS variables, and media queries.
* `js/script.js` — Handles DOM manipulation, API calls, and event listeners.
* `assets/images/` — Contains optimized project images and personal Memoji.
* `docs/` — **Mandatory Documentation:**
    * `ai-usage-report.md`: Detailed log of AI collaboration and problem-solving.
    * `technical-documentation.md`: Deep-dive into implementation logic and the folder structure.

##  Setup & Local Testing
1.  **Clone the Repo:** `git clone [Your-Link-Here]`
2.  **Run Locally:** Open `index.html` with the **Live Server** extension in VS Code.
3.  **Responsive Testing:** Open Developer Tools (`F12`) and test using the following dimensions:
    * **iPhone:** 440px x 956px
    * **iPad:** 834px x 1194px

##  AI Integration Summary
AI (Gemini) was utilized for complex UI debugging—specifically solving the "sticky cursor" bug on touch screens and fixing horizontal overflow on the iPhone viewport. A full breakdown of prompts and learning outcomes is available in `docs/ai-usage-report.md`.

---
**Author:** Lamees Alharbi  
*Software Engineering Student @ KFUPM*
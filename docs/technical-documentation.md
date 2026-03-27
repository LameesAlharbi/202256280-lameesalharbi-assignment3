#  Technical Documentation — Assignment 2

## 1. Project Architecture & Logic
This portfolio has been upgraded from a static HTML site to a dynamic web application. The architecture focuses on modular CSS and asynchronous JavaScript (ES6+).

### A. Folder Structure & Organization
To comply with professional standards and the assignment rubric, the project follows a strict hierarchical structure:

* **`/` (Root):** Contains `index.html` (the entry point) and the `README.md`.
* **`/css`:** Contains `styles.css`. Logic is separated into CSS Variables (Design Tokens), Global Styles, Component Styles (Glass Cards), and Media Queries.
* **`/js`:** Contains `script.js`. Functions are modularized to separate concerns (e.g., UI updates vs. API fetching).
* **`/assets`:** Organized into `/images` and `/icons` to keep the root directory clean.
* **`/docs`:** Dedicated directory for mandatory AI Usage and Technical breakdown reports.

## 2. Advanced Technical Implementations

### B. Asynchronous Data Handling (The API)
One of the core requirements was basic data handling. I implemented a random quote generator using the **DummyJSON API**.
* **Implementation:** I utilized the `fetch()` API combined with `async/await` syntax. This approach was chosen over `.then()` chains to improve code readability and maintainability.
* **Logic Flow:** 1.  Function triggers on page load.
    2.  `DOM` is updated with a "Loading..." string (Requirement #5: User Feedback).
    3.  A `try/catch` block manages the network request to prevent the site from breaking if the API is down.
    4.  Template literals are used to inject the fetched JSON data back into the HTML.

### C. State Persistence (LocalStorage)
To improve User Experience (UX), I implemented a theme-memory feature.
* **Technical Detail:** When the user toggles Light/Dark mode, a key-value pair is stored in the browser's **LocalStorage**. 
* **Logic:** Upon initial page load, a script immediately checks for the `theme` key. This prevents the "white flash" bug, ensuring the user's preferred aesthetic is applied before the full DOM renders.

### D. Responsive Glassmorphism Architecture
The "Apple-style" UI was achieved through complex CSS filtering rather than static images.
* **Backdrop Filters:** I used `backdrop-filter: blur(20px) saturate(150%)`.
* **Cross-Browser Compatibility:** To ensure the effect works on my sister's iPad (Safari), I included the `-webkit-` vendor prefix, which is a common technical requirement for non-Chromium browsers.
* **Box Model Fix:** I implemented `box-sizing: border-box` globally. This was critical for mobile responsiveness, as it prevents internal padding from "pushing" the glass boxes off the screen on iPhone dimensions (393px - 440px).

## 3. Deployment & Testing
* **Environment:** Developed in VS Code using the Live Server extension.
* **Mobile Simulation:** Manual testing was conducted using Chrome DevTools simulating **iPhone 16 Pro** and **iPad Pro** viewports to verify that the Flexbox containers wrap correctly without horizontal scrolling.
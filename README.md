# Rast Turizm - Corporate Website

## 1. Overview

This project is the official corporate website for **Rast Turizm**, a transportation and logistics services company based in Kocaeli, Türkiye. The site serves as a digital brochure and primary point of contact for new clients, showcasing the company's services (personnel/student transport, VIP services, logistics) and quality standards.

It is built as a high-performance, fully responsive, single-page static website. The entire site is crafted from scratch using pure HTML, CSS, and Vanilla JavaScript, with no external frameworks, ensuring maximum speed and simplicity. It is securely hosted on GitHub Pages with a custom domain (`rastturizm.com`) and enforced HTTPS.

## 2. Live Demo

The website is live and can be viewed at:
**[https://rastturizm.com](https://rastturizm.com)**

## 3. Features

* **Fully Responsive:** Adapts seamlessly to all screen sizes, from mobile to desktop, using CSS Grid and Flexbox.
* **Single-Page Design:** Smooth-scrolling navigation provides a fluid, modern user experience.
* **Dynamic Navbar:** The navigation bar is transparent on the hero section and transitions to a solid background with a smaller logo upon scrolling.
* **Functional AJAX Contact Form:** Integrates with **Formspree** to capture quote requests in the background. The user receives a success message on the same page **without** being redirected, thanks to an asynchronous `fetch` request.
* **SEO Optimized:** Includes semantic HTML, dynamic meta tags (Title, Description), and a `favicon` suite to ensure visibility on search engines.
* **Secure:** Deployed with an enforced HTTPS (SSL) certificate via GitHub Pages.

## 4. Technologies Used

* **HTML5:** Used for the core structure and semantic markup.
* **CSS3:** Used for all custom styling, animations, and responsive layouts (Flexbox & CSS Grid).
* **Vanilla JavaScript (ES6+):** Powers all interactive components (mobile menu, scroll navbar, AJAX form submission).
* **Formspree:** Used as the serverless backend to handle "Hızlı Teklif" form submissions.
* **GitHub Pages:** Used for static site hosting and deployment.

## 5. Key Components Explained

This project relies on custom-built JavaScript components for its core functionality:

1.  **Mobile Menu & Smooth Scroll:** Standard event listeners toggle a `.hidden` class on the mobile menu and use `window.scrollTo` with `'smooth'` behavior for navigation links.
2.  **Dynamic Navbar on Scroll:**
    * An event listener on the `window` object tracks the `scrollY` position.
    * If `window.scrollY > 50`, a `.scrolled` class is added to the `.navbar-container`.
    * This `.scrolled` class triggers CSS transitions that change the navbar's `min-height` and the `.logo-img`'s `height`, creating the shrinking effect.
3.  **AJAX Form Submission (Formspree):**
    * The form's `submit` event is intercepted using `event.preventDefault()`.
    * The form data is collected using the `FormData` API.
    * A `fetch` request (POST) is sent asynchronously to the Formspree endpoint (`action` URL) with an `'Accept': 'application/json'` header.
    * If the submission is successful (`response.ok`), the JavaScript shows a success message (`#success-message`) on the page, resets the form fields, and hides the message after 5 seconds. The user is **never** redirected from the main website.

## 6. Setup / Local Development

To run this project locally, no complex installation is required.

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/OzkanCelikkilic/rastturizm.com.git
    ```

2.  **Navigate to the Directory:**
    ```bash
    cd rastturizm.com
    ```

3.  **Open the File:**
    * Simply open the `index.html` file in your web browser to view the site.

`The questions I asked AI to make my website more professional-looking: `

1. Now you are playing the role of my experienced instructor, explain to me in easy and detailed why the nav bar gets over flown by the the project cards when I hover over it ?

 **AI response:** 
- This happens because the project cards use transform: translateY(-5px) on hover. A CSS transform moves the element visually but does not affect the layout of the page. That means the card shifts upward without pushing other elements, so it can slide into the navbar’s space.

- Also, when transform is applied, the element creates its own stacking context. If the navbar does not have a higher z-index, the hovered card can appear on top of it.

- The fix is to give the navbar a positioning value (like position: relative or fixed) and assign it a higher z-index. This keeps the navbar above the project cards while still allowing the hover animation to work correctly.


**My keytake away from this:**
-I gave the`transform: translateY(-5px)` for the hover to `.project-card:hover` inside the project section.

- Also, I added `z-index: 1000;` to the **navbar** so it will keep it above the project cards.  

2. How can I know when do I need a div, and when do I need div inside of another div ?

 **AI response:**
- A div is used to group elements together so they can be styled, positioned, or controlled as one unit.

- Use one div when multiple elements belong together visually and should move or behave together (for example, a card that contains a title and text).

- Use a div inside another div when different parts of a section have different layout or styling responsibilities.
The outer div usually controls the overall layout (like flexbox or grid), while the inner divs control specific parts (like text, images, or buttons).

- Each div should have one clear job. If a div doesn’t control layout, spacing, or structure, it’s probably unnecessary.


3. What height: 100vh; does and when do I need to use it in CSS? 

 **AI response:**
- height: 100vh means an element takes up the full height of the visible screen. The vh unit is based on the viewport, where 1vh equals 1% of the browser’s height, so 100vh always fills the screen no matter the device. This is commonly used for full-screen sections like hero areas or scroll-based layouts where each section should fit exactly one screen. It should be used carefully, because content-heavy sections can overflow, especially on mobile devices, where using min-height: 100vh is often safer.

**My keytake away from this:**
- I changed the height of each sections to `height: 100vh:` to take the full height of the screan. 

- Now, when the user look at my website it showes the full screan of the section makes it easier to navigate through the page, and made the screan scroll a lot better.  
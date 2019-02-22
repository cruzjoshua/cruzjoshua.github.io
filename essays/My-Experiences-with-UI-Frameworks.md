---
layout: essay
type: essay
title: My Experiences with UI Frameworks
# All dates must be YYYY-MM-DD format!
date: 2019-02-21
labels:
  - UI Frameworks
  - HTML5
  - CSS
  - Semantic UI
---

## Thoughts about HTML5 & CSS

After completing the basic UI Design module for this class, I realized that HTML5 and CSS is fairly simple. The three practice WOD's that involved with the BrowserHistory assignments were mostly copying and pasting into index.html, seperating each paragraph or description with the correct tag, applying redirects with pure HTML5, and manipulating the class properties in style.css to make it fancy and tidy. I had no HTML5 or CSS experience before doing any of these assignments and WOD's and I thought I did a great job in quickly learning the basics of it until I experienced my first website development problem. When we had to try our best to completely mimic a website of our choice with the usage of Semantic UI, I had the entire home website layout in my head and processed it into HTML and CSS with Semantic UI. However, while I had the homepage finished, there were uneven lines in between my middle and bottom page and the background color of each container were not fully stretched to the screen. I spent hours... countless hours trying to figure out my error. I did not want to give up and submit the page just the way it is because it was so ugly. I tried many different weird combinations with the classes of Semantic UI but none of them worked just the way I wanted it to be. I made sure my style.css syntax was correct and corresponds to the HTML portion of the code. Then I finally realized that to fix the unevenness of my homepage is to set margins to 0... I wanted to rip my hair out because I thought one of the Semantic UI classes would ignore all margins for me. Now for my other error, the background/color not stretching to the screen size, I tried setting the style to width: 100% but that did not work at all because Semantic UI has already that implemented into their classes. It is past 10 PM and I finally figured the problem out. All I had to do was wrap the current div with another dummy div class called 'middle' or 'footer' and change to the correct background color I wanted. I honestly blame HTML for all this and what are the benefits of this. Nothing really, other than never experiencing that problem ever again.

## Semantic UI & other Frameworks

Semantic UI was a great experience for me. I am so glad theres a UI Framework that makes HTML/CSS easier. My opinion may be slightly biased because Semantic UI is the only framework I have used so far. Is there an image that you need to match the same resolution as your computer screen? In Semantic UI, all you have to do is type ui fluid image and the fluid class will stretch your image to a desired resoluation. In pure HTML/CSS, you probably have to change the height and width manually in the style.css file. Who would want to do that when you can just type fluid. There are a hundred different classes that you can use with Semantic UI and probably more combinations with other classes. You can get creative with the combination of Semantic UI classes to make your webpage extremely cleaner and more appealing to others. Personally, Semantic UI was easy to learn and watching the PluralSight tutorials definitely improved my learning process of Semantic UI. As we are approaching into a new module with React and Meteor in the future, I hope to have the same positive opinion with Semantic UI.

# Short Conclusion
This is a custom JavaScript solution for toggling language (English/Arabic) and color mode (Dark/Light) for certain pictures on my Readymag portfolio. 
RM's built-in tools didn't support this functionality, so I added custom code in order to implement it. I used their code widget to paste and run my code.

## Why This Exists?
I wanted visitors to my portfolio to easily switch/toggle between two options on two dimensions/levels:
+ by first dimension, I mean language: English/Arabic.
+ and by second, I mean color mode: Dark/Light.

***Geeky explanation*** ~~(most probably overexplaining this but whatever)~~: 
I succeeded to implement this logic (w/out custom code, using only native RM animation) on a logo that remains the same on light and dark backgrounds, because I just uploaded the logo to RM with a transparent background, then placed it in front of two shapes (one colored light, other dark). One toggle controlled hiding/showing the logo, while the other toggle controlled hiding/showing the shapes.

But, the problem arised when I had some logos that contained some text that shifted color based on the background (light or dark). This meant that each logo has two distinct versions based on the color mode, so I am not able to just upload it with a transparent bg and do what I did. And, since each logo has two versions based on color, and each one of those two has an English version and an Arabic version, this totals 4 version for each logo. This was a problem because I wanted the visitor to engage with two toggles to showcase the versatility of the brand I designed.

Readymag doesn’t provide native support for such complex/multi-dimensional animations, and after trying every possible workaround using their tools, I realized the only way to achieve this was through custom JavaScript.

## How It Works?
I have two UI toggles (created them using basic shapes, text, and native RM animation); a language switcher (to switch between English/Arabic), and a color mode switcher (to switch between Light/Dark modes). 

The script updates the visibility of Readymag widgets based on the selected language and theme. It does this through basic conditional logic that accesses each widget (by locating it via its unique ID), then either showing or hiding it. I managed to acquire the widgets' ID by inspecting element on my browser, then locating the `data-id` inside the `<div>` tag of each desired widget. 

## Acknowledgements <3
Credits to [Roy Jara's article](https://royjara.medium.com/learn-how-to-extend-readymag-with-javascript-a1922f23dc69) for this, and to my friend [Laith](https://github.com/wlaith), both helped me out a lot thank you!

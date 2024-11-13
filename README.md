# xiwu0654_9103_tut5
My first respository for IDEA9103

This is my first local change to the repo

# Quiz 8 - Design Research for Major Assignment

## Part 1: Imaging Technique Inspiration

### Inspiration: Flowing Starry Sky
For my assignment, I found inspiration in an artwork that depicts stars flowing along a curved trajectory, creating a dynamic and dreamlike effect. I aim to incorporate a similar flowing, starry visual by placing stars on a bezier curve, creating a smooth, continuous movement. This technique brings an ethereal quality to the design, enhancing the viewer's sense of immersion. It’s particularly beneficial for this project, as it adds both visual appeal and a sense of depth through movement.

![Inspiration Image 1](link-to-your-image-1)
![Inspiration Image 2](link-to-your-image-2)

---

## Part 2: Coding Technique Exploration

### Technique: Bezier Curve Animation in p5.js
I discovered a bezier curve animation technique in p5.js that helps create flowing lines with smooth, rainbow-like color transitions. Using this code, I plan to position stars along the curve and animate them to move continuously. This bezier curve technique will act as a path for the stars, making them appear as if they’re gliding along a cosmic trail. Below is the code example I found, which can be adapted to achieve the flowing star effect.

![Coding Technique Image](link-to-code-example-image)

**Code Example and Reference:** [Bezier Curve Animation in p5.js](https://happycoding.io/tutorials/p5js/)

```javascript
// Define strokeHue as a global variable. This variable will be used to color each line.
let strokeHue = 20;

function setup() {
  createCanvas(720, 400);
  noFill();
  strokeWeight(2);
  colorMode(HSB);
}

function draw() {
  background(5);

  // Create 10 bezier lines with anchor points moving with the X coordinate of the cursor.
  for (let i = 0; i < 200; i += 20) {
    let strokeColor = i + 10;
    stroke(strokeColor, 50, 60);
    bezier(mouseX - i / 2, 0 + i, 410, 20, 440, 300, 240 - i / 16, 300 + i / 8);
  }
}

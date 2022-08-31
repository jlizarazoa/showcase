## Breathing Square Illusion

{{<p5-iframe sketch="/showcase/sketches/Breathing Square Illusion.js" width="520" height="520"}}

## Square rotation Illusion
             
{{< p5-widget autoplay=true height="420" width="420" ver="1.4.2" >}}
function setup() {
  createCanvas(600, 600);
  // rectMode(CENTER);
  x_0 = 0;
  y_0 = 255;
  a = true;
}

function draw() {
  background(0);

  push();
  translate(width / 2, height / 2);
  for (let x = 420; x >= 40; x = x / 1.08) {
    noStroke();
    rotate(radians(frameCount / 2));
    fill(y_0, 40);
    rect(0, 0, x, x);
  }
  pop();

  point(300, 300);
  stroke("blue"); // Change the color
  strokeWeight(3); // Make the points 10 pixels in size
}

function mousePressed() {
  if (a == false) {
    noLoop();
    a = true;
  } else {
    loop();
    a = false;
  }
}

{{< /p5-widget >}}

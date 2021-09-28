//shadow: dissappears
let shadowColor = 255;
let colorChange = 1;
let bgColor = 0;

// let part02 rotate(angle)
let part02Angle = 0;
let boxAngle = 0

//part01: grows and shrinks with scale
let part01_width =150;
let part01_Scale = -1;


//part04: grows and shrinks with scale
let part04_width =150;
let part04_Scale = -1;

//part04: grows and shrinks with scale
let part05_width =150;
let part05_Scale = -1;

//part04: grows and shrinks with scale
let circ_width =150;
let circ_Scale = -1;

//TpSound
var song;
var slider;

//poppers
let poppers = [];


function setup() {
  createCanvas(600, 600);
  song= loadSound("tpsong.mp3", loaded);
  slider = createSlider (0,1,0.5,0.01);

  angleMode(degrees);
  for (let i = 0; i < 10; i++) {
      let x = random(width);
      let y = random(height);
      let r = random(20, 60);
      let b = new Popper(x, y, r);
    poppers.push(b);
    }
  }

  function mousePressed() {
    for (let i = poppers.length - 1; i >= 0; i--) {
      if (poppers[i].contains(mouseX, mouseY)) {
      poppers.splice(i, 1);
      }
}
}
function loaded(){
  song.play();
}

function draw() {
  background(random(0));
song.setVolume(slider.value());


  //shadow
  push();
  if (shadowColor > 255 || shadowColor < bgColor) {
colorChange = -colorChange;
}
shadowColor = shadowColor + colorChange;
noStroke();
fill(shadowColor)

  beginShape();
  vertex(0, 508);
  bezierVertex(105, 445, 344, 554, 335, 552);
  bezierVertex(360, 581, 316, 600, 134, 600);
  bezierVertex(29, 563, 48, 539, 0, 508, 0, 508);
  endShape();
  pop();



  //wall
  push();
  fill(16,16,16);
  quad(0, 508, 473, 405, 473, 0, 0, 0);
  pop();


  //back wall
  push();
  fill(3, 3, 3);
  quad(473, 292, 473, 0, 600, 0, 600, 341);
  pop();

  //box
  push()
  fill(153,59,70)
  translate(20,20)
  rotate(boxAngle)
  rect(108, 180, 154, 154);
  //boxAngle -= radians(1)
  pop()

  //part02
  push()
  fill(90)
  beginShape();
vertex(225, 552);
bezierVertex(234, 554, 252, 558, 276, 562);
bezierVertex(288, 563, 315, 562, 324, 560);
bezierVertex(374, 541, 337, 535, 335, 487);
bezierVertex(336, 454, 340, 444, 355, 431);
bezierVertex(380, 404, 395, 376, 398, 356);
bezierVertex(385, 343, 361, 330, 320, 318);
bezierVertex(281, 314, 164, 335, 140, 337);
bezierVertex(117, 342, 225, 552);
endShape();

pop()

  //part01
  push();
  fill(228, 228, 228, 240);

translate(20,20)

if (part01_width > 200 || part01_width < 10) {
  part01_Scale = part01_Scale* -1 ;
}
part01_width = part01_width + part01_Scale;

  beginShape();
  vertex(48, 195);
  bezierVertex(part01_width, 264, part01_width, 315, 53, 359);
  bezierVertex(82, 393, 98, 437, 91, 483);
  bezierVertex(90, 505, 94, 508, 137, 524);
  bezierVertex(185, 544, 213, 554, 248, 557);
  bezierVertex(261, 538, 265, 498, 264, 463);
  bezierVertex(279, 426, 301, 406, 331, 378);
  bezierVertex(333, 373, 279, 367, 234, 360);
  bezierVertex(165, 346, 130, 336, 114, 331);
  bezierVertex(108, 326, 105, 315, 107, 291);
  bezierVertex(110, 248, 111, 224, 109, 212);
  bezierVertex(part01_width, part01_width, 85, 199, 52, 195);
  endShape();
  pop();

  // part04
  push();
  fill(197,98,110);
  translate (-45,-45)
  if (part04_width > 200 || part04_width < 10) {
    part04_Scale = part04_Scale* -1 ;
  }
  part04_width = part04_width + part04_Scale;
  beginShape();
  vertex(48, 195);
  bezierVertex(part04_width, part04_width, part04_width, part04_width, part04_width, part04_width);
  bezierVertex(119, 205, 163, 197, 202, 193);
  bezierVertex(244, 191, 263, 188, 250, 175);
  bezierVertex(part04_width, part04_width, part04_width, part04_width, part04_width, part04_width);
  bezierVertex(part04_width, part04_width, part04_width, part04_width, part04_width, part04_width);
  endShape();
  pop();

  // part05
  // seat shape1
  push();
  fill(73,59,153, 100);
  if (part05_width > 200 || part05_width < 10) {
    part05_Scale = part05_Scale* -1 ;
  }
  part05_width = part05_width + part05_Scale;
  beginShape();
  vertex(part05_width + 2 , part05_width + 2);
  bezierVertex(193, 247, 258, 180, 312, 152);
  bezierVertex(350, 140, 378, 145, 390, 157);
  bezierVertex(part05_width, part05_width, part05_width, part05_width + 7, 355, 248);
  bezierVertex(316, 289, 238, 318, 134, 310);
  bezierVertex(134, 310);
  endShape();
  pop();

  push();
  fill(228, 228, 228);
  translate(width / 3, height / 3);
  rotate(118.7);
  ellipse(55, 80, 210, 80);
  pop();

  //circ
  push();
  fill(109,199,214, 90);
  if (circ_width > 200 || circ_width < 10) {
  circ_Scale = circ_Scale* -1 ;
  }
  circ_width = circ_width + circ_Scale;

  translate(width / 3, height / 3);
  rotate(119.54);
  ellipse(100, 129, 500, circ_width);
  pop();



  //Part 5- back
  push();
  fill(226, 226, 226);
  beginShape();
  vertex(140, 338);
  bezierVertex(174, 328, 219, 300, 290, 313);
  bezierVertex(319, 318, 274, 326, 197, 341);
  bezierVertex(134, 341, 122, 338);
  endShape();
  pop();

  //Part 5- seat shape2
  push()
  beginShape();
  vertex(159, 328);
  bezierVertex(179, 298, 228, 287, 251, 277);
  bezierVertex(328, 255, 383, 244, 401, 246);
  bezierVertex(409, 254, 406, 263, 360, 289);
  bezierVertex(328, 301, 280, 313, 197, 327);
  bezierVertex(197, 327, 177, 330, 159, 328);
  bezierVertex();
  endShape();
  pop()

  //Part 5_ seat shape2_ellipse
  push();
  fill(95, 95, 95);
  translate(width / 3, height / 3);
  rotate(119.13);
  ellipse(60, 110, 200, 35);
  pop();

  //curve finish
  bezier(340, 378, 346, 379, 400, 376, 394, 360);

  //shade 3
  push()
  beginShape();

  vertex(148, 310);
  bezierVertex(249, 182, 325, 148, 327, 148);
  bezierVertex(299, 150, 249, 196, 168, 269);
  bezierVertex(150, 301, 139, 250, 148, 310);
  endShape();
pop()
  // handle 2
  push()
  fill(189)
  beginShape();
  vertex(128, 305);
  bezierVertex(174, 339, 198, 353, 213, 354);
  bezierVertex(240, 351, 226, 362, 195, 365);
  bezierVertex(185, 365, 138, 344, 128, 335);
  bezierVertex(126, 320, 125, 313, 128, 305);
  endShape();
pop()
  // handle 1
push()
fill(189)
  beginShape();
  vertex(128, 306);
  bezierVertex(159, 290, 185, 322, 228, 354);
  bezierVertex(213, 356, 196, 354, 179, 347);
  bezierVertex(166, 337, 142, 319, 128, 306);
  endShape();
  pop()

  //Shade1
  push();
  fill(0, 0, 0, 180);
  beginShape();
  vertex(324, 385);
  bezierVertex(300, 415, 344, 433, 335, 438);
  bezierVertex(312, 447, 260, 539, 261, 514);
  bezierVertex(265, 488, 260, 438, 265, 425);
  bezierVertex(284, 413, 298, 405, 324, 385);
  endShape();
  pop();

  //shade2
  push();
  fill(0, 0, 0, 80);
  beginShape();
  vertex(78, 382);
  bezierVertex(97, 397, 141, 392, 178, 397);
  bezierVertex(100, 399, 98, 414, 78, 382);
  endShape();
  pop();

  //shade4
  push();
  fill(0, 0, 0);
  beginShape();
  vertex(95, 204);
  bezierVertex(236, 192, 296, 180, 121, 210);
  bezierVertex(108, 210, 100, 207, 95, 204);
  endShape();
  pop();
  //button
  rect(121, 159, 19, 5);
  ellipse(130, 159, 20, 4);


  //circ
  push()
  strokeWeight(4);
  stroke(255);
   ellipse(x, y, 25, 25);

  if (circ_width > 200 || circ_width < 10) {
  circ_Scale = circ_Scale* -1 ;
  }
  circ_width = circ_width + circ_Scale;

  translate(width / 3, height / 3);
  rotate(119.54);
  ellipse(120, 130, 200, circ_width-100);
pop()
  for (var x = 500; x <= width; x += 10) {
    for (var y = 1; y <= height; y += 10) {
      fill(random(250,1 ), 0, random(100, 100));
      ellipse(x, y, 5, 5);
    }
  }

  //poppers
  for (let i = 0; i < poppers.length; i++) {
      if (poppers[i].contains(mouseX, mouseY)) {
        poppers[i].changeColor(255);
      } else {
        poppers[i].changeColor(0);
      }
      poppers[i].move();
      poppers[i].show();
    }
  }

  class Popper {
    constructor(x, y, r) {
      this.x = x;
      this.y = y;
      this.r = r;
      this.brightness = 0;
    }

    changeColor(bright) {
      this.brightness = bright;
    }

    contains(px, py) {
      let d = dist(px, py, this.x, this.y);
      if (d < this.r) {
        return true;
      } else {
        return false;
      }
    }

    move() {

      this.x = this.x + random(-1, 1);
      this.y = this.y + random(-1, 1);
    }

    show() {
      push()
      stroke(255);
      strokeWeight(4);
      fill(this.brightness, 125);
      rect(this.x, this.y, this.r * 2,this.r * 2);
      pop()

    }
  }

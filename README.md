# Harsh-character
Life is complicated

![buh](https://github.com/nicolasbaez/Harsh-character/blob/main/xp048.gif)
```javascript
setup = (_) => createCanvas((w = 500), w, WEBGL);
k = 0;
draw = (_) => {
  rotateX(k);
  rotateY(k / 2);
  clear();
  noFill();
  for (i = 0; i <= 3; i += 0.3)
    for (j = 0; j < 6; j += 0.3) {
      stroke(noise(i, j) * 255);
      r = 180;
      push();
      translate(r * sin(i) * cos(j), r * sin(i) * sin(j), r * cos(i));
      sphere(24 + random(8));
      pop();
    }
  if (k == 0) saveGif("xp048.gif", 628, { delay: 0, units: "frames" });
  k += 0.01;
};

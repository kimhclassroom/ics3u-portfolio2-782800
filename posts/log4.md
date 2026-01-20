# Learning Log #4: Arrays & Data Structures

I used an array to store all of the planet images so I could easily access them using an index. Each planet has a type variable, which matches the index of the image in the array. This makes it simple to display the correct image without needing separate variables for each planet image.

```
PImage[] obj = new PImage[9];

  for (int i = 0; i < obj.length; i++) {
    obj[i] = loadImage("image-removebg-preview (" + i + ").png");
  }

image(obj[type], x, y, radius * 2, radius * 2);
```

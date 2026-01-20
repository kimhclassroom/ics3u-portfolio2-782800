# Learning Log #1: Variables & Data Tracking

For my Planet Merge game, I used different types of variables to track the game and its objects. I used int variables for things like the score and to identify different planet types. For example, the score variable increases when planets merge, and the type variable determines which planet image is being used.
```
float score = 0;
int type;
```

I used float variables for the x and y positions of planets and their falling speed so movement looks smooth instead of choppy. This is especially important when gravity is applied to falling planets.
```
float ox, oy;
float oys = 0;
```

I also used boolean variables to control the game state, such as when the game starts or ends. This allows the program to switch between the start screen, gameplay, and game over screen.
```
boolean gameStarted = false;
boolean gameOver = false;
```

I used an array to store all the planet images so I could easily access them using an index based on the planet type. This makes it easier to draw the correct image without creating many separate variables.
```
PImage[] obj = new PImage[9];
```

Finally, I used arrays to store planets that have landed because the number of planets changes constantly as new planets fall and merge. These arrays store each planet’s position and type and are updated throughout the game.
```
float[] sx = new float[50];
float[] sy = new float[50];
int[] stype = new int[50];
```

All of these variables are used together to control movement, detect collisions and merges, track the score, and determine when the game ends.

# Learning Log #3: Repetition Structure

This loop is used to draw all the planets that have already landed in the game. The loop runs from 0 to stored, which represents how many planets are currently saved. Each time the loop runs, it accesses the planet’s position and type from the arrays and draws the correct image. This repetition structure is important because the number of planets in my game is always changing due to merges and new planets being dropped, and using a loop allows the game to handle any number of planets without repeating the same code over and over.

```
for (int i = 0; i < stored; i++) {
  int s = planetSize(stype[i]);
  image(obj[stype[i]], sx[i], sy[i], s, s);
}
```

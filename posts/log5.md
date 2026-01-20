# Learning Log #5: Use of Custom Functions & Error Checking / Restrictions

 I created custom functions to organize important parts of my game and avoid repeating code. The isCollided() function checks for collisions using the size of the images by making sure planets overlap on both the X and Y axes. This function is used in multiple places, such as stopping falling planets, merging planets, and preventing planets from overlapping. The restriction in this function is that both X and Y overlap conditions must be true, which prevents faulty collisions.

```
boolean isCollided(float fx, float fy, int fType, int i) {
  int fSize = planetSize(fType);
  int sSize = planetSize(stype[i]);

  boolean overlapX = fx < sx[i] + sSize && fx + fSize > sx[i];
  boolean overlapY = fy < sy[i] + sSize && fy + fSize > sy[i];

  return overlapX && overlapY;
}
```
The storePlanet() function is for saving a planet once it stops falling. It stores the planet’s position and type into arrays and increases the planet count. It also includes error checking by testing if the planet stops above the danger line, which immediately ends the game. These custom functions support the game by keeping the logic organized, reusable, and preventing errors like overlapping planets or invalid game states.
```
void storePlanet() {
  sx[stored] = ox;
  sy[stored] = oy;
  stype[stored] = type;
  stored++;

  if (oy < dangerLineY) {
    gameOver = true;
    return;
  }

  resetCurrentPlanet();
}
```

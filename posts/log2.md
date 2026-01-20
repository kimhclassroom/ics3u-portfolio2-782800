# Learning Log #2: Selection Structure

Selection structures are used to make decisions in the game based on certain conditions. I used if statements to check whether the game has started or ended so the correct screen is shown. This solves the problem of having multiple states in one game by just being able to overlay a new screen, such as the start screen, and the game over screen.

```

if (!gameStarted) {

  drawStartScreen();

} else if (gameOver) {

  drawGameOver();

}
```

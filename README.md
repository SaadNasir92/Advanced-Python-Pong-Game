# Advanced Python Ping Pong Game

## Description
This multiplayer Pong game, developed in Python using the `turtle` module, showcases advanced object-oriented programming techniques. It features fully controllable paddles, an automated ball that reacts to game events, and a dynamic scoreboard to keep track of the scores. This game is designed to provide a fun and interactive way to understand complex programming concepts such as collision detection, game state management, and more.

## Features
- **Multiplayer Gameplay**: Two players can control their paddles using keyboard inputs, competing in real-time.
- **Dynamic Collision Handling**: Implements collision logic for paddles and boundaries to influence the game mechanics accurately.
- **Score Tracking**: A scoreboard that updates in real-time, recording and displaying scores throughout the game.
- **Customizable Game Mechanics**: Players experience varying paddle speeds and ball dynamics, which can be tailored for different difficulty levels.

## Technologies Used
- Python
- `turtle` module for rendering and animations
- Object-oriented programming for structured and modular design

## Setup and Play
1. Clone the repository:
   ```bash
   git clone https://github.com/SaadNasir92/Advanced-Python-Pong-Game
   ```
2. **Navigate to the cloned directory:**
    ```bash
    cd Advanced-Python-Pong-Game
    ```
3. **Run the game**
    ```bash
    python main.py
    ```
## Controls
- **Player 1:**
    - **'w'** to move paddle up
    - **'s'** to move paddle down

- **Player 2:**
    - **'Up Arrow'** to move paddle up
    - **'Down Arrow'** to move paddle down

## Code Example
```python
# Example of Ball movement logic, check ball.py for ball class logic.
class Ball: ...

def move(self):
        self.ball.forward(self.speed)

    def right_left_correction(self, shift):
        new_heading = 180 - self.ball.heading()
        if shift != 0:
            self.ball.setheading(shift)
        else:
            self.ball.setheading(new_heading)

    def vertical_collision(self):
        if self.ball.ycor() >= TOP_BOUND - BALL_SPEED or self.ball.ycor() <= BOT_BOUND + BALL_SPEED:
            new_heading = self.ball.heading() * -1
            self.ball.setheading(new_heading)
```
## Lessons Learned
- **Advanced Python Constructs:** Gained deeper insights into Python's turtle module and object-oriented programming.
- **Game Loop and State Management:** Developed an understanding of managing the game loop and the states of game objects.
- **User Input Handling:** Enhanced skills in handling user inputs and responding to key events.
- **Creativity:** Improved problem-solving for real-time game physics.

## Future Improvements
- **Advanced AI Opponents:** Develop AI logic for solo play against computer-controlled opponents.
- **Themes and Visuals:** Improve the game's visual appeal with advanced graphics and animations.
- **Sound and Music:** Integrate sound effects and background music to create an immersive gaming experience.

## Known Issues
- **Paddle Collision Bug**: There is a known issue where the ball does not react appropriately when hitting the absolute top or bottom of the left or right paddle. This can occasionally affect gameplay by not reflecting the ball as expected.

## Contributing
We welcome contributions, especially for fixing known issues. If you have a fix or improvement, please fork the repository, make your changes, and submit a pull request. For major changes, please open an issue first to discuss what you would like to change.

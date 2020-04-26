# Snake face

Keyboards are for losers -- play snake by moving your head! 
<a href="https://paruby.github.io/snake-face/">Play live.</a>

<img src="demo.gif" alt="demo" style="width: 640px;"/>

## How does this work?

I use the tensorflow.js model <a href="https://github.com/tensorflow/tfjs-models/tree/master/facemesh">MediaPipe Facemesh</a> to estimate the pose of your head in real time using your device's camera. When the game starts, the direction your head is pointing is estimated as a reference point. Subsequent estimates during game play are compared to this to decide which direction you want to steer the snake.

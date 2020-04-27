# Snake face

Keyboards are for losers -- play snake by moving your head! 

Play live: <a href="https://paruby.github.io/snake-face/">https://paruby.github.io/snake-face/</a>


<img src="demo.gif" alt="demo" style="width: 640px;"/>

## How does this work?

I use the tensorflow.js model <a href="https://github.com/tensorflow/tfjs-models/tree/master/facemesh">MediaPipe Facemesh</a> to estimate the head pose in real time using the device's camera. When the game starts, the direction in which the head is pointing is estimated as a reference point. Subsequent estimates during game play are compared to this to decide which direction to steer the snake.


The head direction is estimated by calculating the vectors connecting
the centre of the lips to the left and right cheeks. These two vectors lie
on a plane that approximates the surface of the face. The cross product of these
vectors is normal to this plane and thus points approximately in the direction
of the head.


You can read more about this here: <a href=""http://paulrubenstein.co.uk/blog/>http://paulrubenstein.co.uk/blog/</a>

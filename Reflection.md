## Describe the effect each of the P, I, D components had in your implementation.

The P component causes the car to adjust the steering angle based on whether the car is left or right of center.

The D component causes the car to adjust the steering angle based on whether the car has drifted further left or further right of center between the last control and this control.

The I component causes the car to bias the steering based on how much time the car spends on the left or right or center, also taking into account how far left or right of center it was during that time. Effectively it corrects for drift.

## Describe how the final hyperparameters were chosen.

I used manual tuning. First I set the D component to 1, then manually twiddled the other components until the car drove well. Then I twiddled the D component to make it drive better.

I also used a PID controller to keep the speed at 30mph.

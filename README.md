# Unscented-Kalman-Filter

Classwork for the Udacity Self Driving Car Nanodegree

---
## Discussion

  Most of the code I used is from the quizzes. For this project, most of what I had to do was just put the code from the quizzes together and make all of the code function together. I got an idea of how to put the code together from https://github.com/gardenermike/unscented-kalman-filter.

  While making the UKF(Unscented Kalman Filter), I ran into several serious bugs which took a long time to fix. The first bug I ran into resulted in a matrix-size error when the UKF started running. I don't even remember what caused the error, but it took a while for me to find the problem. After that, I still had a bug where matrix values would turn to non-numbers, causing the simulator and UKF to lock up and not work. As with the matrix-size error bug, I do not remember the cause. The last bug I ran into, and probably the one that took the most time to find the cause of and fix, was a bug that caused matrix values to shoot up to clearly incorrect numbers often greater than googol cubed, or 10^300. The cause of this bug was the fact that the P matrix was not properly initialized as an identity matrix.

  After I fixed all the serious bugs, all I had to do was a little bit of tuning the hyperparameters longitudinal acceleration standard deviation and yaw acceleration standard deviation. The starting value for these was 30, which is ridiculusly high. The values that worked well for me were 1.8 for longitudinal acceleration and 1.5 for yaw acceleration. The final root-mean-squared-error values I got with those hyperparameter values were:

#### X: 0.0736

#### Y: 0.0839

#### VX: 0.3932

#### VY: 0.2546

# Unscented-Kalman-Filter

Classwork for the Udacity Self Driving Car Nanodegree

---
  This repository has an implentation of an Unscented Kalman Filter(UKF). This is my submission of the Unscented Kalman Filter project of the Udacity Self Driving Car Nanodegree.

## Discussion

### What is an Unscented Kalman Filter?
 A Kalman Filter is a mathmatical technique which merges measurement data, often from unrelated sensors, to measure motion and predict location. Normal Kalman Filters represent motion linearly, while an Unscented Kalman Filter does not. Instead of using a linear motion representation, UKFs can represent turns with a gaussian approximation. While this representation of motion is imperfect, it is much more accurate representation of real-world vehicles than linear motion.

### Building the filter

  To build the UKF, I used a lot of code from the quizzes in the Nanodegree. While building this project, the primary thing I had to do was put together the quiz code and make it function as a whole. I got an idea of how to put the code together from https://github.com/gardenermike/unscented-kalman-filter.

  While making my UKF, I ran into several serious bugs which each took a while to fix. However, after I fixed all the serious bugs, all I had to do was a little bit of tuning two hyperparameters: longitudinal acceleration standard deviation, and yaw acceleration standard deviation. The starting value for these was 30, which is ridiculously high. The values that worked well for me were 1.8 for longitudinal acceleration and 1.5 for yaw acceleration. The final root-mean-squared-error values I got with those hyperparameter values were:

#### X: 0.0736

#### Y: 0.0839

#### VX: 0.3932

#### VY: 0.2546

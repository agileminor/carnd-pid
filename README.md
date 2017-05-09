# Overview
This repository contains the code for the pid project for Term 2 of Udacity's Self-Driving Car Nanodegree.


## Project Introduction
Project takes input from Udacity's driving simulator, in form of cross track error, and sends back a steering angle. Goal is to keep the car on the road around the track.

### Reflection

My plan was to get the simulator/PID combination running, play around with the parameters in order to get a feel for how the car responded, and then code up a version of the "twiddle" algorithm to find parameters that would successfully get it around the track.

But in manually exploring the parameters, I found a set that allowed the car to successfully complete the track.

Here is what I found:<br>
proportional parameter - basic parameter to steer the car, by itself tends to be unstable even at small values<br>
derivative parameter - needed to limit instability introduced by the basic proportional correction. Has little effect by itself<br>
integration parameter - useful to correct bias and reduce instability, but did not seem necessary in this simulator. I had successful lap completions with it set to 0.0.<br>

Overall, I found a small proportional parameter, a large derivative parameter (an order of magnitude larger than Kp) and a very small integration parameter (order of magnitude smaller than Kp) works well.










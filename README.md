# Sensor-Fusion-and-vehicle-tacking-using-Extended-Kalman-Filters

# 1.  Kalman filters
!['Mathematical Equation of Kalman Filter'](https://github.com/sbperceptron/Sensor-Fusion-and-vehicle-tacking-using-Kalman-Filters/blob/master/insight_formula.gif)

The subscript k indicate states of the system
The goal is to find Xk in the equation, which is the estimate of signal x in the equation
Zk is the Measurement value, and Kk is the Kalman Gain
Xk-1 is the estimate of the signal on previous state

The only Unknown component is Kk the Kalman Gain. Since we have measurement values and the previous estimated signal. We can can caliculate the Kalman gain on each consequent state

   # "Kalman filter finds the most optimum averaging factor for each consequent state. Also somehow remembers a little bit about the past states." 


The two kalman filter equations are,

![''](https://github.com/sbperceptron/Sensor-Fusion-and-vehicle-tacking-using-Kalman-Filters/blob/master/equation1.gif)

![''](https://github.com/sbperceptron/Sensor-Fusion-and-vehicle-tacking-using-Kalman-Filters/blob/master/equation2.gif)

# First step:
We need to be sure that kalman filtering conditions apply to the problem.i.e each signal value can be evaluated by using the linear stochastic equation. Inother words each Xk is a linear combination of its previous value plus a control signal and process noise

the second equation tells us that any measurement value is a linaer combination of signal value and measurement noise

The process noise and the measurement noise are statistically independent.
A,B,H form the matrices whose values change with states

Only thing that is left now is the mean and standard deviation of noise functions Wk-1 and vk. We know that, in real life, no signal is pure Gaussian, but we may assume it with some approximation. 

"The better you estimate the noise parameters, the better estimates you get." 
